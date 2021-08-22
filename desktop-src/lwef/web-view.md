---
title: Настройка веб-представления папки
description: веб-представление — это мощный и гибкий способ использования обозревателя Windows для отображения сведений о содержимом папки оболочки.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Веб-представления
- Классический стиль
- Стиль веб-сайта
- баннеры
- Регион FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ebe106bdada4da55eef8891a3c93ee82aba3cc4da9194e1fcd4c7e71bcd4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745698"
---
# <a name="customizing-a-folders-web-view"></a>Настройка веб-представления папки

\[эта функция поддерживается только в Windows XP и более ранних версиях. \]

веб-представление — это мощный и гибкий способ использования обозревателя Windows для отображения сведений о содержимом папки оболочки.

-   [Введение](#introduction)
-   [Использование шаблона веб-представления](#using-the-web-view-template)
    -   [Тело шаблона](#the-template-body)
    -   [Заголовок шаблона](#the-template-head)
-   [Сводка](#summary)

## <a name="introduction"></a>Введение

Windows предлагает пользователям два основных способа просмотра и навигации по пространству имен оболочки. наиболее привычные из них, классический стиль, похожи на знакомый диспетчер файлов Windows. В области справа отображается содержимое выбранной папки в одном из пяти форматов: крупный значок, маленький значок, список, подробности и эскиз. основное отличие от диспетчера файлов Windows — это левая панель, которая очень похожа на панель обозревателя Windows Internet Explorer. Его можно изменить или удалить, а также отобразить несколько панелей в дополнение к знакомому дереву файловой системы, например панели поиска.

> [!Note]  
> информация в этом документе не относится к Windows XP, описанные методики применимы только к предыдущим версиям Windows.

 

На следующем рисунке показана папка "принтеры" в классическом стиле.

![Классический стиль папки "принтеры".](images/webview1.png)

Классический стиль хорошо подходит для обычных папок и файлов файловой системы. однако с появлением Windows 95, файловая система превратилась в пространство имен. Пространство имен позволяет создавать *Виртуальные папки*, такие как принтеры или сетевые окружения, которые могут представлять весьма разные типы информации, чем обычная папка файловой системы.

Веб-стиль, также известный как веб-представление, предлагает более гибкий и эффективный способ представления информации, чем классический стиль. В веб-представлении пользователь по сути просматривает пространство имен и переходит по нему с помощью Internet Explorer. Базовый макет веб-представления аналогичен классическому стилю. Панель обозревателя не изменилась. Тем не менее регион, занятый списком файлов, становится областью для вывода общего назначения, которая фактически является веб-страницей. Веб-представление по-прежнему используется для отображения сведений о содержимом папки, но существует несколько ограничений на отображаемую информацию или как. Каждая папка может иметь собственное веб-представление, настроенное в соответствии с определенными функциями.

На следующем рисунке показано веб-представление папки "принтеры" (показано ранее в классическом стиле).

![веб-представление папки "принтеры" по умолчанию.](images/webview2.png)

Так же, как и обычные веб-страницы, управление ими осуществляется с помощью шаблона на основе HTML. Разработка шаблона веб-представления практически идентична созданию страницы и обеспечивает такую же степень гибкости в содержимом и структуре информации. Шаблоны веб-представлений могут использовать динамический HTML (DHTML) и скрипты для реагирования на события, например, при щелчке элемента пользователем. Они также могут размещать объекты, позволяющие им получать и отображать информацию из папки или ее содержимого.

пользователь может выбрать веб-представление, запустив Windows Explorer, выбрав пункт **свойства папки** в меню **вид** и выбрав этот параметр: **включить веб-содержимое в папках**. Тем не менее пользователь может также запустить Internet Explorer и указать браузер в файловой системе, щелкнув меню **вид** , выбрав пункт **панель обозревателя** и щелкнув **папки**. в веб-представлении не существует практически никаких различий между Internet explorer и проводником Windows.

В левой части области справа в веб-представлении принтеры отображается баннер с именем и значком папки, а затем — блок сведений о папке. Обычный список файлов занимает правой части страницы.

Когда пользователь щелкает элемент, в информационном блоке отображаются подробные сведения об этом элементе. В веб-представлении «принтеры» фактически отображаются те же сведения, что и в классическом стиле, но это делается в более удобном для использования формате. Однако веб-представление — это не просто другой способ отображения классической информации о стиле. Например, ссылка на полезный веб-сайт может отображаться под информационным блоком, компонентом, который недоступен в классическом стиле. Если пользователь щелкнет ссылку, отобразится сайт.

Веб-представление принтеров, показанное на предыдущем рисунке, похоже на классический стиль, поскольку базовый шаблон веб-представления (файл HTT) был написан таким образом. Этот список файлов, например, не создается непосредственно шаблоном веб-представления. Он создается и отображается объектом [**вебвиевфолдерконтентс**](webviewfoldercontents.md) , размещенным в шаблоне веб-представления. Методы и свойства объекта позволяют веб-представлению управлять макетом и получать сведения об определенных элементах. Содержимое и компоновка баннера и информационного блока указываются в шаблоне веб-представления.

Так как веб-представление поддерживает DHTML, этот шаблон можно также использовать для управления взаимодействием с пользователем. Например, когда пользователь щелкает один из значков принтера, объект **вебвиевфолдерикон** запускает событие [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) . Шаблон использует обработчик событий DHTML, написанный в скрипте, для получения запрошенной информации и их вывода в информационном блоке.

Этот простой пример для папки принтеров — это не единственный способ использовать веб-представление. Создавая собственный шаблон и, при необходимости, объекты, вы можете использовать веб-представление для отображения информации и взаимодействия с пользователем любым способом, наиболее эффективным. Обратите внимание, что в настоящее время в шаблонах веб-представлений отображаются только определенные системой виртуальные папки. Хотя разработчики могут создать виртуальную папку путем реализации расширения пространства имен, они должны использовать методы, описанные в разделе [расширения пространства имен](/windows/desktop/shell/nse-works) , чтобы отобразить их.

## <a name="using-the-web-view-template"></a>Использование шаблона веб-представления

Способ отображения данных в веб-представлении можно изменить, изменив файл Desktop.ini папки. Дополнительные сведения см. [в разделе Настройка папок с помощью Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) . Гораздо более гибкий и эффективный способ настройки веб-представления — создание пользовательского шаблона веб-представления.

Шаблон веб-представления определяет, что отображается в веб-представлении и как. Он использует стандартные методы HTML, DHTML и создания сценариев для получения и просмотра информации и взаимодействия с пользователем. В этом разделе описано, как создать веб-представление, изучив простой шаблон — Generic. htt.


```
<html>
    <style>
    <!-- This section defines a variety of styles that can be used
     when displaying the document -->
        body        {font: 8pt/10pt verdana; margin: 0}
        #Banner     {position: absolute; width: 100%; height: 88px; background: URL(res://webvw.dll/folder.gif) no-repeat top left}
        #MiniBanner {position: absolute; width: 100%; height: 32px; background: window}
        #Icon       {position: absolute; left: 11px; top: 12px; width: 64px; height: 64px}
        #FileList   {position: absolute; left: 30%; top: 88px; width: 1px; height: 1px}
        #Info       {position: absolute; top: 88px; width: 30%; background: window; overflow: auto}
        p       {margin-left: 20px; margin-right: 8px}
        p.Title     {font: 16pt/16pt verdana; font-weight: bold; color: #0099FF}
        a:link      {color: #FF6633}
        a:visited   {color: #0099FF}
        a:active    {color: black}
    </style>

    <head>
        <!-- allow references to any resources you might add to the
         folder -->
        <base href="%THISDIRPATH%\">

        <script language="JavaScript">
        
        <!-- This section defines a number of JavaScript utilities -->
            var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br><br>To get information about any of them, click the items icon.<br><br>";
            var L_Multiple_Text = " objects selected.";

            function FixSize() {
            // this function handles layout issues not covered by the style sheet

                var hideTop = 200;
                var hideLeft    = 400;
                var miniHeight  = 32;

                if (200 > document.body.clientHeight) {
                //A short window. Use the minibanner
                    document.all.Banner.style.visibility = "hidden";
                    document.all.MiniBanner.style.visibility = "visible";
                    document.all.FileList.style.top = 32;
                    document.all.Info.style.top = 32;
                }

                else {
                //A normal window. Use the normal banner
                    document.all.Banner.style.visibility = "visible";
                    document.all.MiniBanner.style.visibility = "hidden";
                    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
                    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
                    document.all.Rule.style.width = (document.body.clientWidth > 84 ? document.body.clientWidth - 84 : 0) + "px";     
                }
                if (400 > document.body.clientWidth) {
                //A narrow window. Hide the Info region and expand the file list region
                    document.all.Info.style.visibility = "hidden";
                    document.all.FileList.style.pixelLeft = 0;
                    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
                }

                else {
                //Normal width
                    document.all.Info.style.visibility = "visible";
                    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
                }
                document.all.FileList.style.pixelWidth = document.body.clientWidth - document.all.FileList.style.pixelLeft;
                document.all.FileList.style.pixelHeight = document.body.clientHeight - document.all.FileList.style.pixelTop;
                document.all.Info.style.pixelHeight = document.body.clientHeight - document.all.Info.style.pixelTop;
            }

            function Init() {
                /* Set the initial layout and have FixSize() called whenever the window is resized*/
                window.onresize = FixSize;
                FixSize();
                TextBlock.innerHTML = L_Intro_Text;
            }
        </script>

        <script language="JavaScript" for="FileList" event="SelectionChanged">
            // Updates the TextBlock region when an item is selected
            var data;
            var text;

            // name
            text = "<b>" + FileList.FocusedItem.Name + "</b>";

            // comment
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
            if (data)
                text += "<br>" + data;

            // documents
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
            if (data)
                text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

            // status
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
            if (data)
                text += "<br><br><b><font color=red>" + data + "</font></b>";

            // tip?
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
            if (data != "" && data != FileList.FocusedItem.Name)
                text += "<br><br>" + data;

            TextBlock.innerHTML = text;
        </script>
    </head>
<!-- The body of the document controls the actual data display.
 It uses several scripting objects to communicate with the
 namespace folder, and calls on the JavaScript objects defined
 in the header to handle much of the processing -->
    <body scroll=no onload="Init()">

        <!-- The normal banner. This banner displays the folder
         name and icon at the top of the WebView pane. This banner
         is used if the WebView pane is sufficiently large to
         display the icon and still have room for some information -->
        <div id="Banner" style="visibility: hidden">
            <!-- Display the folder name using a table with nowrap
             to prevent word wrapping. Explorer will replace
              %THISDIRNAME% with the current folder name -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 104px; margin-top: 16px">
                %THISDIRNAME% 
            </td></tr></table>
            <!-- this is more efficient than a long graphic, but it has to be adjusted in FixSize() -->
            <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
            <!-- Load the WebViewFolderIcon object, which extracts the folder's icon -->
            <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
                <param name="scale" value=200>
            </object>
        </div>

        <!-- The mini banner. This banner is used when the
         WebView pane is too short to display the icon. Instead,
          it displays only the folder name -->
        <div id="MiniBanner" style="visibility: hidden">
            <!-- use a table with nowrap to prevent word wrapping -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 16px; margin-top: 4px">
                %THISDIRNAME%
            </td></tr></table>
        </div>

        <!-- The Info region. This displays the information
         associated with a folder or file. Javascript in the header
         is used to generate the regions contents by by assigning
         a text block to TextBlock.innerHTML -->
        <div id="Info">
            <p style="margin-top: 16px");
            <span id="TextBlock">
            </span>
        </div>
        <!-- end left info panel -->

        <!-- Load the WebViewFolderContents object. This object
         returns information on the contents of the folder that
          can be used in the information display.  -->
        <object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>

    </body>
</html>
            
```



Простой способ создать собственный шаблон веб-представления — использовать Generic. htt и изменить его. Так как он довольно ограничен, вы также можете ознакомиться с другими, более сложными примерами для получения дополнительных идей. Их можно найти, выполнив поиск расширения htt, используемого всеми шаблонами веб-представлений, в системе. если вы хотите создать пользовательский шаблон для папки, следует начать с шаблона folder. htt по умолчанию, который обычно хранится в каталоге c: \\ Winnt \\ web или c: \\ Windows \\ Web. обратите внимание, что эти файлы определены как скрытые, поэтому для их просмотра может потребоваться изменить параметры обозревателя Windows. После создания HTT-файла он должен быть помечен как "только для чтения" и скрытым.

Шаблоны веб-представлений используют расширение htt, поскольку они немного отличаются от обычных документов .htm. Основное отличие — несколько специальных переменных в HTT-файлах, которые система заменяет текущими значениями пространства имен. Переменные% СИСДИР% и% СИСДИРПАС% представляют имя и путь выбранной папки. Переменная% ТЕМПЛАТЕДИР% представляет папку, в которой хранятся таблицы стилей веб-представлений.

Как и большинство шаблонов HTML, файлы. htt имеют две основные части: текст и головной элемент. Тело шаблона управляет базовым макетом веб-представления и загружает объекты, используемые для связи с пространством имен и отображаемые сведения. Заголовок содержит сценарии и функции, которые выполняют такие задачи, как обработка изменения размера и получение сведений из папки. Большинство шаблонов, включая Generic. htt, также включают таблицу стилей. В общем случае лучше включить в шаблон сведения о таблице стилей. Отдельные таблицы стилей могут работать неправильно, если веб-представление используется с удаленными пространствами имен.

### <a name="the-template-body"></a>Тело шаблона

В тексте шаблона указывается, что будет представлено веб-представлением. Здесь также загружаются объекты, используемые для вывода сведений и взаимодействия с папками пространства имен. Макет, определяемый Generic. htt, аналогичен показанному на рисунке в предыдущем разделе. Существует три области отображения: баннер и блок сведений в левой части представления, а также список файлов справа.

Регионы — это все назначенные идентификаторы, используемые таблицами стилей и DHTML. Как обсуждалось в следующем разделе, существует два возможных баннера с идентификаторами "Banner" и "Минибаннер". Идентификатор региона информационного блока — "info". Идентификатор объекта списка файлов — "FileList". сведения о [макете](#controlling-the-web-view-layout) области обрабатываются таблицей стилей и функцией Microsoft JScript [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function), которая обсуждается далее в этой главе.

### <a name="the-banner-region"></a>Область заголовка

Баннер находится в верхней части экрана в левом верхнем углу веб-представления. В стандартном баннере отображается имя и значок папки, содержимое которой отображается в списке файлов справа. Однако если окно оказывается слишком коротким, то под значком может отсутствовать место для вывода сведений. По этой причине Generic. htt также определяет минибаннер, который отображает только имя папки. Оба баннера изначально определены как скрытые. [Фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) выбирает, какой из них должен отображаться, и присваивает ему значение "Visible".

Обычный баннер для Generic. htt определяется следующим образом:


```
<div id="Banner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
    <p class=Title style="margin-left: 104px; margin-top: 16px">
        %THISDIRNAME% 
    </td></tr></table>
    <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
    <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
        <param name="scale" value=200>
    </object>
</div>
                    
```



В первой части раздела баннера отображается заголовок с горизонтальным правилом под ним. Теги таблицы используются для управления позицией. Атрибут InAttribute устанавливается для <TD> , чтобы запретить перенос по словам. Система заменит% СИСДИРНАМЕ% именем текущей папки. Затем загружается объект **вебвиевфолдерикон** с идентификатором "Icon" для простоты и извлекается и отображается значок папки.

Раздел минибаннер подобен стандартному баннеру. Формат заголовка размещается немного выше и не имеет правила. Поскольку значок отсутствует, объект **вебвиевфолдерикон** не загружается.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>Область сведений

Часть веб-представления под баннером используется для отображения подробных сведений о выбранном элементе. Если элемент не выбран, отображается сообщение по умолчанию. Поскольку Generic. htt отображает только один блок текста, этот раздел довольно прост.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



Большая часть работы по сбору информации обрабатывается [сценарием сведений о папке](#retrieving-and-displaying-folder-information) , который обсуждается далее в этой главе. Она отображает информацию, присваивая текст [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

Вы можете легко настроить отображение информации, изменив эти элементы или добавив дополнительные. Можно использовать все, что можно разместить на веб-странице. Например, чтобы отобразить ссылку на веб-сайт, можно добавить элемент привязки после текстового блока в Generic. htt.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
        <span>
        <p> Click on <a href="https://your.address"></a>
        </span>
</div>
                    
```



### <a name="the-filelist-region"></a>Регион FileList

Наконец, Generic. htt загружает объект [**вебвиевфолдерконтентс**](webviewfoldercontents.md) для региона filelist. Так как для его идентификатора задано значение "FileList", он будет называться как объект FileList в данный момент.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



Объект FileList находится в большинстве веб-представлений и служит для нескольких целей. FileList отображает список элементов, содержащихся в выбранной папке, с теми же параметрами и оформлением, что и список файлов в классическом стиле. При выборе элемента FileList уведомляет веб-представление, выпуская событие [SelectionChanged](#retrieving-and-displaying-folder-information) . FileList также предоставляет методы и свойства, которые можно использовать для получения сведений об отдельных элементах и управления положением и размером отображаемой области.

Хотя объект FileList очень полезен, он возвращает только стандартные сведения о файловой системе, такие как размер файла или атрибуты. Чтобы получить сведения о других видах из папки оболочки, необходимо загрузить и обработать дополнительные объекты. Любой объект, который может быть размещен на веб-странице, может использоваться с представлением в Интернете.

### <a name="the-template-head"></a>Заголовок шаблона

Заголовок шаблона веб-представления содержит скрипты и функции, которые выполняют большую часть реальной работы. Существует две необходимые задачи, которые необходимо обработать. Одна из них — макет отображения веб-представления, который необходимо настроить для размещения различных областей отображения. Второй — получение и отображение информации из папки при выборе элемента. Как и в случае с таблицами стилей, лучше включить в шаблон все скрипты и функции, а не ссылаться на них как на отдельные файлы.

### <a name="controlling-the-web-view-layout"></a>Управление макетом веб-представления

область, доступная для веб-представления, зависит от размера окна веб-представления и объема, занимаемого панелью Windows Explorer. эта область изменяется всякий раз, когда изменяется размер окна или Windows панели обозревателя. Поэтому макет должен быть сопоставлен с доступной областью, когда веб-представление загружается и соответствующим образом изменяется при изменении размера. Большая часть макета задается в таблице стилей. Область сведений, например, определяется таким образом, чтобы занимать самые левые 30% веб-представления.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



При изменении размера веб-представления ширина области сведений изменится, чтобы поддерживать этот процент. [Фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) управляет проблемами макета, которые не могут быть обработаны таблицей стилей.

### <a name="loading-and-initializing-the-web-view"></a>Загрузка и инициализация веб-представления

При загрузке веб-представления макет необходимо настроить в соответствии с доступной областью отображения. Поскольку элемент еще не выбран, веб-представления обычно отображают некоторые сведения по умолчанию, которые применяются ко всей папке. Для работы с инициализацией элемент управления <BODY> тег для Generic. htt определяет событие [OnLoad](/previous-versions//ms531409(v=vs.85)) и вызывает функцию **init** .


```
<body scroll=no onload="Init">
                    
```



**Init** — это простая JScript функция.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** привязывает [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) к событию [Window. онресизе](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) , чтобы оно вызывалось при каждом изменении области отображения веб-представления. Затем он запускает Фикссизе для установки начального макета и назначает ввод текста в \_ \_ области сведений. \_ \_ Вводный текст — это блок ввода текста, который определен в разделе таблицы стилей.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Настройка макета с помощью функции Фикссизе

Функция [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) используется для указания нескольких аспектов макета, которые не могут быть обработаны таблицей стилей.

Существует два возможных баннера, которые можно использовать в зависимости от высоты веб-представления.


```
if (200 > document.body.clientHeight) {
    //A short window. Use the minibanner.
    document.all.Banner.style.visibility = "hidden";
    document.all.MiniBanner.style.visibility = "visible";
    document.all.FileList.style.top = 32;
    document.all.Info.style.top = 32;
}
else {
    //A normal window. Use the normal banner.
    document.all.Banner.style.visibility = "visible";
    document.all.MiniBanner.style.visibility = "hidden";
    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
    document.all.Rule.style.width = (document.body.clientWidth > 84 ?                                    document.body.clientWidth - 84 : 0) + "px";      
}
                    
```



Generic. htt использует высоту 200 пикселей в качестве разделительной линии между обычным и минибаннерс. Он устанавливает видимость стиля для выбранного баннера, а другой — для скрытого. Он также задает несколько свойств макета для регионов info и FileList, чтобы они правильно соответствовали выбранному баннеру.

Если веб-представление оказывается слишком узким, [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) использует полную ширину области отображения для отображения filelist.


```
if (400 > document.body.clientWidth) {
    //A narrow window. Hide the Info region, and expand the file list region.
    document.all.Info.style.visibility = "hidden";
    document.all.FileList.style.pixelLeft = 0;
    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
}

else {
    //Normal width.
    document.all.Info.style.visibility = "visible";
    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
}
                    
```



Generic. htt использует 400 пикселей в качестве разделительной линии между узким и широким экранами. Если веб-представление слишком узкие, [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) скрывает область сведений и изменяет свойство FileList [пикселлефт](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) , чтобы оно заполнило весь регион под баннером.

Последние несколько строк [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) настраивают несколько свойств макета на основе результатов предыдущего кода. Ширина области FileList корректируется таким образом, чтобы она полностью заполнила часть веб-представления, не занятую областью сведений. Высота области сведений изменяется в соответствии с заголовком и нижней частью веб-представления.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Извлечение и отображение сведений о папке

Когда пользователь выбирает элемент, объект FileList запускает событие [SelectionChanged](#retrieving-and-displaying-folder-information) . Это событие обрабатывается сценарием JScript. Для простоты сценарий, обнаруженный в Generic. htt, предполагает, что одновременно может быть выбран только один элемент.


```
<script language="JavaScript" for="FileList" event="SelectionChanged">
    // Updates the TextBlock region when an item is selected.
    var data;
    var text;

    // Name
    text = "<b>" + FileList.FocusedItem.Name + "</b>";

    // Comment
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
    if (data)
        text += "<br>" + data;

    // Documents
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
    if (data)
        text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

    // Status
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
    if (data)
        text += "<br><br><b><font color=red>" + data + "</font></b>";

    // Tip 
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
    if (data != "" && data != FileList.FocusedItem.Name)
        text += "<br><br>" + data;

    TextBlock.innerHTML = text;
</script>
                    
```



Для получения сведений об элементе скрипт использует два свойства FileList: [**FileList. фокуседитем**](/windows/desktop/shell/shellfolderview-focuseditem)и [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) . **FileList. фокуседитем** определяет выбранный элемент с именем элемента, заданным параметром **FileList.FocusedItem.Name**. **FileList. Folder** фактически является указателем на объект [**Folder**](../shell/folder.md) . Метод [**жетдетаилсоф**](/windows/desktop/shell/folder-getdetailsof) объекта Folder используется для получения оставшихся сведений об элементе.

Вся информация объединяется в одну текстовую строку, разделенную <BR> Теги для удобочитаемости. Затем текст отображается путем присвоения его элементу [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

## <a name="summary"></a>Сводка

в этой главе описываются некоторые методы, которые можно использовать для настройки способа отображения обозревателем Windows сведений о папках оболочки. Создание файла Desktop.ini позволяет выполнить некоторую простую настройку, например отображение пользовательского значка вместо стандартного значка папки. Если папка отображается в веб-представлении, ее макет и отображение управляются с помощью HTML-шаблона, который определяет, какие сведения отображаются и как. Вы можете обеспечить высокий уровень контроля над веб-представлением папки с помощью стандартных методов HTML, DHTML и сценариев для создания пользовательского шаблона.

 

 