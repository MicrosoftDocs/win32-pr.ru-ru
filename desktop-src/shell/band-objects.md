---
description: Панель обозревателя появилась в обозревателе Microsoft Internet Explorer 4,0, чтобы предоставить область просмотра, смежную с областью браузера.
title: Создание пользовательских панелей обозревателя, панелей инструментов и рабочих столов
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104557064"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a><span data-ttu-id="bdf97-103">Создание настраиваемых панелей обозревателя, панелей инструментов и полос рабочих столов</span><span class="sxs-lookup"><span data-stu-id="bdf97-103">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</span></span>

<span data-ttu-id="bdf97-104">Панель обозревателя появилась в обозревателе Microsoft Internet Explorer 4,0, чтобы предоставить область просмотра, смежную с областью браузера.</span><span class="sxs-lookup"><span data-stu-id="bdf97-104">The Explorer Bar was introduced with Microsoft Internet Explorer 4.0 to provide a display area adjacent to the browser pane.</span></span> <span data-ttu-id="bdf97-105">Это, по сути, дочернее окно в окне Internet Explorer, и его можно использовать для вывода информации и взаимодействия с пользователем практически таким же образом.</span><span class="sxs-lookup"><span data-stu-id="bdf97-105">It is basically a child window within the Windows Internet Explorer window, and it can be used to display information and interact with the user in much the same way.</span></span> <span data-ttu-id="bdf97-106">Панели обозревателя чаще всего отображаются в виде вертикальной панели в левой части области браузера.</span><span class="sxs-lookup"><span data-stu-id="bdf97-106">Explorer Bars are most commonly displayed as a vertical pane on the left side of the browser pane.</span></span> <span data-ttu-id="bdf97-107">Однако панель обозревателя также может отображаться горизонтально, под областью браузера.</span><span class="sxs-lookup"><span data-stu-id="bdf97-107">However, an Explorer Bar can also be displayed horizontally, below the browser pane.</span></span>

![Снимок экрана, на котором показаны вертикальная и горизонтальная панели обозревателя.](images/expl1.jpg)

<span data-ttu-id="bdf97-109">Панель обозревателя имеет широкий спектр возможных применений.</span><span class="sxs-lookup"><span data-stu-id="bdf97-109">There is a wide range of possible uses for the Explorer Bar.</span></span> <span data-ttu-id="bdf97-110">Пользователи могут выбрать вариант, который должен отображаться несколькими разными способами, включая его выбор из подменю " **панель обозревателя** " в меню " **вид** " или нажатием кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="bdf97-110">Users can select which option they want to see in several different ways, including selecting it from the **Explorer Bar** submenu of the **View** menu, or clicking a toolbar button.</span></span> <span data-ttu-id="bdf97-111">Internet Explorer предоставляет несколько стандартных панелей обозревателя, включая Избранное и поиск.</span><span class="sxs-lookup"><span data-stu-id="bdf97-111">Internet Explorer provides several standard Explorer Bars, including Favorites and Search.</span></span>

<span data-ttu-id="bdf97-112">Одним из способов настройки обозревателя Internet Explorer является добавление настраиваемой панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-112">One of the ways you can customize Internet Explorer is by adding a custom Explorer Bar.</span></span> <span data-ttu-id="bdf97-113">При реализации и регистрации они будут добавлены в подменю " **панель обозревателя** " меню " **вид** ".</span><span class="sxs-lookup"><span data-stu-id="bdf97-113">When implemented and registered, it will be added to the **Explorer Bar** submenu of the **View** menu.</span></span> <span data-ttu-id="bdf97-114">При выборе пользователем область просмотра панели обозревателя может использоваться для вывода информации и ввода данных пользователем во многом так же, как у обычного окна.</span><span class="sxs-lookup"><span data-stu-id="bdf97-114">When selected by the user, the Explorer Bar's display area can then be used to display information and take user input in much the same way as a normal window.</span></span>

![снимок экрана панели обозревателя](images/expl2.jpg)

<span data-ttu-id="bdf97-116">Чтобы создать настраиваемую панель обозревателя, необходимо реализовать и зарегистрировать *объект диапазона*.</span><span class="sxs-lookup"><span data-stu-id="bdf97-116">To create a custom Explorer Bar, you must implement and register a *band object*.</span></span> <span data-ttu-id="bdf97-117">Объекты управления версиями появились в оболочке версии 4,71 и предоставляют возможности, аналогичные обычным окнам.</span><span class="sxs-lookup"><span data-stu-id="bdf97-117">Band objects were introduced with version 4.71 of the Shell and provide capabilities similar to those of normal windows.</span></span> <span data-ttu-id="bdf97-118">Однако, поскольку они являются объектами модели COM и содержатся в Internet Explorer или оболочке, они реализуются несколько по-разному.</span><span class="sxs-lookup"><span data-stu-id="bdf97-118">However, because they are Component Object Model (COM) objects and contained by either Internet Explorer or the Shell, they are implemented somewhat differently.</span></span> <span data-ttu-id="bdf97-119">Для создания примеров полос обозревателя, отображаемых на первом рисунке, использовались простые объекты полос.</span><span class="sxs-lookup"><span data-stu-id="bdf97-119">Simple band objects were used to create the sample Explorer Bars displayed in the first graphic.</span></span> <span data-ttu-id="bdf97-120">Реализация образца вертикальной панели обозревателя будет подробно рассмотрена в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="bdf97-120">The implementation of the vertical Explorer Bar sample will be discussed in detail in a later section.</span></span>

## <a name="tool-bands"></a><span data-ttu-id="bdf97-121">Полосы инструментов</span><span class="sxs-lookup"><span data-stu-id="bdf97-121">Tool Bands</span></span>

