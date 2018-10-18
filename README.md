# Level1

## Q1
### Расскажите, чем, на ваш взгляд, отличается хорошая верстка от плохой с точки зрения 
* пользователя;
* менеджера проекта;
* дизайнера;
* верстальщика;
* клиентского программиста;
* серверного программиста.

Пользователю абсолютно все равно как внутри устроенно приложение, ему важно чтобы оно решало его проблему. Верстка это то, что видит пользователь и то, с чем он взаимодействует. Пользовать хочет чтобы приложение выглядело одинаково в любом браузере и на любом устройстве. Адаптивность и кросбраузерность это основные аспекты хорошей верстки.

Менеджер проекта - это среднее звено между заказчиком и командой разработчиков. Для него верстка - это один из этапов разработки приложения. Отличная верстка для менеджера - это верска сделанная в срок и полностью соответствовала тому что описано в техническом задании.

Дизайнеру важно чтобы верска соответсвавала макету который он разработал и который утвердил заказчик, чтобы приложение смотрелось на устройстве как он задумал.

Для верстальщика хорошая верстка это когда сложные вещи реализованны наиболее простыми решениями, но при этом достигнуты намеченные цели.

Клиентский программист задает поведение приложение в браузере пользователя, реакцию на действия пользователя. Ему важно интуитивно понять какой блок верски к чему относится и какой класс стиля меняет вид/состояние того или иного блока.

Серверному программисту вообще должно быть все равно на то как сделана верстка. Он предоставляет API для взаимодействия между приложением в браузере пользователя и серверным приложением. Ему куда важнее работа клиентского программиста, ведь от него зависит то, насколько эффективно выполняются запросы к API и то, насколько они безопасны.

---

## Q2
### Опишите основные особенности верстки крупных многостраничных сайтов, дизайн которых может меняться в процессе реализации и поддержки. Расскажите о своем опыте верстки подобных сайтов: какие методологии, инструменты и технологии вы применяли на практике.

Как правило многостраничные сайты имеют множество одинаковых элементов, заголовки, кнопки, формы ввода. Поэтому очень важно не дублировать код а переиспользовать его. Для этого необходимо делать верстку в виде самостоятельных блоков или компонентов. Компонентный подход позволяет решить ряд проблем
* уменьшает размер приложения;
* улучшает читаемость кода;
* уменьшает время разработки.

На практике я использую методологию БЭМ для написания html - разметки и стилей в своих работах. Компонентный подход необходимо применять не только в верстке но и в программировании в целом. В своих работах я использую  Angular 2+ — TypeScript-фреймворк с открытым исходным кодом и могу сказать что в нем заложен компонентный подход что значительно улучшает жизнь программисту. Также я применяю SCSS, стили становятся более читаемыми.

---

## Q3
### Опишите основные особенности верстки сайтов, которые должны одинаково хорошо отображаться как на любом современном компьютере, так и на смартфонах и планшетах под управлением iOS и Android. Расскажите о своем опыте верстки подобных сайтов: какие инструменты и технологии вы применяли, как проверяли результат на различных устройствах, какие именно устройства требовалось поддерживать.

