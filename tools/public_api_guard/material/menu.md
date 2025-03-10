## API Report File for "components-srcs"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AfterContentInit } from '@angular/core';
import { AfterViewInit } from '@angular/core';
import { AnimationEvent as AnimationEvent_2 } from '@angular/animations';
import { AnimationTriggerMetadata } from '@angular/animations';
import { Direction } from '@angular/cdk/bidi';
import { EventEmitter } from '@angular/core';
import { FocusableOption } from '@angular/cdk/a11y';
import { FocusOrigin } from '@angular/cdk/a11y';
import * as i0 from '@angular/core';
import * as i1 from '@angular/material/core';
import * as i2 from '@angular/cdk/overlay';
import * as i7 from '@angular/cdk/scrolling';
import { InjectionToken } from '@angular/core';
import { Observable } from 'rxjs';
import { OnDestroy } from '@angular/core';
import { OnInit } from '@angular/core';
import { Overlay } from '@angular/cdk/overlay';
import { QueryList } from '@angular/core';
import { ScrollStrategy } from '@angular/cdk/overlay';
import { Subject } from 'rxjs';
import { TemplateRef } from '@angular/core';

// @public @deprecated (undocumented)
export const fadeInItems: AnimationTriggerMetadata;

// @public
export const MAT_MENU_CONTENT: InjectionToken<MatMenuContent>;

// @public
export const MAT_MENU_DEFAULT_OPTIONS: InjectionToken<MatMenuDefaultOptions>;

// @public
export const MAT_MENU_PANEL: InjectionToken<MatMenuPanel<any>>;

// @public
export const MAT_MENU_SCROLL_STRATEGY: InjectionToken<() => ScrollStrategy>;

// @public
export const MAT_MENU_SCROLL_STRATEGY_FACTORY_PROVIDER: {
    provide: InjectionToken<() => ScrollStrategy>;
    deps: (typeof Overlay)[];
    useFactory: typeof MAT_MENU_SCROLL_STRATEGY_FACTORY;
};

// @public (undocumented)
export class MatMenu implements AfterContentInit, MatMenuPanel<MatMenuItem>, OnInit, OnDestroy {
    constructor(...args: unknown[]);
    // (undocumented)
    addItem(_item: MatMenuItem): void;
    _allItems: QueryList<MatMenuItem>;
    readonly _animationDone: Subject<AnimationEvent_2>;
    ariaDescribedby: string;
    ariaLabel: string;
    ariaLabelledby: string;
    backdropClass: string;
    // @deprecated
    get classList(): string;
    set classList(classes: string);
    _classList: {
        [key: string]: boolean;
    };
    // @deprecated
    readonly close: EventEmitter<MenuCloseReason>;
    readonly closed: EventEmitter<MenuCloseReason>;
    _directDescendantItems: QueryList<MatMenuItem>;
    direction: Direction;
    focusFirstItem(origin?: FocusOrigin): void;
    _handleKeydown(event: KeyboardEvent): void;
    hasBackdrop?: boolean;
    _hovered(): Observable<MatMenuItem>;
    _isAnimating: boolean;
    // @deprecated
    items: QueryList<MatMenuItem>;
    lazyContent: MatMenuContent;
    // (undocumented)
    static ngAcceptInputType_hasBackdrop: any;
    // (undocumented)
    static ngAcceptInputType_overlapTrigger: unknown;
    // (undocumented)
    ngAfterContentInit(): void;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    ngOnInit(): void;
    _onAnimationDone(event: AnimationEvent_2): void;
    // (undocumented)
    _onAnimationStart(event: AnimationEvent_2): void;
    overlapTrigger: boolean;
    overlayPanelClass: string | string[];
    _panelAnimationState: 'void' | 'enter';
    set panelClass(classes: string);
    // (undocumented)
    readonly panelId: string;
    parentMenu: MatMenuPanel | undefined;
    // @deprecated
    removeItem(_item: MatMenuItem): void;
    resetActiveItem(): void;
    _resetAnimation(): void;
    setElevation(depth: number): void;
    setPositionClasses(posX?: MenuPositionX, posY?: MenuPositionY): void;
    _startAnimation(): void;
    templateRef: TemplateRef<any>;
    get xPosition(): MenuPositionX;
    set xPosition(value: MenuPositionX);
    get yPosition(): MenuPositionY;
    set yPosition(value: MenuPositionY);
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<MatMenu, "mat-menu", ["matMenu"], { "backdropClass": { "alias": "backdropClass"; "required": false; }; "ariaLabel": { "alias": "aria-label"; "required": false; }; "ariaLabelledby": { "alias": "aria-labelledby"; "required": false; }; "ariaDescribedby": { "alias": "aria-describedby"; "required": false; }; "xPosition": { "alias": "xPosition"; "required": false; }; "yPosition": { "alias": "yPosition"; "required": false; }; "overlapTrigger": { "alias": "overlapTrigger"; "required": false; }; "hasBackdrop": { "alias": "hasBackdrop"; "required": false; }; "panelClass": { "alias": "class"; "required": false; }; "classList": { "alias": "classList"; "required": false; }; }, { "closed": "closed"; "close": "close"; }, ["lazyContent", "_allItems", "items"], ["*"], true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatMenu, never>;
}

