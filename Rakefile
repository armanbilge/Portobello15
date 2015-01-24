require 'rake/clean'

$base = 'sift'

['aux', 'log', 'nav', 'out', 'snm', 'toc'].each do |ext|
  CLEAN.include "#$base.#{ext}"
end
CLOBBER.add "#$base.pdf"

task :default => "#$base.pdf"

file "#$base.pdf" => "#$base.tex" do |t|
  2.times do
    sh "pdflatex #$base"
  end
end
