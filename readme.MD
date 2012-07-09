jOdometer is a counter that works like an odometer: moving the numbers up like in a wheel. It supports decimals.

We can configure:

* Start number
* Stop number
* Delay between the number change
* Increment units
* Speed and easing of the animation
* Easing of the animation
* Different styling options, including a PSD to edit the numbers image.
* Whether to format large numbers with comma or not.
* Whether to have unused digits to the left that the odometer will expand into (maxWidth) (v1.3)
* Whether a prefix character (e.g. '$') is displayed (v1.4)

We can also update the numbers manually/dynamically.

Check the demo http://www.frontendmatters.com/demos/jodometer/
More info at http://www.frontendmatters.com/projects/jquery-plugins/jodometer

# License

* Copyright (c) 2008 TrafficBroker <http://www.trafficbroker.co.uk>
* Licensed under GPL and MIT licenses

# Documentation

Usually we will need a "position: relative" and an "overflow: hidden" in the container element.

## Sample Configuration:
    $('.counter').jOdometer({
    	increment: 3.17, 
    	counterStart:'0087.15',
    	counterEnd:'0159.50', 
    	numbersImage: '/images/numbers.png', 
    	spaceNumbers: 2, 
    	offsetRight:5
    });

## Config Options:

* `counterStart`: Number we are starting with. To get a specific number of digits/decimals it have to be a string (e.g. `'0005.50'`) // Default: `'0000.00'`
* `counterEnd`: The counter stop when reach this number. If it is the same as `counterStart` the odometer is static. `false` to don't ever stop. // Default: `false`
* `delayTime`: Delay between each number change // Default: `1000`
* `increment`: Number increment after each delayTime // Default: `0.01`
* `speed`: Speed for the change number animation // Default: `500`
* `easing`: Easing for the change number animation. Other than 'swing' or 'linear' must be provided by plugin // Default: `'swing'`
* `numbersImage`: Image used for the numbers. You can use .psd provided // Default: `'/images/numbers.png'`
* `heightNumber`: The height that each number needs // Default: `31`
* `widthNumber`: Width of the numbers' image // Default: `14`
* `offsetRight`: Distance to the right // Default: `0`
* `spaceNumbers`: Separation between the numbers' columns // Default: `0`
* `widthDot`: Decimal dot's special width // Default: `10`
* `formatNumber`: Whether to format the number with commas every 3 digits // Default: `false`
* `maxDigits`: Maximum digits. If set will allow odometer to 'grow' to the left for `maxDigits` digits w/out leading 0s. If `0` does nothing. // Default: `0`
* `prefixChar`: Whether to display a prefix character (16th element in `numbersImage`). Requires `maxDigits > 0` // Default: `true`
 
## Usage
 
You can override the defaults with:
 	$.fn.jOdometer.defaults.spaceNumbers = 1;
 	
Widget returns an object used for counter manipulation. Available Functions:
 
`goToNumber(number)`: Updates the counter with the number given. Example:
 
 	var counter = $('.counter').jOdometer({...});
 	counter.goToNumber(100);
 