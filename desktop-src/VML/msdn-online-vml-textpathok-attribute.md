---
title: Атрибут Текстпасок VML
description: Атрибут Текстпасок VML
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890692"
---
# <a name="vml-textpathok-attribute"></a><span data-ttu-id="7fcad-103">Атрибут Текстпасок VML</span><span class="sxs-lookup"><span data-stu-id="7fcad-103">VML TextPathOK Attribute</span></span>

<span data-ttu-id="7fcad-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7fcad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7fcad-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7fcad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7fcad-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7fcad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7fcad-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7fcad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7fcad-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7fcad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7fcad-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7fcad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7fcad-110">Определяет, будет ли отображаться текстовый путь.</span><span class="sxs-lookup"><span data-stu-id="7fcad-110">Determines whether a text path will be displayed.</span></span> <span data-ttu-id="7fcad-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7fcad-111">Read/write.</span></span> <span data-ttu-id="7fcad-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="7fcad-112">**VgTriState**.</span></span>

<span data-ttu-id="7fcad-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="7fcad-113">**Applies To**</span></span>

[<span data-ttu-id="7fcad-114">Путь</span><span class="sxs-lookup"><span data-stu-id="7fcad-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="7fcad-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="7fcad-115">**Tag Syntax**</span></span>

<span data-ttu-id="7fcad-116"><v: *element* текстпасок = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="7fcad-116"><v: *element* textpathok=" *expression* "></span></span>

<span data-ttu-id="7fcad-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="7fcad-117">**Script Syntax**</span></span>

<span data-ttu-id="7fcad-118">*элемент* .</span><span class="sxs-lookup"><span data-stu-id="7fcad-118">*element* .</span></span> <span data-ttu-id="7fcad-119">текстпасок = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="7fcad-119">textpathok= "*expression*"</span></span>

<span data-ttu-id="7fcad-120">*выражение* = *элемент*.</span><span class="sxs-lookup"><span data-stu-id="7fcad-120">*expression*=*element*.</span></span> <span data-ttu-id="7fcad-121">текстпасок</span><span class="sxs-lookup"><span data-stu-id="7fcad-121">textpathok</span></span>

<span data-ttu-id="7fcad-122">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="7fcad-122">**Remarks**</span></span>

<span data-ttu-id="7fcad-123">Если **значение равно false**, путь не может иметь текстовый путь.</span><span class="sxs-lookup"><span data-stu-id="7fcad-123">If **False**, the path cannot have a text path.</span></span> <span data-ttu-id="7fcad-124">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="7fcad-124">The default is **False**.</span></span> <span data-ttu-id="7fcad-125">Этот атрибут должен иметь значение **true** для вывода текста по пути.</span><span class="sxs-lookup"><span data-stu-id="7fcad-125">You must have this attribute set to **True** to display text on a path.</span></span>

<span data-ttu-id="7fcad-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="7fcad-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="7fcad-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="7fcad-127">**Example**</span></span>

<span data-ttu-id="7fcad-128">Фигура имеет текстовый путь.</span><span class="sxs-lookup"><span data-stu-id="7fcad-128">The shape has a text path.</span></span> <span data-ttu-id="7fcad-129">Текст "Hello VML" отображается в виде кривой в форме улыбающихся фигур.</span><span class="sxs-lookup"><span data-stu-id="7fcad-129">The text "Hello VML" is displayed along a smile-shaped curve.</span></span>


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 