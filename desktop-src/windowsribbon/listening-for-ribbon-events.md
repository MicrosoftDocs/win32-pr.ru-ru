---
title: Прослушивание событий ленты
description: Платформа Windows Ribbon использует инфраструктуру трассировки событий для Windows (ETW), позволяющую разработчикам узнать, как пользователи взаимодействуют с лентой приложения.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Лента Windows, события
- Лента, события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339449"
---
# <a name="listening-for-ribbon-events"></a><span data-ttu-id="d4d4c-105">Прослушивание событий ленты</span><span class="sxs-lookup"><span data-stu-id="d4d4c-105">Listening for Ribbon Events</span></span>

<span data-ttu-id="d4d4c-106">Платформа Windows Ribbon использует инфраструктуру [трассировки событий для Windows (ETW)](../etw/event-tracing-portal.md) , позволяющую разработчикам узнать, как пользователи взаимодействуют с лентой приложения.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-106">The Windows Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="introduction"></a><span data-ttu-id="d4d4c-107">Введение</span><span class="sxs-lookup"><span data-stu-id="d4d4c-107">Introduction</span></span>

<span data-ttu-id="d4d4c-108">Механизм событий платформы Ribbon разработан таким образом, что платформа сообщает приложению о событиях пользовательского интерфейса ленты, чтобы вы могли отслеживать действия пользователей, изучать их шаблоны взаимодействия и оценивать тенденции использования.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-108">The Ribbon framework event mechanism is designed such that the framework reports ribbon UI events to the application so you can monitor user activity, learn their interaction patterns, and assess usage trends.</span></span> <span data-ttu-id="d4d4c-109">Эти сведения можно использовать для уточнения пользовательского интерфейса для будущих итераций приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-109">This information can be used to refine the user experience for future iterations of your ribbon app.</span></span>

<span data-ttu-id="d4d4c-110">При использовании событий платформы Ribbon происходит следующее.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-110">Using the Ribbon framework events involves the following:</span></span>

