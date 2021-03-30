---
title: Настройка веб-представления папки
description: Веб-представление — это мощный и гибкий способ использования проводника Windows для отображения сведений о содержимом папки оболочки.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Веб-представления
- Классический стиль
- Стиль веб-сайта
- баннеры
- Регион FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e364551d461eff6ae17a780bafc0b69182a1f16f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789672"
---
# <a name="customizing-a-folders-web-view"></a><span data-ttu-id="25961-108">Настройка веб-представления папки</span><span class="sxs-lookup"><span data-stu-id="25961-108">Customizing a Folder's Web View</span></span>

<span data-ttu-id="25961-109">\[Эта функция поддерживается только в Windows XP и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="25961-109">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="25961-110">\]</span><span class="sxs-lookup"><span data-stu-id="25961-110">\]</span></span>

<span data-ttu-id="25961-111">Веб-представление — это мощный и гибкий способ использования проводника Windows для отображения сведений о содержимом папки оболочки.</span><span class="sxs-lookup"><span data-stu-id="25961-111">A Web view is a powerful and flexible way to use the Windows Explorer to display information about the contents of a Shell folder.</span></span>

-   [<span data-ttu-id="25961-112">Введение</span><span class="sxs-lookup"><span data-stu-id="25961-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="25961-113">Использование шаблона веб-представления</span><span class="sxs-lookup"><span data-stu-id="25961-113">Using the Web View Template</span></span>](#using-the-web-view-template)
    -   [<span data-ttu-id="25961-114">Тело шаблона</span><span class="sxs-lookup"><span data-stu-id="25961-114">The Template Body</span></span>](#the-template-body)
    -   [<span data-ttu-id="25961-115">Заголовок шаблона</span><span class="sxs-lookup"><span data-stu-id="25961-115">The Template Head</span></span>](#the-template-head)
-   [<span data-ttu-id="25961-116">Сводка</span><span class="sxs-lookup"><span data-stu-id="25961-116">Summary</span></span>](#summary)

## <a name="introduction"></a><span data-ttu-id="25961-117">Введение</span><span class="sxs-lookup"><span data-stu-id="25961-117">Introduction</span></span>

<span data-ttu-id="25961-118">Windows предлагает пользователям два основных способа просмотра и навигации по пространству имен оболочки.</span><span class="sxs-lookup"><span data-stu-id="25961-118">Windows offers users two primary ways to view and navigate the Shell namespace.</span></span> <span data-ttu-id="25961-119">Наиболее привычные из них, классический стиль, похожи на знакомый Диспетчер файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="25961-119">The most familiar of these, the Classic style, is similar to the familiar Windows File Manager.</span></span> <span data-ttu-id="25961-120">В области справа отображается содержимое выбранной папки в одном из пяти форматов: крупный значок, маленький значок, список, подробности и эскиз.</span><span class="sxs-lookup"><span data-stu-id="25961-120">The right pane lists the contents of the currently selected folder in one of five formats: Large Icon, Small Icon, List, Details, and Thumbnail.</span></span> <span data-ttu-id="25961-121">Основное отличие от диспетчера файлов Windows — это левая панель, которая очень похожа на панель обозревателя Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="25961-121">The major difference from Windows File Manager is the left pane, which looks very similar to the Explorer bar of Windows Internet Explorer.</span></span> <span data-ttu-id="25961-122">Его можно изменить или удалить, а также отобразить несколько панелей в дополнение к знакомому дереву файловой системы, например панели поиска.</span><span class="sxs-lookup"><span data-stu-id="25961-122">It can be resized or removed, and it can display several panes in addition to the familiar file system tree, such as a search pane.</span></span>

> [!Note]  
> <span data-ttu-id="25961-123">Сведения в этом документе не относятся к Windows XP, описанные методики относятся только к предыдущим версиям Windows.</span><span class="sxs-lookup"><span data-stu-id="25961-123">The information in this document does not apply to Windows XP, the techniques discussed apply only to earlier versions of Windows.</span></span>

 

<span data-ttu-id="25961-124">На следующем рисунке показана папка "принтеры" в классическом стиле.</span><span class="sxs-lookup"><span data-stu-id="25961-124">The following illustration shows the Printers folder in Classic style.</span></span>

![Классический стиль папки "принтеры".](images/webview1.png)

<span data-ttu-id="25961-126">Классический стиль хорошо подходит для обычных папок и файлов файловой системы.</span><span class="sxs-lookup"><span data-stu-id="25961-126">The Classic style works reasonably well for normal file system folders and files.</span></span> <span data-ttu-id="25961-127">Однако с появлением Windows 95 файловая система превратилась в пространство имен.</span><span class="sxs-lookup"><span data-stu-id="25961-127">However, with the introduction of Windows 95, the file system has evolved into the namespace.</span></span> <span data-ttu-id="25961-128">Пространство имен позволяет создавать *Виртуальные папки*, такие как принтеры или сетевые окружения, которые могут представлять весьма разные типы информации, чем обычная папка файловой системы.</span><span class="sxs-lookup"><span data-stu-id="25961-128">The namespace allows the creation of *virtual folders*, such as Printers or Network Neighborhood, that can represent very different types of information than a normal file system folder.</span></span>

<span data-ttu-id="25961-129">Веб-стиль, также известный как веб-представление, предлагает более гибкий и эффективный способ представления информации, чем классический стиль.</span><span class="sxs-lookup"><span data-stu-id="25961-129">The Web style, also known as a Web view, offers a more flexible and powerful way of presenting information than Classic style.</span></span> <span data-ttu-id="25961-130">В веб-представлении пользователь по сути просматривает пространство имен и переходит по нему с помощью Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="25961-130">In a Web view, the user basically views and navigates the namespace using Internet Explorer.</span></span> <span data-ttu-id="25961-131">Базовый макет веб-представления аналогичен классическому стилю.</span><span class="sxs-lookup"><span data-stu-id="25961-131">The basic layout of a Web view is similar to Classic style.</span></span> <span data-ttu-id="25961-132">Панель обозревателя не изменилась.</span><span class="sxs-lookup"><span data-stu-id="25961-132">The Explorer bar is unchanged.</span></span> <span data-ttu-id="25961-133">Тем не менее регион, занятый списком файлов, становится областью для вывода общего назначения, которая фактически является веб-страницей.</span><span class="sxs-lookup"><span data-stu-id="25961-133">However, the region that was occupied by the file list becomes a general-purpose display area that is effectively a webpage.</span></span> <span data-ttu-id="25961-134">Веб-представление по-прежнему используется для отображения сведений о содержимом папки, но существует несколько ограничений на отображаемую информацию или как.</span><span class="sxs-lookup"><span data-stu-id="25961-134">A Web view is still used to display information about the contents of a folder, but there are few constraints on what information is displayed, or how.</span></span> <span data-ttu-id="25961-135">Каждая папка может иметь собственное веб-представление, настроенное в соответствии с определенными функциями.</span><span class="sxs-lookup"><span data-stu-id="25961-135">Each folder can have its own Web view, customized to suit its particular features.</span></span>

<span data-ttu-id="25961-136">На следующем рисунке показано веб-представление папки "принтеры" (показано ранее в классическом стиле).</span><span class="sxs-lookup"><span data-stu-id="25961-136">The following illustration shows a Web view of the Printers folder (shown previously in Classic style).</span></span>

![веб-представление папки "принтеры" по умолчанию.](images/webview2.png)

<span data-ttu-id="25961-138">Так же, как и обычные веб-страницы, управление ими осуществляется с помощью шаблона на основе HTML.</span><span class="sxs-lookup"><span data-stu-id="25961-138">Much like conventional webpages, Web views are controlled by an HTML-based template.</span></span> <span data-ttu-id="25961-139">Разработка шаблона веб-представления практически идентична созданию страницы и обеспечивает такую же степень гибкости в содержимом и структуре информации.</span><span class="sxs-lookup"><span data-stu-id="25961-139">Authoring a Web view template is nearly identical to authoring a webpage and provides the same degree of flexibility in content and layout of information.</span></span> <span data-ttu-id="25961-140">Шаблоны веб-представлений могут использовать динамический HTML (DHTML) и скрипты для реагирования на события, например, при щелчке элемента пользователем.</span><span class="sxs-lookup"><span data-stu-id="25961-140">Web view templates can use Dynamic HTML (DHTML) and scripting to respond to events, such as a user clicking an item.</span></span> <span data-ttu-id="25961-141">Они также могут размещать объекты, позволяющие им получать и отображать информацию из папки или ее содержимого.</span><span class="sxs-lookup"><span data-stu-id="25961-141">They can also host objects that allow them to obtain and display information from the folder or its contents.</span></span>

<span data-ttu-id="25961-142">Пользователь может выбрать веб-представление, запустив проводник Windows, выбрав пункт **Свойства папки** в меню **вид** и выбрав этот параметр: **включить веб-содержимое в папках**.</span><span class="sxs-lookup"><span data-stu-id="25961-142">The user can choose a Web view by starting Windows Explorer, clicking **Folder Options** on the **View** menu, and selecting this option: **Enable Web content in folders**.</span></span> <span data-ttu-id="25961-143">Тем не менее пользователь может также запустить Internet Explorer и указать браузер в файловой системе, щелкнув меню **вид** , выбрав пункт **панель обозревателя** и щелкнув **папки**.</span><span class="sxs-lookup"><span data-stu-id="25961-143">However, the user can also start Internet Explorer and point the browser at the file system by clicking the **View** menu, pointing to **Explorer Bar**, and clicking **Folders**.</span></span> <span data-ttu-id="25961-144">В веб-представлении не существует практически никаких различий между Internet Explorer и проводником Windows.</span><span class="sxs-lookup"><span data-stu-id="25961-144">In a Web view, there is virtually no difference between Internet Explorer and Windows Explorer.</span></span>

<span data-ttu-id="25961-145">В левой части области справа в веб-представлении принтеры отображается баннер с именем и значком папки, а затем — блок сведений о папке.</span><span class="sxs-lookup"><span data-stu-id="25961-145">On the left side of the right pane, the Printers Web view displays a banner with the folder's name and icon, followed by a block of information about the folder.</span></span> <span data-ttu-id="25961-146">Обычный список файлов занимает правой части страницы.</span><span class="sxs-lookup"><span data-stu-id="25961-146">The usual file list occupies the right side of the page.</span></span>

<span data-ttu-id="25961-147">Когда пользователь щелкает элемент, в информационном блоке отображаются подробные сведения об этом элементе.</span><span class="sxs-lookup"><span data-stu-id="25961-147">When a user clicks an item, detailed information about the item appears in the information block.</span></span> <span data-ttu-id="25961-148">В веб-представлении «принтеры» фактически отображаются те же сведения, что и в классическом стиле, но это делается в более удобном для использования формате.</span><span class="sxs-lookup"><span data-stu-id="25961-148">The Printers Web view actually displays much the same information that is available in Classic style, but it does so in a more usable format.</span></span> <span data-ttu-id="25961-149">Однако веб-представление — это не просто другой способ отображения классической информации о стиле.</span><span class="sxs-lookup"><span data-stu-id="25961-149">However, a Web view is not simply a different way to display Classic style information.</span></span> <span data-ttu-id="25961-150">Например, ссылка на полезный веб-сайт может отображаться под информационным блоком, компонентом, который недоступен в классическом стиле.</span><span class="sxs-lookup"><span data-stu-id="25961-150">For example, a link to a useful website can be displayed below the information block, a feature that is not available in Classic style.</span></span> <span data-ttu-id="25961-151">Если пользователь щелкнет ссылку, отобразится сайт.</span><span class="sxs-lookup"><span data-stu-id="25961-151">If the user clicks the link, the site will be displayed.</span></span>

<span data-ttu-id="25961-152">Веб-представление принтеров, показанное на предыдущем рисунке, похоже на классический стиль, поскольку базовый шаблон веб-представления (файл HTT) был написан таким образом.</span><span class="sxs-lookup"><span data-stu-id="25961-152">The Printers Web view shown in the preceding illustration is similar to the Classic style, because the underlying Web view template (an .htt file) was written that way.</span></span> <span data-ttu-id="25961-153">Этот список файлов, например, не создается непосредственно шаблоном веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-153">The list of files, for instance, is not generated by the Web view template directly.</span></span> <span data-ttu-id="25961-154">Он создается и отображается объектом [**вебвиевфолдерконтентс**](webviewfoldercontents.md) , размещенным в шаблоне веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-154">It is created and displayed by a [**WebViewFolderContents**](webviewfoldercontents.md) object hosted by the Web view template.</span></span> <span data-ttu-id="25961-155">Методы и свойства объекта позволяют веб-представлению управлять макетом и получать сведения об определенных элементах.</span><span class="sxs-lookup"><span data-stu-id="25961-155">The object's methods and properties allow the Web view to control its layout and obtain information about particular items.</span></span> <span data-ttu-id="25961-156">Содержимое и компоновка баннера и информационного блока указываются в шаблоне веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-156">The content and layout of the banner and information block is specified in the Web view template.</span></span>

<span data-ttu-id="25961-157">Так как веб-представление поддерживает DHTML, этот шаблон можно также использовать для управления взаимодействием с пользователем.</span><span class="sxs-lookup"><span data-stu-id="25961-157">Because a Web view supports DHTML, the template can also be used to handle user interaction.</span></span> <span data-ttu-id="25961-158">Например, когда пользователь щелкает один из значков принтера, объект **вебвиевфолдерикон** запускает событие [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) .</span><span class="sxs-lookup"><span data-stu-id="25961-158">For instance, when a user clicks one of the printer icons, the **WebViewFolderIcon** object fires a [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) event.</span></span> <span data-ttu-id="25961-159">Шаблон использует обработчик событий DHTML, написанный в скрипте, для получения запрошенной информации и их вывода в информационном блоке.</span><span class="sxs-lookup"><span data-stu-id="25961-159">The template uses a DHTML event handler written in script to retrieve the requested information and display it in the information block.</span></span>

<span data-ttu-id="25961-160">Этот простой пример для папки принтеров — это не единственный способ использовать веб-представление.</span><span class="sxs-lookup"><span data-stu-id="25961-160">This simple example for the Printers folder is by no means the only way to use a Web view.</span></span> <span data-ttu-id="25961-161">Создавая собственный шаблон и, при необходимости, объекты, вы можете использовать веб-представление для отображения информации и взаимодействия с пользователем любым способом, наиболее эффективным.</span><span class="sxs-lookup"><span data-stu-id="25961-161">By writing your own template and, if necessary, objects, you can use a Web view to display information and interact with the user in whatever way you find most effective.</span></span> <span data-ttu-id="25961-162">Обратите внимание, что в настоящее время в шаблонах веб-представлений отображаются только определенные системой виртуальные папки.</span><span class="sxs-lookup"><span data-stu-id="25961-162">Note that, at present, Web view templates only display system-defined virtual folders.</span></span> <span data-ttu-id="25961-163">Хотя разработчики могут создать виртуальную папку путем реализации расширения пространства имен, они должны использовать методы, описанные в разделе [расширения пространства имен](/windows/desktop/shell/nse-works) , чтобы отобразить их.</span><span class="sxs-lookup"><span data-stu-id="25961-163">Although developers can create a virtual folder by implementing a namespace extension, they must use the techniques described in [Namespace Extensions](/windows/desktop/shell/nse-works) to display it.</span></span>

## <a name="using-the-web-view-template"></a><span data-ttu-id="25961-164">Использование шаблона веб-представления</span><span class="sxs-lookup"><span data-stu-id="25961-164">Using the Web View Template</span></span>

<span data-ttu-id="25961-165">Способ отображения данных в веб-представлении можно изменить, изменив файл Desktop.ini папки.</span><span class="sxs-lookup"><span data-stu-id="25961-165">The way data is displayed in a Web view can be customized in a limited way by modifying a folder's Desktop.ini file.</span></span> <span data-ttu-id="25961-166">Дополнительные сведения см. [в разделе Настройка папок с помощью Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) .</span><span class="sxs-lookup"><span data-stu-id="25961-166">See [Customizing Folders with Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) for details.</span></span> <span data-ttu-id="25961-167">Гораздо более гибкий и эффективный способ настройки веб-представления — создание пользовательского шаблона веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-167">A much more flexible and powerful way to customize a Web view is to create a custom Web view template.</span></span>

<span data-ttu-id="25961-168">Шаблон веб-представления определяет, что отображается в веб-представлении и как.</span><span class="sxs-lookup"><span data-stu-id="25961-168">The Web view template controls what is displayed in a Web view and how.</span></span> <span data-ttu-id="25961-169">Он использует стандартные методы HTML, DHTML и создания сценариев для получения и просмотра информации и взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="25961-169">It uses standard HTML, DHTML, and scripting techniques to obtain and display information and interact with the user.</span></span> <span data-ttu-id="25961-170">В этом разделе описано, как создать веб-представление, изучив простой шаблон — Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="25961-170">This section discusses how to create a Web view by examining a simple template—Generic.htt.</span></span>


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



<span data-ttu-id="25961-171">Простой способ создать собственный шаблон веб-представления — использовать Generic. htt и изменить его.</span><span class="sxs-lookup"><span data-stu-id="25961-171">A simple way to create your own Web view template is to take Generic.htt and modify it.</span></span> <span data-ttu-id="25961-172">Так как он довольно ограничен, вы также можете ознакомиться с другими, более сложными примерами для получения дополнительных идей.</span><span class="sxs-lookup"><span data-stu-id="25961-172">Because it is rather limited, you should also look at other, more complex examples for additional ideas.</span></span> <span data-ttu-id="25961-173">Их можно найти, выполнив поиск расширения htt, используемого всеми шаблонами веб-представлений, в системе.</span><span class="sxs-lookup"><span data-stu-id="25961-173">You can find them by searching your system for the .htt extension used by all Web view templates.</span></span> <span data-ttu-id="25961-174">Если вы хотите создать пользовательский шаблон для папки, следует начать с шаблона Folder. htt по умолчанию, который обычно хранится в C: \\ WinNT \\ Web или c: \\ Windows \\ Web.</span><span class="sxs-lookup"><span data-stu-id="25961-174">If you want to create a custom template for a folder, you should start with the default Folder.htt template, which is usually stored in either C:\\Winnt\\Web or C:\\Windows\\Web.</span></span> <span data-ttu-id="25961-175">Обратите внимание, что эти файлы определены как скрытые, поэтому для их просмотра может потребоваться изменить параметры проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="25961-175">Note that these files are defined as hidden, so you may need to modify your Windows Explorer settings to view them.</span></span> <span data-ttu-id="25961-176">После создания HTT-файла он должен быть помечен как "только для чтения" и скрытым.</span><span class="sxs-lookup"><span data-stu-id="25961-176">Once an .htt file is created, it should be marked as read-only and hidden.</span></span>

<span data-ttu-id="25961-177">Шаблоны веб-представлений используют расширение htt, поскольку они немного отличаются от обычных документов. htm.</span><span class="sxs-lookup"><span data-stu-id="25961-177">Web view templates use the .htt extension because they differ slightly from conventional .htm documents.</span></span> <span data-ttu-id="25961-178">Основное отличие — несколько специальных переменных в HTT-файлах, которые система заменяет текущими значениями пространства имен.</span><span class="sxs-lookup"><span data-stu-id="25961-178">The main difference is several special variables in .htt files that the system replaces with the current namespace values.</span></span> <span data-ttu-id="25961-179">Переменные% СИСДИР% и% СИСДИРПАС% представляют имя и путь выбранной папки.</span><span class="sxs-lookup"><span data-stu-id="25961-179">The %THISDIR% and %THISDIRPATH% variables represent the name and path of the currently selected folder.</span></span> <span data-ttu-id="25961-180">Переменная% ТЕМПЛАТЕДИР% представляет папку, в которой хранятся таблицы стилей веб-представлений.</span><span class="sxs-lookup"><span data-stu-id="25961-180">The %TEMPLATEDIR% variable represents the folder where the Web view style sheets are stored.</span></span>

<span data-ttu-id="25961-181">Как и большинство шаблонов HTML, файлы. htt имеют две основные части: текст и головной элемент.</span><span class="sxs-lookup"><span data-stu-id="25961-181">Like most HTML templates, .htt files have two basic parts: a body and a head.</span></span> <span data-ttu-id="25961-182">Тело шаблона управляет базовым макетом веб-представления и загружает объекты, используемые для связи с пространством имен и отображаемые сведения.</span><span class="sxs-lookup"><span data-stu-id="25961-182">The template body controls the basic layout of the Web view and loads the objects used to communicate with the namespace and display information.</span></span> <span data-ttu-id="25961-183">Заголовок содержит сценарии и функции, которые выполняют такие задачи, как обработка изменения размера и получение сведений из папки.</span><span class="sxs-lookup"><span data-stu-id="25961-183">The head contains scripts and functions that do tasks such as handling resizing and obtaining information from the folder.</span></span> <span data-ttu-id="25961-184">Большинство шаблонов, включая Generic. htt, также включают таблицу стилей.</span><span class="sxs-lookup"><span data-stu-id="25961-184">Most templates, including Generic.htt, also include a style sheet.</span></span> <span data-ttu-id="25961-185">В общем случае лучше включить в шаблон сведения о таблице стилей.</span><span class="sxs-lookup"><span data-stu-id="25961-185">In general, it is better to include the style sheet information in your template.</span></span> <span data-ttu-id="25961-186">Отдельные таблицы стилей могут работать неправильно, если веб-представление используется с удаленными пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="25961-186">Separate style sheets may not work properly when a Web view is used with remote namespaces.</span></span>

### <a name="the-template-body"></a><span data-ttu-id="25961-187">Тело шаблона</span><span class="sxs-lookup"><span data-stu-id="25961-187">The Template Body</span></span>

<span data-ttu-id="25961-188">В тексте шаблона указывается, что будет представлено веб-представлением.</span><span class="sxs-lookup"><span data-stu-id="25961-188">The body of the template specifies what will be presented by a Web view.</span></span> <span data-ttu-id="25961-189">Здесь также загружаются объекты, используемые для вывода сведений и взаимодействия с папками пространства имен.</span><span class="sxs-lookup"><span data-stu-id="25961-189">It is also where the objects used to display information and communicate with namespace folders are loaded.</span></span> <span data-ttu-id="25961-190">Макет, определяемый Generic. htt, аналогичен показанному на рисунке в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="25961-190">The layout defined by Generic.htt is similar to that shown in the illustration in the previous section.</span></span> <span data-ttu-id="25961-191">Существует три области отображения: баннер и блок сведений в левой части представления, а также список файлов справа.</span><span class="sxs-lookup"><span data-stu-id="25961-191">There are three display regions: the banner and information block on the left side of the view, and the file list on the right.</span></span>

<span data-ttu-id="25961-192">Регионы — это все назначенные идентификаторы, используемые таблицами стилей и DHTML.</span><span class="sxs-lookup"><span data-stu-id="25961-192">The regions are all assigned identifiers to be used by the style sheet and DHTML.</span></span> <span data-ttu-id="25961-193">Как обсуждалось в следующем разделе, существует два возможных баннера с идентификаторами "Banner" и "Минибаннер".</span><span class="sxs-lookup"><span data-stu-id="25961-193">As discussed in the next section, there are two possible banners, with identifiers of "Banner" and "MiniBanner".</span></span> <span data-ttu-id="25961-194">Идентификатор региона информационного блока — "info".</span><span class="sxs-lookup"><span data-stu-id="25961-194">The identifier of the information block's region is "Info".</span></span> <span data-ttu-id="25961-195">Идентификатор объекта списка файлов — "FileList".</span><span class="sxs-lookup"><span data-stu-id="25961-195">The file list object's identifier is "FileList".</span></span> <span data-ttu-id="25961-196">Сведения о [макете](#controlling-the-web-view-layout) области обрабатываются таблицей стилей и функцией Microsoft JScript [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function), которая обсуждается далее в этой главе.</span><span class="sxs-lookup"><span data-stu-id="25961-196">The details of the region's [layout](#controlling-the-web-view-layout) are handled by the style sheet and a Microsoft JScript function, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), which is discussed later in the chapter.</span></span>

### <a name="the-banner-region"></a><span data-ttu-id="25961-197">Область заголовка</span><span class="sxs-lookup"><span data-stu-id="25961-197">The Banner Region</span></span>

<span data-ttu-id="25961-198">Баннер находится в верхней части экрана в левом верхнем углу веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-198">The banner is located at the top of the display, in the upper-left corner of the Web view.</span></span> <span data-ttu-id="25961-199">В стандартном баннере отображается имя и значок папки, содержимое которой отображается в списке файлов справа.</span><span class="sxs-lookup"><span data-stu-id="25961-199">The normal banner displays the name and icon of the folder whose contents are displayed in the file list on the right.</span></span> <span data-ttu-id="25961-200">Однако если окно оказывается слишком коротким, то под значком может отсутствовать место для вывода сведений.</span><span class="sxs-lookup"><span data-stu-id="25961-200">However, if the window becomes too short, there may be no room below the icon to display information.</span></span> <span data-ttu-id="25961-201">По этой причине Generic. htt также определяет минибаннер, который отображает только имя папки.</span><span class="sxs-lookup"><span data-stu-id="25961-201">For this reason, Generic.htt also defines a minibanner that only displays the folder name.</span></span> <span data-ttu-id="25961-202">Оба баннера изначально определены как скрытые.</span><span class="sxs-lookup"><span data-stu-id="25961-202">Both banners are initially defined as hidden.</span></span> <span data-ttu-id="25961-203">[Фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) выбирает, какой из них должен отображаться, и присваивает ему значение "Visible".</span><span class="sxs-lookup"><span data-stu-id="25961-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) chooses which one to display and sets it to "visible".</span></span>

<span data-ttu-id="25961-204">Обычный баннер для Generic. htt определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="25961-204">The normal banner for Generic.htt is defined by:</span></span>


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



<span data-ttu-id="25961-205">В первой части раздела баннера отображается заголовок с горизонтальным правилом под ним.</span><span class="sxs-lookup"><span data-stu-id="25961-205">The first part of the banner section displays the title with a horizontal rule underneath it.</span></span> <span data-ttu-id="25961-206">Теги таблицы используются для управления позицией.</span><span class="sxs-lookup"><span data-stu-id="25961-206">Table tags are used to control its position.</span></span> <span data-ttu-id="25961-207">Атрибут InAttribute устанавливается для</span><span class="sxs-lookup"><span data-stu-id="25961-207">The nowrap attribute is set for the</span></span> <TD> <span data-ttu-id="25961-208">, чтобы запретить перенос по словам.</span><span class="sxs-lookup"><span data-stu-id="25961-208">tag to prevent word wrapping.</span></span> <span data-ttu-id="25961-209">Система заменит% СИСДИРНАМЕ% именем текущей папки.</span><span class="sxs-lookup"><span data-stu-id="25961-209">The system will replace %THISDIRNAME% with the name of the current folder.</span></span> <span data-ttu-id="25961-210">Затем загружается объект **вебвиевфолдерикон** с идентификатором "Icon" для простоты и извлекается и отображается значок папки.</span><span class="sxs-lookup"><span data-stu-id="25961-210">A **WebViewFolderIcon** object, with an identifier of "Icon" for simplicity, is then loaded to extract and display the folder's icon.</span></span>

<span data-ttu-id="25961-211">Раздел минибаннер подобен стандартному баннеру.</span><span class="sxs-lookup"><span data-stu-id="25961-211">The minibanner section is similar to the normal banner.</span></span> <span data-ttu-id="25961-212">Формат заголовка размещается немного выше и не имеет правила.</span><span class="sxs-lookup"><span data-stu-id="25961-212">The format of the title is placed slightly higher and does not have a rule.</span></span> <span data-ttu-id="25961-213">Поскольку значок отсутствует, объект **вебвиевфолдерикон** не загружается.</span><span class="sxs-lookup"><span data-stu-id="25961-213">Because there is no icon, the **WebViewFolderIcon** object is not loaded.</span></span>


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a><span data-ttu-id="25961-214">Область сведений</span><span class="sxs-lookup"><span data-stu-id="25961-214">The Info Region</span></span>

<span data-ttu-id="25961-215">Часть веб-представления под баннером используется для отображения подробных сведений о выбранном элементе.</span><span class="sxs-lookup"><span data-stu-id="25961-215">The portion of the Web view below the banner is used to present detailed information about the selected item.</span></span> <span data-ttu-id="25961-216">Если элемент не выбран, отображается сообщение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25961-216">If no item is selected, a default message is shown.</span></span> <span data-ttu-id="25961-217">Поскольку Generic. htt отображает только один блок текста, этот раздел довольно прост.</span><span class="sxs-lookup"><span data-stu-id="25961-217">Because Generic.htt only displays a single block of text, this section is quite simple.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



<span data-ttu-id="25961-218">Большая часть работы по сбору информации обрабатывается [сценарием сведений о папке](#retrieving-and-displaying-folder-information) , который обсуждается далее в этой главе.</span><span class="sxs-lookup"><span data-stu-id="25961-218">Most of the work of collecting the information is handled by a [folder information script](#retrieving-and-displaying-folder-information) that is discussed later in the chapter.</span></span> <span data-ttu-id="25961-219">Она отображает информацию, присваивая текст [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="25961-219">It displays the information by assigning the text to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

<span data-ttu-id="25961-220">Вы можете легко настроить отображение информации, изменив эти элементы или добавив дополнительные.</span><span class="sxs-lookup"><span data-stu-id="25961-220">You can easily customize the information display by modifying these elements or including additional ones.</span></span> <span data-ttu-id="25961-221">Можно использовать все, что можно разместить на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="25961-221">Anything that you can put on a webpage can be used.</span></span> <span data-ttu-id="25961-222">Например, чтобы отобразить ссылку на веб-сайт, можно добавить элемент привязки после текстового блока в Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="25961-222">For example, to display a link to your website, you can add an anchor element after the text block in Generic.htt.</span></span>


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



### <a name="the-filelist-region"></a><span data-ttu-id="25961-223">Регион FileList</span><span class="sxs-lookup"><span data-stu-id="25961-223">The FileList Region</span></span>

<span data-ttu-id="25961-224">Наконец, Generic. htt загружает объект [**вебвиевфолдерконтентс**](webviewfoldercontents.md) для региона filelist.</span><span class="sxs-lookup"><span data-stu-id="25961-224">Finally, Generic.htt loads a [**WebViewFolderContents**](webviewfoldercontents.md) object for the FileList region.</span></span> <span data-ttu-id="25961-225">Так как для его идентификатора задано значение "FileList", он будет называться как объект FileList в данный момент.</span><span class="sxs-lookup"><span data-stu-id="25961-225">Because its identifier is set to "FileList", it will be referred to as the FileList object from now on.</span></span>


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



<span data-ttu-id="25961-226">Объект FileList находится в большинстве веб-представлений и служит для нескольких целей.</span><span class="sxs-lookup"><span data-stu-id="25961-226">The FileList object is found in most Web views and serves several purposes.</span></span> <span data-ttu-id="25961-227">FileList отображает список элементов, содержащихся в выбранной папке, с теми же параметрами и оформлением, что и список файлов в классическом стиле.</span><span class="sxs-lookup"><span data-stu-id="25961-227">FileList displays the list of items contained by the selected folder with the same options and appearance as the file list in Classic style.</span></span> <span data-ttu-id="25961-228">При выборе элемента FileList уведомляет веб-представление, выпуская событие [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="25961-228">When an item is selected, FileList notifies the Web view by firing a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="25961-229">FileList также предоставляет методы и свойства, которые можно использовать для получения сведений об отдельных элементах и управления положением и размером отображаемой области.</span><span class="sxs-lookup"><span data-stu-id="25961-229">FileList also exposes methods and properties that can be used to retrieve information about individual items and control the position and size of its display area.</span></span>

<span data-ttu-id="25961-230">Хотя объект FileList очень полезен, он возвращает только стандартные сведения о файловой системе, такие как размер файла или атрибуты.</span><span class="sxs-lookup"><span data-stu-id="25961-230">Although the FileList object is very useful, it only returns standard file system information, such as file size or attributes.</span></span> <span data-ttu-id="25961-231">Чтобы получить сведения о других видах из папки оболочки, необходимо загрузить и обработать дополнительные объекты.</span><span class="sxs-lookup"><span data-stu-id="25961-231">To retrieve other kinds of information from a Shell folder, you will have to load and handle additional objects.</span></span> <span data-ttu-id="25961-232">Любой объект, который может быть размещен на веб-странице, может использоваться с представлением в Интернете.</span><span class="sxs-lookup"><span data-stu-id="25961-232">Any object that can be hosted by a webpage can be used with a Web view.</span></span>

### <a name="the-template-head"></a><span data-ttu-id="25961-233">Заголовок шаблона</span><span class="sxs-lookup"><span data-stu-id="25961-233">The Template Head</span></span>

<span data-ttu-id="25961-234">Заголовок шаблона веб-представления содержит скрипты и функции, которые выполняют большую часть реальной работы.</span><span class="sxs-lookup"><span data-stu-id="25961-234">The head of the Web view template contains the scripts and functions that do most of the actual work.</span></span> <span data-ttu-id="25961-235">Существует две необходимые задачи, которые необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="25961-235">There are two essential tasks that need to be handled.</span></span> <span data-ttu-id="25961-236">Одна из них — макет отображения веб-представления, который необходимо настроить для размещения различных областей отображения.</span><span class="sxs-lookup"><span data-stu-id="25961-236">One is the layout of the Web view display, which needs to be adjusted to accommodate different display regions.</span></span> <span data-ttu-id="25961-237">Второй — получение и отображение информации из папки при выборе элемента.</span><span class="sxs-lookup"><span data-stu-id="25961-237">The other is retrieving and displaying information from the folder when an item is selected.</span></span> <span data-ttu-id="25961-238">Как и в случае с таблицами стилей, лучше включить в шаблон все скрипты и функции, а не ссылаться на них как на отдельные файлы.</span><span class="sxs-lookup"><span data-stu-id="25961-238">As with style sheets, it is better to include all scripts and functions in the template instead of referencing them as separate files.</span></span>

### <a name="controlling-the-web-view-layout"></a><span data-ttu-id="25961-239">Управление макетом веб-представления</span><span class="sxs-lookup"><span data-stu-id="25961-239">Controlling the Web View Layout</span></span>

<span data-ttu-id="25961-240">Область, доступная для веб-представления, зависит от размера окна веб-представления и объема, занимаемого панелью проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="25961-240">The area available for a Web view depends on the size of the Web view window and how much of it is taken up by the Windows Explorer bar.</span></span> <span data-ttu-id="25961-241">Эта область изменяется всякий раз, когда изменяется размер окна или панели проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="25961-241">This area will change anytime the window or Windows Explorer bar is resized.</span></span> <span data-ttu-id="25961-242">Поэтому макет должен быть сопоставлен с доступной областью, когда веб-представление загружается и соответствующим образом изменяется при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="25961-242">So the layout needs to be matched to the available area when a Web view is loaded and change appropriately when it is resized.</span></span> <span data-ttu-id="25961-243">Большая часть макета задается в таблице стилей.</span><span class="sxs-lookup"><span data-stu-id="25961-243">Much of the layout is specified in the style sheet.</span></span> <span data-ttu-id="25961-244">Область сведений, например, определяется таким образом, чтобы занимать самые левые 30% веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-244">The Info region, for example, is defined to occupy the leftmost 30 percent of the Web view.</span></span>


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



<span data-ttu-id="25961-245">При изменении размера веб-представления ширина области сведений изменится, чтобы поддерживать этот процент.</span><span class="sxs-lookup"><span data-stu-id="25961-245">As a Web view is resized, the width of the Info region will change to maintain that percentage.</span></span> <span data-ttu-id="25961-246">[Фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) управляет проблемами макета, которые не могут быть обработаны таблицей стилей.</span><span class="sxs-lookup"><span data-stu-id="25961-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) manages the layout issues that can't be handled by a style sheet.</span></span>

### <a name="loading-and-initializing-the-web-view"></a><span data-ttu-id="25961-247">Загрузка и инициализация веб-представления</span><span class="sxs-lookup"><span data-stu-id="25961-247">Loading and Initializing the Web View</span></span>

<span data-ttu-id="25961-248">При загрузке веб-представления макет необходимо настроить в соответствии с доступной областью отображения.</span><span class="sxs-lookup"><span data-stu-id="25961-248">When a Web view is loaded, the layout needs to be adjusted to fit the available display area.</span></span> <span data-ttu-id="25961-249">Поскольку элемент еще не выбран, веб-представления обычно отображают некоторые сведения по умолчанию, которые применяются ко всей папке.</span><span class="sxs-lookup"><span data-stu-id="25961-249">Because no item has been selected yet, Web views normally display some default information that applies to the whole folder.</span></span> <span data-ttu-id="25961-250">Для работы с инициализацией элемент управления</span><span class="sxs-lookup"><span data-stu-id="25961-250">To handle initialization, the</span></span> <BODY> <span data-ttu-id="25961-251">тег для Generic. htt определяет событие [OnLoad](/previous-versions//ms531409(v=vs.85)) и вызывает функцию **init** .</span><span class="sxs-lookup"><span data-stu-id="25961-251">tag for Generic.htt detects the [onload](/previous-versions//ms531409(v=vs.85)) event and calls the **Init** function.</span></span>


```
<body scroll=no onload="Init">
                    
```



<span data-ttu-id="25961-252">**Init** — это простая функция JScript.</span><span class="sxs-lookup"><span data-stu-id="25961-252">**Init** is a simple JScript function.</span></span>


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



<span data-ttu-id="25961-253">**Init** привязывает [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) к событию [Window. онресизе](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) , чтобы оно вызывалось при каждом изменении области отображения веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-253">**Init** binds [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) to the [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) event so that it will be called whenever the Web view display area changes.</span></span> <span data-ttu-id="25961-254">Затем он запускает Фикссизе для установки начального макета и назначает ввод текста в \_ \_ области сведений.</span><span class="sxs-lookup"><span data-stu-id="25961-254">It then runs FixSize to set the initial layout and assigns L\_Intro\_Text to the Info region.</span></span> <span data-ttu-id="25961-255">\_ \_ Вводный текст — это блок ввода текста, который определен в разделе таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="25961-255">L\_Intro\_Text is a block of introductory text that is defined in the style sheet section.</span></span>


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a><span data-ttu-id="25961-256">Настройка макета с помощью функции Фикссизе</span><span class="sxs-lookup"><span data-stu-id="25961-256">Adjusting the Layout by using the FixSize function</span></span>

<span data-ttu-id="25961-257">Функция [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) используется для указания нескольких аспектов макета, которые не могут быть обработаны таблицей стилей.</span><span class="sxs-lookup"><span data-stu-id="25961-257">The [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) function is used to specify several aspects of the layout that can't be handled by the style sheet.</span></span>

<span data-ttu-id="25961-258">Существует два возможных баннера, которые можно использовать в зависимости от высоты веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-258">There are two possible banners that can be used, depending on the height of the Web view.</span></span>


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



<span data-ttu-id="25961-259">Generic. htt использует высоту 200 пикселей в качестве разделительной линии между обычным и минибаннерс.</span><span class="sxs-lookup"><span data-stu-id="25961-259">Generic.htt uses a height of 200 pixels as the dividing line between normal and minibanners.</span></span> <span data-ttu-id="25961-260">Он устанавливает видимость стиля для выбранного баннера, а другой — для скрытого.</span><span class="sxs-lookup"><span data-stu-id="25961-260">It sets the style of the selected banner to visible and the other to hidden.</span></span> <span data-ttu-id="25961-261">Он также задает несколько свойств макета для регионов info и FileList, чтобы они правильно соответствовали выбранному баннеру.</span><span class="sxs-lookup"><span data-stu-id="25961-261">It also sets several layout properties for the Info and FileList regions so that they fit properly with the selected banner.</span></span>

<span data-ttu-id="25961-262">Если веб-представление оказывается слишком узким, [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) использует полную ширину области отображения для отображения filelist.</span><span class="sxs-lookup"><span data-stu-id="25961-262">If a Web view becomes too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) uses the full width of the display area for the FileList display.</span></span>


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



<span data-ttu-id="25961-263">Generic. htt использует 400 пикселей в качестве разделительной линии между узким и широким экранами.</span><span class="sxs-lookup"><span data-stu-id="25961-263">Generic.htt uses 400 pixels as the dividing line between narrow and wide displays.</span></span> <span data-ttu-id="25961-264">Если веб-представление слишком узкие, [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) скрывает область сведений и изменяет свойство FileList [пикселлефт](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) , чтобы оно заполнило весь регион под баннером.</span><span class="sxs-lookup"><span data-stu-id="25961-264">If the Web view is too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) hides the Info region and modifies the FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) property so that it fills the entire region below the banner.</span></span>

<span data-ttu-id="25961-265">Последние несколько строк [фикссизе](#adjusting-the-layout-by-using-the-fixsize-function) настраивают несколько свойств макета на основе результатов предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="25961-265">The final few lines of [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) adjust several layout properties based on the results of the preceding code.</span></span> <span data-ttu-id="25961-266">Ширина области FileList корректируется таким образом, чтобы она полностью заполнила часть веб-представления, не занятую областью сведений.</span><span class="sxs-lookup"><span data-stu-id="25961-266">The width of the FileList region is adjusted so that it exactly fills the portion of the Web view not occupied by the Info region.</span></span> <span data-ttu-id="25961-267">Высота области сведений изменяется в соответствии с заголовком и нижней частью веб-представления.</span><span class="sxs-lookup"><span data-stu-id="25961-267">The height of the Info region is sized to fit between the banner and the bottom of the Web view.</span></span>


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a><span data-ttu-id="25961-268">Извлечение и отображение сведений о папке</span><span class="sxs-lookup"><span data-stu-id="25961-268">Retrieving and Displaying Folder Information</span></span>

<span data-ttu-id="25961-269">Когда пользователь выбирает элемент, объект FileList запускает событие [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="25961-269">When a user selects an item, the FileList object fires a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="25961-270">Это событие обрабатывается сценарием JScript.</span><span class="sxs-lookup"><span data-stu-id="25961-270">This event is handled by a JScript script.</span></span> <span data-ttu-id="25961-271">Для простоты сценарий, обнаруженный в Generic. htt, предполагает, что одновременно может быть выбран только один элемент.</span><span class="sxs-lookup"><span data-stu-id="25961-271">For simplicity, the script found in Generic.htt assumes that only one item can be selected at a time.</span></span>


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



<span data-ttu-id="25961-272">Для получения сведений об элементе скрипт использует два свойства FileList: [**FileList. фокуседитем**](/windows/desktop/shell/shellfolderview-focuseditem)и [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) .</span><span class="sxs-lookup"><span data-stu-id="25961-272">The script uses two FileList properties, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)and [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) to obtain information about the item.</span></span> <span data-ttu-id="25961-273">**FileList. фокуседитем** определяет выбранный элемент с именем элемента, заданным параметром **FileList.FocusedItem.Name**.</span><span class="sxs-lookup"><span data-stu-id="25961-273">**FileList.FocusedItem** identifies the selected item, with the item's name given by **FileList.FocusedItem.Name**.</span></span> <span data-ttu-id="25961-274">**FileList. Folder** фактически является указателем на объект [**Folder**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="25961-274">**FileList.Folder** is actually a pointer to a [**Folder**](../shell/folder.md) object.</span></span> <span data-ttu-id="25961-275">Метод [**жетдетаилсоф**](/windows/desktop/shell/folder-getdetailsof) объекта Folder используется для получения оставшихся сведений об элементе.</span><span class="sxs-lookup"><span data-stu-id="25961-275">The Folder object's [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) method is used to retrieve the remaining information about the item.</span></span>

<span data-ttu-id="25961-276">Вся информация объединяется в одну текстовую строку, разделенную</span><span class="sxs-lookup"><span data-stu-id="25961-276">All the information is concatenated into a single text string, separated by</span></span> <BR> <span data-ttu-id="25961-277">Теги для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="25961-277">tags for readability.</span></span> <span data-ttu-id="25961-278">Затем текст отображается путем присвоения его элементу [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="25961-278">The text is then displayed by assigning it to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="25961-279">Сводка</span><span class="sxs-lookup"><span data-stu-id="25961-279">Summary</span></span>

<span data-ttu-id="25961-280">В этой главе описываются некоторые методы, которые можно использовать для настройки способа отображения в проводнике Windows сведений о папках оболочки.</span><span class="sxs-lookup"><span data-stu-id="25961-280">This chapter outlines some of the techniques you can use to customize the way the Windows Explorer displays information about Shell folders.</span></span> <span data-ttu-id="25961-281">Создание файла Desktop.ini позволяет выполнить некоторую простую настройку, например отображение пользовательского значка вместо стандартного значка папки.</span><span class="sxs-lookup"><span data-stu-id="25961-281">Creating a Desktop.ini file allows you to do some simple customization, such as displaying a custom icon in place of the standard folder icon.</span></span> <span data-ttu-id="25961-282">Если папка отображается в веб-представлении, ее макет и отображение управляются с помощью HTML-шаблона, который определяет, какие сведения отображаются и как.</span><span class="sxs-lookup"><span data-stu-id="25961-282">When a folder appears in a Web view, its layout and display are controlled by an HTML-based template that determines what information is displayed and how.</span></span> <span data-ttu-id="25961-283">Вы можете обеспечить высокий уровень контроля над веб-представлением папки с помощью стандартных методов HTML, DHTML и сценариев для создания пользовательского шаблона.</span><span class="sxs-lookup"><span data-stu-id="25961-283">You can exercise a high degree of control over a folder's Web view by using standard HTML, DHTML, and scripting techniques to create a custom template.</span></span>

 

 