<span data-ttu-id="bdf97-122">Панель *инструментов — это* объект с полосой, который появился в Microsoft Internet Explorer 5 для поддержки функции Windows Radio Tool.</span><span class="sxs-lookup"><span data-stu-id="bdf97-122">A *tool band* is a band object that was introduced with Microsoft Internet Explorer 5 to support the Windows radio toolbar feature.</span></span> <span data-ttu-id="bdf97-123">Панель инструментов Internet Explorer на самом деле является [элементом управления главной](../controls/rebar-controls.md) панели, который содержит несколько [элементов управления ToolBar](../controls/toolbar-control-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bdf97-123">The Internet Explorer toolbar is actually a [rebar control](../controls/rebar-controls.md) that contains several [toolbar controls](../controls/toolbar-control-reference.md).</span></span> <span data-ttu-id="bdf97-124">Создавая панель инструментов, можно добавить полосу к этому элементу управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="bdf97-124">By creating a tool band, you can add a band to that rebar control.</span></span> <span data-ttu-id="bdf97-125">Однако, как и в случае с панелями обозревателя, панель инструментов является окном общего назначения.</span><span class="sxs-lookup"><span data-stu-id="bdf97-125">However, like Explorer Bars, a tool band is a general purpose window.</span></span>

![снимок экрана с полосами инструментов](images/toolband1.jpg)

<span data-ttu-id="bdf97-127">Пользователи выводят панель инструментов, выбирая ее из подменю **панели инструментов** меню **вид** или из контекстного меню, которое отображается щелчком правой кнопкой мыши в области панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="bdf97-127">Users display a toolbar by selecting it from the **Toolbars** submenu of the **View** menu or from the shortcut menu that is displayed by right-clicking the toolbar area.</span></span>

## <a name="desk-bands"></a><span data-ttu-id="bdf97-128">Полосы рабочего стола</span><span class="sxs-lookup"><span data-stu-id="bdf97-128">Desk Bands</span></span>

<span data-ttu-id="bdf97-129">Для создания *полос рабочих столов* также можно использовать объекты полос.</span><span class="sxs-lookup"><span data-stu-id="bdf97-129">Band objects can also be used to create *desk bands*.</span></span> <span data-ttu-id="bdf97-130">Хотя их Базовая реализация похожа на панели обозревателя, полосы рабочего стола не связаны с Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bdf97-130">While their basic implementation is similar to Explorer Bars, desk bands are unrelated to Internet Explorer.</span></span> <span data-ttu-id="bdf97-131">Настольный полоса — это, по сути, способ создания закрепляемого окна на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="bdf97-131">A desk band is basically a way to create a dockable window on the desktop.</span></span> <span data-ttu-id="bdf97-132">Пользователь выбирает его, щелкнув правой кнопкой мыши панель задач и выбрав ее в подменю **панели инструментов** .</span><span class="sxs-lookup"><span data-stu-id="bdf97-132">The user selects it by right-clicking the taskbar and selecting it from the **Toolbars** submenu.</span></span>

![Снимок экрана, на котором показан пример полосы рабочего стола.](images/desk2.png)

<span data-ttu-id="bdf97-134">Изначально полосы рабочего стола закреплены на панели задач.</span><span class="sxs-lookup"><span data-stu-id="bdf97-134">Initially, desk bands are docked on the taskbar.</span></span>

![Снимок экрана, на котором показаны полосы рабочего стола, закрепленные на панели задач.](images/desk1.jpg)

<span data-ttu-id="bdf97-136">Затем пользователь может перетащить полосу настольных ПК на Рабочий стол, и она появится в виде обычного окна.</span><span class="sxs-lookup"><span data-stu-id="bdf97-136">The user can then drag the desk band to the desktop, and it will appear as a normal window.</span></span>

![снимок экрана с полосами рабочих столов](images/desk3.png)

## <a name="implementing-band-objects"></a><span data-ttu-id="bdf97-138">Реализация диапазонных объектов</span><span class="sxs-lookup"><span data-stu-id="bdf97-138">Implementing Band Objects</span></span>

<span data-ttu-id="bdf97-139">Обсуждаются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="bdf97-139">The following topics are discussed.</span></span>

-   [<span data-ttu-id="bdf97-140">Основы использования объекта Band</span><span class="sxs-lookup"><span data-stu-id="bdf97-140">Band Object Basics</span></span>](#band-object-basics)
-   [<span data-ttu-id="bdf97-141">Регистрация аппаратного контроллера управления</span><span class="sxs-lookup"><span data-stu-id="bdf97-141">Band Registration</span></span>](#band-registration)
-   [<span data-ttu-id="bdf97-142">Простой пример настраиваемой панели обозревателя</span><span class="sxs-lookup"><span data-stu-id="bdf97-142">A Simple Example of a Custom Explorer Bar</span></span>](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a><span data-ttu-id="bdf97-143">Основы использования объекта Band</span><span class="sxs-lookup"><span data-stu-id="bdf97-143">Band Object Basics</span></span>

<span data-ttu-id="bdf97-144">Несмотря на то, что их можно использовать во многом в обычных окнах, объекты управления полосами являются COM-объектами, которые существуют в контейнере.</span><span class="sxs-lookup"><span data-stu-id="bdf97-144">Although they can be used much like normal windows, band objects are COM objects that exist within a container.</span></span> <span data-ttu-id="bdf97-145">Панели обозревателя содержатся в Internet Explorer, а полосы рабочего стола — в оболочке.</span><span class="sxs-lookup"><span data-stu-id="bdf97-145">Explorer Bars are contained by Internet Explorer, and desk bands are contained by the Shell.</span></span> <span data-ttu-id="bdf97-146">Хотя они выполняют различные функции, их Базовая реализация очень похожа.</span><span class="sxs-lookup"><span data-stu-id="bdf97-146">While they serve different functions, their basic implementation is very similar.</span></span> <span data-ttu-id="bdf97-147">Основное различие заключается в способе регистрации объекта Band, который, в свою очередь, управляет типом объекта и его контейнером.</span><span class="sxs-lookup"><span data-stu-id="bdf97-147">The primary difference is in how the band object is registered, which in turn controls the type of object and its container.</span></span> <span data-ttu-id="bdf97-148">В этом разделе обсуждаются аспекты реализации, общие для всех объектов полос.</span><span class="sxs-lookup"><span data-stu-id="bdf97-148">This section discusses those aspects of implementation that are common to all band objects.</span></span> <span data-ttu-id="bdf97-149">Дополнительные сведения о реализации см. [в простом примере настраиваемой панели обозревателя](#a-simple-example-of-a-custom-explorer-bar) .</span><span class="sxs-lookup"><span data-stu-id="bdf97-149">See [A Simple Example of a Custom Explorer Bar](#a-simple-example-of-a-custom-explorer-bar) for additional implementation details.</span></span>

<span data-ttu-id="bdf97-150">Помимо [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), все объекты полос должны реализовывать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bdf97-150">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), all band objects must implement the following interfaces.</span></span>

-   [<span data-ttu-id="bdf97-151">**идескбанд**</span><span class="sxs-lookup"><span data-stu-id="bdf97-151">**IDeskBand**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [<span data-ttu-id="bdf97-152">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="bdf97-152">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="bdf97-153">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="bdf97-153">**IPersistStream**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)

<span data-ttu-id="bdf97-154">Кроме регистрации идентификатора класса (CLSID), для соответствующей категории компонентов также должны быть зарегистрированы панель обозревателя и объекты полосы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="bdf97-154">In addition to registering their class identifier (CLSID), the Explorer Bar and desk band objects must also be registered for the appropriate component category.</span></span> <span data-ttu-id="bdf97-155">Регистрация категории компонента определяет тип объекта и его контейнер.</span><span class="sxs-lookup"><span data-stu-id="bdf97-155">Registering the component category determines the object type and its container.</span></span> <span data-ttu-id="bdf97-156">Полосы инструментов используют другую процедуру регистрации и не имеют идентификатора категории (CATID).</span><span class="sxs-lookup"><span data-stu-id="bdf97-156">Tool bands use a different registration procedure and do not have a category identifier (CATID).</span></span> <span data-ttu-id="bdf97-157">CATID для трех объектов с диапазоном, которые им необходимы:</span><span class="sxs-lookup"><span data-stu-id="bdf97-157">The CATIDs for the three band objects that require them are:</span></span>



| <span data-ttu-id="bdf97-158">Тип полосы</span><span class="sxs-lookup"><span data-stu-id="bdf97-158">Band Type</span></span>               | <span data-ttu-id="bdf97-159">Категории компонентов</span><span class="sxs-lookup"><span data-stu-id="bdf97-159">Component Category</span></span> |
|-------------------------|--------------------|
| <span data-ttu-id="bdf97-160">Вертикальная панель обозревателя</span><span class="sxs-lookup"><span data-stu-id="bdf97-160">Vertical Explorer Bar</span></span>   | <span data-ttu-id="bdf97-161">CATID \_ инфобанд</span><span class="sxs-lookup"><span data-stu-id="bdf97-161">CATID\_InfoBand</span></span>    |
| <span data-ttu-id="bdf97-162">Горизонтальная панель обозревателя</span><span class="sxs-lookup"><span data-stu-id="bdf97-162">Horizontal Explorer Bar</span></span> | <span data-ttu-id="bdf97-163">CATID \_ коммбанд</span><span class="sxs-lookup"><span data-stu-id="bdf97-163">CATID\_CommBand</span></span>    |
| <span data-ttu-id="bdf97-164">Настольный полос</span><span class="sxs-lookup"><span data-stu-id="bdf97-164">Desk Band</span></span>               | <span data-ttu-id="bdf97-165">CATID \_ дескбанд</span><span class="sxs-lookup"><span data-stu-id="bdf97-165">CATID\_DeskBand</span></span>    |



 

<span data-ttu-id="bdf97-166">Дополнительные сведения о регистрации объектов с полосами см. в статье [Регистрация аппаратного контроллера управления](#band-registration) .</span><span class="sxs-lookup"><span data-stu-id="bdf97-166">See [Band Registration](#band-registration) for further discussion of how to register band objects.</span></span>

<span data-ttu-id="bdf97-167">Если объект диапазона должен принимать вводимые пользователем данные, он также должна реализовывать [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span><span class="sxs-lookup"><span data-stu-id="bdf97-167">If the band object is to accept user input, it must also implement [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span></span> <span data-ttu-id="bdf97-168">Чтобы добавить элементы в контекстное меню для панели обозревателя или полос рабочего стола, объект диапазона должен экспортировать [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="bdf97-168">To add items to the shortcut menu for Explorer Bar or desk bands, the band object must export [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="bdf97-169">Панели инструментов не поддерживают контекстные меню.</span><span class="sxs-lookup"><span data-stu-id="bdf97-169">Tool bands do not support shortcut menus.</span></span>

<span data-ttu-id="bdf97-170">Поскольку объекты управления доступом реализуют дочернее окно, они также должны реализовать процедуру окна для обработки сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="bdf97-170">Because band objects implement a child window, they must also implement a window procedure to handle Windows messaging.</span></span>

<span data-ttu-id="bdf97-171">Объекты полос могут отсылать команды в контейнер через интерфейс [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) контейнера.</span><span class="sxs-lookup"><span data-stu-id="bdf97-171">Band objects can send commands to their container through the container's [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) interface.</span></span> <span data-ttu-id="bdf97-172">Чтобы получить указатель интерфейса, вызовите метод [**иинпутобжектсите:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) контейнера и запросите IID \_ IOleCommandTarget.</span><span class="sxs-lookup"><span data-stu-id="bdf97-172">To obtain the interface pointer, call the container's [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method and ask for IID\_IOleCommandTarget.</span></span> <span data-ttu-id="bdf97-173">Затем вы отправляете команды в контейнер с помощью [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span><span class="sxs-lookup"><span data-stu-id="bdf97-173">You then send commands to the container with [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span></span> <span data-ttu-id="bdf97-174">Группа команд — КГИД \_ дескбанд.</span><span class="sxs-lookup"><span data-stu-id="bdf97-174">The command group is CGID\_DeskBand.</span></span> <span data-ttu-id="bdf97-175">При вызове метода [**идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) объекта Band контейнер использует параметр *двбандид* , чтобы назначить объект диапазона идентификатор, который используется для трех команд.</span><span class="sxs-lookup"><span data-stu-id="bdf97-175">When a band object's [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) method is called, the container uses the *dwBandID* parameter to assign the band object an identifier that is used for three of the commands.</span></span> <span data-ttu-id="bdf97-176">Поддерживаются четыре идентификатора команды **IOleCommandTarget:: Exec** .</span><span class="sxs-lookup"><span data-stu-id="bdf97-176">Four **IOleCommandTarget::Exec** command IDs are supported.</span></span>

-   <span data-ttu-id="bdf97-177">DBID \_ бандинфочанжед</span><span class="sxs-lookup"><span data-stu-id="bdf97-177">DBID\_BANDINFOCHANGED</span></span>

    <span data-ttu-id="bdf97-178">Сведения о полосе изменились.</span><span class="sxs-lookup"><span data-stu-id="bdf97-178">The band's information has changed.</span></span> <span data-ttu-id="bdf97-179">Задайте для параметра *пваин* идентификатор диапазона, полученный в последнем вызове [**Идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="bdf97-179">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="bdf97-180">Контейнер будет вызывать метод **идескбанд:: жетбандинфо** объекта Band для запроса обновленной информации.</span><span class="sxs-lookup"><span data-stu-id="bdf97-180">The container will call the band object's **IDeskBand::GetBandInfo** method to request the updated information.</span></span>

-   <span data-ttu-id="bdf97-181">DBID \_ максимизебанд</span><span class="sxs-lookup"><span data-stu-id="bdf97-181">DBID\_MAXIMIZEBAND</span></span>

    <span data-ttu-id="bdf97-182">Разверните полосу.</span><span class="sxs-lookup"><span data-stu-id="bdf97-182">Maximize the band.</span></span> <span data-ttu-id="bdf97-183">Задайте для параметра *пваин* идентификатор диапазона, полученный в последнем вызове [**Идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="bdf97-183">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span>

-   <span data-ttu-id="bdf97-184">DBID \_ шовонли</span><span class="sxs-lookup"><span data-stu-id="bdf97-184">DBID\_SHOWONLY</span></span>

    <span data-ttu-id="bdf97-185">Включите или отключите другие полосы в контейнере.</span><span class="sxs-lookup"><span data-stu-id="bdf97-185">Turn other bands in the container on or off.</span></span> <span data-ttu-id="bdf97-186">Задайте для параметра *пваин* \_ Тип VT Unknown с одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bdf97-186">Set the *pvaIn* parameter to the VT\_UNKNOWN type with one of the following values:</span></span>

    

    | <span data-ttu-id="bdf97-187">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf97-187">Value</span></span> | <span data-ttu-id="bdf97-188">Описание</span><span class="sxs-lookup"><span data-stu-id="bdf97-188">Description</span></span>                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="bdf97-189">pUnk</span><span class="sxs-lookup"><span data-stu-id="bdf97-189">pUnk</span></span>  | <span data-ttu-id="bdf97-190">Указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) объекта полосы.</span><span class="sxs-lookup"><span data-stu-id="bdf97-190">A pointer to the band object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bdf97-191">Все остальные полосы рабочего стола будут скрыты.</span><span class="sxs-lookup"><span data-stu-id="bdf97-191">All other desk bands will be hidden.</span></span> |
    | <span data-ttu-id="bdf97-192">0</span><span class="sxs-lookup"><span data-stu-id="bdf97-192">0</span></span>     | <span data-ttu-id="bdf97-193">Скрыть все полосы настольных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="bdf97-193">Hide all desk bands.</span></span>                                                                                        |
    | <span data-ttu-id="bdf97-194">1</span><span class="sxs-lookup"><span data-stu-id="bdf97-194">1</span></span>     | <span data-ttu-id="bdf97-195">Отображение всех полос настольных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="bdf97-195">Show all desk bands.</span></span>                                                                                        |

    

     

-   <span data-ttu-id="bdf97-196">DBID \_ пушчеврон</span><span class="sxs-lookup"><span data-stu-id="bdf97-196">DBID\_PUSHCHEVRON</span></span>

    <span data-ttu-id="bdf97-197">[Версия 5](versions.md).</span><span class="sxs-lookup"><span data-stu-id="bdf97-197">[Version 5](versions.md).</span></span> <span data-ttu-id="bdf97-198">Отображение шевронного меню.</span><span class="sxs-lookup"><span data-stu-id="bdf97-198">Display a chevron menu.</span></span> <span data-ttu-id="bdf97-199">Контейнер отправляет сообщение [**\_ пушчеврон RB**](../controls/rb-pushchevron.md) , а объект Band получает уведомление [ \_ чевронпушед РБН](../controls/rbn-chevronpushed.md) , которое выводит запрос на отображение углового меню.</span><span class="sxs-lookup"><span data-stu-id="bdf97-199">The container sends an [**RB\_PUSHCHEVRON**](../controls/rb-pushchevron.md) message, and the band object receives an [RBN\_CHEVRONPUSHED](../controls/rbn-chevronpushed.md) notification that prompts it to display the chevron menu.</span></span> <span data-ttu-id="bdf97-200">Задайте для параметра *нкмдексекопт* метода [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) идентификатор диапазона, полученный в последнем вызове [**идескбанд:: жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="bdf97-200">Set the [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) method's *nCmdExecOpt* parameter to the band identifier received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="bdf97-201">Установите параметр *пваин* метода **IOleCommandTarget:: Exec** в \_ Тип VT I4 с определенным приложением значением.</span><span class="sxs-lookup"><span data-stu-id="bdf97-201">Set the **IOleCommandTarget::Exec** method's *pvaIn* parameter to the VT\_I4 type with an application-defined value.</span></span> <span data-ttu-id="bdf97-202">Он передается обратно объекту Band в качестве значения *лаппвалуе* \_ уведомления чевронпушед РБН.</span><span class="sxs-lookup"><span data-stu-id="bdf97-202">It passes back to the band object as the *lAppValue* value of the RBN\_CHEVRONPUSHED notification.</span></span>

### <a name="band-registration"></a><span data-ttu-id="bdf97-203">Регистрация аппаратного контроллера управления</span><span class="sxs-lookup"><span data-stu-id="bdf97-203">Band Registration</span></span>

<span data-ttu-id="bdf97-204">Объект диапазона должен быть зарегистрирован как внутрипроцессный сервер OLE, поддерживающий потоковое подразделение.</span><span class="sxs-lookup"><span data-stu-id="bdf97-204">A band object must be registered as an OLE in-process server that supports apartment threading.</span></span> <span data-ttu-id="bdf97-205">Значением по умолчанию для сервера является текстовая строка меню.</span><span class="sxs-lookup"><span data-stu-id="bdf97-205">The default value for the server is a menu text string.</span></span> <span data-ttu-id="bdf97-206">Для панелей обозревателя он будет отображаться в подменю **панели обозревателя** в меню **вид** Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bdf97-206">For Explorer Bars, it will appear in the **Explorer Bar** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="bdf97-207">Для панелей инструментов она появится в подменю **панели** элементов меню **вид** Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bdf97-207">For tool bands, it will appear in the **Toolbars** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="bdf97-208">Для полос рабочего стола она появится в подменю **панели инструментов** контекстного меню панели задач.</span><span class="sxs-lookup"><span data-stu-id="bdf97-208">For desk bands, it will appear in the **Toolbars** submenu of the taskbar's shortcut menu.</span></span> <span data-ttu-id="bdf97-209">Как и в случае с ресурсами меню, размещение амперсанда (&) перед буквой приведет к его подчеркиванием и включению сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="bdf97-209">As with menu resources, placing an ampersand (&) in front of a letter will cause it to be underlined and enable keyboard shortcuts.</span></span> <span data-ttu-id="bdf97-210">Например, строка меню вертикальной панели обозревателя, показанной на первом рисунке, — «пример &вертикальной панели обозревателя».</span><span class="sxs-lookup"><span data-stu-id="bdf97-210">For example, the menu string for the vertical Explorer Bar shown in the first graphic is "Sample &Vertical Explorer Bar".</span></span>

<span data-ttu-id="bdf97-211">Изначально Internet Explorer получает перечисление зарегистрированных объектов панели обозревателя из реестра с помощью категорий компонентов.</span><span class="sxs-lookup"><span data-stu-id="bdf97-211">Initially, Internet Explorer retrieves an enumeration of the registered Explorer Bar objects from the registry using the component categories.</span></span> <span data-ttu-id="bdf97-212">Чтобы повысить производительность, он кэширует это перечисление, представляя впоследствии добавленные панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-212">To increase performance, it then caches this enumeration, causing subsequently added Explorer Bars to be overlooked.</span></span> <span data-ttu-id="bdf97-213">Чтобы заставить Windows Internet Explorer перестроить кэш и распознавать новую панель обозревателя, при регистрации новой панели обозревателя удалите следующие разделы реестра:</span><span class="sxs-lookup"><span data-stu-id="bdf97-213">To force Windows Internet Explorer to rebuild the cache and recognize a new Explorer Bar, delete the following registry keys during the registration of the new Explorer Bar:</span></span>

<span data-ttu-id="bdf97-214">**HKey \_ Текущее \_ пользовательское** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Explorer невозможная \\  \\  \\ Категория компонентов **настройок** \\  \\ **{00021493-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="bdf97-214">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021493-0000-0000-C000-000000000046}**\\**Enum**</span></span>

<span data-ttu-id="bdf97-215">**HKey \_ Текущее \_ пользовательское** \\ **программное обеспечение** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Explorer невозможная \\  \\  \\ Категория компонентов **настройок** \\  \\ **{00021494-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="bdf97-215">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021494-0000-0000-C000-000000000046}**\\**Enum**</span></span>

> [!Note]  
> <span data-ttu-id="bdf97-216">Так как для каждого пользователя создается кэш панели обозревателя, приложению установки может потребоваться перечислить все кусты реестра пользователя или добавить заглушку для каждого пользователя, которая будет запускаться при первом входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="bdf97-216">Because an Explorer Bar cache is created for each user, your setup application may need to enumerate all the user registry hives or add a per-user stub to run when the user first logs on.</span></span>

 

<span data-ttu-id="bdf97-217">Как правило, основная запись реестра для объекта диапазона будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bdf97-217">In general, the basic registry entry for a band object will appear as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

<span data-ttu-id="bdf97-218">Для панелей инструментов также должен быть зарегистрирован CLSID своего объекта в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bdf97-218">Tool bands must also have their object's CLSID registered with Internet Explorer.</span></span> <span data-ttu-id="bdf97-219">Для этого присвойте значение в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **панель инструментов** с идентификатором CLSID объекта панели инструментов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="bdf97-219">To do this, assign a value under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Toolbar** named with the tool band object's CLSID GUID as shown here.</span></span> <span data-ttu-id="bdf97-220">Его значение данных игнорируется, поэтому тип значения не важен.</span><span class="sxs-lookup"><span data-stu-id="bdf97-220">Its data value is ignored, so the value type is unimportant.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

<span data-ttu-id="bdf97-221">В реестр также можно добавить несколько необязательных значений.</span><span class="sxs-lookup"><span data-stu-id="bdf97-221">There are several optional values that can also be added to the registry.</span></span> <span data-ttu-id="bdf97-222">Например, следующее значение необходимо, если вы хотите использовать панель обозревателя для отображения HTML. отображаемое значение не является примером, а действительное значение, которое следует использовать.</span><span class="sxs-lookup"><span data-stu-id="bdf97-222">For instance, the following value is necessary if you want to use the Explorer Bar to display HTML The value shown is not an example, but the actual value that should be used.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

<span data-ttu-id="bdf97-223">Если вы хотите использовать панель обозревателя для отображения HTML, в сочетании с указанным выше значением также необходимо следующее необязательное значение.</span><span class="sxs-lookup"><span data-stu-id="bdf97-223">Used in conjunction with the value shown above, the following optional value is also necessary if you want to use the Explorer Bar to display HTML.</span></span> <span data-ttu-id="bdf97-224">Это значение должно быть установлено в расположение файла, содержащего HTML-содержимое для панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-224">This value should be set to the location of the file that contains the HTML content for the Explorer Bar.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

<span data-ttu-id="bdf97-225">Еще одно необязательное значение определяет ширину или высоту панели обозревателя по умолчанию в зависимости от того, является ли она вертикальной или горизонтальной, соответственно.</span><span class="sxs-lookup"><span data-stu-id="bdf97-225">Another optional value defines the default width or height of the Explorer Bar, depending on whether it is vertical or horizontal, respectively.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

<span data-ttu-id="bdf97-226">Для значения Барсизе должно быть задано значение Width или Height линейки.</span><span class="sxs-lookup"><span data-stu-id="bdf97-226">The BarSize value should be set to the width or height of the bar.</span></span> <span data-ttu-id="bdf97-227">Для этого значения требуется восемь байт и оно помещается в реестр как двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="bdf97-227">The value requires eight bytes and is placed in the registry as a binary value.</span></span> <span data-ttu-id="bdf97-228">Первые четыре байта задают размер в пикселях в шестнадцатеричном формате, начиная с крайнего левого байта.</span><span class="sxs-lookup"><span data-stu-id="bdf97-228">The first four bytes specify the size in pixels, in hexadecimal format, starting from the leftmost byte.</span></span> <span data-ttu-id="bdf97-229">Последние четыре байта зарезервированы и должны быть равны нулю.</span><span class="sxs-lookup"><span data-stu-id="bdf97-229">The last four bytes are reserved and should be set to zero.</span></span>

<span data-ttu-id="bdf97-230">Например, здесь показаны полные записи реестра для панели обозревателя с поддержкой HTML с шириной по умолчанию 291 (0x123) пикселей.</span><span class="sxs-lookup"><span data-stu-id="bdf97-230">As an example, the full registry entries for an HTML-capable Explorer Bar with a default width of 291 (0x123) pixels are shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

<span data-ttu-id="bdf97-231">Регистрацию идентификатора CATID объекта диапазона можно выполнять программным способом.</span><span class="sxs-lookup"><span data-stu-id="bdf97-231">You can handle registration of a band object's CATID programmatically.</span></span> <span data-ttu-id="bdf97-232">Создайте объект диспетчера категорий компонентов (CLSID \_ стдкомпоненткатегориесмгр) и запросите указатель на его интерфейс [**икатрегистер**](/windows/win32/api/comcat/nn-comcat-icatregister) .</span><span class="sxs-lookup"><span data-stu-id="bdf97-232">Create a component categories manager object (CLSID\_StdComponentCategoriesMgr) and request a pointer to its [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) interface.</span></span> <span data-ttu-id="bdf97-233">Передайте идентификаторы CLSID и CATID объекта полоси в [**икатрегистер:: регистерклассимплкатегориес**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span><span class="sxs-lookup"><span data-stu-id="bdf97-233">Pass the band object's CLSID and CATID to [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span></span>

### <a name="a-simple-example-of-a-custom-explorer-bar"></a><span data-ttu-id="bdf97-234">Простой пример настраиваемой панели обозревателя</span><span class="sxs-lookup"><span data-stu-id="bdf97-234">A Simple Example of a Custom Explorer Bar</span></span>

<span data-ttu-id="bdf97-235">В этом примере рассматривается реализация образца вертикальной панели обозревателя, показанного в введении.</span><span class="sxs-lookup"><span data-stu-id="bdf97-235">This example goes through the implementation of the sample vertical Explorer Bar shown in the introduction.</span></span>

<span data-ttu-id="bdf97-236">Ниже приведена базовая процедура создания пользовательской панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-236">The basic procedure for creating a custom Explorer Bar is as follows.</span></span>

1.  <span data-ttu-id="bdf97-237">[Реализуйте функции, необходимые для библиотеки DLL](#dll-functions).</span><span class="sxs-lookup"><span data-stu-id="bdf97-237">[Implement the functions needed by the DLL](#dll-functions).</span></span>
2.  [<span data-ttu-id="bdf97-238">Реализуйте необходимые COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bdf97-238">Implement the required COM interfaces.</span></span>](#required-interface-implementations)
3.  [<span data-ttu-id="bdf97-239">Реализуйте все требуемые необязательные COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bdf97-239">Implement any desired optional COM interfaces.</span></span>](#optional-interface-implementations)
4.  [<span data-ttu-id="bdf97-240">Зарегистрируйте CLSID объекта и, если необходимо, категорию компонента.</span><span class="sxs-lookup"><span data-stu-id="bdf97-240">Register the object's CLSID and, if required, component category.</span></span>](#clsid-registration)
5.  <span data-ttu-id="bdf97-241">Создайте дочернее окно Internet Explorer, чтобы оно соответствовало области отображаемой панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-241">Create a child window of Internet Explorer, sized to fit the Explorer Bar's display region.</span></span>
6.  [<span data-ttu-id="bdf97-242">Используйте дочернее окно для вывода сведений и взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="bdf97-242">Use the child window to display information and interact with the user.</span></span>](#the-window-procedure)

<span data-ttu-id="bdf97-243">Очень простая реализация, используемая в образце панели обозревателя, может фактически использоваться для любого типа панели обозревателя или полосы рабочего стола, просто зарегистрировав ее для соответствующей категории компонента.</span><span class="sxs-lookup"><span data-stu-id="bdf97-243">The very simple implementation used in the Explorer Bar sample could actually be used for either type of Explorer Bar, or a desk band, by simply registering it for the appropriate component category.</span></span> <span data-ttu-id="bdf97-244">Более сложные реализации необходимо настроить для области вывода и контейнера каждого типа объекта.</span><span class="sxs-lookup"><span data-stu-id="bdf97-244">More sophisticated implementations will need to be customized for each object type's display region and container.</span></span> <span data-ttu-id="bdf97-245">Однако большую часть этой настройки можно добиться, приняв пример кода и расширив его, применив привычные методики программирования Windows к дочернему окну.</span><span class="sxs-lookup"><span data-stu-id="bdf97-245">However, much of this customization can be accomplished by taking the sample code and extending it by applying familiar Windows programming techniques to the child window.</span></span> <span data-ttu-id="bdf97-246">Например, можно добавить элементы управления для взаимодействия с пользователем или графики для более насыщенного экрана.</span><span class="sxs-lookup"><span data-stu-id="bdf97-246">For example, you can add controls for user interaction, or graphics for a richer display.</span></span>

### <a name="dll-functions"></a><span data-ttu-id="bdf97-247">Функции DLL</span><span class="sxs-lookup"><span data-stu-id="bdf97-247">DLL Functions</span></span>

<span data-ttu-id="bdf97-248">Все три объекта упаковываются в одну библиотеку DLL, которая предоставляет следующие функции.</span><span class="sxs-lookup"><span data-stu-id="bdf97-248">All three objects are packaged in a single DLL, which exposes the following functions.</span></span>

-   [<span data-ttu-id="bdf97-249">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="bdf97-249">**DllMain**</span></span>](../dlls/dllmain.md)
-   [<span data-ttu-id="bdf97-250">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="bdf97-250">**DllCanUnloadNow**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [<span data-ttu-id="bdf97-251">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="bdf97-251">**DllGetClassObject**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [<span data-ttu-id="bdf97-252">**Регистрация**</span><span class="sxs-lookup"><span data-stu-id="bdf97-252">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

<span data-ttu-id="bdf97-253">Первые три функции — это стандартные реализации, которые не будут обсуждаться здесь.</span><span class="sxs-lookup"><span data-stu-id="bdf97-253">The first three functions are standard implementations and will not be discussed here.</span></span> <span data-ttu-id="bdf97-254">Реализация фабрики класса также является стандартной.</span><span class="sxs-lookup"><span data-stu-id="bdf97-254">The Class Factory implementation is also standard.</span></span>

### <a name="required-interface-implementations"></a><span data-ttu-id="bdf97-255">Требуемые реализации интерфейса</span><span class="sxs-lookup"><span data-stu-id="bdf97-255">Required Interface Implementations</span></span>

<span data-ttu-id="bdf97-256">В вертикальном образце панели обозревателя реализованы четыре необходимых интерфейса: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)и [**идескбанд**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) в составе класса цексплорербар.</span><span class="sxs-lookup"><span data-stu-id="bdf97-256">The vertical Explorer Bar sample implements the four required interfaces: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream), and [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) as part of the CExplorerBar class.</span></span> <span data-ttu-id="bdf97-257">Реализации конструктора, деструктора и **IUnknown** являются простыми и не обсуждаются здесь.</span><span class="sxs-lookup"><span data-stu-id="bdf97-257">The constructor, destructor, and **IUnknown** implementations are straightforward, and will not be discussed here.</span></span> <span data-ttu-id="bdf97-258">Подробности см. в примере кода.</span><span class="sxs-lookup"><span data-stu-id="bdf97-258">See the sample code for details.</span></span>

<span data-ttu-id="bdf97-259">Подробно рассматриваются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bdf97-259">The following interfaces are discussed in detail.</span></span>

-   [<span data-ttu-id="bdf97-260">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="bdf97-260">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="bdf97-261">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="bdf97-261">IPersistStream</span></span>](#ipersiststream)
-   [<span data-ttu-id="bdf97-262">идескбанд</span><span class="sxs-lookup"><span data-stu-id="bdf97-262">IDeskBand</span></span>](#ideskband)

### <a name="iobjectwithsite"></a><span data-ttu-id="bdf97-263">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="bdf97-263">IObjectWithSite</span></span>

<span data-ttu-id="bdf97-264">Когда пользователь выбирает панель обозревателя, контейнер вызывает метод [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) соответствующего объекта полосы.</span><span class="sxs-lookup"><span data-stu-id="bdf97-264">When the user selects an Explorer Bar, the container calls the corresponding band object's [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) method.</span></span> <span data-ttu-id="bdf97-265">Для параметра *пунксите* будет задан указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) сайта.</span><span class="sxs-lookup"><span data-stu-id="bdf97-265">The *punkSite* parameter will be set to the site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="bdf97-266">Как правило, реализация [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) должна выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bdf97-266">In general, a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) implementation should perform the following steps:</span></span>

1.  <span data-ttu-id="bdf97-267">Освобождение любого указателя на сайт, который в данный момент удерживается.</span><span class="sxs-lookup"><span data-stu-id="bdf97-267">Release any site pointer that is currently being held.</span></span>
2.  <span data-ttu-id="bdf97-268">Если указатель, переданный в [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) , имеет значение **null**, полоса удаляется.</span><span class="sxs-lookup"><span data-stu-id="bdf97-268">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is set to **NULL**, the band is being removed.</span></span> <span data-ttu-id="bdf97-269">**SetSite** может вернуть S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bdf97-269">**SetSite** can return S\_OK.</span></span>
3.  <span data-ttu-id="bdf97-270">Если указатель, переданный в [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) , имеет **значение**, отличное от NULL, устанавливается новый сайт.</span><span class="sxs-lookup"><span data-stu-id="bdf97-270">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is non-**NULL**, a new site is being set.</span></span> <span data-ttu-id="bdf97-271">**SetSite** должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bdf97-271">**SetSite** should do the following:</span></span>
    1.  <span data-ttu-id="bdf97-272">Вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на сайте для своего интерфейса [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .</span><span class="sxs-lookup"><span data-stu-id="bdf97-272">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) interface.</span></span>
    2.  <span data-ttu-id="bdf97-273">Вызовите [**иолевиндов:: Onwindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) , чтобы получить маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="bdf97-273">Call [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) to obtain the parent window's handle.</span></span> <span data-ttu-id="bdf97-274">Сохраните маркер для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="bdf97-274">Save the handle for later use.</span></span> <span data-ttu-id="bdf97-275">Выпустите [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="bdf97-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) if it is no longer needed.</span></span>
    3.  <span data-ttu-id="bdf97-276">Создайте окно объекта полоси в качестве дочернего элемента окна, полученного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="bdf97-276">Create the band object's window as a child of the window obtained in the previous step.</span></span> <span data-ttu-id="bdf97-277">Не создавайте его как видимое окно.</span><span class="sxs-lookup"><span data-stu-id="bdf97-277">Do not create it as a visible window.</span></span>
    4.  <span data-ttu-id="bdf97-278">Если объект Band реализует [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на сайте для своего интерфейса [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) .</span><span class="sxs-lookup"><span data-stu-id="bdf97-278">If the band object implements [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) interface.</span></span> <span data-ttu-id="bdf97-279">Сохранить указатель на этот интерфейс для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="bdf97-279">Store the pointer to this interface for use later.</span></span>
    5.  <span data-ttu-id="bdf97-280">Если все шаги выполнены успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bdf97-280">If all steps are successful, return S\_OK.</span></span> <span data-ttu-id="bdf97-281">В противном случае возвращается код ошибки, определенный OLE, указывающий на сбой.</span><span class="sxs-lookup"><span data-stu-id="bdf97-281">If not, return the OLE-defined error code indicating what failed.</span></span>

<span data-ttu-id="bdf97-282">Образец панели обозревателя реализует [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bdf97-282">The Explorer Bar sample implements [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in the following way.</span></span> <span data-ttu-id="bdf97-283">В следующем коде *m \_ псите* является закрытой переменной-членом, содержащей указатель [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) , а *m \_ хвндпарент* содержит маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="bdf97-283">In the following code *m\_pSite* is a private member variable that holds the [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) pointer and *m\_hwndParent* holds the parent window's handle.</span></span> <span data-ttu-id="bdf97-284">В этом примере также обрабатывается создание окна.</span><span class="sxs-lookup"><span data-stu-id="bdf97-284">In this sample, window creation is also handled.</span></span> <span data-ttu-id="bdf97-285">Если окно не существует, этот метод создает окно панели обозревателя как дочерний элемент соответствующего размера родительского окна, полученного с помощью **SetSite**.</span><span class="sxs-lookup"><span data-stu-id="bdf97-285">If the window does not exist, this method creates the Explorer Bar's window as an appropriately sized child of the parent window obtained by **SetSite**.</span></span> <span data-ttu-id="bdf97-286">Дескриптор дочернего окна хранится в *\_ дескрипторе m*.</span><span class="sxs-lookup"><span data-stu-id="bdf97-286">The child window's handle is stored in *m\_hwnd*.</span></span>


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



<span data-ttu-id="bdf97-287">[**Реализация SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) в примере просто заключает вызов метода [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) сайта, используя указатель сайта, сохраненный с помощью [](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span><span class="sxs-lookup"><span data-stu-id="bdf97-287">The sample's [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) implementation simply wraps a call to the site's [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, using the site pointer saved by [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a><span data-ttu-id="bdf97-288">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="bdf97-288">IPersistStream</span></span>

<span data-ttu-id="bdf97-289">Internet Explorer будет вызывать интерфейс [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) панели обозревателя, чтобы позволить панели обозревателя загружать или сохранять постоянные данные.</span><span class="sxs-lookup"><span data-stu-id="bdf97-289">Internet Explorer will call the Explorer Bar's [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to allow the Explorer Bar to load or save persistent data.</span></span> <span data-ttu-id="bdf97-290">Если постоянные данные отсутствуют, методы должны по-прежнему возвращать код успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="bdf97-290">If there is no persistent data, the methods must still return a success code.</span></span> <span data-ttu-id="bdf97-291">Интерфейс **IPersistStream** наследует от [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), поэтому необходимо реализовать пять методов.</span><span class="sxs-lookup"><span data-stu-id="bdf97-291">The **IPersistStream** interface inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), so five methods must be implemented.</span></span>

-   [<span data-ttu-id="bdf97-292">**IPersist::, ClassID**</span><span class="sxs-lookup"><span data-stu-id="bdf97-292">**IPersist::GetClassID**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [<span data-ttu-id="bdf97-293">**IPersistStream:: IsDirty**</span><span class="sxs-lookup"><span data-stu-id="bdf97-293">**IPersistStream::IsDirty**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [<span data-ttu-id="bdf97-294">**IPersistStream:: Load**</span><span class="sxs-lookup"><span data-stu-id="bdf97-294">**IPersistStream::Load**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [<span data-ttu-id="bdf97-295">**IPersistStream:: Save**</span><span class="sxs-lookup"><span data-stu-id="bdf97-295">**IPersistStream::Save**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [<span data-ttu-id="bdf97-296">**IPersistStream:: Жетсиземакс**</span><span class="sxs-lookup"><span data-stu-id="bdf97-296">**IPersistStream::GetSizeMax**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

<span data-ttu-id="bdf97-297">Образец панели обозревателя не использует постоянные данные и имеет только минимальную реализацию [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="bdf97-297">The Explorer Bar sample does not use any persistent data and has only a minimal implementation of [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="bdf97-298">[**IPersist::**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) GETOBJECT Возвращает CLSID объекта (CLSID \_ сампликсплорербар), а остаток возвращает либо s \_ ОК, либо \_ false, либо E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="bdf97-298">[**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) returns the object's CLSID (CLSID\_SampleExplorerBar), and the remainder return either S\_OK, S\_FALSE, or E\_NOTIMPL.</span></span>

### <a name="ideskband"></a><span data-ttu-id="bdf97-299">идескбанд</span><span class="sxs-lookup"><span data-stu-id="bdf97-299">IDeskBand</span></span>

<span data-ttu-id="bdf97-300">Интерфейс [**идескбанд**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) относится к объектам диапазона.</span><span class="sxs-lookup"><span data-stu-id="bdf97-300">The [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) interface is specific to band objects.</span></span> <span data-ttu-id="bdf97-301">В дополнение к одному методу он наследует от [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), который, в свою очередь, наследует от [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span><span class="sxs-lookup"><span data-stu-id="bdf97-301">In addition to its one method, it inherits from [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), which in turn inherits from [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span></span>

<span data-ttu-id="bdf97-302">Существует два метода [**иолевиндов**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) [**: и**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) [**иолевиндов:: контекстсенситивехелп**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span><span class="sxs-lookup"><span data-stu-id="bdf97-302">There are two [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) methods: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) and [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span></span> <span data-ttu-id="bdf97-303">Реализация метода **Window** в образце панели обозревателя возвращает его дескриптор дочернего окна, m и *\_ HWND*.</span><span class="sxs-lookup"><span data-stu-id="bdf97-303">The Explorer Bar sample's implementation of **GetWindow** returns the Explorer Bar's child window handle, *m\_hwnd*.</span></span> <span data-ttu-id="bdf97-304">Контекстно-зависимая справка не реализована, поэтому **контекстсенситивехелп** возвращает **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="bdf97-304">Context-sensitive Help is not implemented, so **ContextSensitiveHelp** returns **E\_NOTIMPL**.</span></span>

<span data-ttu-id="bdf97-305">Интерфейс [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) имеет три метода.</span><span class="sxs-lookup"><span data-stu-id="bdf97-305">The [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface has three methods.</span></span>

-   [<span data-ttu-id="bdf97-306">**Идоккингвиндов:: Шовдв**</span><span class="sxs-lookup"><span data-stu-id="bdf97-306">**IDockingWindow::ShowDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [<span data-ttu-id="bdf97-307">**Идоккингвиндов:: Клоседв**</span><span class="sxs-lookup"><span data-stu-id="bdf97-307">**IDockingWindow::CloseDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [<span data-ttu-id="bdf97-308">**Идоккингвиндов:: Ресизебордердв**</span><span class="sxs-lookup"><span data-stu-id="bdf97-308">**IDockingWindow::ResizeBorderDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

<span data-ttu-id="bdf97-309">Метод [**ресизебордердв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) не используется с каким-либо типом объекта Band и всегда должен возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="bdf97-309">The [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) method is not used with any type of band object and should always return E\_NOTIMPL.</span></span> <span data-ttu-id="bdf97-310">Метод [**шовдв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) либо показывает, либо скрывает окно панели обозревателя в зависимости от значения его параметра.</span><span class="sxs-lookup"><span data-stu-id="bdf97-310">The [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) method either shows or hides the Explorer Bar's window, depending on the value of its parameter.</span></span>


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



<span data-ttu-id="bdf97-311">Метод [**клоседв**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) уничтожает окно панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-311">The [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) method destroys the Explorer Bar's window.</span></span>


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



<span data-ttu-id="bdf97-312">Оставшийся метод, [**жетбандинфо**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), относится к **идескбанд**.</span><span class="sxs-lookup"><span data-stu-id="bdf97-312">The remaining method, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), is specific to **IDeskBand**.</span></span> <span data-ttu-id="bdf97-313">Internet Explorer использует его для указания идентификатора и режима просмотра панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-313">Internet Explorer uses it to specify the Explorer Bar's identifier and viewing mode.</span></span> <span data-ttu-id="bdf97-314">Internet Explorer также может запросить один или несколько фрагментов информации из панели обозревателя, заполнив элемент **двмаск** структуры [**дескбандинфо**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) , которая передается в качестве третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="bdf97-314">Internet Explorer also may request one or more pieces of information from the Explorer Bar by filling the **dwMask** member of the [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) structure that is passed as the third parameter.</span></span> <span data-ttu-id="bdf97-315">**Жетбандинфо** должен хранить идентификатор и режим просмотра и заполнить структуру **дескбандинфо** запрошенными данными.</span><span class="sxs-lookup"><span data-stu-id="bdf97-315">**GetBandInfo** should store the identifier and viewing mode and fill the **DESKBANDINFO** structure with the requested data.</span></span> <span data-ttu-id="bdf97-316">Образец панели обозревателя реализует **жетбандинфо** , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="bdf97-316">The Explorer Bar sample implements **GetBandInfo** as shown in the following code example.</span></span>


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a><span data-ttu-id="bdf97-317">Необязательные реализации интерфейса</span><span class="sxs-lookup"><span data-stu-id="bdf97-317">Optional Interface Implementations</span></span>

<span data-ttu-id="bdf97-318">Существует два необязательных интерфейса, но это может быть полезно для реализации: [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) и [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="bdf97-318">There are two interfaces that are not required, but that may be useful to implement: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="bdf97-319">Образец панели обозревателя реализует **иинпутобжект**.</span><span class="sxs-lookup"><span data-stu-id="bdf97-319">The Explorer Bar sample implements **IInputObject**.</span></span> <span data-ttu-id="bdf97-320">Сведения о том, как реализовать **IContextMenu**, см. в документации.</span><span class="sxs-lookup"><span data-stu-id="bdf97-320">Refer to the documentation for information on how to implement **IContextMenu**.</span></span>

### <a name="iinputobject"></a><span data-ttu-id="bdf97-321">иинпутобжект</span><span class="sxs-lookup"><span data-stu-id="bdf97-321">IInputObject</span></span>

<span data-ttu-id="bdf97-322">Интерфейс [**иинпутобжект**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) должен быть реализован, если объект диапазона принимает вводимые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="bdf97-322">The [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) interface must be implemented if a band object accepts user input.</span></span> <span data-ttu-id="bdf97-323">Internet Explorer реализует [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) и использует **иинпутобжект** для поддержания соответствующего фокуса ввода пользователя, если он содержит несколько окон, содержащихся в них.</span><span class="sxs-lookup"><span data-stu-id="bdf97-323">Internet Explorer implements [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) and uses **IInputObject** to maintain proper user input focus when it has more than one contained window.</span></span> <span data-ttu-id="bdf97-324">Панель обозревателя должна реализовывать три метода.</span><span class="sxs-lookup"><span data-stu-id="bdf97-324">There are three methods that need to be implemented by an Explorer Bar.</span></span>

-   [<span data-ttu-id="bdf97-325">**Иинпутобжект:: Уиактиватеио**</span><span class="sxs-lookup"><span data-stu-id="bdf97-325">**IInputObject::UIActivateIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [<span data-ttu-id="bdf97-326">**Иинпутобжект:: Хасфокусио**</span><span class="sxs-lookup"><span data-stu-id="bdf97-326">**IInputObject::HasFocusIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [<span data-ttu-id="bdf97-327">**Иинпутобжект:: Транслатеакцелераторио**</span><span class="sxs-lookup"><span data-stu-id="bdf97-327">**IInputObject::TranslateAcceleratorIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

<span data-ttu-id="bdf97-328">Internet Explorer вызывает [**уиактиватеио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) , чтобы сообщить панели обозревателя о том, что она активируется или деактивируется.</span><span class="sxs-lookup"><span data-stu-id="bdf97-328">Internet Explorer calls [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) to inform the Explorer Bar that it is being activated or deactivated.</span></span> <span data-ttu-id="bdf97-329">При активации образец панели обозревателя вызывает [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) , чтобы установить фокус на окно.</span><span class="sxs-lookup"><span data-stu-id="bdf97-329">When activated, the Explorer Bar sample calls [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) to set the focus to its window.</span></span>

<span data-ttu-id="bdf97-330">Internet Explorer вызывает [**хасфокусио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) , когда пытается определить, какое окно находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="bdf97-330">Internet Explorer calls [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) when it is attempting to determine which window has focus.</span></span> <span data-ttu-id="bdf97-331">Если окно панели обозревателя или один из его потомков имеет фокус, **хасфокусио** должен вернуть значение s \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bdf97-331">If the Explorer Bar's window or one of its descendants has focus, **HasFocusIO** should return S\_OK.</span></span> <span data-ttu-id="bdf97-332">В противном случае оно должно возвращать \_ значение S false.</span><span class="sxs-lookup"><span data-stu-id="bdf97-332">If not, it should return S\_FALSE.</span></span>

<span data-ttu-id="bdf97-333">[**Транслатеакцелераторио**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) позволяет объекту обрабатывать сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="bdf97-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) allows the object to process keyboard accelerators.</span></span> <span data-ttu-id="bdf97-334">Образец панели обозревателя не реализует этот метод, поэтому он возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="bdf97-334">The Explorer Bar sample does not implement this method, so it returns S\_FALSE.</span></span>

<span data-ttu-id="bdf97-335">Реализация [**иинпутобжектсите**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) в строке примера выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bdf97-335">The sample bar's implementation of [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) is as follows.</span></span>


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a><span data-ttu-id="bdf97-336">Регистрация CLSID</span><span class="sxs-lookup"><span data-stu-id="bdf97-336">CLSID Registration</span></span>

<span data-ttu-id="bdf97-337">Как и для всех COM-объектов, необходимо зарегистрировать CLSID на панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-337">As with all COM objects, the Explorer Bar's CLSID must be registered.</span></span> <span data-ttu-id="bdf97-338">Чтобы объект правильно функционировал в Internet Explorer, он также должен быть зарегистрирован для соответствующей категории компонентов (CATID \_ инфобанд).</span><span class="sxs-lookup"><span data-stu-id="bdf97-338">For the object to function properly with Internet Explorer, it must also be registered for the appropriate component category (CATID\_InfoBand).</span></span> <span data-ttu-id="bdf97-339">Соответствующий раздел кода для панели обозревателя показан в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="bdf97-339">The relevant code section for the Explorer Bar is shown in the following code example.</span></span>


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="bdf97-340">При регистрации объектов Band в образце используются обычные процедуры COM.</span><span class="sxs-lookup"><span data-stu-id="bdf97-340">Registration of band objects in the sample uses normal COM procedures.</span></span>

<span data-ttu-id="bdf97-341">Помимо идентификатора CLSID, серверный объект также должен быть зарегистрирован для одной или нескольких категорий компонентов.</span><span class="sxs-lookup"><span data-stu-id="bdf97-341">In addition to the CLSID, the band object server must also be registered for one or more component categories.</span></span> <span data-ttu-id="bdf97-342">В действительности это основное различие в реализации между вертикальными и горизонтальными образцами панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-342">This is actually the main difference in implementation between the vertical and horizontal Explorer Bar samples.</span></span> <span data-ttu-id="bdf97-343">Этот процесс обрабатывается путем создания объекта диспетчера категорий компонентов (CLSID \_ стдкомпоненткатегориесмгр) и использования метода [**икатрегистер:: регистерклассимплкатегориес**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) для регистрации сервера объектного диапазона.</span><span class="sxs-lookup"><span data-stu-id="bdf97-343">This process is handled by creating a component categories manager object (CLSID\_StdComponentCategoriesMgr) and using the [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) method to register the band object server.</span></span> <span data-ttu-id="bdf97-344">В этом примере регистрация категории компонента обрабатывается путем передачи CLSID и CATID образца панели обозревателя в закрытую функцию —**регистеркомкат**, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="bdf97-344">In this example, component category registration is handled by passing the Explorer Bar sample's CLSID and CATID to a private function—**RegisterComCat**—as shown in the following code example.</span></span>


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a><span data-ttu-id="bdf97-345">Процедура окна</span><span class="sxs-lookup"><span data-stu-id="bdf97-345">The Window Procedure</span></span>

<span data-ttu-id="bdf97-346">Поскольку объект диапазона использует дочернее окно для своего экрана, он должен реализовать процедуру окна для обработки сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="bdf97-346">Because a band object uses a child window for its display, it must implement a window procedure to handle Windows messaging.</span></span> <span data-ttu-id="bdf97-347">Образец "полоса" имеет минимальную функциональность, поэтому процедура окна обрабатывает только пять сообщений:</span><span class="sxs-lookup"><span data-stu-id="bdf97-347">The band sample has minimal functionality, so its window procedure only handles five messages:</span></span>

-   [<span data-ttu-id="bdf97-348">**WM \_ нккреате**</span><span class="sxs-lookup"><span data-stu-id="bdf97-348">**WM\_NCCREATE**</span></span>](../winmsg/wm-nccreate.md)
-   [<span data-ttu-id="bdf97-349">**WM \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="bdf97-349">**WM\_PAINT**</span></span>](../gdi/wm-paint.md)
-   [<span data-ttu-id="bdf97-350">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="bdf97-350">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)
-   [<span data-ttu-id="bdf97-351">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="bdf97-351">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)
-   [<span data-ttu-id="bdf97-352">**WM \_ киллфокус**</span><span class="sxs-lookup"><span data-stu-id="bdf97-352">**WM\_KILLFOCUS**</span></span>](../inputdev/wm-killfocus.md)

<span data-ttu-id="bdf97-353">Процедуру можно легко расширить для размещения дополнительных сообщений, чтобы обеспечить поддержку дополнительных функций.</span><span class="sxs-lookup"><span data-stu-id="bdf97-353">The procedure can easily be expanded to accommodate additional messages to support more features.</span></span>


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



<span data-ttu-id="bdf97-354">\_Обработчик команд WM просто возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="bdf97-354">The WM\_COMMAND handler simply returns zero.</span></span> <span data-ttu-id="bdf97-355">\_Обработчик рисования WM создает простой текст, отображаемый в примере на панели обозревателя во введении.</span><span class="sxs-lookup"><span data-stu-id="bdf97-355">The WM\_PAINT handler creates the simple text display shown in the Explorer Bar example in the introduction.</span></span>


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="bdf97-356">\_Обработчики WM SETFOCUS и WM \_ киллфокус уведомляют сайт об изменении фокуса, вызывая метод [**Иинпутобжектсите:: онфокусчанжеис**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) сайта.</span><span class="sxs-lookup"><span data-stu-id="bdf97-356">The WM\_SETFOCUS and WM\_KILLFOCUS handlers inform the site of a focus change by calling the site's [**IInputObjectSite::OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) method.</span></span>


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



<span data-ttu-id="bdf97-357">Объекты управления доступом обеспечивают гибкий и мощный способ расширения возможностей Internet Explorer путем создания настраиваемых панелей обозревателя.</span><span class="sxs-lookup"><span data-stu-id="bdf97-357">Band objects provide a flexible and powerful way to extend the capabilities of Internet Explorer by creating custom Explorer Bars.</span></span> <span data-ttu-id="bdf97-358">Реализация рабочего диапазона позволяет расширить возможности обычных окон.</span><span class="sxs-lookup"><span data-stu-id="bdf97-358">Implementing a desk band enables you to extend the capabilities of normal windows.</span></span> <span data-ttu-id="bdf97-359">Хотя требуется какое-то программирование COM, оно в конечном итоге предоставляет дочернее окно для пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bdf97-359">Although some COM programming is required, it ultimately serves to provide a child window for your user interface.</span></span> <span data-ttu-id="bdf97-360">В этом случае основная часть реализации может использовать привычные методы программирования Windows.</span><span class="sxs-lookup"><span data-stu-id="bdf97-360">From there, the bulk of the implementation can use familiar Windows programming techniques.</span></span> <span data-ttu-id="bdf97-361">Хотя в приведенном здесь примере используются только ограниченные функциональные возможности, он иллюстрирует все необходимые функции объекта диапазона, и его можно легко расширить для создания уникального и мощного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bdf97-361">While the example discussed here has only limited functionality, it illustrates all the necessary features of a band object and it can be readily extended to create a unique and powerful user interface.</span></span>

 

 