// @public
export const matMenuAnimations: {
    readonly transformMenu: AnimationTriggerMetadata;
    readonly fadeInItems: AnimationTriggerMetadata;
};

// @public
export class MatMenuContent implements OnDestroy {
    constructor(...args: unknown[]);
    attach(context?: any): void;
    readonly _attached: Subject<void>;
    detach(): void;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatMenuContent, "ng-template[matMenuContent]", never, {}, {}, never, never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatMenuContent, never>;
}

// @public
export interface MatMenuDefaultOptions {
    backdropClass: string;
    hasBackdrop?: boolean;
    overlapTrigger: boolean;
    overlayPanelClass?: string | string[];
    xPosition: MenuPositionX;
    yPosition: MenuPositionY;
}

// @public
export class MatMenuItem implements FocusableOption, AfterViewInit, OnDestroy {
    constructor(...args: unknown[]);
    _checkDisabled(event: Event): void;
    disabled: boolean;
    disableRipple: boolean;
    focus(origin?: FocusOrigin, options?: FocusOptions): void;
    readonly _focused: Subject<MatMenuItem>;
    _getHostElement(): HTMLElement;
    getLabel(): string;
    _getTabIndex(): string;
    _handleMouseEnter(): void;
    // (undocumented)
    _hasFocus(): boolean;
    _highlighted: boolean;
    readonly _hovered: Subject<MatMenuItem>;
    // (undocumented)
    static ngAcceptInputType_disabled: unknown;
    // (undocumented)
    static ngAcceptInputType_disableRipple: unknown;
    // (undocumented)
    ngAfterViewInit(): void;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    _parentMenu?: MatMenuPanel<MatMenuItem> | null | undefined;
    role: 'menuitem' | 'menuitemradio' | 'menuitemcheckbox';
    // (undocumented)
    _setHighlighted(isHighlighted: boolean): void;
    // (undocumented)
    _setTriggersSubmenu(triggersSubmenu: boolean): void;
    _triggersSubmenu: boolean;
    // (undocumented)
    static ɵcmp: i0.ɵɵComponentDeclaration<MatMenuItem, "[mat-menu-item]", ["matMenuItem"], { "role": { "alias": "role"; "required": false; }; "disabled": { "alias": "disabled"; "required": false; }; "disableRipple": { "alias": "disableRipple"; "required": false; }; }, {}, never, ["mat-icon, [matMenuItemIcon]", "*"], true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatMenuItem, never>;
}

// @public (undocumented)
export class MatMenuModule {
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatMenuModule, never>;
    // (undocumented)
    static ɵinj: i0.ɵɵInjectorDeclaration<MatMenuModule>;
    // (undocumented)
    static ɵmod: i0.ɵɵNgModuleDeclaration<MatMenuModule, never, [typeof i1.MatRippleModule, typeof i1.MatCommonModule, typeof i2.OverlayModule, typeof i3.MatMenu, typeof i4.MatMenuItem, typeof i5.MatMenuContent, typeof i6.MatMenuTrigger], [typeof i7.CdkScrollableModule, typeof i3.MatMenu, typeof i1.MatCommonModule, typeof i4.MatMenuItem, typeof i5.MatMenuContent, typeof i6.MatMenuTrigger]>;
}

