---
title: Общие сведения о модели автоматизации пользовательского интерфейса
description: Microsoft UI Automation — это платформа специальных возможностей для Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Автоматизация пользовательского интерфейса, сведения
- Модель автоматизации пользовательского интерфейса, Специальные возможности
- Модель автоматизации пользовательского интерфейса, компоненты
- Модель автоматизации пользовательского интерфейса, API поставщика
- Модель автоматизации пользовательского интерфейса, клиентский API
- Автоматизация пользовательского интерфейса, файлы заголовков
- Автоматизация пользовательского интерфейса, модель
- components
- специальные возможности
- API поставщика
- API клиента
- заголовочные файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412456"
---
# <a name="ui-automation-overview"></a><span data-ttu-id="58674-115">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-115">UI Automation Overview</span></span>

<span data-ttu-id="58674-116">Microsoft UI Automation — это платформа специальных возможностей для Windows.</span><span class="sxs-lookup"><span data-stu-id="58674-116">Microsoft UI Automation is an accessibility framework for Windows.</span></span> <span data-ttu-id="58674-117">Он обеспечивает программный доступ к большинству элементов пользовательского интерфейса на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="58674-117">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="58674-118">Она позволяет продуктам с поддержкой специальных возможностей, таким как средства чтения с экрана, предоставлять сведения о пользовательском интерфейсе конечным пользователям и управлять пользовательским интерфейсом средствами, отличными от стандартных входных данных.</span><span class="sxs-lookup"><span data-stu-id="58674-118">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="58674-119">Модель автоматизации пользовательского интерфейса также позволяет скриптам автоматических тестов взаимодействовать с пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="58674-119">UI Automation also allows automated test scripts to interact with the UI.</span></span>

<span data-ttu-id="58674-120">Модель автоматизации пользовательского интерфейса была впервые доступна в Windows XP в составе Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="58674-120">UI Automation was first available in Windows XP as part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="58674-121">Хотя в этот момент также опубликован неуправляемый API C++, полезность функций клиента была ограничена из-за проблем совместимости.</span><span class="sxs-lookup"><span data-stu-id="58674-121">Although an unmanaged C++ API was also published at that time, the usefulness of client functions was limited because of interoperability issues.</span></span> <span data-ttu-id="58674-122">В Windows 7 API был переписан в объектной модели Component (COM).</span><span class="sxs-lookup"><span data-stu-id="58674-122">For Windows 7, the API has been rewritten in the Component Object Model (COM).</span></span>

> [!Note]  
> <span data-ttu-id="58674-123">Хотя функции библиотеки, представленные в предыдущей версии модели автоматизации пользовательского интерфейса, по-прежнему документированы, их не следует использовать в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="58674-123">Although the library functions introduced in the earlier version of UI Automation are still documented, they should not be used in new applications.</span></span>

 

<span data-ttu-id="58674-124">Клиентские приложения модели автоматизации пользовательского интерфейса могут быть написаны с гарантией того, что они будут работать на нескольких платформах элементов управления Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="58674-124">UI Automation client applications can be written with the assurance that they will work on multiple Microsoft Windows control frameworks.</span></span> <span data-ttu-id="58674-125">Ядро автоматизации пользовательского интерфейса маскирует все различия в платформах, которые лежат в основе различных частей пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-125">The UI Automation core masks any differences in the frameworks that underlie various pieces of the UI.</span></span> <span data-ttu-id="58674-126">Например, свойство **содержимого** кнопки Windows Presentation Foundation (WPF), свойство **Caption** кнопки Microsoft Win32 и свойство **ALT** изображения HTML сопоставлены с одним свойством, **именем** в представлении модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-126">For example, the **Content** property of a Windows Presentation Foundation (WPF) button, the **Caption** property of a Microsoft Win32 button, and the **ALT** property of an HTML image are all mapped to a single property, **Name**, in the UI Automation view.</span></span>

<span data-ttu-id="58674-127">Модель автоматизации пользовательского интерфейса обеспечивает полную функциональность Windows XP, Windows Server 2003 и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="58674-127">UI Automation provides full functionality in Windows XP, Windows Server 2003, and later operating systems.</span></span>

