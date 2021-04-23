---
title: Атрибут Бвпуре VML
description: Атрибут Бвпуре VML
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890796"
---
# <a name="vml-bwpure-attribute"></a><span data-ttu-id="0536b-103">Атрибут Бвпуре VML</span><span class="sxs-lookup"><span data-stu-id="0536b-103">VML BWPure Attribute</span></span>

<span data-ttu-id="0536b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0536b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0536b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="0536b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0536b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="0536b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0536b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0536b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0536b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0536b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0536b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0536b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0536b-110">Определяет режим черно-белого цвета для чистых и белых выходных устройств.</span><span class="sxs-lookup"><span data-stu-id="0536b-110">Defines the black-and-white mode for pure black-and-white output devices.</span></span> <span data-ttu-id="0536b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="0536b-111">Read/write.</span></span> <span data-ttu-id="0536b-112">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="0536b-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="0536b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="0536b-113">**Applies To**</span></span>

[<span data-ttu-id="0536b-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="0536b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0536b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="0536b-115">**Tag Syntax**</span></span>

<span data-ttu-id="0536b-116"><v: *element* о:бвпуре = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="0536b-116"><v: *element* o:bwpure=" *expression* "></span></span>

<span data-ttu-id="0536b-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="0536b-117">**Remarks**</span></span>

<span data-ttu-id="0536b-118">Если для [бвмоде](msdn-online-vml-bwmode-attribute.md) задано значение **Auto**, этот атрибут используется для определения способа отрисовки фигуры в чисто черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="0536b-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in pure black and white.</span></span>

<span data-ttu-id="0536b-119">Дополнительные сведения о значениях этого атрибута см. в разделе [вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="0536b-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="0536b-120">Значение по умолчанию — **Auto**.</span><span class="sxs-lookup"><span data-stu-id="0536b-120">The default is **auto**.</span></span>

<span data-ttu-id="0536b-121">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="0536b-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="0536b-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0536b-122">**Example**</span></span>

<span data-ttu-id="0536b-123">Фигура обрабатывается как изображение с высокой контрастностью для выходных данных чистого черного и белого.</span><span class="sxs-lookup"><span data-stu-id="0536b-123">The shape is processed as a high contrast image for pure black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 