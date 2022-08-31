Сделал все согласно задания, но на шаге 6 при выполнении npm run build выдает ошибку:

PS H:\#github_rep\ajs-alexdm> npm run build

> @alekseyad/ajs-alexdm@1.0.0 build
> webpack --mode production

[webpack-cli] Error: For the selected environment is no default script chunk format available:
JSONP Array push can be chosen when 'document' or 'importScripts' is available.
CommonJs exports can be chosen when 'require' or node builtins are available.
Make sure that your 'browserslist' includes only platforms that support these features or select an appropriate 'target' to allow selecting a chunk format by default. Alternatively specify the 'output.chunkFormat' directly.    
    at H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\config\defaults.js:822:11
    at F (H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\config\defaults.js:73:15)
    at applyOutputDefaults (H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\config\defaults.js:803:2)
    at applyWebpackOptionsDefaults (H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\config\defaults.js:197:2)
    at createCompiler (H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\webpack.js:77:2)
    at create (H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\webpack.js:134:16)
    at webpack (H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\webpack.js:142:47)
    at WebpackCLI.f [as webpack] (H:\#github_rep\ajs-alexdm\node_modules\webpack\lib\index.js:64:16)
    at WebpackCLI.createCompiler (H:\#github_rep\ajs-alexdm\node_modules\webpack-cli\lib\webpack-cli.js:1789:29)
    at async WebpackCLI.runWebpack (H:\#github_rep\ajs-alexdm\node_modules\webpack-cli\lib\webpack-cli.js:1890:20)
	
	
Сделал измения в файле .browserslistrc:
так указанно в задании:

last 1 version
> 1%
maintained node versions
not dead

так сделал я:

> 1%

В итоге ответ выполненения npm run build:

PS H:\#github_rep\ajs-alexdm> npm run build

> @alekseyad/ajs-alexdm@1.0.0 build
> webpack --mode production

asset index.js 549 bytes [emitted] [minimized] (name: main)
runtime modules 396 bytes 2 modules
../../#github_rep/ajs-alexdm/src/index.js 142 bytes [built] [code generated]
webpack 5.74.0 compiled successfully in 3819 ms

Я так понимаю все прошло удачно.
