---
title: Атрибут VML Margin-Left
description: Атрибут VML Margin-Left
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f98900e862f22f31ad444bc6fb6f372627eca1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338364"
---
# <a name="vml-margin-left-attribute"></a><span data-ttu-id="61127-103">Атрибут VML Margin-Left</span><span class="sxs-lookup"><span data-stu-id="61127-103">VML Margin-Left Attribute</span></span>

<span data-ttu-id="61127-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="61127-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="61127-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="61127-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="61127-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="61127-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="61127-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="61127-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="61127-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="61127-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="61127-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="61127-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="61127-110">Задает левый конец содержащего прямоугольника фигуры относительно привязки фигуры.</span><span class="sxs-lookup"><span data-stu-id="61127-110">Specifies the left edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="61127-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="61127-111">Read/write.</span></span> <span data-ttu-id="61127-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="61127-112">**String**.</span></span>

<span data-ttu-id="61127-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="61127-113">**Applies To**</span></span>

[<span data-ttu-id="61127-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="61127-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="61127-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="61127-115">**Tag Syntax**</span></span>

<span data-ttu-id="61127-116"><v: Style *элемента* = "левое-левое: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="61127-116"><v: *element* style="margin-left: *expression* "></span></span>

<span data-ttu-id="61127-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="61127-117">**Script Syntax**</span></span>

<span data-ttu-id="61127-118">*element* . Style. MarginLeft = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="61127-118">*element* .style.marginleft="*expression*"</span></span>

<span data-ttu-id="61127-119">*выражение* = *element*. Style. MarginLeft</span><span class="sxs-lookup"><span data-stu-id="61127-119">*expression*=*element*.style.marginleft</span></span>

<span data-ttu-id="61127-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="61127-120">**Remarks**</span></span>

<span data-ttu-id="61127-121">Атрибут **Margin-Left** аналогичен стандартному атрибуту **поля HTML Left** , используемому со таблицами стилей.</span><span class="sxs-lookup"><span data-stu-id="61127-121">The **Margin-Left** attribute is similar to the standard HTML **Margin-Left** attribute used with style sheets.</span></span>

<span data-ttu-id="61127-122">Обратите внимание, что для написания скрипта вместо **поля по левому** краю используется **MarginLeft** .</span><span class="sxs-lookup"><span data-stu-id="61127-122">Note that **marginleft** is used instead of **margin-left** for scripting.</span></span> <span data-ttu-id="61127-123">Также обратите внимание, что если **положение** **абсолютное**, поле не изменится.</span><span class="sxs-lookup"><span data-stu-id="61127-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="61127-124">Это свойство используется вместо **левой** для фигур в Microsoft Word и Microsoft Excel, которые находятся в позиции относительно точки привязки.</span><span class="sxs-lookup"><span data-stu-id="61127-124">This property is used instead of **Left** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="61127-125">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="61127-125">Values include:</span></span>



| <span data-ttu-id="61127-126">Значение</span><span class="sxs-lookup"><span data-stu-id="61127-126">Value</span></span>      | <span data-ttu-id="61127-127">Описание</span><span class="sxs-lookup"><span data-stu-id="61127-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61127-128">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="61127-128">Auto</span></span>       | <span data-ttu-id="61127-129">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="61127-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="61127-130">units</span><span class="sxs-lookup"><span data-stu-id="61127-130">units</span></span>      | <span data-ttu-id="61127-131">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61127-131">Default.</span></span> <span data-ttu-id="61127-132">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="61127-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="61127-133">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="61127-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="61127-134">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="61127-134">The default value is 0.</span></span> |
| <span data-ttu-id="61127-135">процент</span><span class="sxs-lookup"><span data-stu-id="61127-135">percentage</span></span> | <span data-ttu-id="61127-136">Значение, выраженное в процентах от высоты родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="61127-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="61127-137">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="61127-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="61127-138">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="61127-138">**See Also**</span></span>

[<span data-ttu-id="61127-139">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="61127-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="61127-140">**Пример**</span><span class="sxs-lookup"><span data-stu-id="61127-140">**Example**</span></span>

<span data-ttu-id="61127-141">Левое поле устанавливается равным 25 пикселям.</span><span class="sxs-lookup"><span data-stu-id="61127-141">The left margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



<span data-ttu-id="61127-142">[Пример атрибута Margin-Left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span><span class="sxs-lookup"><span data-stu-id="61127-142">[Margin-Left Attribute Example](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span></span> <span data-ttu-id="61127-143">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="61127-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 