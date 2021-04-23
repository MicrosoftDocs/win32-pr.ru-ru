---
title: Атрибут VML V
description: Атрибут VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134066"
---
# <a name="vml-v-attribute"></a><span data-ttu-id="1da41-103">Атрибут VML V</span><span class="sxs-lookup"><span data-stu-id="1da41-103">VML V Attribute</span></span>

<span data-ttu-id="1da41-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1da41-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1da41-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="1da41-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1da41-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="1da41-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1da41-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1da41-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1da41-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1da41-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1da41-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1da41-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1da41-110">Определяет команды, составляющие путь.</span><span class="sxs-lookup"><span data-stu-id="1da41-110">Defines the commands that make up a path.</span></span> <span data-ttu-id="1da41-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1da41-111">Read/write.</span></span> <span data-ttu-id="1da41-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="1da41-112">**String**.</span></span>

<span data-ttu-id="1da41-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="1da41-113">**Applies To**</span></span>

[<span data-ttu-id="1da41-114">Путь</span><span class="sxs-lookup"><span data-stu-id="1da41-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="1da41-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="1da41-115">**Tag Syntax**</span></span>

<span data-ttu-id="1da41-116"><v: *element* v = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="1da41-116"><v: *element* v=" *expression* "></span></span>

<span data-ttu-id="1da41-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="1da41-117">**Script Syntax**</span></span>

<span data-ttu-id="1da41-118">*element* . v = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="1da41-118">*element* .v="*expression*"</span></span>

<span data-ttu-id="1da41-119">*выражение* = *element*. v</span><span class="sxs-lookup"><span data-stu-id="1da41-119">*expression*=*element*.v</span></span>

<span data-ttu-id="1da41-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="1da41-120">**Remarks**</span></span>

<span data-ttu-id="1da41-121">Переопределяет атрибут **path** фигуры.</span><span class="sxs-lookup"><span data-stu-id="1da41-121">Overrides the **Path** attribute of a shape.</span></span> <span data-ttu-id="1da41-122">Координаты могут быть фиксированными числами, относительными числами или ссылками на формулы (с использованием формата " @n ", где n — номер формулы; например, " @2 " ссылается на вторую формулу в массиве формул).</span><span class="sxs-lookup"><span data-stu-id="1da41-122">Coordinates can be fixed numbers, relative numbers, or references to formulas (by using the format of "@n" where n is a formula number; for example, "@2" refers to the second formula in the formula array).</span></span>

<span data-ttu-id="1da41-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="1da41-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1da41-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="1da41-124">**Example**</span></span>

<span data-ttu-id="1da41-125">Прямоугольник создается с помощью атрибута **V** .</span><span class="sxs-lookup"><span data-stu-id="1da41-125">A rectangle is created using the **V** attribute.</span></span> <span data-ttu-id="1da41-126">Обратите внимание, что после первого набора координат с разделителями-запятыми используется строчная буква L (**lineTo** ).</span><span class="sxs-lookup"><span data-stu-id="1da41-126">Note that a lowercase letter L (**lineto** command) is used after the first set of comma-delimited coordinates.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 