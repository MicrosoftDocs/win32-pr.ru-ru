---
title: Нерекомендуемые функции node
description: Нерекомендуемые функции node
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103987955"
---
# <a name="deprecated-node-functions"></a><span data-ttu-id="c268f-103">Нерекомендуемые функции node</span><span class="sxs-lookup"><span data-stu-id="c268f-103">Deprecated Node Functions</span></span>

> [!Note]  
> <span data-ttu-id="c268f-104">Функции шаблона элемента управления, описанные в этом разделе, являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="c268f-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="c268f-105">Клиентские приложения должны использовать интерфейсы модели COM, описанные в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c268f-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="c268f-106">Интерфейсы элементов модели автоматизации пользовательского интерфейса для клиентов</span><span class="sxs-lookup"><span data-stu-id="c268f-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="c268f-107">Интерфейс условий свойств для клиентов</span><span class="sxs-lookup"><span data-stu-id="c268f-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="c268f-108">Интерфейсы шаблонов элементов управления для клиентов</span><span class="sxs-lookup"><span data-stu-id="c268f-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="c268f-109">Интерфейсы обработки событий для клиентов</span><span class="sxs-lookup"><span data-stu-id="c268f-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="c268f-110">Интерфейсы фабрики прокси-серверов для клиентов</span><span class="sxs-lookup"><span data-stu-id="c268f-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="c268f-111">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="c268f-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c268f-112">Функция</span><span class="sxs-lookup"><span data-stu-id="c268f-112">Function</span></span></th>
<th><span data-ttu-id="c268f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c268f-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c268f-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>уиааддевент</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-115">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-115">This function is deprecated.</span></span> <span data-ttu-id="c268f-116">Вместо этого клиентские приложения должны использовать COM-интерфейсы модели автоматизации пользовательского интерфейса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c268f-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-117">Добавляет прослушиватель для событий на узле в дереве модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-117">Adds a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>уиаевентаддвиндов</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-119">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-119">This function is deprecated.</span></span> <span data-ttu-id="c268f-120">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-121">Добавляет окно в прослушиватель событий.</span><span class="sxs-lookup"><span data-stu-id="c268f-121">Adds a window to the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>уиаевенткаллбакк</em></a></span><span class="sxs-lookup"><span data-stu-id="c268f-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-123">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-123">This function is deprecated.</span></span> <span data-ttu-id="c268f-124">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-125">Реализованная клиентом функция, вызываемая автоматизацией пользовательского интерфейса при возникновении события, на которое подписан клиент.</span><span class="sxs-lookup"><span data-stu-id="c268f-125">A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>уиаевентремовевиндов</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-127">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-127">This function is deprecated.</span></span> <span data-ttu-id="c268f-128">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-129">Удаляет окно из прослушивателя событий.</span><span class="sxs-lookup"><span data-stu-id="c268f-129">Removes a window from the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>уиафинд</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-131">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-131">This function is deprecated.</span></span> <span data-ttu-id="c268f-132">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-133">Извлекает один или несколько узлов автоматизации пользовательского интерфейса, соответствующих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="c268f-133">Retrieves one or more UI Automation nodes that match the search criteria.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>уиажетеррордескриптион</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-135">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-135">This function is deprecated.</span></span> <span data-ttu-id="c268f-136">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-137">Возвращает строку ошибки, чтобы ее можно было передать клиенту.</span><span class="sxs-lookup"><span data-stu-id="c268f-137">Gets an error string so that it can be passed to the client.</span></span> <span data-ttu-id="c268f-138">Этот метод не используется клиентами напрямую.</span><span class="sxs-lookup"><span data-stu-id="c268f-138">This method is not used directly by clients.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>уиажетпаттернпровидер</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-140">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-140">This function is deprecated.</span></span> <span data-ttu-id="c268f-141">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-141">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-142">Извлекает <em>шаблон элемента управления</em>.</span><span class="sxs-lookup"><span data-stu-id="c268f-142">Retrieves a <em>control pattern</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>уиажетпропертивалуе</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-144">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-144">This function is deprecated.</span></span> <span data-ttu-id="c268f-145">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-145">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-146">Извлекает значение свойства модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-146">Retrieves the value of a UI Automation property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>уиажетрутноде</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-148">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-148">This function is deprecated.</span></span> <span data-ttu-id="c268f-149">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-149">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-150">Извлекает корневой узел автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-150">Retrieves the root UI Automation node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>уиажетрунтимеид</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-152">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-152">This function is deprecated.</span></span> <span data-ttu-id="c268f-153">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-153">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-154">Получает идентификатор среды выполнения узла модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-154">Retrieves the runtime identifier of a UI Automation node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>уиажетупдатедкаче</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-156">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-156">This function is deprecated.</span></span> <span data-ttu-id="c268f-157">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-157">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-158">Обновляет кэш значений свойств и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="c268f-158">Updates the cache of property values and control patterns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>уиахпаттернобжектфромвариант</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-160">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-160">This function is deprecated.</span></span> <span data-ttu-id="c268f-161">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-161">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-162">Возвращает объект шаблона элемента управления из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c268f-162">Gets a control pattern object from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>уиахтекстранжефромвариант</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-164">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-164">This function is deprecated.</span></span> <span data-ttu-id="c268f-165">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-165">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-166">Возвращает текстовый диапазон из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c268f-166">Gets a text range from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>уиахуианодефромвариант</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-168">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-168">This function is deprecated.</span></span> <span data-ttu-id="c268f-169">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-169">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-170">Возвращает ХУИАНОДЕ из типа <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c268f-170">Gets an HUIANODE from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>уиалукупид</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-172">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-172">This function is deprecated.</span></span> <span data-ttu-id="c268f-173">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-173">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-174">Возвращает целочисленный идентификатор, который может использоваться в методах, требующих PROPERTYID, ПАТТЕРНИД, КОНТРОЛТИПЕИД, ТЕКСТАТТРИБУТЕИД или EVENTID.</span><span class="sxs-lookup"><span data-stu-id="c268f-174">Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>уианавигате</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-176">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-176">This function is deprecated.</span></span> <span data-ttu-id="c268f-177">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-177">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-178">Переходит в дерево модели автоматизации пользовательского интерфейса, при необходимости получая кэшированные данные.</span><span class="sxs-lookup"><span data-stu-id="c268f-178">Navigates in the UI Automation tree, optionally retrieving cached information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>уианодефромфокус</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-180">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-180">This function is deprecated.</span></span> <span data-ttu-id="c268f-181">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-181">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-182">Извлекает узел модели автоматизации пользовательского интерфейса для элемента пользовательского интерфейса, который в данный момент имеет фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="c268f-182">Retrieves the UI Automation node for the UI element that currently has input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>уианодефромхандле</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-184">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-184">This function is deprecated.</span></span> <span data-ttu-id="c268f-185">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-185">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-186">Извлекает узел автоматизации пользовательского интерфейса, связанный с окном.</span><span class="sxs-lookup"><span data-stu-id="c268f-186">Retrieves the UI Automation node associated with a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>уианодефромпоинт</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-188">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-188">This function is deprecated.</span></span> <span data-ttu-id="c268f-189">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-189">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-190">Извлекает узел модели автоматизации пользовательского интерфейса для элемента в указанной точке.</span><span class="sxs-lookup"><span data-stu-id="c268f-190">Retrieves the UI Automation node for the element at the specified point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>уианодефромпровидер</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-192">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-192">This function is deprecated.</span></span> <span data-ttu-id="c268f-193">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-193">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-194">Извлекает узел модели автоматизации пользовательского интерфейса для поставщика необработанных элементов.</span><span class="sxs-lookup"><span data-stu-id="c268f-194">Retrieves the UI Automation node for a raw element provider.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>уианодерелеасе</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-196">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-196">This function is deprecated.</span></span> <span data-ttu-id="c268f-197">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-197">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-198">Удаляет узел из памяти.</span><span class="sxs-lookup"><span data-stu-id="c268f-198">Deletes a node from memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>уиапаттернрелеасе</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-200">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-200">This function is deprecated.</span></span> <span data-ttu-id="c268f-201">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-201">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-202">Удаляет выделенный объект шаблона из памяти.</span><span class="sxs-lookup"><span data-stu-id="c268f-202">Deletes an allocated pattern object from memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>уиапровидеркаллбакк</em></a></span><span class="sxs-lookup"><span data-stu-id="c268f-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-204">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-204">This function is deprecated.</span></span> <span data-ttu-id="c268f-205">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-205">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-206">Определяемая приложением функция, которая вызывается автоматизацией пользовательского интерфейса для получения поставщика на стороне клиента для элемента.</span><span class="sxs-lookup"><span data-stu-id="c268f-206">An application-defined function that is called by UI Automation to obtain a client-side provider for an element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>уиаректисемпти</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-208">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-208">This function is deprecated.</span></span> <span data-ttu-id="c268f-209">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-209">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-210">Возвращает логическое значение, указывающее, имеет ли прямоугольник все его координаты, равные 0.</span><span class="sxs-lookup"><span data-stu-id="c268f-210">Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>уиаректсетемпти</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-212">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-212">This function is deprecated.</span></span> <span data-ttu-id="c268f-213">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-213">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-214">Устанавливает элементы структуры <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>уиарект</strong></a> в значение 0.</span><span class="sxs-lookup"><span data-stu-id="c268f-214">Sets the elements of a <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> structure to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>уиарегистерпровидеркаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-216">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-216">This function is deprecated.</span></span> <span data-ttu-id="c268f-217">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-218">Регистрирует определенный приложением метод, который вызывается автоматизацией пользовательского интерфейса для получения поставщика для элемента.</span><span class="sxs-lookup"><span data-stu-id="c268f-218">Registers the application-defined method that is called by UI Automation to obtain a provider for an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>уиаремовивент</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-220">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-220">This function is deprecated.</span></span> <span data-ttu-id="c268f-221">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-222">Удаляет прослушиватель для событий на узле в дереве модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-222">Removes a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c268f-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>уиасетфокус</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-224">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-224">This function is deprecated.</span></span> <span data-ttu-id="c268f-225">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-226">Устанавливает фокус ввода на указанный элемент в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c268f-226">Sets the input focus to the specified element in the UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c268f-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>уиатекстранжерелеасе</strong></a></span><span class="sxs-lookup"><span data-stu-id="c268f-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c268f-228">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="c268f-228">This function is deprecated.</span></span> <span data-ttu-id="c268f-229">Вместо этого клиентские приложения должны использовать интерфейсы COM модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c268f-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="c268f-230">Удаляет выделенный объект текстового диапазона из памяти.</span><span class="sxs-lookup"><span data-stu-id="c268f-230">Deletes an allocated text range object from memory.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c268f-231">См. также</span><span class="sxs-lookup"><span data-stu-id="c268f-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c268f-232">Клиенты автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c268f-232">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

