# All you need to setup for post css and sass preprocessor set up

# Sass Install and Setup to the directory

-   Extension: Live Sass Compiler

-   Install-Command:

          sudo npm install -g sass

-   Link the directory:

          sass --watch assets/sass/style.sass assets/styles/style.css

Live Sass Compiler Workspace Settings:

    {
        "prettier.tabWidth": 4,
        "liveSassCompile.settings.autoprefix": [],
        "liveSassCompile.settings.includeItems": ["/assets/sass/style.sass"],
        "liveSassCompile.settings.formats": [
            { 
                "format": "compressed", 
                "extensionName": ".min.css",
                "savePath": "/assets/styles" 
            }
        ]
    }

# Webkit Install Process

-   Install-command:

          npm i -G postcss postcss-cli

-   Also Install:

          npm i -D postcss-preset-env

- Usage-command: 
    
        npx postcss assets/styles/style.css -o assets/styles/output.css -w

- At last: 

        npm install

<h1>Create File to the Main directory</h1>

- File Name: postcss.config.js

-   Setup:

          module.exports = {
              plugins: [require("postcss-preset-env")],
          };

- File Name: .browserslistrc

- Setup:

        last 5 versions
        >0.5%
        IE 10
