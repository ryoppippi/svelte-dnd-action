## Svelte Dnd Action - Release Notes

### [0.9.64](https://github.com/isaacHagoel/svelte-dnd-action/pull/657)

Bugfix: change the handling of positioning the shadow element as the last child to support complex layouts like flex-wrap

### [0.9.63](https://github.com/isaacHagoel/svelte-dnd-action/pull/652)

Feature: Added `delayTouchStart` option to improve touch-device UX.

-   Allows distinguishing quick scroll gestures from drag starts.
-   Accepts **boolean** (`true` = 80 ms default) or **number** (custom delay in ms).

### [0.9.62](https://github.com/isaacHagoel/svelte-dnd-action/pull/651)

Bugfix: the dragHandle now respects the `dragDisabled` prop

### [0.9.61](https://github.com/isaacHagoel/svelte-dnd-action/pull/645)

Bugfix: Fixed an issue in `dragHandle` where clicking and releasing without dragging left `isItemsDragDisabled` as `false`, making the entire element draggable.

### [0.9.60](https://github.com/isaacHagoel/svelte-dnd-action/pull/639)

Bugfix: the touchend listener was emulating a click using the click() function and that broke when the user clicked on an SVG

### [0.9.59](https://github.com/isaacHagoel/svelte-dnd-action/pull/638)

Bugfix: fixed an issue that affected $state (for items) that was introduced by version 0.9.58

### [0.9.58](https://github.com/isaacHagoel/svelte-dnd-action/pull/636)

Svelte 5 $state users (if you store items as $state) - please skip this version!
Bugfix: when the items in the origin zone shrink in height right on drag start, the pointer would find itself outside the dragged element

### [0.9.57](https://github.com/isaacHagoel/svelte-dnd-action/pull/629)

Readme update (`on` vs `on:` handlers in Svelte 5)

### [0.9.56](https://github.com/isaacHagoel/svelte-dnd-action/pull/628)

Fixed dndzones inside an element with the 'popover' attribute

### [0.9.55](https://github.com/isaacHagoel/svelte-dnd-action/pull/626)

Fixed logic that could leave the shadow element invisible after drop if the dom wasn't yet updated to reflect the data list (rare)

### [0.9.54](https://github.com/isaacHagoel/svelte-dnd-action/pull/621)

Readme REPL links updated repl -> playground

### [0.9.53](https://github.com/isaacHagoel/svelte-dnd-action/pull/618)

Added a check to address edge cases where multiScroller is undefined when accessed on destroy

### [0.9.52](https://github.com/isaacHagoel/svelte-dnd-action/pull/610)

Fixed a bug that affected dndzone inside scrollable parents - calculated the target index incorrectly when the element was above a hidden part of the zone

### [0.9.51](https://github.com/isaacHagoel/svelte-dnd-action/pull/608)

Added the option to disable the final drop animation

### [0.9.50](https://github.com/isaacHagoel/svelte-dnd-action/pull/598)

Fixed a bug where library would crash when a store updated "considers" in local storage from another tab

### [0.9.49](https://github.com/isaacHagoel/svelte-dnd-action/pull/588)

Fixed a bug where library would crash if one of the canvas had an empty size

### [0.9.48](https://github.com/isaacHagoel/svelte-dnd-action/pull/582)

Fixed a bug where the scroller would stay active and scroll the page after drop

### [0.9.47](https://github.com/isaacHagoel/svelte-dnd-action/pull/578)

Added examples to the README (for the drag handles wrapper actions).

### [0.9.46](https://github.com/isaacHagoel/svelte-dnd-action/pull/576)

Added two wrapper actions (`dragHandleZone` and `dragHandle`) to make using drag handle easy.

### [0.9.45](https://github.com/isaacHagoel/svelte-dnd-action/pull/573)

Bug fix - calling transformDraggedElement after the element was morphed so that changes transform makes aren't overridden by the morphing.

### [0.9.44](https://github.com/isaacHagoel/svelte-dnd-action/pull/567)

Allows Svelte 5.0.0-next as peer dependency.

### [0.9.43](https://github.com/isaacHagoel/svelte-dnd-action/pull/556)

Fixes an issue on some touch devices, where attempting to drag an item causes the page to scroll.

### [0.9.42](https://github.com/isaacHagoel/svelte-dnd-action/pull/553)

Fixes that won't affect most use cases (but do affect recursive nesting).
Fixed updating the items config prior to configure being called.
Restored using the real id throughout the drag operation after the initial frame to prevent issues from implementations relying on it.
This affects the each loop key should be set up when using `data-is-dnd-shadow-item-hint` (see README).

### [0.9.41](https://github.com/isaacHagoel/svelte-dnd-action/pull/549)

The library can now scroll dropzones and any scrollable element that contains dropzones inside, including the window.
This happens when the mouse pointer is near one of the edges of a scrollable container during drag.

### [0.9.40](https://github.com/isaacHagoel/svelte-dnd-action/pull/542)

Added custom events typings with generics to support TypeScript out of the box.

