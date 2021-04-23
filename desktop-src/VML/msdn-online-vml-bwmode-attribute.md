---
title: Атрибут Бвмоде VML
description: Атрибут Бвмоде VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792372"
---
# <a name="vml-bwmode-attribute"></a><span data-ttu-id="20caa-103">Атрибут Бвмоде VML</span><span class="sxs-lookup"><span data-stu-id="20caa-103">VML BWMode Attribute</span></span>

<span data-ttu-id="20caa-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="20caa-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="20caa-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="20caa-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="20caa-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="20caa-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="20caa-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="20caa-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="20caa-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="20caa-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="20caa-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="20caa-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="20caa-110">Определяет, как будет отображаться фигура для устройств вывода черно-белого цвета.</span><span class="sxs-lookup"><span data-stu-id="20caa-110">Determines how a shape will render for black-and-white output devices.</span></span> <span data-ttu-id="20caa-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="20caa-111">Read/write.</span></span> <span data-ttu-id="20caa-112">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="20caa-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="20caa-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="20caa-113">**Applies To**</span></span>

[<span data-ttu-id="20caa-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="20caa-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="20caa-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="20caa-115">**Tag Syntax**</span></span>

<span data-ttu-id="20caa-116"><v: *element* о:бвмоде = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="20caa-116"><v: *element* o:bwmode=" *expression* "></span></span>

<span data-ttu-id="20caa-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="20caa-117">**Remarks**</span></span>

<span data-ttu-id="20caa-118">Если фигура печатается на черно-белом принтере или отображается в виде черно-белого представления в приложении, возможны несколько вариантов.</span><span class="sxs-lookup"><span data-stu-id="20caa-118">When a shape is printed on a black-and-white printer or displayed in a black-and-white view in an application, several options are possible.</span></span> <span data-ttu-id="20caa-119">Дополнительные сведения о значениях этого атрибута см. в разделе [вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="20caa-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="20caa-120">Значение по умолчанию — **Auto**.</span><span class="sxs-lookup"><span data-stu-id="20caa-120">The default value is **auto**.</span></span>

<span data-ttu-id="20caa-121">Если указано значение **Auto** , [бвнормал](msdn-online-vml-bwnormal-attribute.md) используется для определения поведения обычных черно-белых выходных данных, а [бвпуре](msdn-online-vml-bwpure-attribute.md) используется для определения поведения для чистого вывода черно-белого цвета.</span><span class="sxs-lookup"><span data-stu-id="20caa-121">If **auto** is specified, [BWNormal](msdn-online-vml-bwnormal-attribute.md) is used to determine the behavior for normal black-and-white output, and [BWPure](msdn-online-vml-bwpure-attribute.md) is used to determine the behavior for pure black-and-white output.</span></span>

<span data-ttu-id="20caa-122">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="20caa-122">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="20caa-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="20caa-123">**Example**</span></span>

<span data-ttu-id="20caa-124">Черно-белый режим фигуры — **Auto**.</span><span class="sxs-lookup"><span data-stu-id="20caa-124">The black-and-white mode of the shape is **auto**.</span></span>


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 