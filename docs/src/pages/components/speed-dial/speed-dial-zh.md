---
title: React Speed Dial component
components: SpeedDial, SpeedDialAction, SpeedDialIcon
githubLabel: 'component: SpeedDial'
0: 'https://material.io/components/buttons-floating-action-button#types-of-transitions'
waiAria: 'https://www.w3.org/TR/wai-aria-practices/#menubutton'
---

# Speed Dial 快速拨号

<p class="description">当按下一个浮动操作按钮（floating action button）时，它可以弹出 3 到 6 个以快速拨号形式出现的相关操作。</p>

如果您需要展示六个以上的操作，则应使用除浮动操作按钮之外的其他操作来呈现它们。

{{"component": "modules/components/ComponentLinkHeader.js"}}

## 快速拨号实例

浮动操作按钮可以显示相关操作。

{{"demo": "pages/components/speed-dial/BasicSpeedDial.js"}}

## 自定义关闭图标

您可以使用 `SpeedDialIcon` 组件的 `图标` 和 `openIcon` 道具 为关闭和打开状态提供备用图标。

SpeedDialActions工具提示可以持久显示，这样用户无需长按即可在触摸设备上查看工具提示。

## 自定义关闭图标

您可以使用 `SpeedDialIcon` 组件的 `icon` 和 `openIcon` 属性，给关闭和打开状态提供一个备用的图标。

{{"demo": "pages/components/speed-dial/OpenIconSpeedDial.js"}}

## 恒定不变的操作的工具提示

SpeedDialActions 提示组件可以持续显示，这样一来用户不用长按就能在触摸设备上看到提示内容了。

为了演示的目的，该示例为所有设备都启用了该功能，但在生产环境中，它可以使用 `isTouch` 逻辑来有条件地设置属性。

{{"demo": "pages/components/speed-dial/SpeedDialTooltipOpen.js"}}

## 无障碍设计

### ARIA

#### Required

- You should provide an `ariaLabel` for the speed dial component.
- You should provide a `tooltipTitle` for each speed dial action.

#### Provided

- The Fab has `aria-haspopup`, `aria-expanded` and `aria-controls` attributes.
- The speed dial actions container has `role="menu"` and `aria-orientation` set acccording to the direction.
- The speed dial actions have `role="menuitem"`, and an `aria-describedby` attribute that references the associated tooltip.

### 键盘输入

- The speed dial opens on focus.
- The Space and Enter keys trigger the selected speed dial action, and toggle the speed dial open state.
- The cursor keys move focus to the next or previous speed dial action. (Note that any cursor direction can be used initially to open the speed dial. This enables the expected behavior for the actual or percieved orientation of the speed dial, for example for a screen reader user who percieves the speed dial as a drop-down menu.)
- The Escape key closes the speed dial and, if a speed dial action was focused, returns focus to the Fab.