1.  <span data-ttu-id="d4d4c-111">Приложение ленты должно зарегистрировать прослушиватель [трассировки событий Windows (ETW)](../etw/event-tracing-portal.md) для получения уведомлений о событиях ленты из платформы ленты.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-111">The ribbon application must register an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener to receive ribbon event notifications from the Ribbon framework.</span></span>
2.  <span data-ttu-id="d4d4c-112">Платформа Ribbon запускает обратные вызовы событий пользовательского интерфейса ленты во время выполнения, если приложение зарегистрировало прослушиватель [трассировки событий для Windows (ETW)](../etw/event-tracing-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d4c-112">The Ribbon framework fires ribbon UI event callbacks at run time, if the application has registered an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener.</span></span>

## <a name="supported-events"></a><span data-ttu-id="d4d4c-113">Поддерживаемые события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-113">Supported events</span></span>

<span data-ttu-id="d4d4c-114">События, предоставляемые для приложений ленты, описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-114">The events exposed to ribbon applications are described in the following table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4d4c-115">Событие</span><span class="sxs-lookup"><span data-stu-id="d4d4c-115">Event</span></span></th>
<th><span data-ttu-id="d4d4c-116">Отчет о событиях</span><span class="sxs-lookup"><span data-stu-id="d4d4c-116">Event report</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4d4c-117">Активированная вкладка</span><span class="sxs-lookup"><span data-stu-id="d4d4c-117">Tab activated</span></span></td>
<td><span data-ttu-id="d4d4c-118">Идентификатор команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-118">Command ID</span></span><br/> <span data-ttu-id="d4d4c-119">Имя команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-119">Command name</span></span><br/> <span data-ttu-id="d4d4c-120">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-120">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4d4c-121">Активирована контекстная вкладка</span><span class="sxs-lookup"><span data-stu-id="d4d4c-121">Contextual tab activated</span></span></td>
<td><span data-ttu-id="d4d4c-122">Идентификатор команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-122">Command ID</span></span><br/> <span data-ttu-id="d4d4c-123">Имя команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-123">Command name</span></span><br/> <span data-ttu-id="d4d4c-124">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-124">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4d4c-125">Меню приложения открыто</span><span class="sxs-lookup"><span data-stu-id="d4d4c-125">Application Menu opened</span></span></td>
<td><span data-ttu-id="d4d4c-126">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-126">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4d4c-127">Меню приложения закрыто</span><span class="sxs-lookup"><span data-stu-id="d4d4c-127">Application Menu closed</span></span></td>
<td><span data-ttu-id="d4d4c-128">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-128">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4d4c-129">Открыто меню (обычный или Галерея)</span><span class="sxs-lookup"><span data-stu-id="d4d4c-129">Menu (regular or gallery) opened</span></span></td>
<td><span data-ttu-id="d4d4c-130">Идентификатор команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-130">Command ID</span></span><br/> <span data-ttu-id="d4d4c-131">Имя команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-131">Command name</span></span><br/> <span data-ttu-id="d4d4c-132">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-132">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d4d4c-133">События меню QAT не отображаются.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-133">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4d4c-134">Меню (обычный или Галерея) закрыто</span><span class="sxs-lookup"><span data-stu-id="d4d4c-134">Menu (regular or gallery) closed</span></span></td>
<td><span data-ttu-id="d4d4c-135">Идентификатор команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-135">Command ID</span></span><br/> <span data-ttu-id="d4d4c-136">Имя команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-136">Command name</span></span><br/> <span data-ttu-id="d4d4c-137">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-137">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d4d4c-138">События меню QAT не отображаются.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-138">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4d4c-139">Get-Help</span><span class="sxs-lookup"><span data-stu-id="d4d4c-139">Command</span></span></td>
<td><span data-ttu-id="d4d4c-140">Идентификатор команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-140">Command ID</span></span><br/> <span data-ttu-id="d4d4c-141">Имя команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-141">Command name</span></span><br/> <span data-ttu-id="d4d4c-142">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-142">Event verb</span></span><br/> <span data-ttu-id="d4d4c-143">Одно из следующих расположений событий:</span><span class="sxs-lookup"><span data-stu-id="d4d4c-143">One of the following event locations:</span></span>
<ul>
<li><span data-ttu-id="d4d4c-144">ЛЕНТЕ</span><span class="sxs-lookup"><span data-stu-id="d4d4c-144">RIBBON</span></span></li>
<li><span data-ttu-id="d4d4c-145">куиккакцесстулбар</span><span class="sxs-lookup"><span data-stu-id="d4d4c-145">QUICKACCESSTOOLBAR</span></span></li>
<li><span data-ttu-id="d4d4c-146">аппликатионмену</span><span class="sxs-lookup"><span data-stu-id="d4d4c-146">APPLICATIONMENU</span></span></li>
<li><span data-ttu-id="d4d4c-147">контекстпопуп</span><span class="sxs-lookup"><span data-stu-id="d4d4c-147">CONTEXTPOPUP</span></span></li>
</ul>
<br/> <span data-ttu-id="d4d4c-148">ИДЕНТИФИКАТОР родительской команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-148">Parent Command ID</span></span><br/> <span data-ttu-id="d4d4c-149">Имя родительской команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-149">Parent Command name</span></span><br/> <span data-ttu-id="d4d4c-150">Один из следующих методов Invoke:</span><span class="sxs-lookup"><span data-stu-id="d4d4c-150">One of the following invoke methods:</span></span>
<ul>
<li><span data-ttu-id="d4d4c-151">Откройте</span><span class="sxs-lookup"><span data-stu-id="d4d4c-151">CLICK</span></span></li>
<li><span data-ttu-id="d4d4c-152">KEYTIP</span><span class="sxs-lookup"><span data-stu-id="d4d4c-152">KEYTIP</span></span></li>
<li><span data-ttu-id="d4d4c-153">ЭКВИВАЛЕНТ</span><span class="sxs-lookup"><span data-stu-id="d4d4c-153">KEYBOARD</span></span></li>
<li><span data-ttu-id="d4d4c-154">ПЕРСОНИФИЦИРОВАН</span><span class="sxs-lookup"><span data-stu-id="d4d4c-154">TOUCH</span></span></li>
</ul>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d4d4c-155">Коллекции элементов и поля со списком содержат выбранный индекс элемента, но не содержат строковые и целочисленные значения.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-155">Item galleries and combo boxes include the selected item index but do not include string and integer values.</span></span> <span data-ttu-id="d4d4c-156">Счетчики не включают целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-156">Spinners do not include the integer value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4d4c-157">Лента уменьшена</span><span class="sxs-lookup"><span data-stu-id="d4d4c-157">Ribbon minimized</span></span></td>
<td><span data-ttu-id="d4d4c-158">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-158">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4d4c-159">Лента развернута (кнопка развертывания нажата или касание закреплена)</span><span class="sxs-lookup"><span data-stu-id="d4d4c-159">Ribbon expanded (expand button clicked or tap pinned)</span></span></td>
<td><span data-ttu-id="d4d4c-160">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-160">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4d4c-161">Режим приложения переключен</span><span class="sxs-lookup"><span data-stu-id="d4d4c-161">Application mode switched</span></span></td>
<td><span data-ttu-id="d4d4c-162">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-162">Event verb</span></span><br/> <span data-ttu-id="d4d4c-163">Идентификатор режима (значение, заданное с помощью <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>сетмодес</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4d4c-163">Mode ID (value set through <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d4d4c-164">Приложение отвечает за распаковку этого целого числа, чтобы определить, какие режимы были установлены.</span><span class="sxs-lookup"><span data-stu-id="d4d4c-164">The application is responsible for unpacking this integer to determine which modes were set.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4d4c-165">Отображаемая подсказка</span><span class="sxs-lookup"><span data-stu-id="d4d4c-165">Tooltip displayed</span></span></td>
<td><span data-ttu-id="d4d4c-166">Команда события</span><span class="sxs-lookup"><span data-stu-id="d4d4c-166">Event verb</span></span><br/> <span data-ttu-id="d4d4c-167">ИДЕНТИФИКАТОР родительской команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-167">Parent Command ID</span></span><br/> <span data-ttu-id="d4d4c-168">Имя родительской команды</span><span class="sxs-lookup"><span data-stu-id="d4d4c-168">Parent Command name</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d4d4c-169">См. также</span><span class="sxs-lookup"><span data-stu-id="d4d4c-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4d4c-170">Руководства для разработчиков платформы Windows Ribbon</span><span class="sxs-lookup"><span data-stu-id="d4d4c-170">Windows Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)
</dt> <dt>

[<span data-ttu-id="d4d4c-171">Объявление команд и элементов управления с разметкой ленты</span><span class="sxs-lookup"><span data-stu-id="d4d4c-171">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="d4d4c-172">Рекомендации по работе пользователя с лентой</span><span class="sxs-lookup"><span data-stu-id="d4d4c-172">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="d4d4c-173">Процесс разработки ленты</span><span class="sxs-lookup"><span data-stu-id="d4d4c-173">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

