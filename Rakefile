require 'tmpdir'

INPUT_DIRECTORY_NAME = 'source'
INPUT_FILE_EXTENSION = 'md'

PANDOC_FLAGS = [
  '--latex-engine xelatex',
  '--template ./templates/pdf-template.tex',
  '--listings',
  '--verbose',
  '--chapters'
].join(' ')

PANDOC = ['pandoc', PANDOC_FLAGS].join(' ')

# directory OUTPUT_DIRECTORY_NAME

desc "Build the pdf"
task :build => [:clean, :build_pdf, :build_html] do
end

desc "Build pdf"
task :build_pdf do
  Dir.mktmpdir do |dir|
    # Build pdf
    sh "#{PANDOC} source/*.md -o #{dir}/content.pdf"
    sh "pdftk #{Dir.pwd}/source/cover.pdf #{dir}/content.pdf cat output #{Dir.pwd}/pdf/playbook.pdf verbose"
  end
end

desc "Build html"
task :build_html do
  # Build HTML
  sh "#{PANDOC} -t html5 --toc --self-contained --template=./templates/html-template.tex source/*.md -o #{Dir.pwd}/html/index.html"
end

desc "Remove the generated PDF"
task :clean do
  `rm -rf pdf html`
  `mkdir pdf html`
end

task :open do
  sh 'open pdf/playbook.pdf'
  sh 'open html/index.html'
end

task preview: [:build, :open]
task :default => :build
