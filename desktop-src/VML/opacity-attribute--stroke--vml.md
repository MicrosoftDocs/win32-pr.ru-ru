---
title: Атрибут непрозрачности (Stroke) (VML)
description: Атрибут непрозрачности (Stroke) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488241"
---
# <a name="opacity-attribute-strokevml"></a><span data-ttu-id="ffc53-103">Атрибут непрозрачности (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="ffc53-103">Opacity Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="ffc53-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ffc53-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ffc53-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ffc53-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ffc53-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ffc53-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ffc53-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ffc53-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ffc53-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ffc53-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ffc53-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ffc53-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ffc53-110">Определяет степень прозрачности штриха.</span><span class="sxs-lookup"><span data-stu-id="ffc53-110">Defines the amount of transparency of a stroke.</span></span> <span data-ttu-id="ffc53-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ffc53-111">Read/write.</span></span> <span data-ttu-id="ffc53-112">**Вгфрактион**.</span><span class="sxs-lookup"><span data-stu-id="ffc53-112">**VgFraction**.</span></span>

<span data-ttu-id="ffc53-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ffc53-113">**Applies To**</span></span>

[<span data-ttu-id="ffc53-114">Водок</span><span class="sxs-lookup"><span data-stu-id="ffc53-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="ffc53-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ffc53-115">**Tag Syntax**</span></span>

<span data-ttu-id="ffc53-116"><v: Opacity *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ffc53-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="ffc53-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ffc53-117">**Script Syntax**</span></span>

<span data-ttu-id="ffc53-118">*element* . Opacity = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ffc53-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="ffc53-119">*выражение* = *элемент*. Opacity</span><span class="sxs-lookup"><span data-stu-id="ffc53-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="ffc53-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ffc53-120">**Remarks**</span></span>

<span data-ttu-id="ffc53-121">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="ffc53-121">The default value is 1.0.</span></span>

<span data-ttu-id="ffc53-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="ffc53-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="ffc53-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ffc53-123">**Example**</span></span>

<span data-ttu-id="ffc53-124">Штрих имеет прозрачный 50%.</span><span class="sxs-lookup"><span data-stu-id="ffc53-124">The stroke is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 