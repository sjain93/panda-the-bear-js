# DOM Manipulation with Panda the Bear
[See assignment in Alexa.](https://alexa.bitmaker.co/wdi/67/assignments/2051/latest)

#1
profileImage = document.querySelector('.profile-image')
profileImage.src = "http://images.electricpig.co.uk/wp-content/uploads/2011/01/Darth-Vader.png"

#2
imageSky = document.querySelectorAll('img')[1];
imageSky.src= "http://www.ruralclimatenetwork.org/sites/default/files/styles/feed_images/public/field/image/4248409028_c4cbac7c20_z.jpg?itok=Zfmyt1mL";

#3
textChange = document.querySelectorAll('.highlight')[1];
textChange.textContent = "Sanchit Jain";

#4
employmenyTitle = document.querySelector('#employment h3');
employmenyTitle.innerText = "Work Experience";

#5
body = document.querySelector('body');
body.style.color ='red';

#6 Change the colour of each element using the highlight class. Use a for loop to do this.
highlightArray = document.querySelectorAll('.highlight');
for (var i = 0; i < highlightArray.length; i++) {
  highlightArray[i].style.color = 'white';
};

#7 Change the font family of the h1 to 'monospace'.
document.querySelector('h1').style.fontFamily = 'monospace';

#8 Find a way to select the round icons in the sidebar and then change their colour.
document.querySelectorAll('.action-icon-bg')[0].style.backgroundColor = 'red';
document.querySelectorAll('.action-icon-bg')[1].style.backgroundColor = 'red';

#9 Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".
document.querySelector('.contact-info').placeholder = "Identify yourself";

#10 Change the placeholder attribute of the message field to "state your business".
document.getElementById('message').placeholder = "State you business";

#11 Give the name field a "value" attribute of "your nemesis".
document.querySelector('.contact-info').setAttribute("value", "Your nemesis");

#12 Change the value attribute of the email field to "koalathebear@gmail.com".
emailField = document.querySelector('#email')
emailField.value = "koalathebear@gmail.com";

#13 Change the value of the submit button on the contact form to "En garde!".
document.getElementById('submit').setAttribute("value", "En garde!");

#14 We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
var btn = document.getElementById("submit");
btn.disabled = true;

#15 We should help Panda protect their privacy by erasing their personal details from the sidebar.
childObjects = document.querySelectorAll('.bio-info li');
parentObjects = document.querySelector('body > aside > ul ');
parentObjects.removeChild(childObjects[0]);
parentObjects.removeChild(childObjects[1]);
parentObjects.removeChild(childObjects[2]);

-----------------------------------------------------------------------------------------------------------------------
Part 2
-----------------------------------------------------------------------------------------------------------------------
#1
var elem = document.querySelector('#time-travel');
var elemP = elem.parentElement;
elemP.parentNode.removeChild(elemP);

#2
const varNode = document.querySelector("#right-image > img");
var dupNode = varNode.cloneNode();
varNode.parentNode.appendChild(dupNode);

#3
for (var j = 0; j < 10; j++) {
	insPika = varNode.cloneNode(true)
  	varNode.insertAdjacentElement('afterend', insPika);
};

#4

const listItem = document.createElement('li');
undefined
listItem
<li>​</li>​
const leftSpan = document.createElement('span');
undefined
leftSpan
<span>​</span>​
var lastUpdated = document.createTextNode('Page last updated on');
undefined
leftSpan.appendChild(lastUpdated);
"Page last updated on"
leftSpan
<span>​Page last updated on​</span>​
listItem.appendChild(leftSpan);
<span>​Page last updated on​</span>​
const rightSpan = document.createElement('span');
undefined
var d = new Date();
undefined
d
Sat Mar 30 2019 18:21:03 GMT-0400 (Eastern Daylight Time)
var lastUpdated = document.createTextNod(d);
VM3185:1 Uncaught TypeError: document.createTextNod is not a function
    at <anonymous>:1:28
(anonymous) @ VM3185:1
var lastUpdated = document.createTextNode(d);
undefined
lastUpdated
"Sat Mar 30 2019 18:21:03 GMT-0400 (Eastern Daylight Time)"
listItem
<li>​<span>​Page last updated on​</span>​</li>​
lastUpdated
"Sat Mar 30 2019 18:21:03 GMT-0400 (Eastern Daylight Time)"
rightSpan.appendChild(lastUpdated);
"Sat Mar 30 2019 18:21:03 GMT-0400 (Eastern Daylight Time)"
listItem.appendChild(rightSpan);
<span>​Sat Mar 30 2019 18:21:03 GMT-0400 (Eastern Daylight Time)​</span>​
listItem
<li>​<span>​Page last updated on​</span>​<span>​Sat Mar 30 2019 18:21:03 GMT-0400 (Eastern Daylight Time)​</span>​</li>​
let ulAdd = document.querySelector('.bio-info');
undefined
ulAdd
<ul class=​"bio-info">​…​</ul>​
ulAdd.appendChild(listItem);
<li>​…​</li>​
leftSpan.className = "bio-info-title";
"bio-info-title"
rightSpan.className = "bio-info-value bio-info-location";
"bio-info-value bio-info-location"
