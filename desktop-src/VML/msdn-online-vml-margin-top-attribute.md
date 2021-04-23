---
title: Атрибут VML Margin-Top
description: Атрибут VML Margin-Top
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339169"
---
# <a name="vml-margin-top-attribute"></a><span data-ttu-id="36803-103">Атрибут VML Margin-Top</span><span class="sxs-lookup"><span data-stu-id="36803-103">VML Margin-Top Attribute</span></span>

<span data-ttu-id="36803-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="36803-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="36803-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="36803-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="36803-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="36803-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="36803-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="36803-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="36803-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="36803-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="36803-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="36803-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="36803-110">Задает верхнюю границу содержащего прямоугольника фигуры относительно привязки фигуры.</span><span class="sxs-lookup"><span data-stu-id="36803-110">Specifies the top edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="36803-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="36803-111">Read/write.</span></span> <span data-ttu-id="36803-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="36803-112">**String**.</span></span>

<span data-ttu-id="36803-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="36803-113">**Applies To**</span></span>

[<span data-ttu-id="36803-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="36803-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="36803-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="36803-115">**Tag Syntax**</span></span>

<span data-ttu-id="36803-116"><v: поле *элемента* -Top = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="36803-116"><v: *element* margin-top=" *expression* "></span></span>

<span data-ttu-id="36803-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="36803-117">**Script Syntax**</span></span>

<span data-ttu-id="36803-118">*element* . Margins-Top = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="36803-118">*element* .margin-top="*expression*"</span></span>

<span data-ttu-id="36803-119">*выражение* = *элемент*. Margin — сверху</span><span class="sxs-lookup"><span data-stu-id="36803-119">*expression*=*element*.margin-top</span></span>

<span data-ttu-id="36803-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="36803-120">**Remarks**</span></span>

<span data-ttu-id="36803-121">Атрибут **Margin-Top** аналогичен стандартному атрибуту **поля** HTML, используемому в таблицах стилей.</span><span class="sxs-lookup"><span data-stu-id="36803-121">The **Margin-Top** attribute is similar to the standard HTML **Margin-Top** attribute used with style sheets.</span></span>

<span data-ttu-id="36803-122">Обратите внимание, что вместо **полей** для создания скриптов используется **margintop** .</span><span class="sxs-lookup"><span data-stu-id="36803-122">Note that **margintop** is used instead of **margin-top** for scripting.</span></span> <span data-ttu-id="36803-123">Также обратите внимание, что если **положение** **абсолютное**, поле не изменится.</span><span class="sxs-lookup"><span data-stu-id="36803-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="36803-124">Это свойство используется вместо **поверх** фигур в Microsoft Word и Microsoft Excel, которые находятся в позиции относительно точки привязки.</span><span class="sxs-lookup"><span data-stu-id="36803-124">This property is used instead of **Top** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="36803-125">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="36803-125">Values include:</span></span>



| <span data-ttu-id="36803-126">Значение</span><span class="sxs-lookup"><span data-stu-id="36803-126">Value</span></span>      | <span data-ttu-id="36803-127">Описание</span><span class="sxs-lookup"><span data-stu-id="36803-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36803-128">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="36803-128">Auto</span></span>       | <span data-ttu-id="36803-129">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="36803-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="36803-130">units</span><span class="sxs-lookup"><span data-stu-id="36803-130">units</span></span>      | <span data-ttu-id="36803-131">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36803-131">Default.</span></span> <span data-ttu-id="36803-132">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="36803-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="36803-133">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="36803-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="36803-134">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="36803-134">The default value is 0.</span></span> |
| <span data-ttu-id="36803-135">процент</span><span class="sxs-lookup"><span data-stu-id="36803-135">percentage</span></span> | <span data-ttu-id="36803-136">Значение, выраженное в процентах от высоты родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="36803-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="36803-137">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="36803-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="36803-138">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="36803-138">**See Also**</span></span>

[<span data-ttu-id="36803-139">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="36803-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="36803-140">**Пример**</span><span class="sxs-lookup"><span data-stu-id="36803-140">**Example**</span></span>

<span data-ttu-id="36803-141">Верхнее поле имеет значение 25 пикселей.</span><span class="sxs-lookup"><span data-stu-id="36803-141">The top margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



<span data-ttu-id="36803-142">[Пример атрибута Margin-Top](/previous-versions/bb264087(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="36803-142">[Margin-Top Attribute Example](/previous-versions/bb264087(v=vs.85)).</span></span> <span data-ttu-id="36803-143">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="36803-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 