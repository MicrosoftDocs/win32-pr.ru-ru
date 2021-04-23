---
title: Атрибут Бвнормал VML
description: Атрибут Бвнормал VML
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070212"
---
# <a name="vml-bwnormal-attribute"></a><span data-ttu-id="126e0-103">Атрибут Бвнормал VML</span><span class="sxs-lookup"><span data-stu-id="126e0-103">VML BWNormal Attribute</span></span>

<span data-ttu-id="126e0-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="126e0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="126e0-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="126e0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="126e0-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="126e0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="126e0-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="126e0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="126e0-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="126e0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="126e0-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="126e0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="126e0-110">Определяет режим черно-белого цвета для обычных черно-белых выходных устройств.</span><span class="sxs-lookup"><span data-stu-id="126e0-110">Defines the black-and-white mode for normal black-and-white output devices.</span></span> <span data-ttu-id="126e0-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="126e0-111">Read/write.</span></span> <span data-ttu-id="126e0-112">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="126e0-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="126e0-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="126e0-113">**Applies To**</span></span>

[<span data-ttu-id="126e0-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="126e0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="126e0-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="126e0-115">**Tag Syntax**</span></span>

<span data-ttu-id="126e0-116"><v: *element* о:бвнормал = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="126e0-116"><v: *element* o:bwnormal=" *expression* "></span></span>

<span data-ttu-id="126e0-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="126e0-117">**Remarks**</span></span>

<span data-ttu-id="126e0-118">Если для [бвмоде](msdn-online-vml-bwmode-attribute.md) задано значение **Auto**, этот атрибут используется для определения способа отрисовки фигуры в нормальном черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="126e0-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in normal black and white.</span></span>

<span data-ttu-id="126e0-119">Дополнительные сведения о значениях этого атрибута см. в разделе [вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="126e0-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="126e0-120">Значение по умолчанию — **Auto**.</span><span class="sxs-lookup"><span data-stu-id="126e0-120">The default value is **auto**.</span></span>

<span data-ttu-id="126e0-121">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="126e0-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="126e0-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="126e0-122">**Example**</span></span>

<span data-ttu-id="126e0-123">Фигура обрабатывается как изображение в градациях серого для обычных черно-белых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="126e0-123">The shape is processed as a grayscale image for normal black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 