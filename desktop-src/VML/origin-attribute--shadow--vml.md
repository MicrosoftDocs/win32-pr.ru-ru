---
title: Атрибут Origin (тень) (VML)
description: Атрибут Origin (тень) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793645"
---
# <a name="origin-attribute-shadowvml"></a><span data-ttu-id="38254-103">Атрибут Origin (тень) (VML)</span><span class="sxs-lookup"><span data-stu-id="38254-103">Origin Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="38254-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="38254-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="38254-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="38254-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="38254-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="38254-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="38254-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38254-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="38254-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="38254-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="38254-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="38254-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="38254-110">Определяет центр тени.</span><span class="sxs-lookup"><span data-stu-id="38254-110">Defines the center of the shadow.</span></span> <span data-ttu-id="38254-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="38254-111">Read/write.</span></span> <span data-ttu-id="38254-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="38254-112">**VgVector2D**.</span></span>

<span data-ttu-id="38254-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="38254-113">**Applies To**</span></span>

[<span data-ttu-id="38254-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="38254-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="38254-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="38254-115">**Tag Syntax**</span></span>

<span data-ttu-id="38254-116"><v: *элемент* Origin = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="38254-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="38254-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="38254-117">**Script Syntax**</span></span>

<span data-ttu-id="38254-118">*element* . Origin = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="38254-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="38254-119">*выражение* = *элемент*. Origin</span><span class="sxs-lookup"><span data-stu-id="38254-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="38254-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="38254-120">**Remarks**</span></span>

<span data-ttu-id="38254-121">Пара дробных значений фигуры в диапазоне от 50% до-50%.</span><span class="sxs-lookup"><span data-stu-id="38254-121">A pair of fractional values of the shape, ranging from 50% to -50%.</span></span> <span data-ttu-id="38254-122">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="38254-122">The default value is 0,0.</span></span>

<span data-ttu-id="38254-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="38254-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="38254-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="38254-124">**Example**</span></span>

<span data-ttu-id="38254-125">Тень имеет начало координат, равное 20% вниз и 20% справа от начала координат фигуры.</span><span class="sxs-lookup"><span data-stu-id="38254-125">The shadow has an origin that is 20% down and 20% to the right of the shape's origin.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 