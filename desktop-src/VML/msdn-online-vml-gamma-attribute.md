---
title: Атрибут гаммы VML
description: Атрибут гаммы VML
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134210"
---
# <a name="vml-gamma-attribute"></a><span data-ttu-id="a6700-103">Атрибут гаммы VML</span><span class="sxs-lookup"><span data-stu-id="a6700-103">VML Gamma Attribute</span></span>

<span data-ttu-id="a6700-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a6700-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a6700-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="a6700-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a6700-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="a6700-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a6700-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a6700-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a6700-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a6700-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a6700-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a6700-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a6700-110">Определяет степень контрастности изображения.</span><span class="sxs-lookup"><span data-stu-id="a6700-110">Defines the amount of contrast for an image.</span></span> <span data-ttu-id="a6700-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="a6700-111">Read/write.</span></span> <span data-ttu-id="a6700-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="a6700-112">**VgNumber**.</span></span>

<span data-ttu-id="a6700-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="a6700-113">**Applies To**</span></span>

[<span data-ttu-id="a6700-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="a6700-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="a6700-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="a6700-115">**Tag Syntax**</span></span>

<span data-ttu-id="a6700-116"><v: гамма *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="a6700-116"><v: *element* gamma=" *expression* "></span></span>

<span data-ttu-id="a6700-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="a6700-117">**Script Syntax**</span></span>

<span data-ttu-id="a6700-118">*element* . гамма = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="a6700-118">*element* .gamma="*expression*"</span></span>

<span data-ttu-id="a6700-119">*выражение* = *элемент*. гамма</span><span class="sxs-lookup"><span data-stu-id="a6700-119">*expression*=*element*.gamma</span></span>

<span data-ttu-id="a6700-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="a6700-120">**Remarks**</span></span>

<span data-ttu-id="a6700-121">Уменьшение гаммы ниже 1 изменяет изображение, чтобы сделать его более контрастным, а значения больше 1 уменьшают контрастность.</span><span class="sxs-lookup"><span data-stu-id="a6700-121">Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast.</span></span> <span data-ttu-id="a6700-122">Полезные значения — от 0,3 до 3.</span><span class="sxs-lookup"><span data-stu-id="a6700-122">Useful values are from 0.3 to about 3.</span></span> <span data-ttu-id="a6700-123">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a6700-123">The default value is 0.</span></span>

<span data-ttu-id="a6700-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="a6700-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a6700-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="a6700-125">**Example**</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 