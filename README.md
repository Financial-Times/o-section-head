# o-section-head

Typographic styles and layout for sub-headings. This module contains Sass for section title and a list of related links. This list of related links is optional, and uses o-expander to become collapsable at small screen widths.

## Markup

```
<div data-o-component="o-section-head" class="o-section-head" >
	<div class="o-section-head__inner">
		<div class="o-section-head__title-container">
      <!-- TODO: should this be a heading? what is the likely semantic value for this? -->
			<div class="o-section-head__title">Section title</div>
		</div>
	  <div class="o-section-head__related-item-container o-expander"
      <!-- See o-expander documentation for configuration options for this component -->
      data-o-expander-collapsed-toggle-text="RELATED"
      data-o-expander-expanded-toggle-text="RELATED"
      data-o-expander-shrink-to="height"
      data-o-component="o-expander">
      <!-- TODO: should this be a nav? in this case these are 'related' which seems semantically aside-y... -->
	    <aside>
        <!-- TODO: what should this be?-->
        <div class="o-section-head__related-item-title">related</div>
	      <button class="o-section-head__related-item-title-button o-expander__toggle o--if-js">related</button> <!-- TODO: what should this be?-->
	      <ol class="o-section-head__related-item-container-list o-expander__content" >
        <!-- TODO: maybe this should be a ul?-->
	        <li class="o-section-head__related-item"><a href='#'>item 1</a></li>
	        <li class="o-section-head__related-item"><a href='#'>item 2</a></li>
	        <li class="o-section-head__related-item"><a href='#'>item 3</a></li>
	        <li class="o-section-head__related-item"><a href='#'>item 4</a></li>
	        <li class="o-section-head__related-item"><a href='#'>item 5</a></li>
	        <li class="o-section-head__related-item"><a href='#'>item 6</a></li>
	        <li class="o-section-head__related-item"><a href='#'>item 7</a></li>
	      </ol>
	    </aside>
	  </div>
	</div>
</div>
```

`o-section-head__title` should contain the text of the section title.
`data-o-expander-collapsed-toggle-text`, `data-o-expander-expanded-toggle-text` and `o-section-head__related-item-title` should be the title for the list of links and should all be the same.
