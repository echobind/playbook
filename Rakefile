require 'tmpdir'

INPUT_DIRECTORY_NAME = 'source'
INPUT_FILE_EXTENSION = 'md'
OUTPUT_DIRECTORY_NAME = 'pdf'
OUTPUT_FILE_EXTENSION = 'pdf'

PANDOC_FLAGS = [
  '--latex-engine xelatex',
  '--template ./templates/pdf-template.tex',
  '--listings'
].join(' ')

PANDOC = ['pandoc', PANDOC_FLAGS].join(' ')

directory OUTPUT_DIRECTORY_NAME

desc "Build the pdf"
task :build => [:clean, OUTPUT_DIRECTORY_NAME] do
  Dir.mktmpdir do |dir|
    `#{PANDOC} source/*.md -o #{dir}/content.pdf`
    `pdftk source/cover.pdf #{dir}/content.pdf cat output pdf/playbook.pdf`
  end
end

desc "Remove the generated PDF"
task :clean do
  `rm -rf #{OUTPUT_DIRECTORY_NAME}`
  `mkdir #{OUTPUT_DIRECTORY_NAME}`
end

desc "Regenerate the PDF and push it to GitHub."
task :release => :regenerate do
  puts "Releasing new version to GitHub"
  `git commit -am 'New version of PDFs'`
  `git push origin master`
end

task :default => :build

task :open do
  sh 'open pdf/playbook.pdf'
end

task preview: [:build, :open]
