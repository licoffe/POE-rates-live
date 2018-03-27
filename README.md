# POE-rates-live
Support page for the [POE-rates :: Live](http://poe-rates.com/live) online search

### Tutorial video
Feel free to have a look at [this tutorial video](https://www.youtube.com/watch?v=MjHsYp2cLMc) explaining most of the features of the tool.

[![Video preview](https://i.imgur.com/TVh0t1k.png)](https://www.youtube.com/watch?v=MjHsYp2cLMc)

### FAQ

- How do I see if an item is sold?

  After some time, items may get sold or removed from stash. The item entry will be greyed out in this case.
  ![Sold](https://i.imgur.com/4JUwg5H.png)

- Do you support min, max values for item properties?
 
  Sure. You can use the following syntax on all fields except price and affixes:
  - `4-10` for a min value of 4 and a max of 10
  - `<4` for a min value < 4. Works the same with `<=`
  - `>4` for a min value > 4. Work the same with `>=`

- Will you implement the "underpriced" mode available in POE-Sniper?

  Likely when I'm done fixing bugs with the current release and that everything feels stable.
  
- Can I export a search to the other trade websites?

  - Poe.trade is almost fully supported
  - Poeapp has limited support at the moment
  - pathofexile/trade is not supported yet
  
- What are the trade stats?
  
  ![Stats](https://i.imgur.com/btjVsg0.png)
  
  Trade stats return the price distribution for a search on poe.trade with identical parameters. Only prices with different sellers and an occurence > 1 are taken into account.

- Sometimes I stop receiving new items. How does that happen?
  
  This happens when I restart the server for some development purposes. Clients get unsubscribed from the tool but don't get resubscribed when the backend is up. Something I should work on.
  
- How do I move/remove filters into/from groups?

  Adding and removing filters from group is done through drag-and-drop. Drag a filter into a group to add the filter to this group. Drag the filter into the main view to remove it from a group.
  
- Can I set different sounds for different filters? Groups?

  Per filter sound is not supported. However you can set different sounds for groups.

- How do you blacklist someone?

  Click on the hand icon near a seller account name in the item list. A dialog will open, allowing you to blacklist this user.

- How do you edit the blacklist?

  This is not currently possible, but it should be available in the settings eventually.

- I cannot find this item affix. When will you add it?

  Fill free to edit the affix-completion.json file to add the missing affix and send me a pull request. An affix entry has the following syntax:
  "[Explicit,implicit,Unique explicit, Enchant, Total, Pseudo] The affix name with the right case and varying values replaced by #": null
  
  Here is an example:
  "[Explicit] Socketed Gems are Supported by Level # Trap": null,

- I noticed a bug in your tool. How do I report it?
  Please open a new issue and describe the problems you encountered
