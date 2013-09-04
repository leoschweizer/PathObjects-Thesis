require 'fileutils'

task :default => [:clean, :build, :show]

desc "Foo"
task :clean do
	FileUtils.rm_rf('build')
	FileUtils.rm_rf('Thesis.pdf')
end

task :make_build_directory do
	Dir.mkdir("build") unless Dir.exists?("build")
end

desc "Foo"
task :build => [:make_build_directory] do
	Dir.chdir('tex') do
		`pdflatex -output-directory=../build main.tex`
		`biber --output_directory ../build main`
		`pdflatex -output-directory=../build main.tex`
		`pdflatex -output-directory=../build main.tex`
	end
	FileUtils.move 'build/main.pdf', 'Thesis.pdf'
end

desc "Foo"
task :fastbuild => [:make_build_directory] do
	Dir.chdir('tex') do
		`pdflatex -output-directory=../build main.tex`
	end
	FileUtils.move 'build/main.pdf', 'Thesis.pdf'
end

desc "Foo"
task :show do
	puts "opening of the PDF not yet supported :("
end