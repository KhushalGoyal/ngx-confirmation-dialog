
# NgxConfirmationDialog

  

This library was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.2.0.

  

# ngx-confirmation-dialog

  

Directive to be used very time if you want to delete or edit a record from table or anythwhere you want. You can customize the button name also.

  

# Instalation

``` npm install git+https://git@github.com/KhushalGoyal/ngx-confirmation-dialog.git ```

  

# Setup

Add below import in app.module

```
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
@NgModule({
	imports : [
		BrowserAnimationsModule
	]
})
```

  

Add below imports in module file, in which you want to add the given directive

```

import { NgxConfirmationDialogModule, NgxConfirmationDialogComponent } from 'ngx-confirmation-dialog';

@NgModule({
	imports : [
		NgxConfirmationDialogModule
	],
	entryComponents: [
		NgxConfirmationDialogComponent
	]
})

```

Add below lines in styles.css

```
@import '~@angular/cdk/overlay-prebuilt.css';
.mat-dialog-container{
	background-color: #ffffff;
} 
```

Directive which is to be called from the given module

```
<button m-confirmation-message-ok="Delete" m-confirmation-message='Are you sure you want to delete?' (confirm)="delete_(element)">Show Dialog</button>

```

  

# Configuration
Directive | Description | Default
--- | --- | ---
 m-confirmation-message | Message which is to be shown on the dialog box | Are you sure ?
  m-confirmation-message-ok | Button text to be shown on dialog | Ok 
 confirm | Call back event emitter if user press "Ok" | delete_(this) 

*Note :* Default method "delete_" should be declared in ts file of the component / module.