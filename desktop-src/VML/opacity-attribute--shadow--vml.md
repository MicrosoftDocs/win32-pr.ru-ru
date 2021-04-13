---
title: Атрибут непрозрачности (тень) (VML)
description: Атрибут непрозрачности (тень) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413094"
---
# <a name="opacity-attribute-shadowvml"></a><span data-ttu-id="306e4-103">Атрибут непрозрачности (тень) (VML)</span><span class="sxs-lookup"><span data-stu-id="306e4-103">Opacity Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="306e4-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="306e4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="306e4-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="306e4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="306e4-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="306e4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="306e4-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="306e4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="306e4-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="306e4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="306e4-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="306e4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="306e4-110">Определяет прозрачность тени.</span><span class="sxs-lookup"><span data-stu-id="306e4-110">Determines the transparency of a shadow.</span></span> <span data-ttu-id="306e4-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="306e4-111">Read/write.</span></span> <span data-ttu-id="306e4-112">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="306e4-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="306e4-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="306e4-113">**Applies To**</span></span>

[<span data-ttu-id="306e4-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="306e4-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="306e4-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="306e4-115">**Tag Syntax**</span></span>

<span data-ttu-id="306e4-116"><v: Opacity *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="306e4-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="306e4-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="306e4-117">**Script Syntax**</span></span>

<span data-ttu-id="306e4-118">*element* . Opacity = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="306e4-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="306e4-119">*выражение* = *элемент*. Opacity</span><span class="sxs-lookup"><span data-stu-id="306e4-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="306e4-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="306e4-120">**Remarks**</span></span>

<span data-ttu-id="306e4-121">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="306e4-121">The default value is 1.</span></span> <span data-ttu-id="306e4-122">Значение 0 выполнит прозрачную тень.</span><span class="sxs-lookup"><span data-stu-id="306e4-122">A value of 0 will make a completely transparent shadow.</span></span>

<span data-ttu-id="306e4-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="306e4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="306e4-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="306e4-124">**Example**</span></span>

<span data-ttu-id="306e4-125">Фигура имеет тень на 50% прозрачна.</span><span class="sxs-lookup"><span data-stu-id="306e4-125">The shape has a shadow that is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 