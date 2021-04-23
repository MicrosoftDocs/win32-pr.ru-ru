---
title: Атрибут Алсреф (Stroke) (VML)
description: Атрибут Алсреф (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691622"
---
# <a name="althref-attribute-strokevml"></a><span data-ttu-id="39574-103">Атрибут Алсреф (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="39574-103">AltHRef Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="39574-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="39574-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="39574-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="39574-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="39574-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="39574-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="39574-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="39574-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="39574-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="39574-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="39574-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="39574-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="39574-110">Указывает альтернативную ссылку для изображения.</span><span class="sxs-lookup"><span data-stu-id="39574-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="39574-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="39574-111">Read/write.</span></span> <span data-ttu-id="39574-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="39574-112">**String**.</span></span>

<span data-ttu-id="39574-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="39574-113">**Applies To**</span></span>

[<span data-ttu-id="39574-114">Водок</span><span class="sxs-lookup"><span data-stu-id="39574-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="39574-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="39574-115">**Tag Syntax**</span></span>

<span data-ttu-id="39574-116"><v: *element* о:алсреф = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="39574-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="39574-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="39574-117">**Script Syntax**</span></span>

<span data-ttu-id="39574-118">*element* . алсреф = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="39574-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="39574-119">*выражение* = *element*. алсреф</span><span class="sxs-lookup"><span data-stu-id="39574-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="39574-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="39574-120">**Remarks**</span></span>

<span data-ttu-id="39574-121">Поддерживает сохранение данных PICT через HTML переносе.</span><span class="sxs-lookup"><span data-stu-id="39574-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="39574-122">При записи в формате HTML альтернативное представление (т. е. исходные данные PICT, если файл был создан из Macintosh) сохраняется.</span><span class="sxs-lookup"><span data-stu-id="39574-122">On HTML write, the alternate representation (i.e., the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="39574-123">При чтении HTML **алсреф** имеет приоритет над **src**.</span><span class="sxs-lookup"><span data-stu-id="39574-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="39574-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="39574-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="39574-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="39574-125">**Example**</span></span>

<span data-ttu-id="39574-126">Штрих фигуры имеет **алсреф** , указывающий на файл с именем myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="39574-126">The stroke of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 