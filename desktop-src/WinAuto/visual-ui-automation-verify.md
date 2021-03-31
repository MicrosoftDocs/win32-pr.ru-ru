---
title: Проверка визуальной автоматизации пользовательского интерфейса
description: Проверка визуальной автоматизации пользовательского интерфейса (Visual UIA Verify) — это Windows \ 32; Драйвер графического пользовательского интерфейса для библиотеки тестирования UIA, предназначенный для ручного тестирования модели автоматизации пользовательского интерфейса.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779307"
---
# <a name="visual-ui-automation-verify"></a><span data-ttu-id="e7c94-103">Проверка визуальной автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e7c94-103">Visual UI Automation Verify</span></span>

<span data-ttu-id="e7c94-104">Проверка визуальной автоматизации пользовательского интерфейса (Visual UIA Verify) — это драйвер графического пользовательского интерфейса Windows для библиотеки тестирования UIA, предназначенный для ручного тестирования модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e7c94-104">Visual UI Automation Verify (Visual UIA Verify) is a Windows GUI driver for the UIA Test Library that is designed for manual testing of UI automation.</span></span> <span data-ttu-id="e7c94-105">Он предоставляет интерфейс для работы с библиотекой тестирования UIA, который устраняет затраты на написание кода для программы командной строки.</span><span class="sxs-lookup"><span data-stu-id="e7c94-105">It provides an interface to UIA Test Library functionality that eliminates the coding overhead of a command-line tool.</span></span>

