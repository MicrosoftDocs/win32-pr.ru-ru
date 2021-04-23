---
title: Атрибут Фокуссизе VML
description: Атрибут Фокуссизе VML
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070597"
---
# <a name="vml-focussize-attribute"></a><span data-ttu-id="91bec-103">Атрибут Фокуссизе VML</span><span class="sxs-lookup"><span data-stu-id="91bec-103">VML FocusSize Attribute</span></span>

<span data-ttu-id="91bec-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="91bec-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="91bec-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="91bec-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="91bec-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="91bec-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="91bec-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91bec-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="91bec-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="91bec-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="91bec-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="91bec-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="91bec-110">Определяет размер фокуса для радиальных заливок.</span><span class="sxs-lookup"><span data-stu-id="91bec-110">Defines the focus size for radial fills.</span></span> <span data-ttu-id="91bec-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="91bec-111">Read/write.</span></span> <span data-ttu-id="91bec-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="91bec-112">**VgVector2D**.</span></span>

<span data-ttu-id="91bec-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="91bec-113">**Applies To**</span></span>

[<span data-ttu-id="91bec-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="91bec-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="91bec-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="91bec-115">**Tag Syntax**</span></span>

<span data-ttu-id="91bec-116"><v: *element* фокуссизе = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="91bec-116"><v: *element* focussize=" *expression* "></span></span>

<span data-ttu-id="91bec-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="91bec-117">**Script Syntax**</span></span>

<span data-ttu-id="91bec-118">*element* . фокуссизе = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="91bec-118">*element* .focussize="*expression*"</span></span>

<span data-ttu-id="91bec-119">*выражение* = *element*. фокуссизе</span><span class="sxs-lookup"><span data-stu-id="91bec-119">*expression*=*element*.focussize</span></span>

<span data-ttu-id="91bec-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="91bec-120">**Remarks**</span></span>

<span data-ttu-id="91bec-121">Значения — это части ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="91bec-121">The values are fractions of the width and height of the shape.</span></span> <span data-ttu-id="91bec-122">Первый — это процентная доля от заполнения до правого края фигуры, а вторая — процент от заливки до конца фигуры.</span><span class="sxs-lookup"><span data-stu-id="91bec-122">The first is a percentage of the fill to the right edge of the shape and the second is a percentage of the fill to the bottom of the shape.</span></span> <span data-ttu-id="91bec-123">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="91bec-123">The default value is 0,0.</span></span> <span data-ttu-id="91bec-124">Значение **фокуссизе** , равное 100%, 100% и **фокуспоситион** 0, 0, приведет к полному переходу color2.</span><span class="sxs-lookup"><span data-stu-id="91bec-124">A **FocusSize** value of 100%,100% and a **FocusPosition** of 0,0 would make Color2 dominate the blend completely.</span></span> <span data-ttu-id="91bec-125">Для сбалансированных смешений рекомендуется использовать небольшие значения около 10%, 10%.</span><span class="sxs-lookup"><span data-stu-id="91bec-125">Small values of around 10%,10% are recommended for balanced blends.</span></span>

<span data-ttu-id="91bec-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="91bec-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="91bec-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="91bec-127">**Example**</span></span>

<span data-ttu-id="91bec-128">Радиальная заливка создаст смешение, начинающееся синим цветом, и становится красным на всех четырех краях.</span><span class="sxs-lookup"><span data-stu-id="91bec-128">The radial fill will create a blend starting in the center as blue and becoming red on all four edges.</span></span> <span data-ttu-id="91bec-129">Центр Blend определяется **фокуспоситион** , а размер внутреннего начального цвета определяется **фокуссизе**.</span><span class="sxs-lookup"><span data-stu-id="91bec-129">The center of the blend is defined by **FocusPosition** and the size of the inner starting color is determined by **FocusSize**.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 