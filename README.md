Small Example for sbt-web with submodules
=========================================

This project demonstrates https://github.com/sbt/sbt-js-engine/issues/16.

The following uses the package.json from the root directory
and works as expected:

<pre>
rm -rf node_modules subproject/node_modules
sbt web-assets:jseNpmNodeModules
ls -al node_modules
</pre>

This unfortunately does not work:

<pre>   
rm -rf node_modules subproject/node_modules
sbt subproject/web-assets:jseNpmNodeModules
ls -al subproject/node_modules
</pre>