### [0.9.39](https://github.com/isaacHagoel/svelte-dnd-action/pull/538)

Updated README to help set up sveltekit + typescript

### [0.9.38](https://github.com/isaacHagoel/svelte-dnd-action/pull/533)

Added fault tolerance for use cases in which the user removes the shadow item from the list (e.g zones with limited slots)

### [0.9.37](https://github.com/isaacHagoel/svelte-dnd-action/pull/532)

Added support for class instances as list items

### [0.9.36](https://github.com/isaacHagoel/svelte-dnd-action/pull/528)

Added `import` and `require` to the export block in package.json so that types are properly resolved.

### [0.9.35](https://github.com/isaacHagoel/svelte-dnd-action/pull/527)

Added an export block to package.json to remove a Svelte 5 (actually vite) warning about the deprecated "svelte" entry

### [0.9.34](https://github.com/isaacHagoel/svelte-dnd-action/pull/524)

Don't use this version please. It has a silly mistake that cause an error with Sveltekit 2

### [0.9.33](https://github.com/isaacHagoel/svelte-dnd-action/pull/499)

bugfix - now works properly inside a `<dialog>` element

### [0.9.32](https://github.com/isaacHagoel/svelte-dnd-action/pull/517)

Fixed canvas content not getting cloned on dragged node.

### [0.9.31](https://github.com/isaacHagoel/svelte-dnd-action/pull/496)