-   [<span data-ttu-id="e7c94-106">Команды меню</span><span class="sxs-lookup"><span data-stu-id="e7c94-106">Menu Commands</span></span>](#menu-commands)
-   [<span data-ttu-id="e7c94-107">Функциональные панели</span><span class="sxs-lookup"><span data-stu-id="e7c94-107">Functional Panes</span></span>](#functional-panes)
    -   [<span data-ttu-id="e7c94-108">Панель дерева элементов автоматизации</span><span class="sxs-lookup"><span data-stu-id="e7c94-108">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
    -   [<span data-ttu-id="e7c94-109">Панель "тесты"</span><span class="sxs-lookup"><span data-stu-id="e7c94-109">Tests Pane</span></span>](#tests-pane)
    -   [<span data-ttu-id="e7c94-110">Область результатов тестирования</span><span class="sxs-lookup"><span data-stu-id="e7c94-110">Test Results Pane</span></span>](#test-results-pane)
    -   [<span data-ttu-id="e7c94-111">Панель "Свойства"</span><span class="sxs-lookup"><span data-stu-id="e7c94-111">Properties Pane</span></span>](#properties-pane)

<span data-ttu-id="e7c94-112">Visual UIA Verify поддерживает только средство ведения журнала "Проверка XML" (WUIALoggerXml.dll) в собственном коде.</span><span class="sxs-lookup"><span data-stu-id="e7c94-112">Visual UIA Verify supports only the UIA Verify XML logger (WUIALoggerXml.dll) natively.</span></span> <span data-ttu-id="e7c94-113">Пользовательские преобразования XML, выбираемые пользователем, включены в Visual UIA Verify для представления различных представлений отчета средства ведения журнала XML в области **Результаты теста** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-113">User-selectable XML transformations are incorporated into Visual UIA Verify to present various views of the XML logger report in the **Test Results** pane.</span></span>

<span data-ttu-id="e7c94-114">По умолчанию Visual UIA проверяет загрузку клиентского поставщика автоматизации пользовательского интерфейса, который поставляется с первоначальным выпуском модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e7c94-114">By default, Visual UIA Verify loads the UI Automation client-side provider that shipped with the original release of UI Automation.</span></span> <span data-ttu-id="e7c94-115">Вы можете отказаться от загрузки этого поставщика, добавив **/ноклиентсидепровидер** в параметр командной строки VisualUIVerifyNative.exe.</span><span class="sxs-lookup"><span data-stu-id="e7c94-115">You can choose not to load this provider by adding **/NOCLIENTSIDEPROVIDER** in the command-line option of VisualUIVerifyNative.exe.</span></span>

<span data-ttu-id="e7c94-116">На следующем снимке экрана показаны основные функциональные области пользовательского интерфейса Visual UIA Verify.</span><span class="sxs-lookup"><span data-stu-id="e7c94-116">The following screen shot shows the main functional areas of the Visual UIA Verify user interface.</span></span>

![Основные функциональные области пользовательского интерфейса Visual UIA Verify](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a><span data-ttu-id="e7c94-118">Команды меню</span><span class="sxs-lookup"><span data-stu-id="e7c94-118">Menu Commands</span></span>

<span data-ttu-id="e7c94-119">В следующей таблице описаны команды в меню Visual UIA Verify.</span><span class="sxs-lookup"><span data-stu-id="e7c94-119">The following table describes the commands in the Visual UIA Verify menu.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7c94-120">Меню</span><span class="sxs-lookup"><span data-stu-id="e7c94-120">Menu</span></span></th>
<th><span data-ttu-id="e7c94-121">Get-Help</span><span class="sxs-lookup"><span data-stu-id="e7c94-121">Command</span></span></th>
<th><span data-ttu-id="e7c94-122">Описание</span><span class="sxs-lookup"><span data-stu-id="e7c94-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7c94-123"><strong>Файл</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-123"><strong>File</strong></span></span></td>
<td><span data-ttu-id="e7c94-124"><strong>Выход</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-124"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="e7c94-125">Выйдите из проверки Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e7c94-125">Exit Visual UIA Verify.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7c94-126"><strong>Вид</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-126"><strong>View</strong></span></span></td>
<td><span data-ttu-id="e7c94-127"><strong>Выделение</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-127"><strong>Highlighting</strong></span></span></td>
<td><span data-ttu-id="e7c94-128">Выделите ограничивающий прямоугольник выбранного элемента на панели <strong>дерева элементов автоматизации</strong> .</span><span class="sxs-lookup"><span data-stu-id="e7c94-128">Highlight the bounding rectangle of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="e7c94-129">Доступны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="e7c94-129">The following options are available.</span></span>
<ul>
<li><span data-ttu-id="e7c94-130"><strong>Прямоугольник</strong>— сплошная красная линия.</span><span class="sxs-lookup"><span data-stu-id="e7c94-130"><strong>Rectangle</strong>—A solid red line.</span></span></li>
<li><span data-ttu-id="e7c94-131"><strong>Прямоугольник с плавным</strong>переходом — сплошная красная линия, которая исчезает через несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="e7c94-131"><strong>Fading Rectangle</strong>—A solid red line that disappears after a few seconds.</span></span></li>
<li><span data-ttu-id="e7c94-132"><strong>Лучи и прямоугольник</strong>— сплошная красная линия с дополнительными выделенными синими линиями, которые обходятся из каждого угла ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e7c94-132"><strong>Rays and Rectangle</strong>—A solid red line with additional blue highlight lines that radiate from each corner of the bounding rectangle.</span></span></li>
<li><span data-ttu-id="e7c94-133"><strong>Нет</strong>— выделение не отображается.</span><span class="sxs-lookup"><span data-stu-id="e7c94-133"><strong>None</strong>—No visible highlight.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="e7c94-134"><strong>Дерево элементов автоматизации</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="e7c94-134"><strong>Automation Elements Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="e7c94-135"><strong>Обновить выбранный элемент</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-135"><strong>Refresh Selected Element</strong></span></span></td>
<td><span data-ttu-id="e7c94-136">Обновите дочерние элементы выбранного элемента на панели <strong>дерева элементов автоматизации</strong> .</span><span class="sxs-lookup"><span data-stu-id="e7c94-136">Refresh the children of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="e7c94-137">Список элементов является статическим и не обновляется динамически (автоматически) при изменении дерева элементов.</span><span class="sxs-lookup"><span data-stu-id="e7c94-137">The list of elements is static and does not refresh dynamically (automatically) if the element tree changes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7c94-138"><strong>Навигация</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-138"><strong>Navigation</strong></span></span></td>
<td><span data-ttu-id="e7c94-139">Перейдите по иерархии дерева элементов к одному из следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="e7c94-139">Navigate through the element tree hierarchy to one of the following elements.</span></span>
<ul>
<li><span data-ttu-id="e7c94-140"><strong>Parent</strong>— переход к родительскому элементу.</span><span class="sxs-lookup"><span data-stu-id="e7c94-140"><strong>Parent</strong>—Go to parent element.</span></span></li>
<li><span data-ttu-id="e7c94-141"><strong>Первый дочерний</strong>объект — переход к первому дочернему элементу.</span><span class="sxs-lookup"><span data-stu-id="e7c94-141"><strong>First Child</strong>—Go to first child element.</span></span></li>
<li><span data-ttu-id="e7c94-142"><strong>Следующий элемент с общим родителем</strong>— переход к первому элемента того же уровня.</span><span class="sxs-lookup"><span data-stu-id="e7c94-142"><strong>Next Sibling</strong>—Go to first sibling element.</span></span></li>
<li><span data-ttu-id="e7c94-143"><strong>Предыдущий элемент с общим родителем</strong>— переход к предыдущему однорангового элемента.</span><span class="sxs-lookup"><span data-stu-id="e7c94-143"><strong>Previous Sibling</strong>—Go to previous sibling element.</span></span></li>
<li><span data-ttu-id="e7c94-144"><strong>Последний дочерний</strong>объект — переход к последнему дочернему элементу.</span><span class="sxs-lookup"><span data-stu-id="e7c94-144"><strong>Last Child</strong>—Go to last child element.</span></span></li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="e7c94-145"><strong>Режим</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="e7c94-145"><strong>Mode</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="e7c94-146"><strong>Always On сверху</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-146"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="e7c94-147">Окно проверки Visual UIA остается в верхней части z-порядка рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e7c94-147">The Visual UIA Verify window remains at the top of the desktop z-order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7c94-148"><strong>Режим наведения указателя (используйте CTRL)</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-148"><strong>Hover Mode (Use Ctrl)</strong></span></span></td>
<td><span data-ttu-id="e7c94-149">При нажатии клавиши CTRL элемент под курсором мыши определяется как интересующий элемент.</span><span class="sxs-lookup"><span data-stu-id="e7c94-149">When the Ctrl key is pressed, the element under the mouse cursor is identified as the element of interest.</span></span> <span data-ttu-id="e7c94-150">Панель <strong>дерева элементов автоматизации</strong> обновляется, и соответствующий элемент в списке элементов выделяется.</span><span class="sxs-lookup"><span data-stu-id="e7c94-150">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e7c94-151"><strong>Отслеживание фокуса</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-151"><strong>Focus Tracking</strong></span></span></td>
<td><span data-ttu-id="e7c94-152">При изменении фокуса элемент с фокусом определяется как интересующий элемент.</span><span class="sxs-lookup"><span data-stu-id="e7c94-152">As the focus changes, the element with the focus is identified as the element of interest.</span></span> <span data-ttu-id="e7c94-153">Панель <strong>дерева элементов автоматизации</strong> обновляется, и соответствующий элемент в списке элементов выделяется.</span><span class="sxs-lookup"><span data-stu-id="e7c94-153">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="e7c94-154"><strong>Тесты</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="e7c94-154"><strong>Tests</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="e7c94-155"><strong>Переход влево</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-155"><strong>Go Left</strong></span></span></td>
<td><span data-ttu-id="e7c94-156">Перемещение одного узла влево в дереве <strong>тестов</strong> .</span><span class="sxs-lookup"><span data-stu-id="e7c94-156">Move one node left in the <strong>Tests</strong> tree.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7c94-157"><strong>Вверх</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-157"><strong>Go Up</strong></span></span></td>
<td><span data-ttu-id="e7c94-158">Переместить один узел вверх в дереве <strong>тестов</strong> .</span><span class="sxs-lookup"><span data-stu-id="e7c94-158">Move one node up in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e7c94-159"><strong>Перейти вниз</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-159"><strong>Go Down</strong></span></span></td>
<td><span data-ttu-id="e7c94-160">Перемещение одного узла вниз в дереве <strong>тестов</strong> .</span><span class="sxs-lookup"><span data-stu-id="e7c94-160">Move one node down in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e7c94-161"><strong>Вправо</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-161"><strong>Go Right</strong></span></span></td>
<td><span data-ttu-id="e7c94-162">Перемещение одного узла прямо в дереве <strong>тестов</strong> .</span><span class="sxs-lookup"><span data-stu-id="e7c94-162">Move one node right in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e7c94-163"><strong>Выполнить выбранные тесты для выбранного элемента</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-163"><strong>Run Selected Test(s) On Selected Element</strong></span></span></td>
<td><span data-ttu-id="e7c94-164">Выполнение выбранных тестов из дерева <strong>тестов</strong> выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="e7c94-164">Run the selected tests from the <strong>Tests</strong> tree on the selected element.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e7c94-165"><strong>Фильтрация известных проблем</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-165"><strong>Filter Known Problems</strong></span></span></td>
<td><span data-ttu-id="e7c94-166">Отфильтруйте известные ошибки автоматизации пользовательского интерфейса на основе результатов теста.</span><span class="sxs-lookup"><span data-stu-id="e7c94-166">Filter known UI Automation bugs from the test results.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e7c94-167"><strong>Справка</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-167"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="e7c94-168"><strong>О проверке визуальной автоматизации пользовательского интерфейса</strong></span><span class="sxs-lookup"><span data-stu-id="e7c94-168"><strong>About Visual UI Automation Verify</strong></span></span></td>
<td><span data-ttu-id="e7c94-169">Отображение версии программного обеспечения и сведений об авторских правах для проверки Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e7c94-169">Display the software version and copyright information for Visual UIA Verify.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a><span data-ttu-id="e7c94-170">Функциональные панели</span><span class="sxs-lookup"><span data-stu-id="e7c94-170">Functional Panes</span></span>

<span data-ttu-id="e7c94-171">В этом разделе описываются функциональные панели в пользовательском интерфейсе проверки Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e7c94-171">This section describes the functional panes in the Visual UIA Verify user interface.</span></span>

-   [<span data-ttu-id="e7c94-172">Панель дерева элементов автоматизации</span><span class="sxs-lookup"><span data-stu-id="e7c94-172">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
-   [<span data-ttu-id="e7c94-173">Панель "тесты"</span><span class="sxs-lookup"><span data-stu-id="e7c94-173">Tests Pane</span></span>](#tests-pane)
-   [<span data-ttu-id="e7c94-174">Область результатов тестирования</span><span class="sxs-lookup"><span data-stu-id="e7c94-174">Test Results Pane</span></span>](#test-results-pane)
-   [<span data-ttu-id="e7c94-175">Панель "Свойства"</span><span class="sxs-lookup"><span data-stu-id="e7c94-175">Properties Pane</span></span>](#properties-pane)

### <a name="automation-elements-tree-pane"></a><span data-ttu-id="e7c94-176">Панель дерева элементов автоматизации</span><span class="sxs-lookup"><span data-stu-id="e7c94-176">Automation Elements Tree Pane</span></span>

<span data-ttu-id="e7c94-177">Панель **дерева элементов автоматизации** содержит иерархический моментальный снимок объектов элементов автоматизации, доступных для тестирования.</span><span class="sxs-lookup"><span data-stu-id="e7c94-177">The **Automation Elements Tree** pane contains a hierarchical snapshot of automation element objects that are available for testing.</span></span> <span data-ttu-id="e7c94-178">Верхний элемент в дереве представляет рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="e7c94-178">The top element in the tree represents the desktop.</span></span>

<span data-ttu-id="e7c94-179">Это представление представляет собой статическую коллекцию, которая компилируется при запуске проверки Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e7c94-179">This view is a static collection that is compiled when Visual UIA Verify starts.</span></span> <span data-ttu-id="e7c94-180">Чтобы обновить представление на выбранном узле, используйте команду меню **Обновить выбранный элемент** или кнопку на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="e7c94-180">To refresh the view at the selected node, use the **Refresh Selected Element** menu command or toolbar button.</span></span>

<span data-ttu-id="e7c94-181">На следующем снимке экрана показана панель **дерева элементов автоматизации** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-181">The following screen shot shows the **Automation Elements Tree** pane.</span></span>

![Панель дерева элементов автоматизации в Visual UIA проверка](images/automation-elements-tree-pane.png)

<span data-ttu-id="e7c94-183">Недоступный узел в **дереве элементов автоматизации** указывает на то, что элемент является членом необработанного представления модели автоматизации пользовательского интерфейса, но не соответствует условиям, необходимым для рассмотрения элементом представления содержимого или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e7c94-183">A dimmed (unavailable) node in the **Automation Elements Tree** indicates that the element is a member of the UI Automation raw view, but does not meet the conditions necessary to be considered a member of the content view or control view.</span></span> <span data-ttu-id="e7c94-184">Тем не менее элемент можно протестировать с помощью проверки визуальной модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e7c94-184">However, the element can still be tested from Visual UI Automation Verify.</span></span> <span data-ttu-id="e7c94-185">Дополнительные сведения см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e7c94-185">For more information, see the [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="e7c94-186">Команды, доступные на панели инструментов **дерева элементов автоматизации** , включают:</span><span class="sxs-lookup"><span data-stu-id="e7c94-186">Commands available from the **Automation Elements Tree** toolbar include:</span></span>

-   <span data-ttu-id="e7c94-187">**Обновить**— обновить выбранный узел и его дочерние узлы.</span><span class="sxs-lookup"><span data-stu-id="e7c94-187">**Refresh**—Refresh the selected node and its children.</span></span> <span data-ttu-id="e7c94-188">Эта команда не обновляет дерево элементов целиком, если не выбран корневой узел.</span><span class="sxs-lookup"><span data-stu-id="e7c94-188">This command does not refresh the entire element tree unless the root node is selected.</span></span>
-   <span data-ttu-id="e7c94-189">**Parent (Ctrl + Shift + F6)**— переход к родительскому элементу текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-189">**Parent (Ctrl+Shift+F6)**—Go to parent of the current node.</span></span>
-   <span data-ttu-id="e7c94-190">**Первый дочерний элемент (Ctrl + Shift + F7)**— переход к первому дочернему элементу текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-190">**First Child (Ctrl+Shift+F7)**—Go to first child of the current node..</span></span>
-   <span data-ttu-id="e7c94-191">**Следующий одноуровневый элемент (Ctrl + Shift + F8)**— переход к следующему дочернему элементу текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-191">**Next Sibling (Ctrl+Shift+F8)**—Go to next sibling child of the current node.</span></span>
-   <span data-ttu-id="e7c94-192">**Предыдущий элемент того же уровня (Ctrl + Shift + F9)**— переход к предыдущему элементу того же уровня текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-192">**Previous Sibling (Ctrl+Shift+F9)**—Go to previous sibling of the current node.</span></span>
-   <span data-ttu-id="e7c94-193">**Последний дочерний элемент (Ctrl + Shift + F10)**— переход к последнему дочернему элементу текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-193">**Last Child (Ctrl+Shift+F10)**—Go to last child of the current node.</span></span>
-   <span data-ttu-id="e7c94-194">**Отслеживание фокуса**— включение или отключение выбора узлов в зависимости от отслеживания фокуса.</span><span class="sxs-lookup"><span data-stu-id="e7c94-194">**Focus Tracking**—Toggle node selection on or off based on focus tracking.</span></span>

### <a name="tests-pane"></a><span data-ttu-id="e7c94-195">Панель "тесты"</span><span class="sxs-lookup"><span data-stu-id="e7c94-195">Tests Pane</span></span>

<span data-ttu-id="e7c94-196">Панель " **тесты** " содержит список тестов автоматизации пользовательского интерфейса, упорядоченных по типу теста (**элемент автоматизации**, **элемент управления** и **шаблон**) и приоритет (**Проверка сборки**, **приоритет 0**, **приоритет 1**, **приоритет 2** и **приоритет 3**).</span><span class="sxs-lookup"><span data-stu-id="e7c94-196">The **Tests** pane contains a list of UI Automation tests organized by test type (**Automation Element**, **Control**, and **Pattern**) and priority (**Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, and **Priority 3**).</span></span> <span data-ttu-id="e7c94-197">Этот список создается на основе типа элемента управления выбранного элемента на панели **дерева элементов автоматизации** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-197">This list is generated based on the control type of the selected element in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="e7c94-198">Для получения дополнительной информации см. [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e7c94-198">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="e7c94-199">На следующем снимке экрана показана область **тесты** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-199">The following screen shot shows the **Tests** pane.</span></span>

![Тестовая область](images/test-pane.png)

<span data-ttu-id="e7c94-201">Команды, доступные на панели инструментов " **тесты** ", включают:</span><span class="sxs-lookup"><span data-stu-id="e7c94-201">Commands available from the **Tests** toolbar include:</span></span>

-   <span data-ttu-id="e7c94-202">**Показать**— указывает тесты автоматизации пользовательского интерфейса для отображения; то есть отобразить все тесты или только тесты, которые подходят для типа элемента управления выбранного элемента в **дереве элементов автоматизации** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e7c94-202">**Show**—Specifies the UI Automation tests to display; that is, display all tests or only tests suited to the control type of the selected element in the **Automation Elements Tree** (default).</span></span>
-   <span data-ttu-id="e7c94-203">**Тип**— указывает типы тестов для вывода: **элемент автоматизации**, **шаблон** или **элемент управления**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-203">**Type**—Specifies the test types to display: **Automation Element**, **Pattern**, or **Control**.</span></span>
-   <span data-ttu-id="e7c94-204">**Приоритеты**— задает приоритеты тестов для вывода: **Проверка сборки**, **приоритет 0**, **приоритет 1**, **приоритет 2** или **приоритет 3**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-204">**Priorities**—Specifies the test priorities to display: **Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, or **Priority 3**.</span></span>
-   <span data-ttu-id="e7c94-205">**Переход влево**— переход к родительскому элементу текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-205">**Go Left**—Go to the parent of the current node.</span></span>
-   <span data-ttu-id="e7c94-206">**Переход вверх**— переход к предыдущему элементу того же уровня текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-206">**Go Up**—Go to the previous sibling of the current node.</span></span>
-   <span data-ttu-id="e7c94-207">**Вниз**— переход к следующему элементу того же уровня текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-207">**Go Down**—Go to the next sibling of the current node.</span></span>
-   <span data-ttu-id="e7c94-208">**Переход вправо**— переход к первому дочернему элементу текущего узла.</span><span class="sxs-lookup"><span data-stu-id="e7c94-208">**Go Right**—Go to the first child of the current node.</span></span>
-   <span data-ttu-id="e7c94-209">**Выполнить выбранные тесты**— выполняет тесты для элемента, выбранного в **дереве элементов службы автоматизации**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-209">**Run Selected Test(s)**—Runs the tests on the element selected in the **Automation Elements Tree**.</span></span>

### <a name="test-results-pane"></a><span data-ttu-id="e7c94-210">Область результатов тестирования</span><span class="sxs-lookup"><span data-stu-id="e7c94-210">Test Results Pane</span></span>

<span data-ttu-id="e7c94-211">Панель **Результаты теста** содержит функцию ведения журнала проверки Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e7c94-211">The **Test Results** pane contains the Visual UIA Verify logging functionality.</span></span> <span data-ttu-id="e7c94-212">На следующем снимке экрана показана панель **Результаты теста** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-212">The following screen shot shows the **Test Results** pane.</span></span>

![панель результатов теста](images/test-results-pane.png)

<span data-ttu-id="e7c94-214">Команды, доступные на панели инструментов **результатов тестов** , включают:</span><span class="sxs-lookup"><span data-stu-id="e7c94-214">Commands available from the **Tests Results** toolbar include:</span></span>

-   <span data-ttu-id="e7c94-215">**Назад — переход** на страницу назад в журнале просмотра отчета.</span><span class="sxs-lookup"><span data-stu-id="e7c94-215">**Back**—Page backward in report viewing history.</span></span>
-   <span data-ttu-id="e7c94-216">**Вперед**— страница пересылается в журнале просмотра отчетов.</span><span class="sxs-lookup"><span data-stu-id="e7c94-216">**Forward**—Page forward in report viewing history.</span></span>
-   <span data-ttu-id="e7c94-217">**Общие**— отображает сводку по результатам теста (**пройденные**, **неудачные** и **непредвиденные ошибки**).</span><span class="sxs-lookup"><span data-stu-id="e7c94-217">**Overall**—Displays a summary of the test results (**Passed**, **Failed**, and **Unexpected Error**).</span></span> <span data-ttu-id="e7c94-218">Результат теста связан с представлением " **все результаты** ".</span><span class="sxs-lookup"><span data-stu-id="e7c94-218">The test result is linked to the **All Results** view.</span></span> <span data-ttu-id="e7c94-219">**Общая** команда выводит таблицу следующего вида.</span><span class="sxs-lookup"><span data-stu-id="e7c94-219">The **Overall** command displays a table like the following one.</span></span>

    ![Таблица общих результатов теста](images/overall-test-results.png)

-   <span data-ttu-id="e7c94-221">**Все результаты**— отображает подробный журнал для каждого результата теста, как показано в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="e7c94-221">**All Results**— Displays a detailed log for each test result, as shown in the following tables.</span></span>

    ![Пример сведений о результатах журнала в представлении "все результаты"](images/all-results-log.png)

    <span data-ttu-id="e7c94-223">Имя теста в таблице **все результаты** связано с описанием тестового случая для элемента, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e7c94-223">The test name in the **All Results** table is linked to a test case description for the element, as in the following table.</span></span>

    ![сведения о тестовом случае](images/test-case-detail.png)

-   <span data-ttu-id="e7c94-225">**Полный журнал**— отображает альтернативное представление подробного журнала для каждого результата теста, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="e7c94-225">**Full Log**—Displays an alternate view of the detailed log for each test result, as shown in the following screen shot.</span></span>

    ![Альтернативное представление сведений о тестовом случае](images/alt-view-of-test-case-detail.png)

-   <span data-ttu-id="e7c94-227">**XML**— отображает необработанный XML-код, созданный средством ведения журнала XML.</span><span class="sxs-lookup"><span data-stu-id="e7c94-227">**XML**—Displays the raw XML generated by the XML logger.</span></span>
-   <span data-ttu-id="e7c94-228">**Быстрый поиск**— простой текст для поиска в текущем представлении в области **Результаты теста** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-228">**Quick Find**—Simple text search of the current view in the **Test Results** pane.</span></span>
-   <span data-ttu-id="e7c94-229">**Открыть в новом окне**— открытие текущего представления в новом экземпляре Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e7c94-229">**Open in New Window**—Opens the current view in a new instance of Internet Explorer.</span></span>

### <a name="properties-pane"></a><span data-ttu-id="e7c94-230">Панель «Свойства»</span><span class="sxs-lookup"><span data-stu-id="e7c94-230">Properties Pane</span></span>

<span data-ttu-id="e7c94-231">Панель **свойств** содержит список свойств и значений свойств автоматизации пользовательского интерфейса, упорядоченных по типу свойства: **общий доступ**, **Идентификация**, **шаблоны** (шаблоны элементов управления), **состояние** и **видимость**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-231">The **Properties** pane contains a list of UI Automation properties and property values organized by property type: **General Accessibility**, **Identification**, **Patterns** (control patterns), **State**, and **Visibility**.</span></span> <span data-ttu-id="e7c94-232">Значения свойств заполняются динамически на основе типа элемента управления объекта, выбранного на панели **дерева элементов автоматизации** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-232">The property values are dynamically populated based on the control type of the object selected in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="e7c94-233">На следующем снимке экрана показана панель **свойств** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-233">The following screen shot shows the **Properties** pane.</span></span>

![панель "Свойства"](images/properties-pane.png)

<span data-ttu-id="e7c94-235">Если выбранный элемент управления поддерживает конкретный шаблон элемента управления, Visual UIA Verify предоставляет возможность вызывать методы, поддерживаемые этим шаблоном элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e7c94-235">If the selected control supports a specific control pattern, Visual UIA Verify provides the ability to call methods that are supported by that control pattern.</span></span> <span data-ttu-id="e7c94-236">Например, [тип элемента управления Window](uiauto-supportwindowcontroltype.md) поддерживает [шаблон элемента управления Window](uiauto-implementingwindow.md), который имеет метод [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) , который может быть вызван из панели **свойств** , как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="e7c94-236">For example, the [Window control type](uiauto-supportwindowcontroltype.md) supports the [Window control pattern](uiauto-implementingwindow.md), which has a [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) method that can be invoked from the **Properties** pane, as shown in the following screen shot.</span></span> <span data-ttu-id="e7c94-237">Для получения дополнительной информации см. [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e7c94-237">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

![метод Close шаблона элемента управления Window, вызываемый из панели свойств](images/close-invoked-from-properties-pane.png)

<span data-ttu-id="e7c94-239">Ниже перечислены команды, доступные на панели инструментов « **Свойства** ».</span><span class="sxs-lookup"><span data-stu-id="e7c94-239">Commands available from the **Properties** toolbar include:</span></span>

-   <span data-ttu-id="e7c94-240">**Обновить**— обновление дерева **свойств** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-240">**Refresh**—Refresh the **Properties** tree.</span></span>
-   <span data-ttu-id="e7c94-241">**Развернуть все**— разворачивает все узлы в дереве **свойств** .</span><span class="sxs-lookup"><span data-stu-id="e7c94-241">**Expand All**—Expands all nodes in the **Properties** tree.</span></span>

 

 




