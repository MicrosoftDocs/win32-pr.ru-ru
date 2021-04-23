---
title: Атрибут Кроптоп VML
description: Атрибут Кроптоп VML
ms.assetid: b54939b6-0505-43b0-bf82-c3df82dc2633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8b2606c7ac5835caeecc145a885de48eaeaf8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337721"
---
# <a name="vml-croptop-attribute"></a><span data-ttu-id="a9073-103">Атрибут Кроптоп VML</span><span class="sxs-lookup"><span data-stu-id="a9073-103">VML CropTop Attribute</span></span>

<span data-ttu-id="a9073-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a9073-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a9073-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="a9073-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a9073-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="a9073-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a9073-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9073-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a9073-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a9073-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a9073-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a9073-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a9073-110">Определяет процент удаления изображения с верхней стороны.</span><span class="sxs-lookup"><span data-stu-id="a9073-110">Defines the percentage of picture removal from the top side.</span></span> <span data-ttu-id="a9073-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="a9073-111">Read/write.</span></span> <span data-ttu-id="a9073-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="a9073-112">**VgNumber**.</span></span>

<span data-ttu-id="a9073-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="a9073-113">**Applies To**</span></span>

[<span data-ttu-id="a9073-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="a9073-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="a9073-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="a9073-115">**Tag Syntax**</span></span>

<span data-ttu-id="a9073-116"><v: *element* кроптоп = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="a9073-116"><v: *element* croptop=" *expression* "></span></span>

<span data-ttu-id="a9073-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="a9073-117">**Script Syntax**</span></span>

<span data-ttu-id="a9073-118">*element* . кроптоп = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="a9073-118">*element* .croptop="*expression*"</span></span>

<span data-ttu-id="a9073-119">*выражение* = *element*. кроптоп</span><span class="sxs-lookup"><span data-stu-id="a9073-119">*expression*=*element*.croptop</span></span>

<span data-ttu-id="a9073-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="a9073-120">**Remarks**</span></span>

<span data-ttu-id="a9073-121">Объем обрезки может варьироваться от-1,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="a9073-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="a9073-122">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a9073-122">The default value is 0.</span></span> <span data-ttu-id="a9073-123">Обратите внимание, что значение 1 не будет показывать ни одного рисунка.</span><span class="sxs-lookup"><span data-stu-id="a9073-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="a9073-124">Отрицательные значения приводят к сжатию изображения из края (пустое пространство между рисунком и обрезанной границей будет заполнено цветом заливки фигуры).</span><span class="sxs-lookup"><span data-stu-id="a9073-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="a9073-125">Положительные значения меньше 1 приводят к тому, что оставшаяся картинка будет растягиваться по размеру фигуры.</span><span class="sxs-lookup"><span data-stu-id="a9073-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="a9073-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="a9073-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="a9073-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="a9073-127">**Example**</span></span>

<span data-ttu-id="a9073-128">Изображение будет сжато в виде узких Серебряный в нижней части фигуры.</span><span class="sxs-lookup"><span data-stu-id="a9073-128">The picture will be squeezed into a narrow sliver at the bottom of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata croptop="-.8" src="kids.jpg"/>
   </v:shape>
```





 

 