---
title: Атрибут Алсреф (Fill) (VML)
description: Атрибут Алсреф (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487885"
---
# <a name="althref-attribute-fillvml"></a><span data-ttu-id="ee662-103">Атрибут Алсреф (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="ee662-103">AltHRef Attribute (Fill)(VML)</span></span>

<span data-ttu-id="ee662-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ee662-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ee662-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ee662-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ee662-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ee662-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ee662-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee662-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ee662-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ee662-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ee662-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ee662-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ee662-110">Определяет альтернативную ссылку для изображения.</span><span class="sxs-lookup"><span data-stu-id="ee662-110">Defines an alternate reference for an image.</span></span> <span data-ttu-id="ee662-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ee662-111">Read/write.</span></span> <span data-ttu-id="ee662-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="ee662-112">**String**.</span></span>

<span data-ttu-id="ee662-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ee662-113">**Applies To**</span></span>

[<span data-ttu-id="ee662-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="ee662-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="ee662-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ee662-115">**Tag Syntax**</span></span>

<span data-ttu-id="ee662-116"><v: *element* о:алсреф = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ee662-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="ee662-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ee662-117">**Script Syntax**</span></span>

<span data-ttu-id="ee662-118">*element* . алсреф = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ee662-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="ee662-119">*выражение* = *element*. алсреф</span><span class="sxs-lookup"><span data-stu-id="ee662-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="ee662-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ee662-120">**Remarks**</span></span>

<span data-ttu-id="ee662-121">Поддерживает сохранение данных PICT через HTML переносе.</span><span class="sxs-lookup"><span data-stu-id="ee662-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="ee662-122">При записи в формате HTML альтернативное представление (исходные данные PICT, если файл был создан из Apple Macintosh) сохраняется.</span><span class="sxs-lookup"><span data-stu-id="ee662-122">On HTML write, the alternate representation (the original PICT data if the file originated from the Apple Macintosh) is saved.</span></span> <span data-ttu-id="ee662-123">При чтении HTML **алсреф** имеет приоритет над **src**.</span><span class="sxs-lookup"><span data-stu-id="ee662-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="ee662-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="ee662-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="ee662-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ee662-125">**Example**</span></span>

<span data-ttu-id="ee662-126">Заливка фигуры имеет **алсреф** , указывающую на файл с именем myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="ee662-126">The fill of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 