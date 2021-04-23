---
title: Атрибут VML XScale
description: Атрибут VML XScale
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337700"
---
# <a name="vml-xscale-attribute"></a><span data-ttu-id="0cba8-103">Атрибут VML XScale</span><span class="sxs-lookup"><span data-stu-id="0cba8-103">VML XScale Attribute</span></span>

<span data-ttu-id="0cba8-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0cba8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0cba8-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="0cba8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0cba8-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="0cba8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0cba8-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0cba8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0cba8-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0cba8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0cba8-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0cba8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0cba8-110">Определяет, будет ли использоваться прямой текстпас вместо пути к фигуре.</span><span class="sxs-lookup"><span data-stu-id="0cba8-110">Determines whether a straight textpath will be used instead of the shape path.</span></span> <span data-ttu-id="0cba8-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="0cba8-111">Read/write.</span></span> <span data-ttu-id="0cba8-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="0cba8-112">**VgTriState**.</span></span>

<span data-ttu-id="0cba8-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="0cba8-113">**Applies To**</span></span>

[<span data-ttu-id="0cba8-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="0cba8-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="0cba8-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="0cba8-115">**Tag Syntax**</span></span>

<span data-ttu-id="0cba8-116"><v: Style *элемента* = "XScale: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0cba8-116"><v: *element* style="xscale: *expression* "></span></span>

<span data-ttu-id="0cba8-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="0cba8-117">**Script Syntax**</span></span>

<span data-ttu-id="0cba8-118">*element* . Style. XScale = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="0cba8-118">*element* .style.xscale="*expression*"</span></span>

<span data-ttu-id="0cba8-119">*выражение* = *элемент*. Style. XScale</span><span class="sxs-lookup"><span data-stu-id="0cba8-119">*expression*=*element*.style.xscale</span></span>

<span data-ttu-id="0cba8-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="0cba8-120">**Remarks**</span></span>

<span data-ttu-id="0cba8-121">Если **значение равно true**, текст выполняется вдоль АПАС слева направо вдоль значения x нижней границы фигуры.</span><span class="sxs-lookup"><span data-stu-id="0cba8-121">If **True**, the text runs along apath from left to right along the x value of the lower boundary of the shape.</span></span> <span data-ttu-id="0cba8-122">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="0cba8-122">The default value is **False**.</span></span>

<span data-ttu-id="0cba8-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="0cba8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0cba8-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0cba8-124">**Example**</span></span>

<span data-ttu-id="0cba8-125">Текст будет выглядеть так, будто он был нарисован на горизонтальной линии, даже если контур фигуры является диагональным.</span><span class="sxs-lookup"><span data-stu-id="0cba8-125">The text will appear as if it were drawn on a horizontal line, even though the shape path is a diagonal.</span></span>


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 