<span data-ttu-id="58674-128">Поставщики автоматизации пользовательского интерфейса — это компоненты, реализующие поддержку автоматизации пользовательского интерфейса для элементов управления и предлагающие некоторую поддержку клиентских приложений Microsoft Active Accessibility через встроенную службу моста.</span><span class="sxs-lookup"><span data-stu-id="58674-128">UI Automation providers are components that implement UI Automation support on controls and offer some support for Microsoft Active Accessibility client applications, through a built-in bridging service.</span></span>

> [!Note]  
> <span data-ttu-id="58674-129">Модель автоматизации пользовательского интерфейса не обеспечивает обмен данными между процессами, запущенными разными пользователями, с помощью команды **запуска от имени** .</span><span class="sxs-lookup"><span data-stu-id="58674-129">UI Automation does not enable communication between processes that are started by different users through the **Run as** command.</span></span>

 

<span data-ttu-id="58674-130">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="58674-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="58674-131">Компоненты модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-131">UI Automation Components</span></span>](#ui-automation-components)
-   [<span data-ttu-id="58674-132">Файлы заголовков модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-132">UI Automation Header Files</span></span>](#ui-automation-header-files)
-   [<span data-ttu-id="58674-133">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-133">UI Automation Model</span></span>](#ui-automation-model)
-   [<span data-ttu-id="58674-134">См. также</span><span class="sxs-lookup"><span data-stu-id="58674-134">Related topics</span></span>](#related-topics)

## <a name="ui-automation-components"></a><span data-ttu-id="58674-135">Компоненты модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-135">UI Automation Components</span></span>

<span data-ttu-id="58674-136">Модель автоматизации пользовательского интерфейса состоит из четырех основных компонентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="58674-136">UI Automation has four main components, as shown in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58674-137">Компонент</span><span class="sxs-lookup"><span data-stu-id="58674-137">Component</span></span></th>
<th><span data-ttu-id="58674-138">Описание</span><span class="sxs-lookup"><span data-stu-id="58674-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58674-139">API поставщика</span><span class="sxs-lookup"><span data-stu-id="58674-139">Provider API</span></span></td>
<td><span data-ttu-id="58674-140">Набор COM-интерфейсов, реализованных поставщиками автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-140">A set of COM interfaces that are implemented by UI Automation providers.</span></span> <span data-ttu-id="58674-141">Поставщики автоматизации пользовательского интерфейса — это объекты, предоставляющие сведения об элементах пользовательского интерфейса и реагирующие на программный ввод.</span><span class="sxs-lookup"><span data-stu-id="58674-141">UI Automation providers are objects that provide information about UI elements and respond to programmatic input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58674-142">API клиента</span><span class="sxs-lookup"><span data-stu-id="58674-142">Client API</span></span></td>
<td><span data-ttu-id="58674-143">Набор COM-интерфейсов, которые позволяют клиентским приложениям получать сведения о пользовательском интерфейсе и передавать входные данные в элементы управления.</span><span class="sxs-lookup"><span data-stu-id="58674-143">A set of COM interfaces that enable client applications to obtain information about the UI and to send input to controls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="58674-144">Функции, описанные в нерекомендуемых <a href="uiauto-entry-cpfunctions.md">функциях шаблона элемента управления</a> и <a href="uiauto-entry-uianodefunctions.md">устаревших функциях узла</a> , являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="58674-144">The functions described in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> and <a href="uiauto-entry-uianodefunctions.md">Deprecated Node Functions</a> are deprecated.</span></span> <span data-ttu-id="58674-145">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса, описанные в <a href="uiauto-entry-uiautoclientinterfaces.md">интерфейсах элементов модели автоматизации пользовательского интерфейса для клиентов</a>.</span><span class="sxs-lookup"><span data-stu-id="58674-145">Instead, client applications should use the UI Automation COM interfaces described in <a href="uiauto-entry-uiautoclientinterfaces.md">UI Automation Element Interfaces for Clients</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58674-146">UIAutomationCore.dll</span><span class="sxs-lookup"><span data-stu-id="58674-146">UIAutomationCore.dll</span></span></td>
<td><span data-ttu-id="58674-147">Библиотека времени выполнения, которая иногда называется ядром автоматизации пользовательского интерфейса, которая управляет взаимодействием между поставщиками и клиентами.</span><span class="sxs-lookup"><span data-stu-id="58674-147">The run-time library, sometimes called the UI Automation core, that handles communication between providers and clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58674-148">Oleacc.dll</span><span class="sxs-lookup"><span data-stu-id="58674-148">Oleacc.dll</span></span></td>
<td><span data-ttu-id="58674-149">Библиотека времени выполнения для Microsoft Active Accessibility и прокси-объектов.</span><span class="sxs-lookup"><span data-stu-id="58674-149">The run-time library for Microsoft Active Accessibility and the proxy objects.</span></span> <span data-ttu-id="58674-150">Библиотека также предоставляет прокси-объекты, используемые Microsoft Active Accessibility для прокси-сервера автоматизации пользовательского интерфейса для поддержки элементов управления Win32.</span><span class="sxs-lookup"><span data-stu-id="58674-150">The library also provides proxy objects used by the Microsoft Microsoft Active Accessibility to UI Automation Proxy to support Win32 controls.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="58674-151">Существует два способа использования модели автоматизации пользовательского интерфейса: для создания поддержки пользовательских элементов управления с помощью API поставщика, а также для создания клиентских приложений, использующих ядро автоматизации пользовательского интерфейса для взаимодействия с, и получения сведений о элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-151">There are two ways of using UI Automation: to create support for custom controls by using the provider API, and to create client applications that use the UI Automation core to communicate with, and retrieve information about, UI elements.</span></span> <span data-ttu-id="58674-152">В зависимости от ключевых целей вы должны обращаться к разным частям документации.</span><span class="sxs-lookup"><span data-stu-id="58674-152">Depending on your focus, you should refer to different parts of the documentation.</span></span> <span data-ttu-id="58674-153">Сведения о создании поддержки пользовательских элементов управления см. в разделе [руководств программиста по поставщику автоматизации пользовательского интерфейса](uiauto-providerportal.md).</span><span class="sxs-lookup"><span data-stu-id="58674-153">If you need to create support for custom controls, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span> <span data-ttu-id="58674-154">Если необходимо связаться со сведениями о элементах пользовательского интерфейса или получить информацию о них, см. статью в разделе [руководств по программированию клиента автоматизации пользовательского интерфейса](uiauto-clientportal.md).</span><span class="sxs-lookup"><span data-stu-id="58674-154">If you need to communicate with or retrieve information about UI elements, see [UI Automation Client Programmer's Guide](uiauto-clientportal.md).</span></span>

## <a name="ui-automation-header-files"></a><span data-ttu-id="58674-155">Файлы заголовков модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-155">UI Automation Header Files</span></span>

<span data-ttu-id="58674-156">API модели автоматизации пользовательского интерфейса определяется в нескольких разных файлах заголовков C/C++, которые входят в состав пакета средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="58674-156">The UI Automation API is defined in several different C/C++ header files that are included with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="58674-157">Файлы заголовков модели автоматизации пользовательского интерфейса описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="58674-157">The UI Automation header files are described in the following table:</span></span>



| <span data-ttu-id="58674-158">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="58674-158">Header file</span></span>           | <span data-ttu-id="58674-159">Описание</span><span class="sxs-lookup"><span data-stu-id="58674-159">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58674-160">UIAutomationClient. h</span><span class="sxs-lookup"><span data-stu-id="58674-160">UIAutomationClient.h</span></span>  | <span data-ttu-id="58674-161">Определяет интерфейсы и связанные элементы программирования, используемые клиентами автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-161">Defines the interfaces and related programming elements used by UI Automation clients.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="58674-162">Уиаутоматионкоре. h</span><span class="sxs-lookup"><span data-stu-id="58674-162">UIAutomationCore.h</span></span>    | <span data-ttu-id="58674-163">Определяет интерфейсы и связанные элементы программирования, используемые поставщиками автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-163">Defines the interfaces and related programming elements used by UI Automation providers.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="58674-164">Уиаутоматионкореапи. h</span><span class="sxs-lookup"><span data-stu-id="58674-164">UIAutomationCoreApi.h</span></span> | <span data-ttu-id="58674-165">Определяет общие константы, идентификаторы GUID, типы данных и структуры, используемые клиентами и поставщиками модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-165">Defines general constants, GUIDs, data types, and structures used by UI Automation clients and providers.</span></span> <span data-ttu-id="58674-166">Он также содержит определения для устаревших функций узла и шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="58674-166">It also contains definitions for the deprecated node and control pattern functions.</span></span>                                                                                    |
| <span data-ttu-id="58674-167">UIAutomation. h</span><span class="sxs-lookup"><span data-stu-id="58674-167">UIAutomation.h</span></span>        | <span data-ttu-id="58674-168">Включает все остальные файлы заголовков модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58674-168">Includes all of the other UI Automation header files.</span></span> <span data-ttu-id="58674-169">Так как большинству приложений автоматизации пользовательского интерфейса требуются элементы из всех файлов заголовков модели автоматизации пользовательского интерфейса, лучше всего включить UIAutomation. h в проекты приложения автоматизации пользовательского интерфейса, а не включать каждый файл по отдельности.</span><span class="sxs-lookup"><span data-stu-id="58674-169">Because most UI Automation applications require elements from all UI Automation header files, it is best to include UIAutomation.h in your UI Automation application projects instead of including each file individually.</span></span> |



 

<span data-ttu-id="58674-170">При разработке приложения, использующего API автоматизации пользовательского интерфейса, необходимо включить UIAutomation. h в проект.</span><span class="sxs-lookup"><span data-stu-id="58674-170">If you are developing an application that uses the UI Automation API, you should include UIAutomation.h in your project.</span></span> <span data-ttu-id="58674-171">Если приложение поддерживает Microsoft Active Accessibility, включите файл заголовка Олеакк. h.</span><span class="sxs-lookup"><span data-stu-id="58674-171">If your application supports Microsoft Active Accessibility, include the Oleacc.h header file.</span></span> <span data-ttu-id="58674-172">Для приложений автоматизации пользовательского интерфейса, использующих идентификаторы GUID, также требуется файл заголовка Инитгуид. h.</span><span class="sxs-lookup"><span data-stu-id="58674-172">UI Automation applications that use GUIDs also require the Initguid.h header file.</span></span> <span data-ttu-id="58674-173">При необходимости Инитгуид. h должен быть добавлен перед UIAutomation. h.</span><span class="sxs-lookup"><span data-stu-id="58674-173">If needed, Initguid.h should be included before UIAutomation.h.</span></span>

## <a name="ui-automation-model"></a><span data-ttu-id="58674-174">Модель автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-174">UI Automation Model</span></span>

<span data-ttu-id="58674-175">Модель автоматизации пользовательского интерфейса предоставляет каждому элементу пользовательского интерфейса доступ к клиентским приложениям как к объекту, представленному интерфейсом [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) .</span><span class="sxs-lookup"><span data-stu-id="58674-175">UI Automation exposes every element of the UI to client applications as an object represented by the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="58674-176">Элементы содержатся в древовидной структуре с рабочим столом в качестве корневого элемента.</span><span class="sxs-lookup"><span data-stu-id="58674-176">Elements are contained in a tree structure, with the desktop as the root element.</span></span> <span data-ttu-id="58674-177">Клиенты могут фильтровать базовое представление дерева как представление элемента управления или представление содержимого.</span><span class="sxs-lookup"><span data-stu-id="58674-177">Clients can filter the raw view of the tree as a control view or a content view.</span></span> <span data-ttu-id="58674-178">Эти стандартные представления структуры можно легко просмотреть с помощью приложения [проверки](inspect-objects.md) , которое входит в состав Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="58674-178">These standard views of the structure can easily be seen by using the [Inspect](inspect-objects.md) application that is included with the Windows SDK.</span></span> <span data-ttu-id="58674-179">Приложения также могут создавать настраиваемые представления.</span><span class="sxs-lookup"><span data-stu-id="58674-179">Applications can also create custom views.</span></span>

<span data-ttu-id="58674-180">Элемент модели автоматизации пользовательского интерфейса предоставляет свойства элемента управления или элемента пользовательского интерфейса, который он представляет.</span><span class="sxs-lookup"><span data-stu-id="58674-180">A UI Automation element exposes properties of the control or UI element that it represents.</span></span> <span data-ttu-id="58674-181">Одним из этих свойств является тип элемента управления, который определяет базовый внешний вид и функциональность элемента управления или элемента пользовательского интерфейса в виде одной распознаваемой сущности, например кнопки или флажка.</span><span class="sxs-lookup"><span data-stu-id="58674-181">One of these properties is the control type, which defines the basic appearance and functionality of the control or UI element as a single recognizable entity, for example, a button or check box.</span></span> <span data-ttu-id="58674-182">Дополнительные сведения о типах элементов управления см. в разделе [Общие сведения о типах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="58674-182">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="58674-183">Кроме того, элемент модели автоматизации пользовательского интерфейса предоставляет один или несколько шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="58674-183">In addition, a UI Automation element exposes one or more control patterns.</span></span> <span data-ttu-id="58674-184">Шаблон элемента управления предоставляет набор свойств, относящихся к конкретному типу элемента управления.</span><span class="sxs-lookup"><span data-stu-id="58674-184">A control pattern provides a set of properties that are specific to a particular control type.</span></span> <span data-ttu-id="58674-185">Шаблон элемента управления также предоставляет методы, позволяющие клиентским приложениям получать дополнительные сведения об элементе и предоставлять входные данные для элемента.</span><span class="sxs-lookup"><span data-stu-id="58674-185">A control pattern also exposes methods that enable client applications to get more information about the element and to provide input to the element.</span></span> <span data-ttu-id="58674-186">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="58674-186">For more information about control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="58674-187">Между типами элементов управления и шаблонами элементов управления нет соответствия "один к одному".</span><span class="sxs-lookup"><span data-stu-id="58674-187">There is no one-to-one correspondence between control types and control patterns.</span></span> <span data-ttu-id="58674-188">Шаблон элемента управления может поддерживаться несколькими типами элементов управления, и элемент управления может поддерживать несколько шаблонов элементов управления, каждый из которых представляет различные аспекты его поведения.</span><span class="sxs-lookup"><span data-stu-id="58674-188">A control pattern may be supported by multiple control types, and a control may support multiple control patterns, each of which exposes different aspects of its behavior.</span></span> <span data-ttu-id="58674-189">Например, поле со списком имеет по крайней мере два шаблона элементов управления: один представляет его возможность разворачиваться и сворачиваться, а другой представляет механизм выбора.</span><span class="sxs-lookup"><span data-stu-id="58674-189">For example, a combo box has at least two control patterns: one that represents its ability to expand and collapse, and another that represents the selection mechanism.</span></span> <span data-ttu-id="58674-190">Однако элемент управления может демонстрировать только один тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="58674-190">However, a control can exhibit only a single control type.</span></span>

 

<span data-ttu-id="58674-191">Модель автоматизации пользовательского интерфейса предоставляет сведения клиентским приложениям с помощью событий.</span><span class="sxs-lookup"><span data-stu-id="58674-191">UI Automation provides information to client applications through events.</span></span> <span data-ttu-id="58674-192">В отличие от Виневентс, события модели автоматизации пользовательского интерфейса не основаны на механизме вещания.</span><span class="sxs-lookup"><span data-stu-id="58674-192">Unlike WinEvents, UI Automation events are not based on a broadcast mechanism.</span></span> <span data-ttu-id="58674-193">Клиенты автоматизации пользовательского интерфейса регистрируются для конкретных уведомлений о событиях и могут запрашивать, чтобы определенные свойства и данные шаблона элемента управления передавались в свои обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="58674-193">UI Automation clients register for specific event notifications and can request that specific properties and control pattern information be passed to their event handlers.</span></span> <span data-ttu-id="58674-194">Кроме того, событие модели автоматизации пользовательского интерфейса содержит ссылку на элемент, который его вызвал.</span><span class="sxs-lookup"><span data-stu-id="58674-194">In addition, a UI Automation event contains a reference to the element that raised it.</span></span> <span data-ttu-id="58674-195">Поставщики могут повысить производительность, вызывая события выборочно, в зависимости от того, являются ли клиенты прослушивающими.</span><span class="sxs-lookup"><span data-stu-id="58674-195">Providers can improve performance by raising events selectively, depending on whether any clients are listening.</span></span> <span data-ttu-id="58674-196">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="58674-196">For more information about events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58674-197">См. также</span><span class="sxs-lookup"><span data-stu-id="58674-197">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="58674-198">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="58674-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="58674-199">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-199">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="58674-200">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-200">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="58674-201">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="58674-201">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 





