---
title: Атрибут color2 (Fill) (VML)
description: Атрибут color2 (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672355"
---
# <a name="color2-attribute-fillvml"></a><span data-ttu-id="b37a2-103">Атрибут color2 (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="b37a2-103">Color2 Attribute (Fill)(VML)</span></span>

<span data-ttu-id="b37a2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b37a2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b37a2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b37a2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b37a2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b37a2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b37a2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b37a2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b37a2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b37a2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b37a2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b37a2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b37a2-110">Определяет второй цвет для заливок.</span><span class="sxs-lookup"><span data-stu-id="b37a2-110">Defines a second color for fills.</span></span> <span data-ttu-id="b37a2-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b37a2-111">Read/write.</span></span> <span data-ttu-id="b37a2-112">[Вгколор](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="b37a2-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="b37a2-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b37a2-113">**Applies To**</span></span>

[<span data-ttu-id="b37a2-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="b37a2-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="b37a2-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b37a2-115">**Tag Syntax**</span></span>

<span data-ttu-id="b37a2-116"><v: *element* color2 = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b37a2-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="b37a2-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="b37a2-117">**Script Syntax**</span></span>

<span data-ttu-id="b37a2-118">*element* . color2 = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="b37a2-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="b37a2-119">*выражение* = *element*. color2</span><span class="sxs-lookup"><span data-stu-id="b37a2-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="b37a2-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b37a2-120">**Remarks**</span></span>

<span data-ttu-id="b37a2-121">Второй цвет используется, если тип заливки является шаблоном или градиентом.</span><span class="sxs-lookup"><span data-stu-id="b37a2-121">A second color is used when a fill type is a pattern or a gradient.</span></span> <span data-ttu-id="b37a2-122">Значение по умолчанию — **белый**.</span><span class="sxs-lookup"><span data-stu-id="b37a2-122">The default value is **White**.</span></span>

<span data-ttu-id="b37a2-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="b37a2-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b37a2-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="b37a2-124">**Example**</span></span>

<span data-ttu-id="b37a2-125">Тип заливки фигуры — это шаблон, где Заливка переднего плана определяется исходным изображением, но прозрачный фон определяется вторым цветом.</span><span class="sxs-lookup"><span data-stu-id="b37a2-125">The shape's fill type is a pattern where the foreground fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 