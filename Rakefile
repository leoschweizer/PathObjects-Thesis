require 'fileutils'
require 'open-uri'

task :default => [:clean, :build, :show]

desc "Remove all generated files"
task :clean do
	FileUtils.rm_rf 'build'
	FileUtils.rm_rf 'tmp'
	FileUtils.rm_rf 'thumbs'
	FileUtils.rm_rf 'Thesis.pdf'
end

task :make_build_directory do
	Dir.mkdir("build") unless Dir.exists?("build")
end

desc "Multi run build"
task :build => [:make_build_directory] do
	Dir.chdir('tex') do
		`pdflatex -output-directory=../build main.tex`
		`biber --output_directory ../build main`
		`pdflatex -output-directory=../build main.tex`
		`pdflatex -output-directory=../build main.tex`
	end
	FileUtils.move 'build/main.pdf', 'Thesis.pdf'
end

desc "Single run build"
task :fastbuild => [:make_build_directory] do
	Dir.chdir('tex') do
		`pdflatex -output-directory=../build main.tex`
	end
	FileUtils.move 'build/main.pdf', 'Thesis.pdf'
end

desc "open the generated PDF file"
task :show do
	puts "opening of the PDF not yet supported :("
end

desc "generate thumbnails of every page"
task :thumbs do
	Dir.mkdir('tmp') unless Dir.exists?('tmp')
	# fetch PDFBox
	File.open('tmp/pdfbox-app-1.8.2.jar', 'wb') do |saved_file|
		open('http://apache.mirror.iphh.net/pdfbox/1.8.2/pdfbox-app-1.8.2.jar', 'rb') do |read_file|
			saved_file.write(read_file.read)
		end
	end
	# generate PDF if necessary
	Rake::Task[:build].reenable
	Rake::Task[:build].invoke unless File.exists?('Thesis.pdf')
	FileUtils.cp 'Thesis.pdf', 'tmp/Thesis.pdf'
	Dir.chdir('tmp') do
		`java -jar pdfbox-app-1.8.2.jar PDFToImage -imageType png Thesis.pdf`
		FileUtils.rm_rf 'pdfbox-app-1.8.2.jar'
		FileUtils.rm_rf 'Thesis.pdf'
	end
	FileUtils.mv 'tmp', 'thumbs'
end