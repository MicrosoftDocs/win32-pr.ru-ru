---
title: Атрибут Кропригхт VML
description: Атрибут Кропригхт VML
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21604fb341840847690e9e086386d46f7124908a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487769"
---
# <a name="vml-cropright-attribute"></a><span data-ttu-id="9be50-103">Атрибут Кропригхт VML</span><span class="sxs-lookup"><span data-stu-id="9be50-103">VML CropRight Attribute</span></span>

<span data-ttu-id="9be50-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9be50-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9be50-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="9be50-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9be50-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="9be50-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9be50-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be50-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9be50-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9be50-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9be50-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9be50-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9be50-110">Определяет процент удаления изображения с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="9be50-110">Defines the percentage of picture removal from the right side.</span></span> <span data-ttu-id="9be50-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="9be50-111">Read/write.</span></span> <span data-ttu-id="9be50-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="9be50-112">**VgNumber**.</span></span>

<span data-ttu-id="9be50-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="9be50-113">**Applies To**</span></span>

[<span data-ttu-id="9be50-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="9be50-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="9be50-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="9be50-115">**Tag Syntax**</span></span>

<span data-ttu-id="9be50-116"><v: *element* кропригхт = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="9be50-116"><v: *element* cropright=" *expression* "></span></span>

<span data-ttu-id="9be50-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="9be50-117">**Script Syntax**</span></span>

<span data-ttu-id="9be50-118">*element* . кропригхт = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="9be50-118">*element* .cropright="*expression*"</span></span>

<span data-ttu-id="9be50-119">*выражение* = *element*. кропригхт</span><span class="sxs-lookup"><span data-stu-id="9be50-119">*expression*=*element*.cropright</span></span>

<span data-ttu-id="9be50-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="9be50-120">**Remarks**</span></span>

<span data-ttu-id="9be50-121">Объем обрезки может варьироваться от-1,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9be50-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="9be50-122">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="9be50-122">The default value is 0.</span></span> <span data-ttu-id="9be50-123">Обратите внимание, что значение 1 не будет показывать ни одного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9be50-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="9be50-124">Отрицательные значения приводят к сжатию изображения из края (пустое пространство между рисунком и обрезанной границей будет заполнено цветом заливки фигуры).</span><span class="sxs-lookup"><span data-stu-id="9be50-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="9be50-125">Положительные значения меньше 1 приводят к тому, что оставшаяся картинка будет растягиваться по размеру фигуры.</span><span class="sxs-lookup"><span data-stu-id="9be50-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="9be50-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="9be50-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="9be50-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="9be50-127">**Example**</span></span>

<span data-ttu-id="9be50-128">Изображение будет сжато с правой стороны на 20% от ширины.</span><span class="sxs-lookup"><span data-stu-id="9be50-128">The picture will be squeezed from the right side by 20% of the width.</span></span> <span data-ttu-id="9be50-129">Пустое пространство между изображением и правым ребром будет заполнено цветом заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="9be50-129">The empty space between the picture and the right edge will be filled by the fill color of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 