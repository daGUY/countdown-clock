# Countdown Clock
- By James Scariati
- May 2015

## Description
Display a live countdown clock.

**[View Demo](http://scariati.kissr.com/github/countdown/)**

## Dependencies
- [jQuery](http://jquery.com)

## Use
Include jQuery and the `jquery.countdown.js` plugin in your HTML:

```html
<head>
	<script src="lib/jquery.min.js"></script>
	<script src="lib/jquery.countdown.js"></script>
</head>
```

Then call `countdown()` on the element where you want the countdown to appear:

```javascript
$("#countdown").countdown();
```

## Options
The following options are available:

```javascript
$("#countdown").countdown({
	onComplete: function() {},
	padding: true,
	seconds: 60
});
```

* `onComplete`: an optional function that triggers when the countdown completes. For example, to show an alert, `function() { alert("Time's up!"); }`
* `padding`: pads single digits with leading zeros. Defaults to `true` so that the width of the countdown doesn't change as it updates. Setting to `false` gives a cleaner look, e.g. `5:00` vs `05:00`
* `seconds`: the number of seconds to count down. Defaults to `60`

## Notes
If `padding` is set to `false`, but the countdown is one hour or longer, the minutes will remain padded so that the time reads correctly. For example, 3600 seconds (one hour) will display as `1:00:00` rather than `1:0:00`, but 300 seconds (five minutes) will display as `5:00`. Seconds are always padded.