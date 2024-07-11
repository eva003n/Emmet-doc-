# Learn all about Emmet to elevate your vs code typing skills and reduce the over dependencies on the mouse.

# How it works 
EMMET- uses syntax similar to CSS selectors for describing elements positions inside generated tree and elements’ attributes.
  Any word written in vs code can be converted to a HTML tag.
# NEASTING ELEMENTS
  Child-with ">" selector you are able to nest child elements inside of a parent Basically you are descending down the generated tree.
# Example
div>ul>li results to-->>
<div>
    <ul>
        <li></li>
    </ul>
</div>
  Sibling -with "+" selector you are able to place elements near each other on the same level.
# Example
h1+h2+h3+h4 results to -->>
<h1></h1>
<h2></h2>
<h3></h3>
<h4></h4>
   Climb up-with "^"selector you are doing the opposite action of the ">" since you are able to move one level up the generated tree.
# Example
div+div>p>p+em^bq results to-->
<div></div>
<div>
    <p><span></span><em></em></p>
    <blockquote></blockquote>
</div>
    You can use as many ^ operators as you like, each operator will move one level up:
# Example
div+div>p>p+em^h1+span^^b+em results to-->
  <div></div>
  <div>
    <p>
      <p></p>
      <em></em>
    </p>
    <h1></h1>
    <span></span>
  </div>
  <b></b>
  <em></em>
    Multiplication-with * you can define how many times an element is repeated.
# Example
ul>li*5
  <ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
    Group- with () parenthesis you are able to group sub-trees together 
# Example
div>(header>ul>li*2>a)+footer>p+em expands to-->
<div>
  <header>here header is the subtree
    <ul>
      <li><a href=""></a></li>
      <li><a href=""></a></li>
    </ul>
  </header>
  <footer>
    <p></p>
  </footer>
  <em></em>
</div
# Example 2
(div>dl>(dt+dd)*3)+footer>p results to-->
<div>
  <dl>
    <dt></dt>
    <dd></dd>
    <dt></dt>
    <dd></dd>
    <dt></dt>
    <dd></dd>
  </dl>
</div>
<footer>
  <p></p>
</footer>
# Attribute Operators 
# ID and CLASS
    Class-with "." you can add a class attribute to any HTML tag.
    Id-with "#" you can add an id attribute to any HTML tag.
# Example 
div#header+div.page+div#footer.class1.class2.class3 results to -->  

<div id="header"></div>
<div class="page"></div>
<div id="footer" class="class1 class2 class3"></div>

# Custom attributes
# Example
td[title="Hello world!" colspan=3] results to -->
<td title="Hello world!" colspan="3"></td>

# Item numbering
    The $ operator allows you to number element name's attribute names and attribute values with auto-incrementation.
# Example
div>ul>li.item-$*5 results to -->
<div>
  <ul>
    <li class="item-1"></li>
    <li class="item-2"></li>
    <li class="item-3"></li>
    <li class="item-4"></li>
    <li class="item-5"></li>
  </ul>
</div> 
# Example 2
ul>li.items$$$*5 results to -->
<ul>
  <li class="items001"></li>
  <li class="items002"></li>
  <li class="items003"></li>
  <li class="items004"></li>
  <li class="items005"></li>
</ul>
# Changing numbering base and direction
    @ modifier, you can change numbering direction (ascending or descending) and base (e.g. start value
# Example
ul>li.item@-*5 results to-->
<ul>
  <li class="item5"></li>
  <li class="item4"></li>
  <li class="item3"></li>
  <li class="item2"></li>
  <li class="item1"></li>
</ul>
# Example 2
ul>li.item$@3*5 results to -->
<ul>
  <li class="item3"></li>
  <li class="item4"></li>
  <li class="item5"></li>
  <li class="item6"></li>
  <li class="item7"></li>
</ul>
# Example 3
ul>li.items$@-3*5 results to-->
<ul>
  <li class="items7"></li>
  <li class="items6"></li>
  <li class="items5"></li>
  <li class="items4"></li>
  <li class="items3"></li>
</ul>

# Text
    with {} You can use curly braces to add text to an element.
# Example
a{Click me} results to-->
<a href="">Click me</a>
# Example 2
 a{click}+b{here} -->
<a href="">click</a><b>here</b>
# Example 3
 a>{click}+b{here} -->
<a href="">click<b>here</b></a>






    




  
  
  
