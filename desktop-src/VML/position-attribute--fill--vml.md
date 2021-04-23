---
title: Атрибут расположения (Заливка) (VML)
description: Атрибут расположения (Заливка) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134503"
---
# <a name="position-attribute-fillvml"></a><span data-ttu-id="c326b-103">Атрибут расположения (Заливка) (VML)</span><span class="sxs-lookup"><span data-stu-id="c326b-103">Position Attribute (Fill)(VML)</span></span>

<span data-ttu-id="c326b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c326b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c326b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c326b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c326b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c326b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c326b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c326b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c326b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c326b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c326b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c326b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c326b-110">Определяет расположение изображения заливки.</span><span class="sxs-lookup"><span data-stu-id="c326b-110">Defines the position of fill image.</span></span> <span data-ttu-id="c326b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c326b-111">Read/write.</span></span> <span data-ttu-id="c326b-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="c326b-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="c326b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c326b-113">**Applies To**</span></span>

[<span data-ttu-id="c326b-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="c326b-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c326b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c326b-115">**Tag Syntax**</span></span>

<span data-ttu-id="c326b-116"><v: расположение *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c326b-116"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="c326b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c326b-117">**Script Syntax**</span></span>

<span data-ttu-id="c326b-118">*element* . Disposition = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c326b-118">*element* .position="*expression*"</span></span>

<span data-ttu-id="c326b-119">*выражение* = *element*. позиционировать</span><span class="sxs-lookup"><span data-stu-id="c326b-119">*expression*=*element*.position</span></span>

<span data-ttu-id="c326b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c326b-120">**Remarks**</span></span>

<span data-ttu-id="c326b-121">Задает точку в фигуре для позиционирования начала изображения.</span><span class="sxs-lookup"><span data-stu-id="c326b-121">Specifies a point in the shape to position the origin of the image.</span></span> <span data-ttu-id="c326b-122">По умолчанию используется центр прямоугольника контейнера.</span><span class="sxs-lookup"><span data-stu-id="c326b-122">Default is the center of the container rectangle.</span></span> <span data-ttu-id="c326b-123">Вектор представляет собой часть ширины и высоты изображения.</span><span class="sxs-lookup"><span data-stu-id="c326b-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="c326b-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="c326b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c326b-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c326b-125">**Example**</span></span>

<span data-ttu-id="c326b-126">Изображение заливки смещается вправо до точки 50% ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="c326b-126">The image of the fill is shifted right to a point 50% of the width of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 