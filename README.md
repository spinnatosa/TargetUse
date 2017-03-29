# TargetUse
<br/><br/>
TargetUse is a simple accordion created with <b>CSS-only</b>.
<br/>
<b>Why do we use Javascript when we can use CSS?</b>
<br/><br/>
So I wanna show how TargetUse works.
<br/><br/>
### HTML

```html
<main class="targetUse">

  <section id="section-1">
    <a href="#section-1">
      Primo Accordion
    </a>
    <article>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ut ex eu nulla posuere porttitor. 
    </article>
  </section>
  
  <section id="section-2">
    <a href="#section-2">
      Primo Accordion
    </a>
    <article>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ut ex eu nulla posuere porttitor. 
    </article>
  </section>
  
</main>
```
### CSS/SCSS

```css
$space = 10px;

.targetUse {
  padding: $space*3;
  
  section {
    margin: $space*3 0;

    a {
      transition: color .5s ease;
      color: black;
      text-decoration: none;
      border-bottom: 1px solid black;
      padding-bottom: $space/2;
      display: inline-block;
      margin-bottom: $space;
    }
    
    article {
      max-height: 0;
      overflow:hidden;
      transition: all 1s ease;
    }
  
  // OPEN ACCORDION
    &:target {

      a {
        color: grey;
        border-bottom: 1px solid grey
      }
      
      article {
        max-height: $space*3;
      }
    }
  }
}

```
I used "<b>:target</b>" pseudo-class to do it.
<br/>
The :target pseudo-class is supported by all Browsers.<br/>
You can see an demo <a href="https://jsfiddle.net/spinnatosa/bsgj4x07/">here</a>.
