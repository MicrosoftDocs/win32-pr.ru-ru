---
title: Атрибут Color (тень) (VML)
description: Атрибут Color (тень) (VML)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691526"
---
# <a name="color-attribute-shadowvml"></a><span data-ttu-id="bd0df-103">Атрибут Color (тень) (VML)</span><span class="sxs-lookup"><span data-stu-id="bd0df-103">Color Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="bd0df-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bd0df-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bd0df-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="bd0df-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bd0df-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="bd0df-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bd0df-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bd0df-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bd0df-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bd0df-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bd0df-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bd0df-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bd0df-110">Определяет цвет тени.</span><span class="sxs-lookup"><span data-stu-id="bd0df-110">Defines the color of the shadow.</span></span> <span data-ttu-id="bd0df-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="bd0df-111">Read/write.</span></span> <span data-ttu-id="bd0df-112">**Вгколор**.</span><span class="sxs-lookup"><span data-stu-id="bd0df-112">**VgColor**.</span></span>

<span data-ttu-id="bd0df-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="bd0df-113">**Applies To**</span></span>

[<span data-ttu-id="bd0df-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="bd0df-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="bd0df-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="bd0df-115">**Tag Syntax**</span></span>

<span data-ttu-id="bd0df-116"><v: Color *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="bd0df-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="bd0df-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="bd0df-117">**Script Syntax**</span></span>

<span data-ttu-id="bd0df-118">*element* . Color = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="bd0df-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="bd0df-119">*выражение* = *элемент*. Color</span><span class="sxs-lookup"><span data-stu-id="bd0df-119">*expression*=*element*.color</span></span>

<span data-ttu-id="bd0df-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="bd0df-120">**Remarks**</span></span>

<span data-ttu-id="bd0df-121">Используйте атрибут Color, чтобы задать или получить цвет тени.</span><span class="sxs-lookup"><span data-stu-id="bd0df-121">Use the color attribute to set or get the color of a shadow.</span></span>

<span data-ttu-id="bd0df-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="bd0df-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="bd0df-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="bd0df-123">**Example**</span></span>

<span data-ttu-id="bd0df-124">Тень горит зеленым цветом.</span><span class="sxs-lookup"><span data-stu-id="bd0df-124">The shadow is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 