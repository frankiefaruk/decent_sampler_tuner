# Decent Sampler Tuner

This application allows you to easily view and modify `.dspreset` files used by Decent Sampler. You can adjust tuning for individual notes, rename image files referenced within the preset, and modify keyboard color ranges directly from a user-friendly interface.

## Features

-   **Load .dspreset files**: Upload your Decent Sampler preset files for editing.
-   **Tuning Adjustment**:
    -   Visualize a keyboard with editable tuning values (in cents) for each note.
    -   Apply Turkish Makam presets (Usak, Rast, Suzinak, Zirguleli Hicaz) based on a selected tonic.
    -   Reset all tuning to standard (0 cents).
-   **Image File Renaming**: Identify image files used in the preset and rename them directly within the app. This updates the references in the XML to match your new file names.
-   **Color Editing**:
    -   Detect and allow modification of color values (hex codes) defined in the XML script.
    -   View and change the background color and dimensions of the UI as defined in the `dspreset` file.
-   **Keyboard Color Customization**:
    -   Analyze and display the defined color ranges for the virtual keyboard in your `dspreset` file.
    -   Edit the colors associated with specific note ranges.
-   **XML Output**: View the modified XML content and copy it to your clipboard for use in Decent Sampler.

## How to Use

1.  **Load a .dspreset file**: Click the "Load .dspreset file" button and select your preset file.
2.  **Adjust UI Dimensions**: (Optional) If your `dspreset` file defines UI dimensions, you can see and edit them in the preview area.
3.  **Tune Notes**:
    -   Use the keyboard interface to manually enter tuning values (in cents) for each note.
    -   Select a tonic from the dropdown.
    -   Click on "Usak Makamı", "Rast Makamı", "Suzinak Makamı", or "Zirguleli Hicaz Makamı" to apply preset tunings relative to your chosen tonic.
    -   Click "Standard Tuning" to reset all note tunings to 0 cents.
4.  **Rename Images**: In the "Image File Renaming" section, if image files are found, you can type new names for them in the input fields. *Do not include the file extension.*
5.  **Edit Colors**: In the "Colors in XML Script" section, you can change any detected color values using the color pickers.
6.  **Edit Keyboard Colors**: In the "Keyboard Colors" section, you can change the colors for specific note ranges using the provided color pickers.
7.  **Update Changes**: After making your desired modifications, click "Update Changes". The modified XML will appear in the output box at the bottom.
8.  **Copy XML**: Click "Copy XML" to copy the generated XML content to your clipboard. You can then paste this into your `.dspreset` file or directly into Decent Sampler.
9.  **Reset All**: Click "Reset All" to clear all inputs and loaded data.

## Important Notes

-   **Save Your Work**: Remember to copy the generated XML and save it back into your `.dspreset` file or directly into Decent Sampler. This application does not automatically save files.
-   **File Extensions**: When renaming image files, only provide the new base name; the original file extension will be preserved automatically.
-   **Tuning Values**: Tuning values are applied to the `tuning` attribute of `<sample>` tags. If a sample does not have a `rootNote`, its tuning will not be modified by the global tuning adjustments.
-   **Error Handling**: The application provides basic feedback for file loading errors.

## Development

This is a single-page HTML application built with standard web technologies (HTML, CSS, JavaScript). No external frameworks or build tools are required.
