## Who am I?

Aliaksei Palanevich

## My contacts:

- _email_ -- palanevich.aleksey@gmail.com
- _telegram_ -- @palanevich

## What's I want to do

How many people before me I'd like to do funny things, traveling around the World and no think about next breakfast. From summer 2020 I plunged into communication with people not only in my social space but from other groups and country. It's a inspiring experience so I'd like to continue to communicate with different people.

## What's I can to do

I can:

- create pages on __html&css__ or on some preprocessors like __pug&sass__.
- setup page logic with __js__ (or __ts__).
- do two previous work on __React__ (and if you need with __Redux__).
- do first two work on __Vue__ but no such good.
- use __git&Github__ to improve team productivity.

I also know how to work __Python3__, __unix console :D__

## Code examples

Here I automate typical actions when you work with vanilla js.

```js
export default class Unit {
  /**
   *
   * @param {string} tag - html tag like 'div', 'nav' and etc.
   * @param {(string|string[])} CSSClass - CSS class for element
   * @param {string[]} otherClass - next CSS classes for element
   *
   * @example
   * const img = new Unit('img');
   * const img = new Unit('img', 'class1');
   * const img = new Unit('img', ['class1', 'class2'], 'class3');
   */
  constructor(tag, CSSClass = "", ...otherClass) {
    this.subscriptions = [];
    this.unit = document.createElement(tag);
    if (CSSClass) this.addClass(CSSClass);
    if (otherClass.length) this.addClass(otherClass);
  }

  /**
   * Add CSS class to unit
   * @param {(string|string[])} className
   */
  addClass = (className) => {
    if (Array.isArray(className)) {
      this.unit.classList.add(...className);
    } else {
      this.unit.classList.add(className);
    }
  };

  /**
   * Remove CSS class from unit
   * @param {(string|string[])} className
   */
  removeClass = (className) => {
    if (Array.isArray(className)) {
      this.unit.classList.remove(...className);
    } else {
      this.unit.classList.remove(className);
    }
  };

  /**
   * Add attributes to tag
   * @param {object} attrObj - The object that containing attributes
   *
   * @example
   * img.addAttr({
   *  id: 'myImg',
   *  src: '/some/path/img.jpg',
   * })
   */
  addAttr = (attrObj) => {
    Object.keys(attrObj).forEach((attr) => {
      this.unit[attr] = attrObj[attr];
    });
  };

  /**
   * Remove attributes from tag
   * @param {(string|string[])}
   */
  removeAttr = (attrArr) => {
    if (Array.isArray(attrArr)) {
      attrArr.forEach((attr) => {
        this.unit.removeAttribute(attr);
      });
    } else {
      this.unit.removeAttribute(attrArr);
    }
  };

  /**
   * Add dataset-attributes to tag
   * @param {object} data - The object that containing dataset-attributes
   * @example
   * img.addDataset({
   *  name: 'John',
   *  dateOfBirth: '2000-10-10',
   * })
   */
  addDataset = (data) => {
    Object.keys(data).forEach((key) => {
      this.unit.dataset[key] = data[key];
    });
  };

  setInnerText = (text) => {
    this.unit.innerText = text;
  };

  /**
   * Inserts nodes after the last child of node.
   * @param {(string|Node)[]} nodes
   */
  append = (...nodes) => {
    if (Array.isArray(nodes)) {
      this.unit.append(...nodes);
    } else {
      this.unit.append(nodes);
    }
  };

  /**
   * Delete all node's children
   */
  clearChildren = () => {
    this.unit.innerHTML = "";
  };

  /**
   * Appends an events listener for tag
   * @param {string} event - type of event
   * @param {Function} func - the callback that will be invoked when the event is dispatched
   */
  subscribe = (event, func) => {
    this.subscriptions.push([event, func]);
    this.unit.addEventListener(event, func);
  };

  /**
   * Removes the event listener from tag with the same type and callback.
   * @param {string} event- type of event to delete
   * @param {Function} func - the callback that will be deleted
   */
  unsubscribe = (event, func) => {
    for (let i = 0; i < this.subscriptions.length - 1; i += 1) {
      const element = this.subscriptions[i];

      if (event === element[0] && func === element[1]) {
        this.unit.removeEventListener(event, func);
        this.subscriptions.splice(i, 1);
        i -= 1;
      }
    }
  };
}
```

## Experience:

Responsive markup: [code](https://github.com/GolDOragon/singolo) and [demo](https://goldoragon.github.io/singolo/);
Simple work with DOM: [code](https://github.com/GolDOragon/virtual-keyboard) and [demo](https://goldoragon.github.io/virtual-keyboard/);
React: [code](https://github.com/GolDOragon/songbird) and [demo](https://goldoragon-songbird.netlify.app/)

I can't fork rep and show you code but it's my works, really:

- [english-for-kids](https://goldoragon-english-for-kids.netlify.app/) -- first app with interesting logic.
- [movie-search](https://goldoragon-movie-search.netlify.app/) -- work with API.
- [RSLang](https://rslang-team42-andreimedvedevsaratov.netlify.app/) -- team works.

And I solve many katas:

- [codewars](https://www.codewars.com/users/GolDOragon)
- [checkio](https://py.checkio.org/user/palanevich.aleksey/list/)

## Education:

I have few certificates:

- [RSSchool](https://app.rs.school/certificate/n4knovsx)
- [git](https://stepik.org/cert/229740)
- [Python](https://stepik.org/course/67)

I have graduated with distinctions from Belarusian National Technical University, power supply specialize, and now study at International Institute of Distance Education, automatization specialize like masters.

## English

EPAM testing system shows a B1 level in reading and understanding text. Maybe an A2 or A2+ in conversation. Now I look for information on English resources, watch technical videos without subs but fast native speakers are poorly perceived.
