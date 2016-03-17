# o-section-head [![Build Status](https://circleci.com/gh/Financial-Times/o-section-head/tree/master.png?style=shield&circle-token=:circle-token)](https://circleci.com/gh/Financial-Times/o-section-head)

Typographic styles and layout for sub-headings. This module contains Sass for section title and a list of related links. This list of related links is optional, and uses o-expander to become collapsable at small screen widths.

## Markup

```
<div class="o-section-head" data-o-component="o-section-head">
	<div class="o-section-head__inner">
		<div class="o-section-head__title-container">
			<h1 class="o-section-head__title">Section title</h1>
		</div>
	  <div class="o-section-head__nav-item-container o-expander"
				data-o-expander-collapsed-toggle-text="RELATED"
				data-o-expander-expanded-toggle-text="RELATED"
				data-o-expander-shrink-to="height"
				data-o-component="o-expander" >
				<button class="o-expander__toggle o--if-js o-section-head__nav-item-toggler">
					RELATED
				</button>
				<nav class="o-section-head__nav-item-list o-expander__content">
	        <a class="o-section-head__nav-item" href='#'>item 1</a>
	        <a class="o-section-head__nav-item" href='#'>item 2</a>
	        <a class="o-section-head__nav-item" href='#'>item 3</a>
	        <a class="o-section-head__nav-item" href='#'>item 4</a>
	        <a class="o-section-head__nav-item" href='#'>item 5</a>
	        <a class="o-section-head__nav-item" href='#'>item 6</a>
	        <a class="o-section-head__nav-item" href='#'>item 7</a>
				</nav>
	    </div>
	  </div>
	</div>
</div>
```

`o-section-head__title` should contain the text of the section title. It can be any element, it does not need to he an `<h1>`.
`data-o-expander-collapsed-toggle-text` and `data-o-expander-expanded-toggle-text` should be the title for the list of links. This is only shown at narrow screen widths where the list becomes expandable.

As described in [o-link-list](https://github.com/Financial-Times/o-link-list#markup-for-navigational-elements), where the `<nav>` element is used, links should not be in a `<ol>` or `<ul>` as this adds more clutter for screen reader users.
