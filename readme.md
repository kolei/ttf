# **https://github.com/kolei/ttf**

![](/img/qrcode.png)

# Билет в будущее

[(6-9) 45 мин]: _

## О компетенции **Разработка мобильных приложений**

[5 мин]: _

В настоящее время люди делают много операций с мобильным устройством: общаются со своими друзьями, заказывают пиццу, управляют банковским счетом и покупают еду для своего питомца. Мобильные приложения являются важнейшим инструментом развития современных технологий. Каждый день люди отказываются от обычного использования персонального компьютера в пользу смартфона или планшета - это является причиной роста рынка разработки мобильных приложений. Основная задача
специалиста - разработать надежное приложение, позволяющее упростить взаимодействие пользователя со знакомыми системами и сервисами.

Основная задача специалиста по разработке мобильных приложений — создание мобильного приложения, сочетающего в себе такие обязательные качества, как безотказная работа на одной или нескольких мобильных операционных платформах (Apple iOS, Google Android), понятный интерфейс, чтобы у пользователя не возникало проблем при работе с экранами небольшого размера (например, умными часами). Все взаимодействие с внешними ресурсами должно быть защищено, чтобы данные не попадали в руки злоумышленников. Приложения могут решать какую-либо проблему пользователя или иметь развлекательный характер.

Разработчик мобильных приложений занимается проектированием и разработкой приложений для мобильных устройств: смартфонов, планшетов, умных часов, а также систем Smart TV. Для разработки используется различное программное обеспечение, выбор которого зависит от целевой операционной системы. В настоящий момент наиболее распространенными являются операционные системы iOS и Android.

Информационные технологии в целом, и программирование, в частности, развиваются очень активно. Разработка мобильных приложений является одной из наиболее быстроразвивающихся отраслей, поскольку популярность портативных устройств только растет. Смартфоны и планшеты используются не только для игр и досуга, но и для занятий спортом, приобретения товаров, ведения бизнеса, общения, образования, удовлетворения многих других потребностей современного человека.

Повсеместное внедрение мобильных технологий делает данную профессию очень перспективной.

Ключевыми навыками разработчика мобильных приложений являются умение программировать,
знание принципов построения удобного пользовательского интерфейса, внимательность. Владение английским языком также является важным навыком любого разработчика, поскольку вся документация публикуется на английском языке.

Помимо образования необходима специализация: изучение необходимых инструментов самостоятельно или при прохождении каких-либо курсов (онлайн или офлайн).

## Постановка задачи

[5 мин]: _

* ТБ

    ...

* формулировка задания

    Необходимо разработать мобильное приложение согласно представленному макету. Приложение должно поддерживать запуск на устройствах с операционной системой Android 9.0 и новее.

* выдача материалов

    Откройте в браузере репозиторий https://github.com/kolei/ttf

* демонстрация финального продукта

    ![финальный продукт](/img/ttf00.jpg)

## Выполнение (возрастная категория 6-11 класс)

[30 мин]: _

### Установите Android Studio 

[Инструкция по установке](https://github.com/kolei/yotc/blob/master/articles/android_studio_install.md)

### Создайте новый проект

* Создайте новый проект (File - New - New Project...)

    ![создание нового проекта](/img/as007.png)    

* Выберите "Empty Activity"

    ![создание нового проекта](/img/as001.png)    

* Задайте название (Name) и, если нужно, местоположение (Save location) проекта. Выберите *Minimum API level* в соответствии с заданием (Версия Андроид 9 и выше). Остальные настройки по-умолчанию:

    ![настройка проекта](/img/as002.png)

* Запустите проект чтобы убедиться, что все установлено нормально. Если проект не запускается - обратитесь к наставнику.

    Кнопка запуска вверху Android Studio: 

    ![настройка проекта](/img/ttf11.png)

### Стили и константы

1. В левой части экрана расположена структура проекта (вкладка *Project*). Откройте файл *colors.xml* расположенный в папке **res -> values**

    ![colors.xml](/img/ttf01.png)

    Замените значения основных цветов приложения на следующие (значения находятся между угловыми скобками):

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <resources>
        <color name="colorPrimary">#C48D50</color>
        <color name="colorPrimaryDark">#BD6B2D</color>
        <color name="colorAccent">#8D311E</color>
    </resources>
    ```

2. Откройте файл *strings.xml* (там же в ресурсах проекта) замените заголовок приложения и добавьте строковую константу *label* с текстом "Какая твоя любимая порода?". 

    Должно получиться следующее:

    ```xml
    <resources>
        <string name="app_name">Favourite Dog</string>
        <string name="label">Какая твоя любимая порода?</string>
    </resources>
    ```

    >Константы нужны для того, чтобы упростить перевод приложения на разные языки. Для этого в коде приложения вместо текста используются ссылки на текстовые константы и для перевода на нужный язык достаточно создать *strings.xml* для нужного языка.

3. Откройте файл *AndroidManifest.xml* в папке манифест (всё там же в структуре проекта) и измените название проекта и окна:

    ![Манифест](/img/ttf02.png)

    Конструкция **@string/** в значении атрибута как раз и указывает что данные надо взять из ресурсов.

Запустите проект и посмотрите, как изменились цвета и заголовок экрана.

### Добавьте в проект изображения 

Добавьте изображения собак из папки *Ресурсы*, которая прилагается к репозиторию. Для этого необходимо перетянуть (drag-and-drop) файлы изображений в папку *res -> drawable* проекта.

![](/img/ttf04.png)

>Можно скачать архив: ![](/img/ttf03.png)
>
>Либо, если умеете, клонировать репозиторий
>
>Либо просто открывать картинки и сохранять средствами браузера

Структура проекта после добавления картинок:

![](/img/ttf05.png)

### Добавление на экран приложения кнопок с изображениями собак.

1. Откройте файл *activity_main.xml* в папке *res -> layout* (но, скорее всего, он у вас уже открыт). Убедитесь, что выбран режим *Design*. На форме (белая область в центре) есть надпись "Hello world!". Выделите ее с помощью мыши и удалите, нажав кнопку Delete на клавиатуре.

    ![](/img/ttf06.png)


2. Откройте закладку Buttons на палитре элементов. Выберите элемент ImageButton и перетащите его на форму с помощью мыши

    ![](/img/ttf07.png)

    В появившемся окне выберите изображение собаки и нажмите "OK".

    ![](/img/ttf08.png)

    Аналогичным образом добавьте еще три кнопки с ранее не использованными изображениями собак. Расположите кнопки на экране произвольным образом (размеры кнопок можно менять):

    ![](/img/ttf09.png)

3. Закрепите позиции кнопок на экране, создав ограничения (наш шаблон основан на *constraintlayout*, а для него у каждого элемента должны быть заданы две координаты). Для этого нажмите кнопку *Infer Constraints*

    ![](/img/ttf10.png)


4. Запустите приложение и убедитесь в работоспособности и соответствии шаблону.

[Оценка 6-9: 
Задание успешно выполнено, если мобильное приложение запускается, внешний вид соответствует макету. При оценке следует учитывать время, затраченное на выполнение задания, уверенность в совершаемых действиях]: _

[## Выполнение (продолжение, возрастная категория 10-11 класс)
обработать клики - добавить внизу textlabel и выводить в него породу выбранной собаки]: _

[## Рефлексия]: _
[5-10 мин]: _
