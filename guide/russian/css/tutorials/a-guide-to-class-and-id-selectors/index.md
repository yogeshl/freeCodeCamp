---
title: A Guide to Class and Id Selectors
localeTitle: Руководство по выбору классов и идентификаторов
---
## Руководство по выбору классов и идентификаторов

Это статья, основанная на CSS-селекторах. CSS используется для стилизации HTML-элементов и веб-страницы в целом. Чтобы CSS мог стилизовать элемент на странице, необходимо сначала выбрать этот элемент.

Как и то, как вам нужно выбрать файл на вашем компьютере, прежде чем удалять его. Вы должны указать своей машине точно, какой файл вы хотите изменить или удалить. Точно так же вам нужно указать CSS, какой элемент должен быть нацелен при применении на нем разных стилей и цветов.

Хотя CSS может очень хорошо выбирать элементы, вы можете поручить ему выбрать очень конкретные элементы. В конце этой статьи вы уйдете со знанием, чтобы выбрать и подстроить определенные элементы.

### Что такое класс и идентификатор?

Допустим, у вас есть 5 элементов абзаца в вашем коде HTML.

```html

<p> First paragraph </p> 
 <p> Second paragraph </p> 
 <p> Third paragraph </p> 
 <p> Fourth paragraph </p> 
 <p> Fifth paragraph </p> 
```

Вы можете дать каждому из них цвет шрифта красного цвета с помощью CSS.

```css
p { 
    color: red; 
 } 
```

Это очень легко! Но что, если вы только хотите дать второму абзацу цвет шрифта? Сейчас это немного сложно. Поскольку мы не можем идентифицировать каждый элемент абзаца индивидуально, мы не можем выбирать их отдельно.

_Класс и идентификатор для спасения_

Класс и идентификатор действуют как удостоверения личности для элементов HTML. Оба помогают отделить один элемент от другого, но немного отличаются.

* * *

Допустим, вы встречаете парня из какого-то клуба. Когда вы спрашиваете этого человека для удостоверения личности своего клуба, они показывают его своим именем клуба. Теперь все члены одного клуба будут иметь тот же удостоверение личности?

Если есть 3 клуба - A, B и C. Тогда все члены клуба A будут иметь одинаковые удостоверения личности. Все члены клуба B также будут иметь те же самые, хотя они будут отличаться от удостоверений личности клуба A и клуба C. Вот как вы знаете, кто из какого клуба.

Вот как работает `class` . Вы можете дать кучу элементов класса, и они будут в одном клубе. Точно так же, как новое правило в клубе должно сопровождаться всеми членами клуба, аналогичным образом, все новые правила стиля применяются к элементам в одном клубе.

```html

<p class="bike"> Hayabusa </p> 
 <p class="car"> Chevrolet </p> 
 <p class="bike"> Hayley-Davidson </p> 
 <p class="car"> Lamborghini </p> 
```

Здесь у нас есть 4 параграфа. Если вы посмотрите на имена классов, есть 2 «клуба». Теперь мы можем выбрать клуб (или группу), который мы хотим, и применить стили, которые мы хотим на них.

```css
.bike { 
    color: blue; 
 } 
```

Вы можете выбрать группу вместо определенного элемента, добавив имя группы с периодом `.` и примените стили, которые вы хотите к этой группе. В этом примере цвет шрифта синего применяется только к параграфам, которые имеют класс `bike` .

* * *

Если вы понимаете, какой `class` , то идентификатор будет легко понять.

Из предыдущего примера, удостоверение личности клуба представляет клуб, и все его члены имеют его. Однако, если вы попросите их предоставить удостоверение личности, у человека появится другое удостоверение личности, которое у них есть. У каждого есть другое и может использоваться для идентификации их по отдельности.

Это идентификатор. Как и личные удостоверения личности, только один элемент HTML может иметь определенный `id` . Ни один из двух элементов не имеет одинакового `id` .

```html

<p id="car"> Ferrari </p> 
 <p id="car"> Ford </p> 
 <!-- This is incorrect--> 
 
 <p id="harley"> Harley-Davidson </p> 
 <p id="hayabusa"> Hayabusa </p> 
 <!--This is correct since an id is only used once.--> 
```

`id` также может быть похож на закрытый ключ для вашего шкафчика в клубе. У всех в клубе есть один и тот же карточный идентификационный номер клуба, но все ключи для шкафчиков различны и уникальны.

Как и в примере с `class` , вы можете выбрать конкретный элемент и применить к нему стили, добавив имя id с `#` .

```css
#hayabusa { 
    font-style: bold; 
 } 
```

* * *

Легко запомнить - использовать `.` перед именем для _класса_ и `#` перед именем для _id_ .

Оба имеют свои собственные цели.

> class используется, когда стили должны применяться к нескольким элементам, а id используется, когда стили должны применяться к определенному элементу.

Помните об этом, когда вы используете класс и идентификатор для выбора и стиля отдельных элементов.

При этом вы добавили больше инструментов в панель инструментов для стилизации элементов на веб-странице.