Существует несколько подходов, позволяющих хорошо отображать сайты на различных устройствах с различными разрешениями экранов. Самый сложный из них - сделать отдельную версию сайта под конкретный экран. Тоесть будет загружаться некий код в браузер, который определит размер экрана и разрешение и перенаправит на нужную страницу или подгрузит нужные стили. Раньше так и делали. А еще определяли версию MS Internet Explorer и в зависимости от ситуации применяли конкретные "хаки". К счасью эти времена прошли, браузеры стали отображать верстку более или менее одинаково хотя и случаются сюрпризы. За последние годы сильно шагнул вперед html и css. Сегодня CSS flexbox - простой и незаменимый инструмент в создании резиновой адаптивной верстки. Также существуют методология формирования сетки в двумерной системе координат при помощи CSS3, фреймворки типа - Bootstrap реализуют эту прадигму. Еще забыл сказать про медиазапросы они тоже решают проблемы с адаптивностью. В своих работах я использовал чистый flexbox и [flexboxgrid24](https://www.npmjs.com/package/flexboxgrid24). 

---

## Q4
### Расскажите, какие инструменты помогают вам экономить время в процессе написания, проверки и отладки кода.

Незаменимый помощник в написании кода - среда разработки. Я попробовал работать в Atom, VS Code, WebStorm. Автоподсказки и линтеры сразу указывают на ошибки, позволяют формировать хорошие привычки у разработчика. Кроме того каждое изменение в вайлах приводит к автоматической пересборке проекта и результат этих действий тутже отбражается в браузере. Кроме того в IDE есть все для отладки приложения при непонятном его поведении. Современные браузеры имеют встроенные мощные инструменты разработчика, позволяющие отладить код и стили в вэб приложении. Иногда результат той или иной JS-функции/константы я вывожу в консоль (console.log(myFunc(arg)))

---

## Q5
### Вам нужно понять, почему страница отображается некорректно в Safari на iOS и в IE на Windows. Код писали не вы, доступа к исходникам у вас нет. Ваши действия? Сталкивались ли вы с подобными проблемами на практике?

Знакомая ситуация, но это не проблема, ведь весь код уже загружен и работает в моем браузере, мне ничего не мешает просмотреть код того или иного элемента страницы через инструменты разработчика и определить неисправность. Отсутствие доступа к исходникам не позволит мне исправить ситуацию.

---

## Q6
### Дизайнер отдал вам макет, в котором не показано, как должны выглядеть интерактивные элементы при наведении мыши. Ваши действия?

Я попрошу дизайнера проянить этот момент для меня, если ответа не последует предложу свой вариант.

---

## Q7
### Какие ресурсы вы используете для развития в профессиональной сфере? Приведите несколько конкретных примеров (сайты, блоги и так далее).

Книги которые я прочитал:
* Структура и интерпретация компьютерных программ (Харольд Абельсон, Джеральд Джей Сассман)
* Грокаем алгоритмы (Адитья Бхаргава)
* Операционная система UNIX (Андрей Робачевский, Сергей Немнюгин, Ольга Стесик)

Сайты:
* https://google.com
* https://developer.mozilla.org
* https://stackoverflow.com
* https://toster.ru
* https://habr.com
* https://hexlet.io
* https://udemy.com
* http://eng-word.ru

###  Какое направление развития вам более близко: JS-программирование, HTML/CSS-верстка или и то, и другое?

Мне все интересно и JS-программирование, и HTML/CSS-верстка. Я хочу сосредоточиться на чем-то одном чтобы научиться это делать правильно а затем перейти на что-то смежное.

### Какие ещё области знаний, кроме тех, что непосредственно относятся к работе, вам интересны?

Я увлекающаяся натура. Я люблю конструировать что-нибудь своими руками. Это может быть и полка в комнате, и макет ракеты, и светофор для ребенка на микроконтоллере. Увлекюсь и гуманитарными науками - история, психология.

---

## Q8
### Расскажите нам о себе и предоставьте несколько ссылок на последние работы, выполненные вами.

В детстве я был любознательным ребенком. Мне было интересно, как устроены самые простые вещи. Однажды моему школьному другу на день рождения родители подарили игровую приставку Dendy и мы каждый день после школы рубились в нее что было сил. Но мне это все быстро надоело, мой пытливый ум пытался понять как в эту маленькую коробочку – картридж, помещаются персонажи из игры, карты локаций, звуки и вообще на каких принципах эта техника работает? Однажды на мои глаза попался журнал об электронике "Левша". В одном из номеров журнала была опубликована схема радиолюбительского компьютера на основе аналога 8-и битного процессора Z80. Я смотрел на эту схему и мечтал собрать себе такой компьютер. Сам того не ведая я начал изучать электронику.

Шли годы, я взрослел, но тяга к компьютерной технике не угасала. После девятого класса передо мной встал выбор, продолжать учебу в школе или начать получать профессию, я выбрал второе. И вот я студент профессионального лицея информатики, бизнеса и дизайна. Учебе в лицее я отдавал всего себя, на стипендию я покупал книги по компьютерным наукам и электронике. Тогда впервые в лаборатории я познакомился с IBM PC c операционной системой MS DOS 6.22 и тогда с горящими глазами и такими же "одержимыми" студентами, начал пропадать в лаборатории допоздна. Рефераты я больше не писал от руки, набирал их на компьютере в текстовом редакторе Edit, блок-схемы рисовал в PCPaint. Распечатка на матричном принтере занимала много времени, но оторвать взгляд от его работы было невозможно :-). На последнем курсе лицея мы проходили практику в компьютерной фирме, где меня заметил руководитель и взял на работу на полставки. Мне нравилось получать теоретические знания и тут же их применять на практике. Таким образом, я мог продолжать учебу и стал зарабатывать первые деньги. На эти деньги я купил свой первый компьютер с dial-up модемом. Я был на седьмом небе от счастья, ведь теперь у меня дома появился интернет!

