---
title: Атрибут фокусировки VML
description: Атрибут фокусировки VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070599"
---
# <a name="vml-focus-attribute"></a><span data-ttu-id="c2d07-103">Атрибут фокусировки VML</span><span class="sxs-lookup"><span data-stu-id="c2d07-103">VML Focus Attribute</span></span>

<span data-ttu-id="c2d07-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c2d07-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c2d07-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c2d07-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c2d07-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c2d07-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c2d07-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2d07-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c2d07-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c2d07-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c2d07-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c2d07-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c2d07-110">Определяет центр заливки линейного градиента.</span><span class="sxs-lookup"><span data-stu-id="c2d07-110">Defines the center of a linear gradient fill.</span></span> <span data-ttu-id="c2d07-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c2d07-111">Read/write.</span></span> <span data-ttu-id="c2d07-112">**Вгфрактион**.</span><span class="sxs-lookup"><span data-stu-id="c2d07-112">**VgFraction**.</span></span>

<span data-ttu-id="c2d07-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c2d07-113">**Applies To**</span></span>

[<span data-ttu-id="c2d07-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="c2d07-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c2d07-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c2d07-115">**Tag Syntax**</span></span>

<span data-ttu-id="c2d07-116"><v: *элемент* Focus = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c2d07-116"><v: *element* focus=" *expression* "></span></span>

<span data-ttu-id="c2d07-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c2d07-117">**Script Syntax**</span></span>

<span data-ttu-id="c2d07-118">*element* . Focus = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c2d07-118">*element* .focus="*expression*"</span></span>

<span data-ttu-id="c2d07-119">*выражение* = *element*. Focus</span><span class="sxs-lookup"><span data-stu-id="c2d07-119">*expression*=*element*.focus</span></span>

<span data-ttu-id="c2d07-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c2d07-120">**Remarks**</span></span>

<span data-ttu-id="c2d07-121">Определяет начальную координату центра Blend.</span><span class="sxs-lookup"><span data-stu-id="c2d07-121">Defines the center starting position of the blend.</span></span> <span data-ttu-id="c2d07-122">Диапазон значений — от 100% до-100%.</span><span class="sxs-lookup"><span data-stu-id="c2d07-122">Values range from 100% to -100%.</span></span> <span data-ttu-id="c2d07-123">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="c2d07-123">The default value is 0.</span></span> <span data-ttu-id="c2d07-124">Значение 100% (или-100%) переместит фокус, чтобы направление смешения было обратным (в силе **Color** и **color2**).</span><span class="sxs-lookup"><span data-stu-id="c2d07-124">A value of 100% (or -100%) will shift the focus so that the direction of the blend will reverse (in effect reversing **Color** and **Color2**).</span></span> <span data-ttu-id="c2d07-125">Значение 50% изменит смешение, чтобы **Цвет** **наColor2ся** на концах, а в середине —.</span><span class="sxs-lookup"><span data-stu-id="c2d07-125">A value of 50% will change the blend so that **Color** is at both ends and **Color2** is in the middle.</span></span> <span data-ttu-id="c2d07-126">Значение-50% изменит смешение, чтобы **color2** на обоих концах, а **Цвет** — в середине.</span><span class="sxs-lookup"><span data-stu-id="c2d07-126">A value of -50% will change the blend so that **Color2** is at both ends and **Color** is in the middle.</span></span>

<span data-ttu-id="c2d07-127">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="c2d07-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="c2d07-128">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c2d07-128">**Example**</span></span>

<span data-ttu-id="c2d07-129">Фокус градиента заливки смещается таким образом, что красный **Цвет (Color**) будет полосой в центре фигуры, а верхняя и Нижняя будут синими (**color2**).</span><span class="sxs-lookup"><span data-stu-id="c2d07-129">The gradient focus of the fill is shifted so that red (**Color**) will be a band in the center of the shape and that the top and bottom will be blue (**Color2**).</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 