# Citavi projects

This repository serves as an overview of all projects related to the literature management software Citavi. My work is divided into macros I use to quickly read information and useful tools in form of addons.

## Macros

- [ShowLoadedAddonsMacro](/macros/cm001.md)
- [ShowPDFNetVersionMacro](/macros/cm002.md)

## Addons

- [AddCitaviProjectToRecentListAddon](https://github.com/lutz/AddCitaviProjectToRecentListAddon)
- [AutoRefAddon](https://github.com/lutz/AutoRefAddon)
- [CopyTextOfSelectedAnnotationAddon](https://github.com/lutz/CopyTextOfSelectedAnnotationAddon)
- [DocFetcherSelectionAddon](https://github.com/lutz/DocFetcherSelectionAddon)
- [FormatCodeAddon](https://github.com/lutz/FormatCodeAddon)
- [GoToPdfPageAddon](https://github.com/lutz/GoToPdfPageAddon)
- [HideKnowledgeItemFileFormHelpBoxAddon](https://github.com/lutz/HideKnowledgeItemFileFormHelpBoxAddon)
- [HideKnowledgeItemTextFormHelpBoxAddon](https://github.com/lutz/HideKnowledgeItemTextFormHelpBoxAddon)
- [JumpToLastPositionAfterActionExecutionAddon](https://github.com/lutz/JumpToLastPositionAfterActionExecutionAddon)
- [KnownProjectsCleanerAddon](https://github.com/lutz/KnownProjectsCleanerAddon)
- [OpenWithAddon](https://github.com/lutz/OpenWithAddon)
- [PDFSplitAddon](https://github.com/lutz/PDFSplitAddon)
- [PDFThumbnailAddon](https://github.com/lutz/PDFThumbnailAddon)
- [SetPDFSelectionAsAddon](https://github.com/lutz/SetPDFSelectionAsAddon)
- [SynchronizeFiltersWithFullscreenPreviewAddon](https://github.com/lutz/SynchronizeFiltersWithFullscreenPreviewAddon)

## FAQ

### How do I use a macro?

1. Start Citavi.
2. Open the macro editor (_Tools > Macro Editor..._)
3. Remove the template code and paste the macro code.
4. Press the **Compile** button.
5. If no errors showed in the error list, press the **Run** button

### How do I install an addon?

1. Shut down Citavi.
2. Download the desired add-on from the internet (usually a ZIP archive).
3. Unzip the ZIP archive with the right mouse button using the command "Extract All".
4. Copy the unzipped files into the directory "[installation directory]\AddOns" (usually `C:\Program Files (x86)\Citavi 6\AddOns`). You may have to create the folder _AddOns_ when using it for the first time!
5. Start Citavi

### Is there any cost associated with using macros or addons?

You may freely use, modify and distribute the macros and addons available here for any purpose or cost. Please note only the license terms under which these macros and addons are published.

### I want develop my own addon. How can i find material?

There is no official documentation or instructions for programming Citavi add-ons. The first way should be via the old German tutorial on Citavi 3 add-ons, which can be found in the [wiki](https://github.com/Citavi/C6-Add-Ons-and-Online-Sources/wiki) of the public [Citavi 6 add-on repository](https://github.com/Citavi/C6-Add-Ons-and-Online-Sources). Although this is an old tutorial, the basic principles are the same. In addition, there are several examples of add-ons, whose source code gives a first overview. Also my add-ons published [here](https://github.com/lutz/CitaviProjects#addons) can be viewed and developed further.

### Is there a way to develop an addon for unsupported form?

Currently the official Citavi addon api supports some kind of citavi forms but not all. So i have developed a extended version of the `CitaviAddOn` class. More informations you will find [here](https://github.com/lutz/CitaviAddOnEx).

### Is it possible to call `async` methods in macros?

Absolutely yes. To use `async` and `await` the modern way of asynchronous developing you can change the return value of the `Main` method to `Task` and add the function word `async`to the signature. If you want consistently in naming you can use `MainAsync` instead of `Main`. There is one aspect to consider. If you use asynchronous methods the gui is not blocked anymore (in general not everytime :sweat_smile:). So in this case it could be helpfull to show a progress dialog to avoid user handling. Citavi is shipped with a huge customizable dialog for this use case called `GenericProgressDialog`. An example macro you will find here with some comments.

## Disclaimer

> There are no support claims by the company **Swiss Academic Software GmbH**, the provider of **Citavi** or other liability claims for problems or data loss. Any use is at your own risk. All rights to the name **Citavi** and any logos used are owned by **Swiss Academic Software GmbH**.

## License

This project is licensed under the [MIT](LICENSE) License
