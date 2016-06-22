DEST="_gh-pages"


desc "publish the handout to github pages"
task :publish do |t|
  FileUtils.rm_rf "#{DEST}/*"
  FileUtils.cp("handout.html", "#{DEST}/index.html")
  FileUtils.cp("handout.txt", DEST)
  Dir.chdir(DEST) do |dest|
    sh "git checkout gh-pages && git add --all && git commit -m #{Time.now.strftime("%FT%T")} && git push -u origin gh-pages"
  end
end
