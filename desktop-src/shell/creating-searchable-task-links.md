---
description: Начиная с Windows Vista, представление категории панели управления содержит ссылки на задачи под каждым значком элемента панели управления, как показано ниже.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Создание ссылок на задачи с возможностью поиска для элемента панели управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896894"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a><span data-ttu-id="36bd4-103">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="36bd4-103">Creating Searchable Task Links for a Control Panel Item</span></span>

<span data-ttu-id="36bd4-104">Начиная с Windows Vista, представление категории панели управления содержит ссылки на задачи под каждым значком элемента панели управления, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="36bd4-104">As of Windows Vista, the Control Panel category view provides task links beneath each Control Panel item's icon as shown here.</span></span>

![ссылки на задачи на странице категории "система и обслуживание"](images/controlpaneltasklinks.png)

<span data-ttu-id="36bd4-106">Когда пользователь вводит текст в поле **поиска** в правом верхнем углу окна, в результаты поиска включаются следующие ссылки на задачи, как показано здесь для поиска по слову "дисплей".</span><span class="sxs-lookup"><span data-stu-id="36bd4-106">When a user enters text in the **Search** box in the upper right of the window, the search results include these task links as shown here for a search on the word "display".</span></span>

![ссылки на задачи в результатах поиска панели управления](images/controlpanelsearchresults.png)

<span data-ttu-id="36bd4-108">В этом разделе обсуждается следующее.</span><span class="sxs-lookup"><span data-stu-id="36bd4-108">This topic discusses the following:</span></span>

