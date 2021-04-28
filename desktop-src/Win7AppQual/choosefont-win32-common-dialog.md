---
description: ChooseFont () общее диалоговое окно Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () общее диалоговое окно Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dd8eb6ec226f8dbf5220f5a90dac802cf149dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088612"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="4baff-103">ChooseFont () общее диалоговое окно Win32</span><span class="sxs-lookup"><span data-stu-id="4baff-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4baff-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="4baff-104">Affected Platforms</span></span>

<span data-ttu-id="4baff-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="4baff-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="4baff-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4baff-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="4baff-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="4baff-107">Feature Impact</span></span>

<span data-ttu-id="4baff-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="4baff-108">**Severity** - Low</span></span>  
<span data-ttu-id="4baff-109">**Частота** — средний</span><span class="sxs-lookup"><span data-stu-id="4baff-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="4baff-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4baff-110">Description</span></span>

<span data-ttu-id="4baff-111">В состав Windows 7 входит несколько обновлений для общего диалогового окна ChooseFont () Win32.</span><span class="sxs-lookup"><span data-stu-id="4baff-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="4baff-112">Они делятся на две категории:</span><span class="sxs-lookup"><span data-stu-id="4baff-112">These fall into two categories:</span></span>

-   <span data-ttu-id="4baff-113">Визуальное обновление диалогового окна</span><span class="sxs-lookup"><span data-stu-id="4baff-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="4baff-114">Поддержка новой функции "Показать/скрыть шрифты"</span><span class="sxs-lookup"><span data-stu-id="4baff-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="4baff-115">**Диалоговое окно Обновление** обновляет стандартный шаблон, чтобы диалоговое окно больше в строке с другими макетами диалоговых окон в Windows.</span><span class="sxs-lookup"><span data-stu-id="4baff-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="4baff-116">В нем представлено представление WYSIWYG для списков шрифтов, помогающих пользователям выбирать шрифты.</span><span class="sxs-lookup"><span data-stu-id="4baff-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="4baff-117">Он также содержит ссылку на CPL, обеспечивающую удобный доступ для пользователей, желающих настроить списки шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4baff-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="4baff-118">**Показать/скрыть шрифты** — это новая функция платформы Windows 7, в которой шрифты, не подходящие для языковых параметров текущего пользователя (методы ввода), не отображаются по умолчанию в списках выбора шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4baff-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="4baff-119">Пользователи могут настроить шрифты, которые должны отображаться в CPL, или отключить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="4baff-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4baff-120">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="4baff-120">Manifestation of Impact</span></span>

<span data-ttu-id="4baff-121">**Визуальное обновление диалогового окна**</span><span class="sxs-lookup"><span data-stu-id="4baff-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="4baff-122">В Windows 7 появились два новых шаблона (одна для приложений, которые загружают версию 6 или более поздней comctl32.dll а другая — для приложений, загружая более ранние версии).</span><span class="sxs-lookup"><span data-stu-id="4baff-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="4baff-123">В целях совместимости приложений эти новые шаблоны будут загружены только для приложений, которые не применяют очередь сообщений ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="4baff-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="4baff-124">Приложения, которые применяют очередь сообщений, будут по-прежнему видеть старый макет диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4baff-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="4baff-125">Приложения, предоставляющие собственные шаблоны, по прежнему смогут их использовать.</span><span class="sxs-lookup"><span data-stu-id="4baff-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="4baff-126">Приложения, не получающие новые шаблоны, не увидят изменений макета диалога из Vista.</span><span class="sxs-lookup"><span data-stu-id="4baff-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="4baff-127">Однако они должны по-прежнему получить новый предварительный просмотр шрифта WYSIWYG.</span><span class="sxs-lookup"><span data-stu-id="4baff-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="4baff-128">**Показать/скрыть шрифты**</span><span class="sxs-lookup"><span data-stu-id="4baff-128">**Show/hide fonts**</span></span>

<span data-ttu-id="4baff-129">Для всех версий ChooseFont диалоговое окно будет использовать параметры отображения и скрытия шрифта текущего пользователя, чтобы определить список шрифтов для отображения.</span><span class="sxs-lookup"><span data-stu-id="4baff-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="4baff-130">Это приведет к отображению меньшего числа списков шрифтов в большинстве экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4baff-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="4baff-131">Устранение рисков для конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="4baff-131">End-user Mitigation</span></span>

<span data-ttu-id="4baff-132">**Показать/скрыть шрифты:** Чтобы отключить скрытие шрифтов, пользователи должны открыть страницу «параметры шрифта» в панели «шрифты» и снять флажок «</span><span class="sxs-lookup"><span data-stu-id="4baff-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="4baff-133">Флажок "скрыть шрифты, основанные на языковых параметрах"</span><span class="sxs-lookup"><span data-stu-id="4baff-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="4baff-134">Устранение рисков для разработчиков</span><span class="sxs-lookup"><span data-stu-id="4baff-134">Developer Mitigation</span></span>

-   <span data-ttu-id="4baff-135">**Визуальное обновление:** Разработчикам приложений, которые предоставляют собственные шаблоны, может потребоваться обновить это, чтобы они были в соответствии с новым шаблоном Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4baff-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="4baff-136">Новые шаблоны доступны в файле шаблона Font. DLG.</span><span class="sxs-lookup"><span data-stu-id="4baff-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="4baff-137">**Примечание.** Новый опубликованный шаблон содержит дополнительный элемент управления SysLink, который предоставляет ярлык, позволяющий пользователям запускать значок CPL для вывода дополнительных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4baff-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="4baff-138">Для элемента управления Link требуется версия 6 библиотеки общих элементов управления Windows (comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="4baff-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="4baff-139">Разработчики должны предоставить манифест или директиву, указывающую на использование библиотеки DLL версии 6, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="4baff-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="4baff-140">Когда приложение использует более раннюю версию библиотеки общих элементов управления, используйте вместо него тип элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="4baff-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="4baff-141">**Показать/скрыть шрифты:** Разработчики могут отключить эту функцию, предоставив дополнительный флаг (CF \_ инактивефонтс) в элементе flags структуры CHOOSEFONT.</span><span class="sxs-lookup"><span data-stu-id="4baff-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="4baff-142">Установка этого флага приводит к тому, что все установленные шрифты отображаются в списке шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4baff-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="4baff-143">**Показать/скрыть шрифты:** В приложениях, предоставляющих содержимое справки ChooseFont, может потребоваться добавить содержимое, объясняющее, почему список шрифтов уменьшается, и направлять пользователей на панели CPL для настройки их списков шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4baff-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="4baff-144">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="4baff-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="4baff-145">Разработчики, чьи приложения заключают очередь сообщений ChooseFont для настройки диалогового окна, должны убедиться, что их приложения сохраняют все имеющиеся функции.</span><span class="sxs-lookup"><span data-stu-id="4baff-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="4baff-146">Приложения, которые сильно обрезают список шрифтов с помощью флагов, должны убедиться, что представленный список шрифтов остается приемлемым.</span><span class="sxs-lookup"><span data-stu-id="4baff-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



