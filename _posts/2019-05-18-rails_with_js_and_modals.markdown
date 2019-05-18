---
layout: post
title:      "Rails with JS and Modal's "
date:       2019-05-18 12:25:40 +0000
permalink:  rails_with_js_and_modals
---



I really enjoyed working on this project because I really like the idea of a single page application and not having to redirect to a new page. There were some challenges while creating my project though. For instance I had my rails project already set up with Modal's instead of redirecting to another page for all my forms. The page would fade out and a form with pop up making the rest of the page inaccessible until you exited the form or hit submit like so:

![](https://i.imgur.com/5zp3LVdl.png)

I loved this feature but when it came time to not redirecting to a new page it caused some difficulties. I first had to assign all of the part attributes to a data object:

```
$(document).on('turbolinks:load', function () {

  $("form#new_part").toArray().forEach(f => {
	
    $(f).on("submit", function(e){
		
      e.preventDefault()
			
      url = this.action + '.json'
			
      const data = {
			
        'authenticity_token': f.authenticity_token.value,
				
          'name': e.target.part_name.value,
					
          'price':  e.target.part_price.value,
					
          'description':  e.target.part_description.value,
					
          'manufacturer':  e.target.part_manufacturer.value,
					
          'qty': e.target.part_qty.value
        }
```

I then had to remove all of the modal's attributes, classes and css after the submit button was clicked in order to continue using the page. I did that with the following code:

```
      $('.modal').removeClass('in');
			
      $('.modal').attr("aria-hidden","true");
			
      $('.modal').css("display", "none");
			
      $('.modal-backdrop').remove();
			
      $('body').removeClass('modal-open');
```

This was amazing it worked! After clicking the submit button the form would dissapear and I could continue using the page but there was another issue. If I wanted to add another part I clicked on the add part button and the form would pop up with all of the data filled in from the previous part and the submit button was unclickable:

![](https://i.imgur.com/4FzeFjEl.png)

This was actually a very simple fix. After my fetch method I would simply have to reset the form so I just called the following method: 

```
f.reset()
```

That was it this fixed my issue and now i was able to add multiple parts one after the other without having to refresh the page. I hope this was helpful to someone else also trying to incorporate modal's into their projects. If you would like to check out my application here is the link to my website: [Van Builder](http://www.van-builder.com/) and the link to my pages [Git Hub](https://github.com/mikeygbd/Van-builder).

