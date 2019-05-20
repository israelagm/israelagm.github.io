# Bootstrap 4

## Media Queries

Bootstrap is developed to be mobile first. Start your designs from mobile and scale up. It's important to note that breakpoints have been update as well.


New screen size ranges:
```json
xs =	<	-	575.98px

sm =	576px	-	767.98px

md =	768px	-	991.98px

lg =	992px	-	1199.98px

xl =	1200px	-	>
```


```css
// Extra small devices (portrait phones, less than 576px)
// No media query necessary for xs breakpoint as it's effectively @media (min-width: 0) { ... }

// Small devices (landscape phones, 576px and up)
@include media-breakpoint-up(sm) { ... }
// compiles to:
@media (min-width: 576px) { ... }

// Medium devices (tablets, 768px and up)
@include media-breakpoint-up(md) { ... }
// compiles to:
@media (min-width: 768px) { ... }

// Large devices (desktops, 992px and up)
@include media-breakpoint-up(lg) { ... }
// compiles to:
@media (min-width: 992px) { ... }

// Extra large devices (large desktops, 1200px and up)
@include media-breakpoint-up(xl) { ... }
// compiles to:
@media (min-width: 1200px) { ... }
```

When you need to go the other direction:
```css
// Extra small devices (portrait phones, less than 576px)
@include media-breakpoint-down(xs) { ... }
// compiles to:
@media (max-width: 575.98px) { ... }

// Small devices (landscape phones, less than 768px)
@include media-breakpoint-down(sm) { ... }
// compiles to:
@media (max-width: 767.98px) { ... }

// Medium devices (tablets, less than 992px)
@include media-breakpoint-down(md) { ... }
// compiles to:
@media (max-width: 991.98px) { ... }

// Large devices (desktops, less than 1200px)
@include media-breakpoint-down(lg) { ... }
// compiles to:
@media (max-width: 1199.98px) { ... }

// Extra large devices (large desktops)
// No media query since the extra-large breakpoint has no upper bound on its width
```

For targeting a single segment of screen sizes using the minimum and maximum breakpoint widths:
```css
// Extra small devices (portrait phones, less than 576px)
@include media-breakpoint-only(xs) { ... }
// compiles to:
@media (max-width: 575.98px) { ... }

// Small devices (landscape phones, 576px and up)
@include media-breakpoint-only(sm) { ... }
// compiles to:
@media (min-width: 576px) and (max-width: 767.98px) { ... }

// Medium devices (tablets, 768px and up)
@include media-breakpoint-only(md) { ... }
// compiles to:
@media (min-width: 768px) and (max-width: 991.98px) { ... }

// Large devices (desktops, 992px and up)
@include media-breakpoint-only(lg) { ... }
// compiles to:
@media (min-width: 992px) and (max-width: 1199.98px) { ... }

// Extra large devices (large desktops, 1200px and up)
@include media-breakpoint-only(xl) { ... }
// compiles to:
@media (min-width: 1200px) { ... }
```

If you need to span multiple breakpoint widths:
```css
@include media-breakpoint-between(md, xl) { ... }
// compiles to:
@media (min-width: 768px) and (max-width: 1199.98px) { ... }

```