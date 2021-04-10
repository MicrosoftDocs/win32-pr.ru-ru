---
title: Атрибут Trim VML
description: Атрибут Trim VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f7aa2ce17d5b2b8df772954cee323e3d5ea2db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891005"
---
# <a name="vml-trim-attribute"></a><span data-ttu-id="bb7ee-103">Атрибут Trim VML</span><span class="sxs-lookup"><span data-stu-id="bb7ee-103">VML Trim Attribute</span></span>

<span data-ttu-id="bb7ee-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bb7ee-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bb7ee-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bb7ee-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bb7ee-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bb7ee-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bb7ee-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bb7ee-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bb7ee-110">Определяет, удаляется ли дополнительное пространство выше и ниже текста.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-110">Determines whether extra space is removed above and below the text.</span></span> <span data-ttu-id="bb7ee-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-111">Read/write.</span></span> <span data-ttu-id="bb7ee-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-112">**VgTriState**.</span></span>

<span data-ttu-id="bb7ee-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="bb7ee-113">**Applies To**</span></span>

[<span data-ttu-id="bb7ee-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="bb7ee-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="bb7ee-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="bb7ee-115">**Tag Syntax**</span></span>

<span data-ttu-id="bb7ee-116"><v: Style *элемента* = "Trim: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="bb7ee-116"><v: *element* style="trim: *expression* "></span></span>

<span data-ttu-id="bb7ee-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="bb7ee-117">**Script Syntax**</span></span>

<span data-ttu-id="bb7ee-118">*element* . Style. Trim = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="bb7ee-118">*element* .style.trim="*expression*"</span></span>

<span data-ttu-id="bb7ee-119">*выражение* = *element*. Style. Trim</span><span class="sxs-lookup"><span data-stu-id="bb7ee-119">*expression*=*element*.style.trim</span></span>

<span data-ttu-id="bb7ee-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="bb7ee-120">**Remarks**</span></span>

<span data-ttu-id="bb7ee-121">Если **значение — true**, пространство, зарезервированное для верхних и нижних колонтитулов, удаляется.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-121">If **True**, space reserved for ascenders and descenders is removed.</span></span> <span data-ttu-id="bb7ee-122">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-122">The default value is **False**.</span></span>

<span data-ttu-id="bb7ee-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="bb7ee-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bb7ee-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="bb7ee-124">**Example**</span></span>

<span data-ttu-id="bb7ee-125">Дополнительное пространство, расположенное выше и ниже, усекается.</span><span class="sxs-lookup"><span data-stu-id="bb7ee-125">The extra space above and below is trimmed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 