Introduce zoneItemTabindex - It allows the user to set custom tabindex to the list container items when not dragging. Can be useful if you use [Drag handles](https://github.com/isaacHagoel/svelte-dnd-action#examples-and-recipes)

### [0.9.30](https://github.com/isaacHagoel/svelte-dnd-action/pull/493)

This version introduces a way for the user to set the flipdurationms to 0, and have it actually have 0 animation (20ms or 1 frame animation). Useful for gaming
as before the 100ms minimum made it so that it was too slow.

### [0.9.29](https://github.com/isaacHagoel/svelte-dnd-action/pull/488)

This version addresses some issues around nested zones. By-default the shadow element now has a temporary id until it's dropped.
This version also adds the option to provide a hint data attribute (`data-is-dnd-shadow-item-hint`) that helps the lib optimise when there is a lot of nesting (see readme).

### [0.9.28](https://github.com/isaacHagoel/svelte-dnd-action/pull/484)

A revert of the problematic part in 0.9.27. This version is functionally equal to 0.9.26

### [0.9.27](https://github.com/isaacHagoel/svelte-dnd-action/pull/481)

PLEASE DON'T USE THIS VERSION
An unsuccessful attempt to support for dropzone being added mid-drag. It breaks in nested scenarios.

### [0.9.26](https://github.com/isaacHagoel/svelte-dnd-action/pull/476)

Readme typo fix in an example: setFeatueFlag -> setFeatureFlag

### [0.9.25](https://github.com/isaacHagoel/svelte-dnd-action/pull/473)

Made the fix that was introduced in version 0.9.23 available via feature flag but inactive by default

### [0.9.24](https://github.com/isaacHagoel/svelte-dnd-action/pull/459)

Updated readme with Svelte 4 types configuration

### [0.9.23](https://github.com/isaacHagoel/svelte-dnd-action/pull/457)

Fix morphing when within css grid

### [0.9.22](https://github.com/isaacHagoel/svelte-dnd-action/pull/410)

Fix repl examples in Readme. Add svelte >=3.23.0 as peerDependency

### [0.9.21](https://github.com/isaacHagoel/svelte-dnd-action/pull/405)

transformDraggedElement is called even if morphing is disabled and a bug that has to do with morphing is now fixed (it was moving the element before styling it)

### [0.9.20](https://github.com/isaacHagoel/svelte-dnd-action/pull/401)

update README to fix global.d.ts example

### [0.9.19](https://github.com/isaacHagoel/svelte-dnd-action/pull/382)

enhancement: DndEvent now allows the use of generics.

### [0.9.18](https://github.com/isaacHagoel/svelte-dnd-action/pull/365)

fix: if a drop zone is removed mid-drag it was causing the lib to throw errors

### [0.9.17](https://github.com/isaacHagoel/svelte-dnd-action/pull/320)

fix: dropdowns (select elements) will now maintain their value during drag

### [0.9.16](https://github.com/isaacHagoel/svelte-dnd-action/pull/356)

fixed a bug that made dropTargetClasses and dropTarget styles work incorrectly when applied to nested zones

### [0.9.15](https://github.com/isaacHagoel/svelte-dnd-action/pull/350)

made the aria support more friendly for multi-page apps (ex: SvelteKit) by having the lib lazy init and clean up the aria divs when the last instance is removed

### [0.9.14](https://github.com/isaacHagoel/svelte-dnd-action/pull/340/)

fixed an issue with items sometimes not making way for the dragged element after autoscroll

### [0.9.13](https://github.com/isaacHagoel/svelte-dnd-action/pull/331/)

fixed the typescript type for dropTargetClasses

### [0.9.12](https://github.com/isaacHagoel/svelte-dnd-action/pull/328/)

added a link example for a basic implementation of multi-drag in the README

### [0.9.11](https://github.com/isaacHagoel/svelte-dnd-action/pull/315/)

added a new option, `zoneTabIndex`, that allows to set custom tabindex in the list container.

### 0.9.10

Please do not use. It was deployed with unintended changes

### [0.9.9](https://github.com/isaacHagoel/svelte-dnd-action/pull/301)

bugfix - works properly when under shadow dom

### [0.9.7](https://github.com/isaacHagoel/svelte-dnd-action/pull/290)

bugfix - works properly now when dropFromOtherDisabled is set to true while the shadow element is in the zone

### [0.9.5](https://github.com/isaacHagoel/svelte-dnd-action/pull/271)

added a new option, `morphDisabled`, that allows to disable morphing of dragged item.

### [0.9.4](https://github.com/isaacHagoel/svelte-dnd-action/pull/274)

bug fix - not crashing when a new dnd zone is created mid drag

### [0.9.3](https://github.com/isaacHagoel/svelte-dnd-action/pull/273)

exporting `DRAGGED_ELEMENT_ID` to allow targeting the dragged element and its subtree using CSS or to fetch it with `document.getElementById`.

### [0.9.2](https://github.com/isaacHagoel/svelte-dnd-action/pull/264)

fixed a race condition that could happen under extremely rapid drag-start -> drop while spam-clicking feverishly

### [0.9.1](https://github.com/isaacHagoel/svelte-dnd-action/pull/256)

exporting `SHADOW_PLACEHOLDER_ITEM_ID` for easier filtering in recursive zones use-cases

### [0.9.0](https://github.com/isaacHagoel/svelte-dnd-action/pull/250)

added the `centreDraggedOnCursor` option to deal with zones that have large items (wide, tall or both) in them that can be dragged over much smaller items. <br/>
in these cases, having the center of the items (which is the focal point that triggers all dnd events), and the cursor be the same point makes it more intuitive to drag the large items around.

### [0.8.6](https://github.com/isaacHagoel/svelte-dnd-action/pull/231)

fixed an issue when dragging an item on top of a droppedFromItemsDisabled zone (it is treated as outside of any now, as it should)

### [0.8.4](https://github.com/isaacHagoel/svelte-dnd-action/pull/226)

fixed a keyboard related bug - it is now possible to tab back to the dragged item after tabbing to external elements mid drag

### [0.8.2](https://github.com/isaacHagoel/svelte-dnd-action/pull/221)

accessibility features now work when the library is dynamically imported (in other words, keyboard navigation now works in the REPL again).

### [0.8.1](https://github.com/isaacHagoel/svelte-dnd-action/pull/220)

Made `dropTargetClasses` when initiating drag via keyboard.

### [v0.8.0](https://github.com/isaacHagoel/svelte-dnd-action/pull/218)

Added a new option, `dropTargetClasses`, that allows adding global classes to a dnd-zone when it is a potential drop target (during drag).

### [v0.7.4](https://github.com/isaacHagoel/svelte-dnd-action/pull/213)

This release introduces a subtle change to the dragStarted event. <br />
If you are using [Dragula Copy on Drag](https://svelte.dev/playground/924b4cc920524065a637fa910fe10193?version=3.31.2), you will need to update your consider handler (add 1 line of code to remove the newly added shadow placeholder, see linked REPL). <br />
Same goes for the [crazy nesting](https://svelte.dev/playground/fe8c9eca04f9417a94a8b6041df77139?version=3.31.2) example <br />
Starting with this version, the initial consider event (dragStarted) places a placeholder item with a new id instead of the dragged item in the items list (old behaviour: removing the dragged item from the list altogether). The placeholder is replaced with the real shadow element (the one that has the same id as the original item) in the next event (basically instantly).
This change makes the initial behaviour of large items (relative to their peers) much smoother.

### [v0.7.0](https://github.com/isaacHagoel/svelte-dnd-action/pull/202)

All the changes in this release only affect pointer (mouse/ touch) based drag and drop operations.
It changes some default behaviours (for the better).

-   When an element is being dragged outside of any dnd zone, the placeholder element now appears in the original dnd zone in the original index and indicates where the element would land if dropped. This was added for better UX and to address single sortable list use cases.
-   This change includes the introduction of two new triggers, that can be intercepted by the `consider` handler: `DRAGGED_LEFT_ALL` which fires when the placeholder is added to the origin dndzone, and `DRAGGED_ENTERED_ANOTHER` which fires when the placeholder is removed from the origin dnd zone.
-   When drag starts - the library now locks the minimum width and height of the origin dropzone for the duration of the drag operation. This is done in order to prevent the container from shrinking and growing jarringly as the element is dragged around. This is especially helpful when the user drags the last element, which in previous versions could make the dndzone shrink underneath such that the dragged element wasn't over it anymore.