-   [<span data-ttu-id="36bd4-109">Рекомендации по использованию ссылок на задачи</span><span class="sxs-lookup"><span data-stu-id="36bd4-109">Task Link Best Practices</span></span>](#task-link-best-practices)
-   [<span data-ttu-id="36bd4-110">Создание XML-файла задачи</span><span class="sxs-lookup"><span data-stu-id="36bd4-110">Creating a Task XML File</span></span>](#creating-a-task-xml-file)
-   [<span data-ttu-id="36bd4-111">Локализация ссылок задач</span><span class="sxs-lookup"><span data-stu-id="36bd4-111">Localizing Task Links</span></span>](#localizing-task-links)
-   [<span data-ttu-id="36bd4-112">Ключевые слова и поиск</span><span class="sxs-lookup"><span data-stu-id="36bd4-112">Keywords and Searching</span></span>](#keywords-and-searching)
-   [<span data-ttu-id="36bd4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="36bd4-113">Related topics</span></span>](#related-topics)

## <a name="task-link-best-practices"></a><span data-ttu-id="36bd4-114">Рекомендации по использованию ссылок на задачи</span><span class="sxs-lookup"><span data-stu-id="36bd4-114">Task Link Best Practices</span></span>

<span data-ttu-id="36bd4-115">Рекомендуется предоставлять ссылки на задачи для элементов панели управления в качестве вспомогательных пользователей для поиска функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="36bd4-115">It is recommended that you provide task links for your Control Panel items as an aid to users searching for functionality.</span></span> <span data-ttu-id="36bd4-116">Также можно добавить ключевые слова в ссылки задач, чтобы пользователь мог найти их даже без знания названия или терминологии задачи.</span><span class="sxs-lookup"><span data-stu-id="36bd4-116">It is also possible to add keywords to the task links so that a user can find them even without knowing a task's title or terminology.</span></span>

<span data-ttu-id="36bd4-117">Ссылки на наиболее подходящие задачи служат трем целям:</span><span class="sxs-lookup"><span data-stu-id="36bd4-117">The best task links serve three purposes:</span></span>

1.  <span data-ttu-id="36bd4-118">Предоставьте ярлык функциональности элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="36bd4-118">Provide a shortcut to the functionality of the Control Panel item.</span></span>
2.  <span data-ttu-id="36bd4-119">Укажите ключевые слова, чтобы пользователи могли выполнять поиск с помощью собственного языка.</span><span class="sxs-lookup"><span data-stu-id="36bd4-119">Provide keywords so that users can search using their own language.</span></span> <span data-ttu-id="36bd4-120">Пользователю может потребоваться ввести "сжатие", так как он знает технический термин.</span><span class="sxs-lookup"><span data-stu-id="36bd4-120">A user may want to type "compaction" because he or she knows the technical term.</span></span> <span data-ttu-id="36bd4-121">Пользователь может ввести "база данных слишком велика" или "Database размер файла".</span><span class="sxs-lookup"><span data-stu-id="36bd4-121">A user may type "DB too big", or "database filesize".</span></span> <span data-ttu-id="36bd4-122">Добавление подходящих ключевых слов для задачи означает, что пользователи могут найти свой элемент панели управления.</span><span class="sxs-lookup"><span data-stu-id="36bd4-122">Adding suitable keywords to the task means that users can find your Control Panel item.</span></span>
3.  <span data-ttu-id="36bd4-123">Укажите подсказки о том, что делает элемент панели управления.</span><span class="sxs-lookup"><span data-stu-id="36bd4-123">Provide hints about what the Control Panel item does.</span></span> <span data-ttu-id="36bd4-124">Когда пользователь видит ссылки под значком элемента панели управления, он может получить дополнительные сведения об использовании элемента панели управления, а не только имя и значок, которые могут быть предоставлены.</span><span class="sxs-lookup"><span data-stu-id="36bd4-124">When a user sees the links beneath a Control Panel item's icon, they can get more information about what the Control Panel item is used for than the name and icon alone can provide.</span></span>

<span data-ttu-id="36bd4-125">Ссылки на задачи должны быть ориентированы на конечные пользователи, не ориентированные на технологии или функции.</span><span class="sxs-lookup"><span data-stu-id="36bd4-125">Task links should be end-user focused, not technology- or feature-focused.</span></span> <span data-ttu-id="36bd4-126">Например, «включение сжатия базы данных» будет неправильным, так как это технический жаргоне, не знакомый большинству пользователей.</span><span class="sxs-lookup"><span data-stu-id="36bd4-126">For example, "Enable database compaction" would be bad wording because it is technical jargon unfamiliar to the majority of users.</span></span> <span data-ttu-id="36bd4-127">"Сделать файл базы данных меньше" лучше, так как он упоминает фактическую конечную цель пользователя, а не механизм его получения.</span><span class="sxs-lookup"><span data-stu-id="36bd4-127">"Make my database file smaller" is better because it mentions the user's actual end goal rather than the mechanism to get there.</span></span> <span data-ttu-id="36bd4-128">Цель заключается не в упрощении, а в том, чтобы заменять задачу с точки зрения пользователя.</span><span class="sxs-lookup"><span data-stu-id="36bd4-128">The goal is not to oversimplify, but rather to phrase the task in terms of what the user wants to accomplish.</span></span>

## <a name="creating-a-task-xml-file"></a><span data-ttu-id="36bd4-129">Создание XML-файла задачи</span><span class="sxs-lookup"><span data-stu-id="36bd4-129">Creating a Task XML File</span></span>

<span data-ttu-id="36bd4-130">Ссылки на задачи определяются в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="36bd4-130">Task links are defined in an XML file.</span></span> <span data-ttu-id="36bd4-131">В этом разделе содержатся сведения о файле example. XML, который определяет три ссылки на задачи для элемента панели управления « **Блокнот**».</span><span class="sxs-lookup"><span data-stu-id="36bd4-131">This section provides the details of an example .xml file that defines three task links for a Control Panel item called **Notepad**.</span></span> <span data-ttu-id="36bd4-132">Он определяет заголовки, ключевые слова и командные строки для ссылок на задачи.</span><span class="sxs-lookup"><span data-stu-id="36bd4-132">It defines titles, keywords, and the command lines for the task links.</span></span> <span data-ttu-id="36bd4-133">Здесь также показано, как указать ссылки на задачи, которые отображаются в категории.</span><span class="sxs-lookup"><span data-stu-id="36bd4-133">It also illustrates how to specify which task links appear under which category.</span></span> <span data-ttu-id="36bd4-134">Элемент панели управления, зарегистрированный для отображения в нескольких категориях, имеет возможность отображения различных ссылок в зависимости от категории.</span><span class="sxs-lookup"><span data-stu-id="36bd4-134">A Control Panel item that is registered to appear in more than one category has the option of showing different links depending on the category.</span></span> <span data-ttu-id="36bd4-135">Описания различных элементов и предоставленных сведений задаются в виде комментариев в самом XML.</span><span class="sxs-lookup"><span data-stu-id="36bd4-135">Explanations of the various elements and information provided are given as comments in the XML itself.</span></span>


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> <span data-ttu-id="36bd4-136">Начиная с Windows 7, элемент панели управления может идентифицироваться по каноническому имени, а не к имени исполняемого файла: **<SH: контролпанел>** можно использовать вместо **<sh: Command>**.</span><span class="sxs-lookup"><span data-stu-id="36bd4-136">As of Windows 7, a Control Panel item can be identified by its canonical name rather than its executable name: the **<sh:controlpanel>** element can be used in place of **<sh:command>**.</span></span> <span data-ttu-id="36bd4-137">Элемент **<SH: контролпанел>** также предоставляет атрибут для указания страницы элемента, к которому он должен быть открыт.</span><span class="sxs-lookup"><span data-stu-id="36bd4-137">The **<sh:controlpanel>** element also provides an attribute to specify the page of the item to which it should open.</span></span> <span data-ttu-id="36bd4-138">Ниже приведен пример элемента **<SH: контролпанел>** .</span><span class="sxs-lookup"><span data-stu-id="36bd4-138">The following shows an example of the **<sh:controlpanel>** element:</span></span>

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a><span data-ttu-id="36bd4-139">Локализация ссылок задач</span><span class="sxs-lookup"><span data-stu-id="36bd4-139">Localizing Task Links</span></span>

<span data-ttu-id="36bd4-140">Текст для названий и ключевых слов ссылок задач может храниться в таблице строк в модуле элемента панели управления.</span><span class="sxs-lookup"><span data-stu-id="36bd4-140">The text for the task links' titles and keywords can be stored in a string table in the Control Panel item's module.</span></span> <span data-ttu-id="36bd4-141">В этом случае формат, используемый в XML-файле, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="36bd4-141">In that case, the format used in the XML file becomes:</span></span>


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



<span data-ttu-id="36bd4-142">В этом примере текст для имени задачи отображается в строковом ресурсе с ИДЕНТИФИКАТОРом 100 в myTextResources.dll, а текст ключевых слов отображается в строковом ресурсе с ИДЕНТИФИКАТОРом 101.</span><span class="sxs-lookup"><span data-stu-id="36bd4-142">In this example, the text for the task's name appears in string resource ID 100 in myTextResources.dll, and the text for the keywords appears in string resource ID 101.</span></span>

## <a name="keywords-and-searching"></a><span data-ttu-id="36bd4-143">Ключевые слова и поиск</span><span class="sxs-lookup"><span data-stu-id="36bd4-143">Keywords and Searching</span></span>

<span data-ttu-id="36bd4-144">Поиск на панели управления находит ссылки задач на основе их имени, а также их ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="36bd4-144">The Control Panel search finds task links based on their name and also on their keywords.</span></span> <span data-ttu-id="36bd4-145">Он сопоставляет каждое слово в поиске с префиксом слов в имени и ключевых словах.</span><span class="sxs-lookup"><span data-stu-id="36bd4-145">It matches each word in the search with the prefix of words in the name and keywords.</span></span> <span data-ttu-id="36bd4-146">Например, строка запроса "CPU" будет соответствовать задаче "ознакомьтесь с запущенными процессами" в предыдущем примере, так как "ЦП" содержится в списке ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="36bd4-146">For example, the query string "cpu" would match the task "See running processes" in the earlier example because "cpu" is in the keyword list.</span></span> <span data-ttu-id="36bd4-147">Строка запроса "Pro" также обнаружит этот результат, так как название "процессы" начинается с этой строки.</span><span class="sxs-lookup"><span data-stu-id="36bd4-147">The query string "pro" would also find that result because the title word "processes" begins with that string.</span></span> <span data-ttu-id="36bd4-148">Обратите внимание, что запрос соответствует только префиксам.</span><span class="sxs-lookup"><span data-stu-id="36bd4-148">Note that the query only matches prefixes.</span></span> <span data-ttu-id="36bd4-149">Строка запроса "Шаблоны" не будет соответствовать результату, поскольку эта строка, в то время как часть слова "процесс", не начинается с этого слова.</span><span class="sxs-lookup"><span data-stu-id="36bd4-149">The query string "rocess" would not match a result because that string, while part of the title word "process", does not begin that word.</span></span>

<span data-ttu-id="36bd4-150">Если поисковый запрос содержит несколько токенов, все маркеры должны соответствовать префиксу некоторого ключевого слова или части названия задачи для результата.</span><span class="sxs-lookup"><span data-stu-id="36bd4-150">When a search query contains multiple tokens, all the tokens must match the prefix of some keyword or part of the task title for a result.</span></span> <span data-ttu-id="36bd4-151">Запрос "уровень ЦП" не соответствует, так как "Level" не задано в ключевом слове.</span><span class="sxs-lookup"><span data-stu-id="36bd4-151">The query "cpu level" would not match, because "level" is not in the keyword set.</span></span> <span data-ttu-id="36bd4-152">Запрос "Загрузка ЦП" приведет к результату, так как "ЦП" соответствует ключевому слову, а "Run" — префикс слова "выполняется" в заголовке задачи.</span><span class="sxs-lookup"><span data-stu-id="36bd4-152">The query "cpu run" would give a result, because "cpu" matches a keyword, and "run" is the prefix of the word "running" in the task's title.</span></span>

<span data-ttu-id="36bd4-153">На панели управления не предусмотрена автоматическая проверка орфографии или варианты, такие как множественные или переносы.</span><span class="sxs-lookup"><span data-stu-id="36bd4-153">Control Panel does not automatically provide spelling correction or variations such as plurals or hyphenation.</span></span> <span data-ttu-id="36bd4-154">В совпадениях также учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="36bd4-154">Matches are also case-insensitive.</span></span> <span data-ttu-id="36bd4-155">Чтобы обеспечить успешный список ключевых слов, рекомендуется предоставить собственные варианты, например для этой ссылки, которая включает экранные заставки: "заставки; экраны-заставки; экранные заставки".</span><span class="sxs-lookup"><span data-stu-id="36bd4-155">To ensure a successful keyword list, it is recommended to provide variations yourself, such as for this task link that involves screen savers: "screensavers;screen-savers;screen savers;"</span></span>

<span data-ttu-id="36bd4-156">Нет необходимости добавлять «экранную заставку», так как запрос, который находит «экранные заставки», также найдет «заставка» из-за совпадения префикса.</span><span class="sxs-lookup"><span data-stu-id="36bd4-156">There is no need to add the singular "screensaver", because a query that finds "screensavers" will also find "screensaver" due to the prefix match.</span></span> <span data-ttu-id="36bd4-157">При вводе пользователем даже части слова, например "экраны", по-прежнему будет отображаться совпадение со ссылкой на задачу, которая содержит ключевое слово "заставки".</span><span class="sxs-lookup"><span data-stu-id="36bd4-157">A user typing even part of the word, like "screensa" will still see a match on a task link that has "screensavers" as a keyword.</span></span> <span data-ttu-id="36bd4-158">Для языков, в которых формы во множественном числе изменяют слово, необходимо разместить все формы, которые пользователь может ожидать ввести в ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="36bd4-158">For languages where plural forms change the word, it is necessary to put all the forms a user could reasonably be expected to type into the keywords.</span></span>

<span data-ttu-id="36bd4-159">В качестве соглашения Корпорация Майкрософт пропустила небольшие слова, например "практические руководства" или "я хочу" из набора ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="36bd4-159">As a convention, Microsoft has omitted small words like "how do I" or "I want to" from the set of keywords.</span></span> <span data-ttu-id="36bd4-160">Ожидание заключается в том, что большинство пользователей просто вводят наиболее важные слова, такие как «мышь», «высокая контрастность» или «видеодрайвер», чтобы получить результаты.</span><span class="sxs-lookup"><span data-stu-id="36bd4-160">The expectation is that most users will simply type the most important words such as "mouse", "high contrast", or "video driver" to get results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36bd4-161">См. также</span><span class="sxs-lookup"><span data-stu-id="36bd4-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bd4-162">Элементы панели управления</span><span class="sxs-lookup"><span data-stu-id="36bd4-162">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="36bd4-163">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="36bd4-163">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="36bd4-164">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="36bd4-164">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="36bd4-165">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="36bd4-165">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="36bd4-166">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="36bd4-166">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="36bd4-167">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="36bd4-167">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="36bd4-168">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="36bd4-168">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="36bd4-169">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="36bd4-169">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="36bd4-170">Доступ к панели управления в защищенном режиме в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36bd4-170">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



