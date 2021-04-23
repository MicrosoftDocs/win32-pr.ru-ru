---
title: VML V-Text-обратный атрибут
description: VML V-Text-обратный атрибут
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070309"
---
# <a name="vml-v-text-reverse-attribute"></a><span data-ttu-id="d6646-103">VML V-Text-обратный атрибут</span><span class="sxs-lookup"><span data-stu-id="d6646-103">VML V-Text-Reverse Attribute</span></span>

<span data-ttu-id="d6646-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d6646-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d6646-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d6646-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d6646-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d6646-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d6646-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d6646-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d6646-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d6646-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d6646-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d6646-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d6646-110">Определяет, изменяется ли порядок макета строк на обратный.</span><span class="sxs-lookup"><span data-stu-id="d6646-110">Determines whether the layout order of rows is reversed.</span></span> <span data-ttu-id="d6646-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d6646-111">Read/write.</span></span> <span data-ttu-id="d6646-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="d6646-112">**VgTriState**.</span></span>

<span data-ttu-id="d6646-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="d6646-113">**Applies To**</span></span>

[<span data-ttu-id="d6646-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="d6646-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="d6646-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="d6646-115">**Tag Syntax**</span></span>

<span data-ttu-id="d6646-116"><v: Style *элемента* = "v-Text-Reverse: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="d6646-116"><v: *element* style="v-text-reverse: *expression* "></span></span>

<span data-ttu-id="d6646-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="d6646-117">**Script Syntax**</span></span>

<span data-ttu-id="d6646-118">*element* . Style. v-Text-Reverse = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="d6646-118">*element* .style.v-text-reverse="*expression*"</span></span>

<span data-ttu-id="d6646-119">*выражение* = *element*. Style. v-Text-Reverse</span><span class="sxs-lookup"><span data-stu-id="d6646-119">*expression*=*element*.style.v-text-reverse</span></span>

<span data-ttu-id="d6646-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="d6646-120">**Remarks**</span></span>

<span data-ttu-id="d6646-121">Если **значение равно true**, порядок расположения строк изменяется на обратный.</span><span class="sxs-lookup"><span data-stu-id="d6646-121">If **True**, the layout order of rows is reversed.</span></span> <span data-ttu-id="d6646-122">Этот атрибут используется для вертикального макета текста.</span><span class="sxs-lookup"><span data-stu-id="d6646-122">This attribute is used for vertical text layout.</span></span> <span data-ttu-id="d6646-123">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="d6646-123">The default value is **False**.</span></span>

<span data-ttu-id="d6646-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="d6646-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d6646-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="d6646-125">**Example**</span></span>

<span data-ttu-id="d6646-126">Порядок макета изменяется на обратный.</span><span class="sxs-lookup"><span data-stu-id="d6646-126">The layout order is reversed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 