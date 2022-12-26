## Setting up your environment

1. Download [Visual Studio Code](https://code.visualstudio.com/)

2. In VS Code install the following extensions:
   * `Live Server` by **Ritwick Dey**
   * `Live Sass Compiler` by **Glenn Marks**

3. Press `ctrl`+`shift`+`p` to open the command palette and type `Open User Settings (JSON)`

4. At the end of the JSON file, add 
   ```json
    "liveSassCompile.settings.formats": [
      {
        "format": "expanded",
        "extensionName": ".css",
        "savePath": "/dist",
        "savePathReplacementPairs": null
      }
    ],
   ```

5. To watch your Sass files, click on the button that says `Watch Sass` at the bottom of VS Code. A `dist` folder will automatically be generated.
