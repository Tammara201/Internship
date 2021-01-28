# Internship with Prosper IT Consulting

## Introduction

#### As part of a 2-week sprint, I worked with a team developing a Lifestyle website using HTML, CSS and JavaScript. In addition I learned how to use Azure for version control and got experience in the Agile/Scrum methodologies.

#### Below are descriptions of the tasks I worked on and a brief description of each. Examples of this work are below and more detailed examples can be found in the Code Example folder within the Portfolio repository.

## Examples of work

### Grid System
#### Developed a grid system to display preparation recommendations.

##### HTML
```
<section id="preparation">
                <div class="container">
                    <h1>BEFORE YOU GO</h1>
                    <h6>Central Oregon has an amazing search and rescue team, 
                        but you don't want to use them.  Make sure you are prepared.</h6>
                    <div class="row">
                        <div class="col-sm-6" style="font-weight: bold;">Preparation                           
                        </div>
                        <div class="col-sm-6" style="font-weight: bold;">Pack                        
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-sm-6">
                            Let someone know where you are going<br>
                            Dress in layers<br>
                            Wear good hiking shoes<br>                            
                        </div>
                        <div class="col-sm-6">
                            Plenty of food and water<br>
                            Map and compass<br>
                            First-aid kit<br>
                        </div>
                    </div>                    
                </div>
</section>
```
### Carousel
#### Created a carousel to show pictures and descriptions of various hikes.

##### HTML
```
<div id="carouselCaptions" class="carousel slide" data-bs-ride="carousel">
                <ol class="carousel-indicators">
                    <li data-bs-target="#carouselCaptions" data-bs-slide-to="0" class="active"></li>
                    <li data-bs-target="#carouselCaptions" data-bs-slide-to="1"></li>
                    <li data-bs-target="#carouselCaptions" data-bs-slide-to="2"></li>
                    <li data-bs-target="#carouselCaptions" data-bs-slide-to="3"></li>
                </ol>

            <div class="carousel-inner">
                <div class="carousel-item active">
                    <img src="./static/images/smithrock2.jpg" class="d-block w-100" alt="smithrock">
                    <div class="carousel-caption d-none d-md-block">
                    <h3>Smith Rock</h3>
                    <p>At Smith Rock is know as the birthplace of American sport climbing. Cliffs of tuff and<br>
                        basalt are ideal for rock climbing of all difficulty levels. There are aslo many trails of varying<br>
                        difficulty. If you are looking for a real challenge and an amazing view give Misery Ridge a try.</p>
                    </div>
                </div>

                    <div class="carousel-item">
                        <img src="./static/images/greenlakes.jpg" class="d-block w-100" alt="greenlakes">
                        <div class="carousel-caption d-none d-md-block">
                        <h3>Green Lakes</h3>
                        <p>Green Lakes trail is one of the most popular day hike and backpacking destinations in<br>
                            Central Oregon, and for good reason. This hike takes you through a variety of terrain-<br>
                            including waterfalls, meadows, lava flows and lots of old growth trees. The most popular<br>
                            trailhead is the official Green Lakes/Soda Creek trailhead right off of the Cascade Lakes Highway.</p>
                        </div>
                    </div>

                    <div class="carousel-item">
                        <img src="./static/images/toddlake.jpg" class="d-block w-100" alt="toddlake">
                        <div class="carousel-caption d-none d-md-block">
                        <h3>Todd Lake</h3>
                        <p>Todd Lake trail is the perfect spot for a leisurely stroll or for young kids.<br>
                            The trail is flat but you do not compromise on views. Early August is a great<br>
                            time to take kids on this hike, there are literally thousands of frogs and tadpoles.<br>
                            The water is shallow and warm, perfect for little ones to take a swim.</p>
                        </div>
                    </div>

                    <div class="carousel-item">
                        <img src="./static/images/mirrorlake.jpg" class="d-block w-100" alt="mirrorlake">
                        <div class="carousel-caption d-none d-md-block">
                        <h3>Mirror Lake</h3>
                        <p>Sisters Mirror Lake Loop via Mirror Lakes Trail is a 10 mile moderately difficult trail.<br>
                            If you are feeling adventurous, go into the treeline on the other side of the lake. You will<br>
                            find the hidden lakes Lancelot and Camelot.</p>
                        </div>
                    </div>
                </div>
```
 ##### CSS               
