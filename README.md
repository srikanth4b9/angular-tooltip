# Tooltip


Dowload `tooltip` folder and place anywhere within code and import `TooltipModule` in app.module.ts of your application.

## Usage

Options can be set in the directive tag, so they have the highest priority.

```html
<span tooltip="Tooltip text" placement="top" showDelay="500">Tooltip on top</span>
```

On Angular material button.. `autoPlacement: boolean = false`, if you want to override placement other than `top`

```html

<button mat-raised-button
        tooltip="Info about the action"
        [autoPlacement]="autoPlacement"
        placement="right"
        aria-label="Button that displays a tooltip when focused or hovered over">
  Action
</button>
```

You may pass `options` as an object:

```html
<span tooltip="Tooltip text" [options]="myOptions"> Tooltip on left </span>
```

```ts
myOptions: TooltipOptions = {
  placement: 'left',
  autoPlacement: false
}
```

## Properties

| name             | type                                | default | description                                 |
|------------------|-------------------------------------|---------|---------------------------------------------|
| placement        | "top", "bottom", "left", "right"    | "top"   | The position of the tooltip.                |
| autoPlacement    | boolean                             | true    | Place the tooltip so that it does not go beyond the borders of the browser window. |
| showDelay       | number                              | 0       | The delay in ms before showing the tooltip. |
| hideDelay       | number                              | 300     | The delay in ms before removing the tooltip. |


