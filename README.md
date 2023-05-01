# Vanilla JS Accordion Example

Instead of looking for a pre-written accordion component, I just wrote a quick one in plain Javascript

```javascript
export default function() {
  document.addEventListener('DOMContentLoaded', function () {
    let accordion = document.getElementsByClassName('accordion-item');
    for (let i=0; i<accordion.length; i++) {
      // add click event to accordion header
      let accordionHeader = accordion[i].querySelector('.accordion-header');
      if (accordionHeader) {
        accordionHeader.addEventListener('click', () => {
          // toggle accordion text
          let accordionText = accordion[i].querySelector('.accordion-text')
          if (accordionText) {
            accordionText.style.display === "block" ? accordionText.style.display = "none" : accordionText.style.display = "block" ;
          }
          // toggle plus/minus symbol
          let accordionSymbol = accordion[i].querySelector('.accordion-symbol');
          if (accordionSymbol) {
            accordionSymbol.innerHTML === "+" ? accordionSymbol.innerHTML = "-" : accordionSymbol.innerHTML = "+";
          }
        })
      }
    }
  }, false);
}
```
