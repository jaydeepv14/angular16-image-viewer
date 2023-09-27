# NgxImageViewer

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 16.1.2

## Features

- Configurable
- Resizeble component
- Supports JPEG, PNG, GIF
- Support File Objects
- Avaliable actions:
  - **Rotate**
  - **Zoom**
  - Reset to maximize size
  - Free movable

Optionaly, you can also install the font library via npm

> when using another icon font, you should provide a config object with the button icon mapping

## Basic Usage

After import the module `ImageViewerModule`:

```typescript
import { NgxImageViewerModule } from '@jay_vish/angular16-image-viewer';

@NgModule({
  imports: [NgxImageViewerModule],
})
export class AppModule {}

//component.ts
previewConfig = {
    btnClass: 'default', // The CSS class(es) that will apply to the buttons
    zoomFactor: 0.1, // The amount that the scale will be increased by
    containerBackgroundColor: '#ccc', // The color to use for the background. This can provided in hex, or rgb(a).
    wheelZoom: true, // If true, the mouse wheel can be used to zoom in
    allowFullscreen: true, // If true, the fullscreen button will be shown, allowing the user to entr fullscreen mode
    allowKeyboardNavigation: true, // If true, the left / right arrow keys can be used for navigation
    btnIcons: { // The icon classes that will apply to the buttons. By default, font-awesome is used.
      zoomIn: 'fa fa-plus',
      zoomOut: 'fa fa-minus',
      rotateClockwise: 'fa fa-repeat',
      rotateCounterClockwise: 'fa fa-undo',
      next: 'fa fa-arrow-right',
      prev: 'fa fa-arrow-left',
      fullscreen: 'fa fa-arrows-alt',
    },
    btnShow: {
      zoomIn: true,
      zoomOut: true,
      rotateClockwise: true,
      rotateCounterClockwise: true,
      next: false,
      prev: false
    }
  };
```

Use the follow code on your html:

```html
<ngx-imageviewer [src]="imageSrc" [(config)]="previewConfig" />
```

Optionaly, you can provide the fields `width` and `height`. If you omit those values, the width and height in the config object will be used.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
