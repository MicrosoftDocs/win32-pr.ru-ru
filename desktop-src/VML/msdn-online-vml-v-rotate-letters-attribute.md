---
title: Атрибут VML V-поверните-Letters
description: Атрибут VML V-поверните-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133943"
---
# <a name="vml-v-rotate-letters-attribute"></a><span data-ttu-id="2a604-103">Атрибут VML V-поверните-Letters</span><span class="sxs-lookup"><span data-stu-id="2a604-103">VML V-Rotate-Letters Attribute</span></span>

<span data-ttu-id="2a604-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2a604-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2a604-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="2a604-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2a604-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="2a604-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2a604-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2a604-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2a604-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2a604-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2a604-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2a604-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2a604-110">Определяет, поворачиваются ли буквы текста.</span><span class="sxs-lookup"><span data-stu-id="2a604-110">Determines whether the letters of the text are rotated.</span></span> <span data-ttu-id="2a604-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="2a604-111">Read/write.</span></span> <span data-ttu-id="2a604-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="2a604-112">**VgTriState**.</span></span>

<span data-ttu-id="2a604-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="2a604-113">**Applies To**</span></span>

[<span data-ttu-id="2a604-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="2a604-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="2a604-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="2a604-115">**Tag Syntax**</span></span>

<span data-ttu-id="2a604-116"><v: Style *элемента* = "v-вращение-Letters: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="2a604-116"><v: *element* style="v-rotate-letters: *expression* "></span></span>

<span data-ttu-id="2a604-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="2a604-117">**Script Syntax**</span></span>

<span data-ttu-id="2a604-118">*element* . Style. v-вращение-Letters = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="2a604-118">*element* .style.v-rotate-letters="*expression*"</span></span>

<span data-ttu-id="2a604-119">*выражение* = *element*. Style. v-вращение-буквы</span><span class="sxs-lookup"><span data-stu-id="2a604-119">*expression*=*element*.style.v-rotate-letters</span></span>

<span data-ttu-id="2a604-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="2a604-120">**Remarks**</span></span>

<span data-ttu-id="2a604-121">Если **значение равно true**, буквы текста поворачиваются в 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="2a604-121">If **True**, the letters of the text are rotated 90 degrees.</span></span> <span data-ttu-id="2a604-122">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="2a604-122">The default value is **False**.</span></span>

<span data-ttu-id="2a604-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="2a604-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="2a604-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="2a604-124">**Example**</span></span>

<span data-ttu-id="2a604-125">Буквы поворачиваются на 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="2a604-125">The letters are rotated 90 degrees.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 