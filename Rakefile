require 'fileutils'
require 'open-uri'

MAIN_INPUT		= "main"
MAIN_INPUT_TEX	= "#{MAIN_INPUT}.tex"
OUTPUT_NAME		= "Thesis.pdf"
PDFBOX_VERSION 	= "1.8.2"

task :default => [:clean, :build, :show]

desc "Remove all generated files"
task :clean do
	FileUtils.rm_rf 'build'
	FileUtils.rm_rf 'tmp'
	FileUtils.rm_rf 'thumbs'
	FileUtils.rm_rf OUTPUT_NAME
end

task :make_build_directory do
	Dir.mkdir("build") unless Dir.exists?("build")
end

desc "Multi run build"
task :build => [:make_build_directory] do
	Dir.chdir('tex') do
		`pdflatex -shell-escape -output-directory=../build #{MAIN_INPUT_TEX}`
		`biber --output_directory ../build #{MAIN_INPUT}`
		`pdflatex -shell-escape -output-directory=../build #{MAIN_INPUT_TEX}`
		`pdflatex -shell-escape -output-directory=../build #{MAIN_INPUT_TEX}`
	end
	FileUtils.move 'build/main.pdf', OUTPUT_NAME
end

desc "Single run build"
task :fastbuild => [:make_build_directory] do
	Dir.chdir('tex') do
		`pdflatex -output-directory=../build #{MAIN_INPUT_TEX}`
	end
	FileUtils.move 'build/main.pdf', OUTPUT_NAME
end

desc "open the generated PDF file"
task :show do
	puts "opening of the PDF not yet supported :("
end

desc "generate thumbnails of every page"
task :thumbs do
	Dir.mkdir('tmp') unless Dir.exists?('tmp')
	# fetch PDFBox
	pdfbox = "pdfbox-app-#{PDFBOX_VERSION}.jar"
	File.open("tmp/#{pdfbox}", 'wb') do |saved_file|
		open("http://apache.mirror.iphh.net/pdfbox/#{PDFBOX_VERSION}/#{pdfbox}", 'rb') do |read_file|
			saved_file.write(read_file.read)
		end
	end
	# generate PDF if necessary
	if !File.exists?(OUTPUT_NAME)
		Rake::Task[:build].reenable
		Rake::Task[:build].invoke
	end
	FileUtils.cp OUTPUT_NAME, "tmp/#{OUTPUT_NAME}"
	Dir.chdir('tmp') do
		`java -jar #{pdfbox} PDFToImage -imageType png #{OUTPUT_NAME}`
		FileUtils.rm_rf pdfbox
		FileUtils.rm_rf OUTPUT_NAME
		Dir.glob("*.png") do |thumb|
			`convert #{thumb} -resize 10% #{thumb}`
		end
	end
	FileUtils.mv 'tmp', 'thumbs'
end