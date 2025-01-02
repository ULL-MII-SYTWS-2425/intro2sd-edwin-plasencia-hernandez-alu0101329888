task :serve do
  sh "bundle exec jekyll s --watch --incremental --future -V -P 4000"
end

task :build do
  sh "bundle exec jekyll build --future -V"
  sh "head -n 30 _site/assets/src/search.json"
end

task deploy: [ :build ] do
  sh "npm run build && npx gh-pages -d _site"
end
