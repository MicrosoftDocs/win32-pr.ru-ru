---
title: Целевой атрибут VML
description: Целевой атрибут VML
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672291"
---
# <a name="vml-target-attribute"></a><span data-ttu-id="67628-103">Целевой атрибут VML</span><span class="sxs-lookup"><span data-stu-id="67628-103">VML Target Attribute</span></span>

<span data-ttu-id="67628-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="67628-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="67628-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="67628-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="67628-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="67628-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="67628-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67628-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="67628-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="67628-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="67628-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="67628-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="67628-110">Определяет фрейм или окно, в котором отображается URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="67628-110">Defines a frame or window that a URL is displayed in.</span></span> <span data-ttu-id="67628-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="67628-111">Read/write.</span></span> <span data-ttu-id="67628-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="67628-112">**String**.</span></span>

<span data-ttu-id="67628-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="67628-113">**Applies To**</span></span>

[<span data-ttu-id="67628-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="67628-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="67628-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="67628-115">**Tag Syntax**</span></span>

<span data-ttu-id="67628-116"><v: *элемент* Target = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="67628-116"><v: *element* target=" *expression* "></span></span>

<span data-ttu-id="67628-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="67628-117">**Remarks**</span></span>

<span data-ttu-id="67628-118">**Целевой** атрибут аналогичен стандартному **целевому** атрибуту HTML привязок.</span><span class="sxs-lookup"><span data-stu-id="67628-118">The **Target** attribute is similar to the standard HTML **Target** attribute of anchors.</span></span>

<span data-ttu-id="67628-119">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="67628-119">Values include:</span></span>



| <span data-ttu-id="67628-120">Значение</span><span class="sxs-lookup"><span data-stu-id="67628-120">Value</span></span>      | <span data-ttu-id="67628-121">Описание</span><span class="sxs-lookup"><span data-stu-id="67628-121">Description</span></span>                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67628-122">TargetName</span><span class="sxs-lookup"><span data-stu-id="67628-122">TargetName</span></span> | <span data-ttu-id="67628-123">Строка, содержащая имя фрейма или окна, в который загружается документ.</span><span class="sxs-lookup"><span data-stu-id="67628-123">String containing the name of the frame or window in which to load the document.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="67628-124">\_свобод</span><span class="sxs-lookup"><span data-stu-id="67628-124">\_blank</span></span>    | <span data-ttu-id="67628-125">Указывает, что связанный документ загружается в новое пустое окно.</span><span class="sxs-lookup"><span data-stu-id="67628-125">Specifies that the linked document is loaded into a new blank window.</span></span> <span data-ttu-id="67628-126">Это окно не называется.</span><span class="sxs-lookup"><span data-stu-id="67628-126">This window is not named.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="67628-127">\_носител</span><span class="sxs-lookup"><span data-stu-id="67628-127">\_media</span></span>    | <span data-ttu-id="67628-128">Начиная с версии Internet Explorer 6 для Windows XP с пакетом обновления 2 (SP2) \_ атрибут Media устарел и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67628-128">As of Internet Explorer 6 for Windows XP Service Pack 2, the \_media attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="67628-129">Первый доступ в Internet Explorer 6, это значение указывает, что связанный документ должен быть загружен на панель медиа.</span><span class="sxs-lookup"><span data-stu-id="67628-129">First available in Internet Explorer 6, this value specified that the linked document should be loaded into the Media Bar.</span></span>                |
| <span data-ttu-id="67628-130">\_источника</span><span class="sxs-lookup"><span data-stu-id="67628-130">\_parent</span></span>   | <span data-ttu-id="67628-131">Указывает, что связанный документ загружается в ближайший родительский элемент документа, содержащего ссылку.</span><span class="sxs-lookup"><span data-stu-id="67628-131">Specifies that the linked document is loaded into the immediate parent of the document containing the link.</span></span>                                                                                                                                                      |
| <span data-ttu-id="67628-132">\_осуществлять</span><span class="sxs-lookup"><span data-stu-id="67628-132">\_search</span></span>   | <span data-ttu-id="67628-133">Начиная с версии Internet Explorer 7 для Windows XP с пакетом обновления 2 (SP2), \_ атрибут поиска устарел и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67628-133">As of Internet Explorer 7 for Windows XP Service Pack 2, : The \_search attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="67628-134">Первый доступ в Internet Explorer 6, это значение указывает, что связанный документ был загружен в панель поиска в браузере.</span><span class="sxs-lookup"><span data-stu-id="67628-134">First available in Internet Explorer 6, this value specified that the linked document was to be loaded into the browser's search pane.</span></span> |
| <span data-ttu-id="67628-135">\_самообслуживания</span><span class="sxs-lookup"><span data-stu-id="67628-135">\_self</span></span>     | <span data-ttu-id="67628-136">Указывает, что связанный документ загружается в окно, в котором была нажата ссылка (активное окно).</span><span class="sxs-lookup"><span data-stu-id="67628-136">Specifies that the linked document is loaded into the window in which the link was clicked (the active window).</span></span>                                                                                                                                                  |
| <span data-ttu-id="67628-137">\_Вверх</span><span class="sxs-lookup"><span data-stu-id="67628-137">\_top</span></span>      | <span data-ttu-id="67628-138">Указывает, что связанный документ загружается в самое верхнее окно.</span><span class="sxs-lookup"><span data-stu-id="67628-138">Specifies that the linked document is loaded into the topmost window.</span></span>                                                                                                                                                                                            |



 

<span data-ttu-id="67628-139">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="67628-139">*VML Standard Attribute*</span></span>

<span data-ttu-id="67628-140">**Пример**</span><span class="sxs-lookup"><span data-stu-id="67628-140">**Example**</span></span>

<span data-ttu-id="67628-141">При щелчке прямоугольника браузер загружает домашнюю страницу корпорации Майкрософт в том же окне.</span><span class="sxs-lookup"><span data-stu-id="67628-141">When the rectangle is clicked, the browser loads the Microsoft Corporation home page in the same window.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="67628-142">[Пример целевого атрибута](/previous-versions/bb264096(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67628-142">[Target Attribute Example](/previous-versions/bb264096(v=vs.85)).</span></span> <span data-ttu-id="67628-143">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="67628-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 