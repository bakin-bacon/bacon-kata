# bacon-kata
Determine Perfect Bakin' Bacon Timing

## The Bacon Method

The [Bacon Method](http://www.baconmethod.com) is a way to make perfect bacon, __every time__.

__Bacon Method Summary:__

1. Put bacon on a cookie sheet (or other oven safe pan with sides)
1. Put pan of bacon into cold oven
1. Turn oven to 400 degrees Fahrenheit
1. Cook bacon for 20 minutes

The main variable is time: __how long should we cook the bacon?__

## The Bacon Algorithm

__Goal:__ find the optimal bacon cooking time.

Some requirements:

* Starting point is 20 minutes, 400 degrees.
* Each time the _bacon-maker_ makes bacon, the _bacon-maker_ provides feedback and tells you the bacon was too crispy, too floppy, or just right.
* If the bacon was too crispy the time should be adjusted to be less.
* If the bacon was too floppy the time should be adjust to be more.
* If the bacon was just right, the time should not be adjusted.
* Time adjustment should be cut in half each time the user changes their answer from too crispy to too floppy or vice versa.
  * Time adjustments should start at 2:00.
  * Time adjustments should be no less than 0:30.

## Some examples

### Base case (no previous bacon'ings)

__Answer:__ 20 minutes

### One bacon'ing (with _just right_ feedback)

| Duration | Feedback |
| --- | --- |
| 20:00 | just right |

__Answer:__ 20 minutes

### One bacon'ing (with _too floppy_ feedback)

| Duration | Feedback |
| --- | --- |
| 20:00 | too floppy |

__Answer:__ 22 minutes

### One bacon'ing (with _too crispy_ feedback)

| Duration | Feedback |
| --- | --- |
| 20:00 | too crispy |

__Answer:__ 18 minutes

### Multiple bacon'ings

| Duration | Feedback |
| --- | --- |
| 20:00 | too crispy |
| 18:00 | too crispy |
| 16:00 | too floppy |
| 17:00 | too crispy |
| 16:30 | perfect |
| 16:30 | too crispy |

__Answer:__ 16 minutes

