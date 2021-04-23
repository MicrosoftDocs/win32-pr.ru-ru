---
title: На атрибуте (shadow) (VML)
description: На атрибуте (shadow) (VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987718"
---
# <a name="on-attribute-shadowvml"></a><span data-ttu-id="d584b-103">На атрибуте (shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="d584b-103">On Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="d584b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d584b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d584b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d584b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d584b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d584b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d584b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d584b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d584b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d584b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d584b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d584b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d584b-110">Определяет, будет ли отображаться тень.</span><span class="sxs-lookup"><span data-stu-id="d584b-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="d584b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d584b-111">Read/write.</span></span> <span data-ttu-id="d584b-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="d584b-112">**VgTriState**.</span></span>

<span data-ttu-id="d584b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="d584b-113">**Applies To**</span></span>

[<span data-ttu-id="d584b-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="d584b-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="d584b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="d584b-115">**Tag Syntax**</span></span>

<span data-ttu-id="d584b-116"><v: *element* on = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="d584b-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="d584b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="d584b-117">**Script Syntax**</span></span>

<span data-ttu-id="d584b-118">*element* . on = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="d584b-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="d584b-119">*выражение* = *element*. on</span><span class="sxs-lookup"><span data-stu-id="d584b-119">*expression*=*element*.on</span></span>

<span data-ttu-id="d584b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="d584b-120">**Remarks**</span></span>

<span data-ttu-id="d584b-121">Если **значение — true**, теневое отображение будет отображено.</span><span class="sxs-lookup"><span data-stu-id="d584b-121">If **True**, the shadow will be displayed.</span></span> <span data-ttu-id="d584b-122">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="d584b-122">The default value is **False**.</span></span>

<span data-ttu-id="d584b-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="d584b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="d584b-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="d584b-124">**Example**</span></span>

<span data-ttu-id="d584b-125">Будет отображена тень.</span><span class="sxs-lookup"><span data-stu-id="d584b-125">The shadow will be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 