После лицея я решил расширить свои знания и поступил в институт. Институт и общежития охватывала большая локальная сеть с внутренними сайтами и файлообменниками. Эту сеть построили сами студенты. Тогда я увлекся Borland Turbo Assembler, я писал программы под математический сопроцессор Intel 8087, на низком уровне работал с Com-портом. В институте я впервые познакомился с AVR микроконтроллерами, которые меня тоже сильно увлекали. Тогда же я узнал, что такое UNIX и web-программирование. Я сделал несколько сайтов визиток, а также один интернет магазин на LAMP. Мной был написан парсер, который занес все товары в базу данных с чужого сайта-каталога.

С годами интерес ко всему новому не пропал. Я стараюсь идти в ногу со временем и применять полученные знания на практике. В каждой организации, где мне доводилось работать, я учился чему-то новому и как мог, улучшал существующие бизнес-процессы. В одной крупной торговой компании я разработал программно-аппаратный комплекс для тестирования Com-портов. Это позволило оперативно находить неисправности кассового оборудования. В муниципальной организации, я настроил сервер корпоративной электронной почты, а также внедрил систему электронного документооборота, что позволило ускорить работу специалистов и сократить расходы на бумагу. В другой организации я перевел информационную систему на сервер с операционной системы Linux, что позволило обслуживать клиентов в два раза быстрее, чем раньше. Передо мной никто не ставил такие задачи, я сам искал слабые места, обосновывал необходимость тех или иных решений, искал финансирование и воплощал идеи в жизнь.

Конечно это здорово когда ты можешь и комп с принтером починить, и сервак на любой оси поднять, и письмо накатать в какое-нибудь министерство. В маленьком городе чем больше айтишник умеет тем он лучше :-). Среди юристов и бухгалтеров ты конечно же первый парень на деревне, но это не делает тебя крутым специалистом в принципе. Ты занимаешься всем и сразу, а в итоге ничем. Распыляешь свою энергию и не можешь углубится ни во что конкретно. Вот я и превратился в 33-х летнего эникейщика, у меня нет карьерного роста, большой зарплаты или льготной ипотеки. Нет ничего, за что стоило бы держаться на этой или аналогичной работе. А самое главное, нет профессионального развития. Многие из моих бывших коллег не "парятся по жизни", до сих пор заправляют картриджи и устанавливают "паленую винду". Они даже понятия не имеют о параллельной Unix вселенной, зачем оно им? Я слишком много времени потратил впустую, и больше этого делать не намерен.

Прозрение наступило мгновенно, примерно год назад. Меня как будто молнией прошибло. На местном городском форуме я начал спрашивать ребят как жить дальше и к чему двигаться. И один человек мне рассказал про Hexlet и про то как там прокачивают навыки. Теперь в моей жизни появилась новая цель. Программирование меня очень увлекло и я понял как выбраться из того порочного круга куда я сам себя загнал. Я хочу стать программистом! На сегодняшний день пройдено половину курса по профессии "Бэкенд JS-программист (node.js)", прочитано несколько книг по профессии из списка рекомендованной литературы. И скажу что это очень круто! Мне раньше тоже приходилось писать программы, но я понятия не имел про рекурсию, свойство замыкания, ООП, git и т.д.

Четыре месяца назад я познакомился с действующим программистом "удаленщиком" из моего города. От него я узнал что на рынке труда больше востребованы фронтендеры нежели бэкендеры. И могу сказать, что эти четыре месяца прошли не зря. Он окунул меня в мир фреймворков Angular 2+, VueJs. Я поработал в Visual Studio Code и WebStorm. Научился отладке и поработал с Git, немного прокачался в верстке (БЭМ, flexbox, Css Grid). А еще познакомился с новым для меня языком TypeScript. За эти четыре месяца я сделал две тестовые работы по фронтенду.

Текущая работа, конечно, сильно мешает мне учиться, приходится использовать каждую свободную минуту, чтобы шаг за шагом продвигаться вперед. Часто приходится сидеть по ночам. Но это меня не останавливает, потому что я хочу реализовать свой нерастраченный потенциал и получить первую работу в качестве удаленного фронтенд разработчика в Вашей компании. Стремлюсь работать в сплоченном коллективе с хорошей инженерной культурой.

Мои хобби - катание на велосипеде, Arduino, шашки. Еще всегда отвечаю за шашлык на природе, уж очень люблю я это дело.

Моя работа

https://github.com/le2xx/Aviasales

# Level2

https://github.com/le2xx/CatShop
