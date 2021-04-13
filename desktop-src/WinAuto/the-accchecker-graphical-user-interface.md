---
title: Графический пользовательский интерфейс Аккчеккер
description: В этом разделе описаны элементы, составляющие графический интерфейс пользователя Аккчеккер.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "104568821"
---
# <a name="the-accchecker-graphical-user-interface"></a><span data-ttu-id="ebba5-103">Графический пользовательский интерфейс Аккчеккер</span><span class="sxs-lookup"><span data-stu-id="ebba5-103">The AccChecker Graphical User Interface</span></span>

<span data-ttu-id="ebba5-104">В этом разделе описаны элементы, составляющие графический интерфейс пользователя Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="ebba5-104">This topic describes the elements that make up the AccChecker GUI.</span></span>

-   [<span data-ttu-id="ebba5-105">Вкладка "проверки"</span><span class="sxs-lookup"><span data-stu-id="ebba5-105">Verifications Tab</span></span>](#verifications-tab)
-   [<span data-ttu-id="ebba5-106">Вкладка "результаты"</span><span class="sxs-lookup"><span data-stu-id="ebba5-106">Results Tab</span></span>](#results-tab)
-   [<span data-ttu-id="ebba5-107">Вкладки средства чтения с экрана MSAA и UIA</span><span class="sxs-lookup"><span data-stu-id="ebba5-107">MSAA and UIA Screen Reader Tabs</span></span>](#msaa-and-uia-screen-reader-tabs)
-   [<span data-ttu-id="ebba5-108">Вкладки дерева MSAA и UIA</span><span class="sxs-lookup"><span data-stu-id="ebba5-108">MSAA and UIA Tree Tabs</span></span>](#msaa-and-uia-tree-tabs)
-   [<span data-ttu-id="ebba5-109">Меню "файл"</span><span class="sxs-lookup"><span data-stu-id="ebba5-109">File Menu</span></span>](#file-menu)
-   [<span data-ttu-id="ebba5-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ebba5-110">Related topics</span></span>](#related-topics)

## <a name="verifications-tab"></a><span data-ttu-id="ebba5-111">Вкладка "проверки"</span><span class="sxs-lookup"><span data-stu-id="ebba5-111">Verifications Tab</span></span>

<span data-ttu-id="ebba5-112">Аккчеккер начинается с представления по умолчанию на вкладке **проверки** :</span><span class="sxs-lookup"><span data-stu-id="ebba5-112">AccChecker starts with the default view of the **Verifications** tab:</span></span>

![Снимок экрана, на котором показана вкладка "проверки" в средстве проверки читаемости U.](images/accchecker-verifications-tab.png)

<span data-ttu-id="ebba5-114">Вкладка **проверки** содержит следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="ebba5-114">The **Verifications** tab contains the following components.</span></span>

-   <span data-ttu-id="ebba5-115">**Селектор цели проверки** Предлагает следующие варианты выбора целевого приложения или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ebba5-115">**Verification target selector** Offers the following options for selecting a target application or control.</span></span>
    -   <span data-ttu-id="ebba5-116">Выберите целевой объект из предварительно заполненного раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="ebba5-116">Choose a target from the pre-populated drop-down list.</span></span> <span data-ttu-id="ebba5-117">Этот список содержит все HWND верхнего уровня, указанные при запуске.</span><span class="sxs-lookup"><span data-stu-id="ebba5-117">This list contains all top-level HWNDs identified at start-up.</span></span>
    -   <span data-ttu-id="ebba5-118">Выберите HWND на основе положения курсора мыши (выбираемые элементы управления выделяются красным прямоугольником).</span><span class="sxs-lookup"><span data-stu-id="ebba5-118">Choose an HWND based on the location of the mouse cursor (selectable controls are highlighted with a red rectangle).</span></span> <span data-ttu-id="ebba5-119">Этот параметр позволяет выбрать любой видимый объект, имеющий HWND.</span><span class="sxs-lookup"><span data-stu-id="ebba5-119">This option lets you select any visible object that has an HWND.</span></span>
    -   <span data-ttu-id="ebba5-120">Введите определенный HWND.</span><span class="sxs-lookup"><span data-stu-id="ebba5-120">Enter a particular HWND.</span></span>
-   <span data-ttu-id="ebba5-121">**Контрольный список подпрограмм проверки** Предоставляет возможность выбрать нужную подпрограммы проверки для приложения или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ebba5-121">**Verification routines checklist** Provides the ability to select the desired verification routine to be performed against an application or control.</span></span> <span data-ttu-id="ebba5-122">Дополнительные сведения см. в статье о процедуре проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-122">See Verification Routines for more information.</span></span>
-   <span data-ttu-id="ebba5-123">Средство **выбора файлов для подавления ошибок и предупреждений** Файлы подавления создаются на вкладке **результаты** проверки. Если щелкнуть правой кнопкой мыши сообщение об ошибке или предупреждение и выбрать в контекстном меню пункт **подавлять** , для этого сообщения устанавливается флаг.</span><span class="sxs-lookup"><span data-stu-id="ebba5-123">**Error and warning suppression file selector** Suppression files are generated from the verification **Results** tab. By right-clicking an error or warning message and selecting **Suppress** from the context menu, a flag is set for that message.</span></span> <span data-ttu-id="ebba5-124">Если флажок **подавить** установлен, в списке отображаются подавленные записи.</span><span class="sxs-lookup"><span data-stu-id="ebba5-124">If the **Suppressions** check box is checked, suppressed entries appear in the list.</span></span> <span data-ttu-id="ebba5-125">Подавленную запись можно не подавлять с помощью того же контекстного меню, которое использовалось для его подавления.</span><span class="sxs-lookup"><span data-stu-id="ebba5-125">A suppressed entry can be unsuppressed by using the same context menu used to suppress it.</span></span>

    <span data-ttu-id="ebba5-126">Файл подавления сохраняется в формате XML путем выбора команды **сохранить подавление** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="ebba5-126">A suppression file is saved in XML format by selecting **Save Suppression** from the **File** menu.</span></span> <span data-ttu-id="ebba5-127">Этот файл используется при последующих проверках, когда сообщения будут скрыты.</span><span class="sxs-lookup"><span data-stu-id="ebba5-127">This file is consumed on subsequent verification runs where the messages will be hidden.</span></span> <span data-ttu-id="ebba5-128">Чтобы удалить файл подавления, нажмите кнопку **очистить**.</span><span class="sxs-lookup"><span data-stu-id="ebba5-128">To remove the suppression file, click **Clear**.</span></span> <span data-ttu-id="ebba5-129">Сведения о конкретных сообщениях см. в разделе сообщения журнала проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-129">For information on specific messages, see Verification Log Messages.</span></span> <span data-ttu-id="ebba5-130">Используйте команду **сохранить журнал** из меню **файл** , чтобы сохранить весь список как файл журнала в формате XML или в виде форматированного текстового файла.</span><span class="sxs-lookup"><span data-stu-id="ebba5-130">Use **Save Log** from the **File** menu to save the entire list as a log file in XML or as a formatted text file.</span></span>

    ![Вкладка "результаты аккчеккер" с выделенным элементом "подавлять контекст"](images/accchecker-results-tab-with-suppress.png)

    <span data-ttu-id="ebba5-132">В следующем примере показано содержимое файла подавления, созданного при запуске проверки **свойств** в приложении панели управления брандмауэра Windows.</span><span class="sxs-lookup"><span data-stu-id="ebba5-132">The following example shows the content of a suppression file generated by running the **Properties** verifications on the Windows Firewall control panel application.</span></span> <span data-ttu-id="ebba5-133">В этом примере была выбрана ошибка с ИДЕНТИФИКАТОРом "Елеменсаснонаме" для подавления.</span><span class="sxs-lookup"><span data-stu-id="ebba5-133">The error with an ID of "ElementHasNoName" was chosen for suppression in this example.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   <span data-ttu-id="ebba5-134">**Отобразить результаты с приоритетом** Предлагает следующие варианты фильтрации результатов проверки по приоритету.</span><span class="sxs-lookup"><span data-stu-id="ebba5-134">**Show prioritized results** Offers the following options for filtering the verification results by priority.</span></span>
    -   <span data-ttu-id="ebba5-135">**Все** Включить все результаты независимо от приоритета.</span><span class="sxs-lookup"><span data-stu-id="ebba5-135">**All** Include all all results regardless of priority.</span></span>
    -   <span data-ttu-id="ebba5-136">**Только P1** Включайте только результаты с приоритетом 0 и приоритетом 1.</span><span class="sxs-lookup"><span data-stu-id="ebba5-136">**P1 only** Include only priority 0 and priority 1 results.</span></span>
    -   <span data-ttu-id="ebba5-137">**Только P1 P2** Используйте результаты с приоритетом 0 по приоритету 2.</span><span class="sxs-lookup"><span data-stu-id="ebba5-137">**P1   P2 only** Include priority 0 through priority 2 results.</span></span>
-   <span data-ttu-id="ebba5-138">**Выполнить выбранные проверки** Содержит кнопку **Запуск проверок** для запуска процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-138">**Run selected verifications** Provides the **Run Verifications** button for starting the verification process.</span></span> <span data-ttu-id="ebba5-139">При выполнении проверок кнопка изменяется на **Отмена проверок** и может использоваться для прекращения проверок после завершения текущего.</span><span class="sxs-lookup"><span data-stu-id="ebba5-139">While verifications are running, the button changes to **Cancel Verifications** and can be used to stop the verifications after the current one completes.</span></span>

## <a name="results-tab"></a><span data-ttu-id="ebba5-140">Вкладка «Результаты»</span><span class="sxs-lookup"><span data-stu-id="ebba5-140">Results Tab</span></span>

<span data-ttu-id="ebba5-141">Вкладка **результаты** заполняется после завершения выбранных задач проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-141">The **Results** tab is populated after the selected verification tasks are complete.</span></span> <span data-ttu-id="ebba5-142">Он состоит из следующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="ebba5-142">It consists of the following components.</span></span>

-   <span data-ttu-id="ebba5-143">Список сообщений, отображающий ошибки, предупреждения и информационные сообщения, созданные выбранными задачами проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-143">The message list, which displays the error, warning, and informational messages generated by the selected verification tasks.</span></span> <span data-ttu-id="ebba5-144">Отображаемые сообщения можно фильтровать по типу, используя флажки над списком сообщений.</span><span class="sxs-lookup"><span data-stu-id="ebba5-144">The messages displayed can be filtered by type using the checkboxes above the message list.</span></span>
-   <span data-ttu-id="ebba5-145">Сведения о сообщении и снимок экрана целевого объекта проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-145">The message details and a screen capture of the verification target.</span></span> <span data-ttu-id="ebba5-146">При выборе сообщения из списка сообщений отображаются дополнительные сведения и выделяется соответствующий элемент на панели снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="ebba5-146">Selecting a message from the message list displays further details and highlights the corresponding element in the screen capture pane.</span></span> <span data-ttu-id="ebba5-147">Кнопка **визуализировать** , переключает аккчеккер на вкладку **дерево MSAA** . Если на вкладке **результаты** выделено сообщение об ошибке, соответствующий элемент выделяется на вкладке **дерево MSAA** .</span><span class="sxs-lookup"><span data-stu-id="ebba5-147">The **Visualize** button, switches AccChecker to the **MSAA Tree** tab. If an error is highlighted on the **Results** tab, the corresponding element is highlighted on the **MSAA Tree** tab.</span></span>

<span data-ttu-id="ebba5-148">Щелчок сообщения правой кнопкой мыши открывает контекстное меню со следующими элементами.</span><span class="sxs-lookup"><span data-stu-id="ebba5-148">Right-clicking on a message exposes a context menu with the following items.</span></span>

-   <span data-ttu-id="ebba5-149">**Подавлять** Добавляет сообщение в список подавления.</span><span class="sxs-lookup"><span data-stu-id="ebba5-149">**Suppress** Adds the message to the suppression list.</span></span>
-   <span data-ttu-id="ebba5-150">**Копировать в буфер обмена** Копирует сведения о сообщении в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="ebba5-150">**Copy to clipboard** Copies the message details to the clipboard.</span></span>
-   <span data-ttu-id="ebba5-151">**Визуализировать** Переключает Аккчеккер на вкладку **дерева MSAA** . Элемент, соответствующий выбранной ошибке, выделен.</span><span class="sxs-lookup"><span data-stu-id="ebba5-151">**Visualize** Switches AccChecker to the **MSAA Tree** tab. The element that corresponds to the selected error is highlighted.</span></span>
-   <span data-ttu-id="ebba5-152">**Справка** Отображает дополнительные сведения о сообщении.</span><span class="sxs-lookup"><span data-stu-id="ebba5-152">**Help** Displays additional information about the message.</span></span>

## <a name="msaa-and-uia-screen-reader-tabs"></a><span data-ttu-id="ebba5-153">Вкладки средства чтения с экрана MSAA и UIA</span><span class="sxs-lookup"><span data-stu-id="ebba5-153">MSAA and UIA Screen Reader Tabs</span></span>

<span data-ttu-id="ebba5-154">Средства чтения с экрана MSAA и вкладки средства чтения с помощью программы на экране похожи.</span><span class="sxs-lookup"><span data-stu-id="ebba5-154">The MSAA Screen reader and the UIA Screen reader tabs are similar.</span></span> <span data-ttu-id="ebba5-155">В обоих случаях отображается запись об элементах, обнаруженных в смоделированном обходе для средства чтения с экрана, за исключением того, что в одной показана реализация MSAA, а другая — реализация UIA.</span><span class="sxs-lookup"><span data-stu-id="ebba5-155">Both display a transcript of elements encountered in a simulated traversal of the verification target by a screen reader, except that one shows the MSAA implementation, and the other shows the UIA implemention.</span></span>

<span data-ttu-id="ebba5-156">Элементы навигации и записываются в журнал, как только средство чтения с экрана считывает их.</span><span class="sxs-lookup"><span data-stu-id="ebba5-156">Elements are navigated and logged just as a screen reader would read them.</span></span> <span data-ttu-id="ebba5-157">Сведения, представленные на этой вкладке, необходимы для подтверждения того, что объявляются только полезные и релевантные сведения.</span><span class="sxs-lookup"><span data-stu-id="ebba5-157">The information presented on this tab is essential to confirm that only useful and relevant information is being announced.</span></span> <span data-ttu-id="ebba5-158">Например, допустимое имя элемента управления звуком, например "MenuItem Edit" или "Кнопка" Закрыть ", является приемлемым. Тем не менее, имя элемента управления, которое не имеет смысла, например "CPNavPanel22" или "DefaultValue1", неприемлемо.</span><span class="sxs-lookup"><span data-stu-id="ebba5-158">For example, a normal-sounding control name such as "MenuItem Edit" or "PushButton Close" is acceptable; however, a control name that doesn't make sense, such as "CPNavPanel22" or "DefaultValue1", is not acceptable.</span></span> <span data-ttu-id="ebba5-159">Кнопка " **визуализировать** " приводит к тому, что аккчеккер переключается на **дерево MSAA** или на вкладку " **дерево UIA** ". Если элемент выделен на вкладке **средство чтения с экрана** , соответствующий элемент выделяется на вкладке «Дерево **MSAA** » или « **дерево UIA** ».</span><span class="sxs-lookup"><span data-stu-id="ebba5-159">The **Visualize** button, causes AccChecker to switch to the **MSAA Tree** or **UIA Tree** tab. If an element is highlighted on the **Screen Reader** tab, the corresponding element is highlighted on the **MSAA Tree** or **UIA Tree** tab.</span></span>

<span data-ttu-id="ebba5-160">Подпрограмма проверки **скринреадер** на **консистенце** должна быть выбрана на вкладке **проверки** для отображаемой **вкладки средство чтения с экрана MSAA** .</span><span class="sxs-lookup"><span data-stu-id="ebba5-160">The **ScreenReader** verification routine under **Consistence** must be selected in the **Verifications** tab for the **MSAA Screen reader tab** to be displayed.</span></span> <span data-ttu-id="ebba5-161">Аналогичным образом необходимо выбрать подпрограмму проверки **уиаскринреадер** , чтобы отображалась вкладка **средство чтения с экрана UIA** .</span><span class="sxs-lookup"><span data-stu-id="ebba5-161">Similarly, the **UiaScreenReader** verification routine must be selected for the **UIA Screen reader** tab to be displayed.</span></span>

<span data-ttu-id="ebba5-162">На следующем снимке экрана показана вкладка средство чтения на экране UIA с примером проверки блокнота.</span><span class="sxs-lookup"><span data-stu-id="ebba5-162">The following screen shot shows the UIA Screen reader tab with a sample verification of Notepad.</span></span>

![Вкладка средства чтения с экрана аккчеккер, отображающая примеры результатов проверки](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a><span data-ttu-id="ebba5-164">Вкладки дерева MSAA и UIA</span><span class="sxs-lookup"><span data-stu-id="ebba5-164">MSAA and UIA Tree Tabs</span></span>

<span data-ttu-id="ebba5-165">Выполнение любой подпрограммы проверки приводит к тому, что Аккчеккер компилирует все видимые элементы в целевом объекте проверки и отображает их иерархически на вкладке **дерева MSAA** и на вкладке « **дерево UIA** ». На следующем снимке экрана показана вкладка дерево MSAA с иерархией элементов для блокнота.</span><span class="sxs-lookup"><span data-stu-id="ebba5-165">Running any verification routine causes AccChecker to compile all visible elements in the verification target and display them hierarchically on the **MSAA Tree** tab and the **UIA Tree** tab. The following screen shot shows the MSAA Tree tab with the hierarchy of elements for Notepad.</span></span>

![Вкладка дерева аккчеккер MSAA](images/accchecker-tree-tab.png)

## <a name="file-menu"></a><span data-ttu-id="ebba5-167">Меню «Файл»</span><span class="sxs-lookup"><span data-stu-id="ebba5-167">File Menu</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebba5-168">Меню</span><span class="sxs-lookup"><span data-stu-id="ebba5-168">Menu</span></span></th>
<th><span data-ttu-id="ebba5-169">Get-Help</span><span class="sxs-lookup"><span data-stu-id="ebba5-169">Command</span></span></th>
<th><span data-ttu-id="ebba5-170">Описание</span><span class="sxs-lookup"><span data-stu-id="ebba5-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="ebba5-171"><strong>Файл</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ebba5-171"><strong>File</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ebba5-172"><strong>Открыть</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-172"><strong>Open</strong></span></span></td>
<td><span data-ttu-id="ebba5-173">Предоставляет следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="ebba5-173">Provides the following options.</span></span><br/>
<ul>
<li><span data-ttu-id="ebba5-174"><strong>Библиотека DLL для проверки</strong> Открывает библиотеку DLL проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-174"><strong>Verifications DLL</strong> Opens a verification DLL.</span></span> <span data-ttu-id="ebba5-175">Машинные проверки Аккчеккер инкапсулируются в автономной библиотеке DLL (VerificationRoutines.dll).</span><span class="sxs-lookup"><span data-stu-id="ebba5-175">Native AccChecker verifications are encapsulated in a standalone DLL (VerificationRoutines.dll).</span></span> <span data-ttu-id="ebba5-176">Такая схема позволяет группам тестирования создавать собственный набор проверок на основе тестируемой платформы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ebba5-176">This design allows test teams to create their own set of verifications based on the UI platform being tested.</span></span></li>
<li><span data-ttu-id="ebba5-177"><strong>Файл журнала</strong> Позволяет выбрать файл журнала проверки для открытия.</span><span class="sxs-lookup"><span data-stu-id="ebba5-177"><strong>Log file</strong> Lets you choose a verification log file to open.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebba5-178"><strong>Автоматически загружать доступные проверки</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-178"><strong>Automatically load available verifications</strong></span></span></td>
<td><span data-ttu-id="ebba5-179">Автоматически загружает все доступные проверки Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="ebba5-179">Automatically loads all available AccChecker verifications.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ebba5-180"><strong>Сохранить журнал</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-180"><strong>Save Log</strong></span></span></td>
<td><span data-ttu-id="ebba5-181">Сохраните журнал проверки в формате XML или в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="ebba5-181">Save the verification log as XML or as plain text.</span></span> <span data-ttu-id="ebba5-182">Обычный текст более удобен для чтения.</span><span class="sxs-lookup"><span data-stu-id="ebba5-182">Plain text is more readable.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ebba5-183"><strong>Сохранить подавление</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-183"><strong>Save Suppression</strong></span></span></td>
<td><span data-ttu-id="ebba5-184">Сохраните журнал подавления как XML.</span><span class="sxs-lookup"><span data-stu-id="ebba5-184">Save the suppression log as XML.</span></span> <span data-ttu-id="ebba5-185">В этом файле указываются сообщения проверки, пропускаемые при регрессионном тестировании.</span><span class="sxs-lookup"><span data-stu-id="ebba5-185">This file specifies the verification messages to ignore in regression testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ebba5-186"><strong>Выход</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-186"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="ebba5-187">Закрывает средство Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="ebba5-187">Closes the AccChecker tool.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="ebba5-188"><strong>Проверки</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ebba5-188"><strong>Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ebba5-189"><strong>Запустить сейчас</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-189"><strong>Run Now</strong></span></span></td>
<td><span data-ttu-id="ebba5-190">Выполните подпрограммы проверки, как указано для выбранного целевого объекта проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-190">Run the verification routines as specified for the chosen verification target.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebba5-191"><strong>Включить все</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-191"><strong>Enable All</strong></span></span></td>
<td><span data-ttu-id="ebba5-192">Проверьте все флажки проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-192">Check all verification routine check boxes.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ebba5-193"><strong>Отключить все</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-193"><strong>Disable All</strong></span></span></td>
<td><span data-ttu-id="ebba5-194">Снимите все флажки для всех подпрограмм проверки.</span><span class="sxs-lookup"><span data-stu-id="ebba5-194">Uncheck all verification routine check boxes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ebba5-195"><strong>Параметры</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-195"><strong>Options</strong></span></span></td>
<td><span data-ttu-id="ebba5-196"><strong>Always On сверху</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-196"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="ebba5-197">Сделайте Аккчеккер в самом верхнем окне в z-порядке.</span><span class="sxs-lookup"><span data-stu-id="ebba5-197">Make AccChecker the topmost window in the z-order.</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="ebba5-198"><strong>Справка</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ebba5-198"><strong>Help</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ebba5-199"><strong>Справка</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-199"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="ebba5-200">Отображение справочной информации.</span><span class="sxs-lookup"><span data-stu-id="ebba5-200">Display help information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebba5-201"><strong>О программе</strong></span><span class="sxs-lookup"><span data-stu-id="ebba5-201"><strong>About</strong></span></span></td>
<td><span data-ttu-id="ebba5-202">Отображение версии Аккчеккер и адреса электронной почты для обращения в корпорацию Майкрософт о Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="ebba5-202">Display the AccChecker version and an email address for contacting Microsoft about AccChecker.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ebba5-203">См. также</span><span class="sxs-lookup"><span data-stu-id="ebba5-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebba5-204">Средство UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="ebba5-204">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