// @public
export interface MatMenuPanel<T = any> {
    // @deprecated (undocumented)
    addItem?: (item: T) => void;
    // (undocumented)
    backdropClass?: string;
    // (undocumented)
    readonly close: EventEmitter<void | 'click' | 'keydown' | 'tab'>;
    // (undocumented)
    direction?: Direction;
    // (undocumented)
    focusFirstItem: (origin?: FocusOrigin) => void;
    // (undocumented)
    hasBackdrop?: boolean;
    // (undocumented)
    lazyContent?: MatMenuContent;
    // (undocumented)
    overlapTrigger: boolean;
    // (undocumented)
    overlayPanelClass?: string | string[];
    // (undocumented)
    readonly panelId?: string;
    // (undocumented)
    parentMenu?: MatMenuPanel | undefined;
    // @deprecated (undocumented)
    removeItem?: (item: T) => void;
    // (undocumented)
    resetActiveItem: () => void;
    // (undocumented)
    setElevation?(depth: number): void;
    // (undocumented)
    setPositionClasses?: (x: MenuPositionX, y: MenuPositionY) => void;
    // (undocumented)
    templateRef: TemplateRef<any>;
    // (undocumented)
    xPosition: MenuPositionX;
    // (undocumented)
    yPosition: MenuPositionY;
}

// @public
export class MatMenuTrigger implements AfterContentInit, OnDestroy {
    constructor(...args: unknown[]);
    closeMenu(): void;
    // @deprecated (undocumented)
    get _deprecatedMatMenuTriggerFor(): MatMenuPanel | null;
    set _deprecatedMatMenuTriggerFor(v: MatMenuPanel | null);
    get dir(): Direction;
    focus(origin?: FocusOrigin, options?: FocusOptions): void;
    _handleClick(event: MouseEvent): void;
    _handleKeydown(event: KeyboardEvent): void;
    _handleMousedown(event: MouseEvent): void;
    get menu(): MatMenuPanel | null;
    set menu(menu: MatMenuPanel | null);
    readonly menuClosed: EventEmitter<void>;
    menuData: any;
    get menuOpen(): boolean;
    readonly menuOpened: EventEmitter<void>;
    // (undocumented)
    ngAfterContentInit(): void;
    // (undocumented)
    ngOnDestroy(): void;
    // @deprecated
    readonly onMenuClose: EventEmitter<void>;
    // @deprecated
    readonly onMenuOpen: EventEmitter<void>;
    // (undocumented)
    _openedBy: Exclude<FocusOrigin, 'program' | null> | undefined;
    openMenu(): void;
    restoreFocus: boolean;
    toggleMenu(): void;
    triggersSubmenu(): boolean;
    updatePosition(): void;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<MatMenuTrigger, "[mat-menu-trigger-for], [matMenuTriggerFor]", ["matMenuTrigger"], { "_deprecatedMatMenuTriggerFor": { "alias": "mat-menu-trigger-for"; "required": false; }; "menu": { "alias": "matMenuTriggerFor"; "required": false; }; "menuData": { "alias": "matMenuTriggerData"; "required": false; }; "restoreFocus": { "alias": "matMenuTriggerRestoreFocus"; "required": false; }; }, { "menuOpened": "menuOpened"; "onMenuOpen": "onMenuOpen"; "menuClosed": "menuClosed"; "onMenuClose": "onMenuClose"; }, never, never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<MatMenuTrigger, never>;
}

// @public @deprecated
export const MENU_PANEL_TOP_PADDING = 8;

// @public
export type MenuCloseReason = void | 'click' | 'keydown' | 'tab';

// @public
export type MenuPositionX = 'before' | 'after';

// @public (undocumented)
export type MenuPositionY = 'above' | 'below';

// @public @deprecated (undocumented)
export const transformMenu: AnimationTriggerMetadata;

// (No @packageDocumentation comment for this package)

```
