require 'tmpdir'

INPUT_DIRECTORY_NAME = 'source'
INPUT_FILE_EXTENSION = 'md'
OUTPUT_DIRECTORY_NAME = 'pdf'
OUTPUT_FILE_EXTENSION = 'pdf'

PANDOC_FLAGS = [
  '--latex-engine xelatex',
  '--template ./templates/pdf-template.tex',
  '--listings',
  '--verbose',
  '--chapters'
].join(' ')

PANDOC = ['pandoc', PANDOC_FLAGS].join(' ')

directory OUTPUT_DIRECTORY_NAME

desc "Build the pdf"
task :build => [:clean, OUTPUT_DIRECTORY_NAME] do
  Dir.mktmpdir do |dir|
    sh "#{PANDOC} source/*.md -o #{dir}/content.pdf"
    sh "pdftk #{Dir.pwd}/source/cover.pdf #{dir}/content.pdf cat output #{Dir.pwd}/pdf/playbook.pdf verbose"
  end
end

desc "Remove the generated PDF"
task :clean do
  `rm -rf #{OUTPUT_DIRECTORY_NAME}`
  `mkdir #{OUTPUT_DIRECTORY_NAME}`
end

task :default => :build

task :open do
  sh 'open pdf/playbook.pdf'
end

task preview: [:build, :open]