```
/*Carousel formatting*/
.carousel .carousel-item {
  height: 500px;
}
.carousel-item img {
    position: absolute;
    object-fit:cover;
    top: 0;
    left: 0;
    min-height: 500px;
} 
```

### Modal and Sign Up Form with Functionality
#### Implemented an email sign up form and linked that to an email to receive notification of requests.

##### HTML
```
<div class="modal fade" id="myModal" tabindex="-1" aria-labelledby="modalLabel" aria-hidden="true">
                <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                    <h4 class="modal-title" id="modalLabel">Email Newsletter Sign Up</h4>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <form action="https://formspree.io/f/myybozpp" method="POST" onsubmit='this.submit();this.reset();return false;'>
                            <div class="form-group">
                                <label for="lastName">Last Name:</label>
                                <input type="text" class="form-control" id="lastName" name="name">
                            </div>
                            <div class="form-group">
                                <label for="firstName">First Name:</label>
                                <input type="text" class="form-control" id="firstName" name="name">                                
                            </div>
                            <div class="form-group">
                                <label for="email">Email address:</label>
                                <input type="email" class="form-control" id="email" name="_replyto">
                            </div>
                            <div class="checkbox">
                              <label><input type="checkbox">&nbsp;&nbsp;I Accept terms and conditions</label>
                            </div>
                            <div class="checkbox">
                                <label><input type="checkbox">&nbsp;&nbsp;I Agree to receive emails</label>
                            </div>
                            <button type="submit" class="btn btn-outline-secondary">Submit</button>        
                          </form>                        
                    </div>                    
                </div>
                </div>
            </div> 
```

##### JavaScript
```
// Modal
var myModal = document.getElementById('myModal')
var modalLabel = document.getElementById('modalLabel')

myModal.addEventListener('shown.bs.modal', function () {
  modalLabel.focus()
})
```

### Dark Theme
#### Created dark theme toggle button.

##### HTML
```
<button onclick="darkFunction()" class="btn btn-sm btn-outline-secondary" style="z-index: 99;">Toggle dark mode</button> 
```

##### CSS
```
/*Dark mode*/
body.dark-mode * {
  background-color: black;
  color: white;
} 
```

##### JavaScript
```
//Get the button scroll to top
var scrollToTopBtn = document.querySelector(".scrollToTopBtn")
var rootElement = document.documentElement

function handleScroll() {
  // Display button when .80 through page
  var scrollTotal = rootElement.scrollHeight - rootElement.clientHeight
  if ((rootElement.scrollTop / scrollTotal ) > 0.80) {
    // Show button
    scrollToTopBtn.classList.add("showBtn")
  } else {
    // Hide button
    scrollToTopBtn.classList.remove("showBtn")
  }
} 
```

### Back to Top Button
#### Created a back to top buttons that appears when you reach the bottom of the page.

##### HTML
``` 
/*Scroll to top button*/
.scrollToTopBtn {
  background-color: bisque;
  border: 1px solid rgb(80, 62, 62);
  border-radius: 1px;
  color: rgb(80, 62, 62);
  cursor: pointer;
  font-size: 16px;
  line-height: 48px;
  width: 48px; 
  ```
  
  ##### CSS
  ```
  /* place it at the bottom right corner */
  position: fixed;
  bottom: 30px;
  right: 30px;
  /* keep it at the top of everything else */
  z-index: 100;
  /* hide with opacity */
  opacity: 0;
  /* also add a translate effect */
  transform: translateY(100px);
  /* and a transition */
  transition: all .5s ease
}
    
.showBtn {
  opacity: 1;
  transform: translateY(0)
  } 
  ```
  
  ##### JavaScript
  ```
  function scrollToTop() {
  // Scroll to top
  rootElement.scrollTo({
    top: 0,
    behavior: "smooth"
  })
}
scrollToTopBtn.addEventListener("click", scrollToTop)
document.addEventListener("scroll", handleScroll) 
```

## Other Skills Learned

#####      -Identifying and working through bugs
#####      -Version control
#####      -Team development skills

## Conclusion

##### This was a valuable learning experience. I learned how to use version control, how to debug a live site and gained practical knowledge in developing a usable site.
