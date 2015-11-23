<h1>A Selenium Cheat Sheet</h1>
<h2>Sabrina Soong</h2>
<hr/>

<h3>Setup</h3>
<p>require 'selenium-webdriver'</p>

<h3>Execute</h3>
<p>driver = Selenium::WebDriver.for :firefox</p>
<p>driver.get <em>url</em></p>
<p>driver.navigate to <em>url</em></p>
<p>driver.execute_script "alert(<em>Enter message here!</em>);"</p>

<h4>Finding Elements</h4>
<p>a = driver.find_element name: "something"</p>
<p>a = driver.find_element id: "someid"</p>
<p>a = driver.find_element css: "h1 .foo"</p>
<p>a = driver.find_element class: "foo"</p>
<p>a = driver.find_element xpath: "//h2[@class='someclass']"</p>
<p>a = driver.find_element tag_name: "tagname"</p>
<p>a = driver.find_elements tag_name: "tagname"</p>

<h4>Element Methods</h4>
<p>a.location
<p>a.location_once_scrolled_into_view</p>
<p>a.size</p>
<p>a.displayed?</p>
<p>a.text</p>
<p>a.attribute "class"</p>
<p>a.click</p>
<p>a.send_keys "Hello"</p>
<p>a.click</p>
<p>a.selected?</p>
<p>a.submit</p>
<p>a.find_element id: "someid"</p>
<p>a.find_elements tag_name: "input"</p>
<p>a.methods - Object.new.methods</p>

<h4>Waiting Methods</h4>
<p>wait = Selenium::WebDriver::Wait.new(timeout: <em>Enter time here</em>)
<p>wait.methods - Object.new.methods</p>
<h5>Waiting Methods with Elements</h5>
<p>a = wait.until do <br/>
&nbsp;&nbsp;browser.find_element(tag_name: "h1")<br/>
    end
<br/>
puts "<em>Enter a test passing/failing string here</em>" if wait.until do<br/>
&nbsp;&nbsp; browser.find_element(tag_name: "<em>Enter Your tag here</em>").text.match /<em>Enter your string here</em>/<br/>
end</p>

<h4>Resizing The Browser</h4>
<p>driver.manage.window.move_to(<em>number</em>, <em>number</em>) <br/>
Example: driver.manage.window.move_to(300,400)</p>
<p>driver.manage.resize_to(<em>number</em>, <em>number</em>) <br/>
Example: driver.manage.window.resize_to(500,800)</p>
<p>driver.manage.window.maximize</p>

<h3>Teardown</h3>
<p>driver.quit</p>

