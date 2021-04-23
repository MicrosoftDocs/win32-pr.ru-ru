---
title: Атрибут вставки VML
description: Атрибут вставки VML
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134030"
---
# <a name="vml-inset-attribute"></a><span data-ttu-id="4f39b-103">Атрибут вставки VML</span><span class="sxs-lookup"><span data-stu-id="4f39b-103">VML Inset Attribute</span></span>

<span data-ttu-id="4f39b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4f39b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4f39b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4f39b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4f39b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="4f39b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4f39b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4f39b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4f39b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4f39b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4f39b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4f39b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4f39b-110">Задает значения внутренних полей для текстового поля.</span><span class="sxs-lookup"><span data-stu-id="4f39b-110">Specifies inner margin values for textbox text.</span></span> <span data-ttu-id="4f39b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="4f39b-111">Read/write.</span></span> <span data-ttu-id="4f39b-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="4f39b-112">**String**.</span></span>

<span data-ttu-id="4f39b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="4f39b-113">**Applies To**</span></span>

[<span data-ttu-id="4f39b-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="4f39b-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="4f39b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="4f39b-115">**Tag Syntax**</span></span>

<span data-ttu-id="4f39b-116"><v: вставка *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="4f39b-116"><v: *element* inset=" *expression* "></span></span>

<span data-ttu-id="4f39b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="4f39b-117">**Script Syntax**</span></span>

<span data-ttu-id="4f39b-118">*element* . вкладыш = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="4f39b-118">*element* .inset="*expression*"</span></span>

<span data-ttu-id="4f39b-119">*выражение* = *element*. вкладыш</span><span class="sxs-lookup"><span data-stu-id="4f39b-119">*expression*=*element*.inset</span></span>

<span data-ttu-id="4f39b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="4f39b-120">**Remarks**</span></span>

<span data-ttu-id="4f39b-121">Внутреннее значение текстового поля задается как строка, содержащая четыре значения, разделенные запятыми или пробелами.</span><span class="sxs-lookup"><span data-stu-id="4f39b-121">The internal text margin value is specified as a string containing four values, each separated by commas or spaces.</span></span> <span data-ttu-id="4f39b-122">Величина отступа измеряется слева, сверху, справа и снизу от нижнего края поля, заданного атрибутом [Текстбоксрект](msdn-online-vml-textboxrect-attribute.md) **пути**.</span><span class="sxs-lookup"><span data-stu-id="4f39b-122">The values measure inset from the left, top, right, and bottom edges of the box specified by the [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) attribute of **Path**.</span></span> <span data-ttu-id="4f39b-123">Отсутствующие значения задаются по умолчанию: "0,1 в, 0,05 в, 0,1 в, 0,05 в".</span><span class="sxs-lookup"><span data-stu-id="4f39b-123">Missing values are set to the default, which is "0.1in, 0.05in, 0.1in, 0.05in".</span></span>

<span data-ttu-id="4f39b-124">Для повернутых фигур в браузерах, которые не поддерживают поворот, ограничивающий прямоугольник будет привязан к ближайшему к 90 градусам.</span><span class="sxs-lookup"><span data-stu-id="4f39b-124">For rotated shapes in browsers that do not support rotation, the bounding box will snap to the closest multiple of 90 degrees.</span></span>

<span data-ttu-id="4f39b-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="4f39b-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="4f39b-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="4f39b-126">**Example**</span></span>

<span data-ttu-id="4f39b-127">Текстовое поле будет иметь отступ в 10 пикселей.</span><span class="sxs-lookup"><span data-stu-id="4f39b-127">The textbox will have an inset margin of 10 pixels.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 