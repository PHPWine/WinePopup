# WinePopup
WinePopup a collection snippet for PHPWine v2.2.0 (these features are just added safe to migrate

```PHP
composer require phpwine/winepopup
```

```PHP
  /**
   * --------------------------------------------------------------------------------------------
   * @method accordion
   * -------------------------------------------------------------------------------------------- 
   * This method is a hook to execute the new instance of accordion 
   * 
   * $popup = new WinePopUp([
   *   prefix => 'wine_',
   *   popup => [
   *     'months' => [], // means all months by default // [1,2,3,4,5,6,7,8,9,10,11,12], // [1, 2] means january and february
   *     'days'   => [], // all days // [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31], // [13, 14] // 31 days base on the calendar only in 13 and 14 of the month
   *     'every' =>  '', // means every page load  // Every 6 AM 8 Total of hrs from 1 to 24 means every 8AM
   *     'event' => 'reload', 
   *     'close_id' => 'my_id', // id for close icon
   *  ],
   *  hooks => [
   *    \Project\HookA::class // Main contents of Popup
   *  ]
   * ]);
   *
   * OR 
   * 
   * $popup = new WinePopUp([
   *   prefix => 'wine_',
   *   popup => [
   *    'event' => [
   *      'click' => 'elem_id' // id of elem you will click!
   *   ], 
   *   'close_id' => 'my_id', // id for close icon
   *   ],
   *   hooks => [
   *     \Project\HookA::class // Main contents of Popup
   *   ]
   * ]);
   * 
   * print $popup->popup();
   *
   * HOOKS:
   * 
   * ATTR: @method
   * public function attr_prefix_awssscca() {...}
   * 
   * VALUE: @method 
   * public function prefix_awssscca() {...}
   * 
   * TOP and BOTTOM @function
   * function top_prefix_awssscca() {...}
   * function bottom_prefix_awssscca() {...}
   * 
   * @Defined : execute new instance accordion
   * @since: v1.0 doctrine
   * @since: v2.5.0 wine */
```

```PHP
 // ex. PHP Date will popup show 
 $post_to = date("m.d.y");
 // Date you schedule < string >
 $schedule = "12.25.23"

 // If condition get true then all html will visible to front end!
 if($schedule == $post_to) {
  print $popup->popup();
 }
```
