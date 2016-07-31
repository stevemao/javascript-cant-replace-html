Since we write a lot of JavaScript now, we tend to write less HTML and css code.

We used to have Ext.js that turns your HTML into something like this:

```html
<div class="div">
  <div class="content">
    <div class="body">
      <div class="text">
        <div class="link">
          A clickable link here
        </div>
      </div>
    </div>
  </div>
</div>
```

We now have React.js that encourages you to write HTML in your JavaScript. They even build the whole event system. People using JavaScript (EG: form validation) to make sure the HTML has consistent behaviors across different browsers.

It seems like every HTML tag just have some special use agent. For example, an `an` tag is an anchor link. You can click to go to another website. Text is blue with underscore. You could write JavaScript (or/and css) to turn a `<div>` into `<a>`. Or can you?

*Note:* This list does not include things like calling `createElement()` in your JavaScript, because an `<a>` created by `createElement()` is a real `<a>`.

*Note:* There are other important reasons: semantics, free functionalities, default styles and performance.

## ARIA

No, you can't command your VoiceOver to call a `<div>` an anchor link. In fact, you can hardly control your VoiceOver in general.

## Context Menu

EG: "Open Link In New Tab". You can't add this to your "right click menu" in JavaScript. No You can't. [You can't even do customize context menu in most browsers](http://caniuse.com/#search=context).

## Search engine

Yes, search engines do run JavaScript now. No they won't treat a `<div>` with a click event listener the same as an `<a>`. [They will probably ignore the changes made by JavaScript in your `<head>` metadata](http://stackoverflow.com/a/413455/2075423).

## Sync form post

Surprise! [The only way to do a sync form post is through HTML](http://stackoverflow.com/a/133997/2075423). Read more on [`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData/Using_FormData_Objects) and [`HTMLFormElement.submit()`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/submit).

## `<iframe>`

This is the only way to have a "browser" inside your website.
