---
title: Атрибут Арровок VML
description: Атрибут Арровок VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413190"
---
# <a name="vml-arrowok-attribute"></a><span data-ttu-id="12a7a-103">Атрибут Арровок VML</span><span class="sxs-lookup"><span data-stu-id="12a7a-103">VML ArrowOK Attribute</span></span>

<span data-ttu-id="12a7a-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="12a7a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="12a7a-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="12a7a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="12a7a-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="12a7a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="12a7a-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="12a7a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="12a7a-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="12a7a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="12a7a-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="12a7a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="12a7a-110">Определяет, будут ли отображаться стрелки.</span><span class="sxs-lookup"><span data-stu-id="12a7a-110">Determines whether arrowheads will be displayed.</span></span> <span data-ttu-id="12a7a-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="12a7a-111">Read/write.</span></span> <span data-ttu-id="12a7a-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-112">**VgTriState**.</span></span>

<span data-ttu-id="12a7a-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="12a7a-113">**Applies To**</span></span>

[<span data-ttu-id="12a7a-114">Путь</span><span class="sxs-lookup"><span data-stu-id="12a7a-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="12a7a-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="12a7a-115">**Tag Syntax**</span></span>

<span data-ttu-id="12a7a-116"><v: *element* арровок = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="12a7a-116"><v: *element* arrowok=" *expression* "></span></span>

<span data-ttu-id="12a7a-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="12a7a-117">**Script Syntax**</span></span>

<span data-ttu-id="12a7a-118">*element* . арровок = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="12a7a-118">*element* .arrowok="*expression*"</span></span>

<span data-ttu-id="12a7a-119">*выражение* = *element*. арровок</span><span class="sxs-lookup"><span data-stu-id="12a7a-119">*expression*=*element*.arrowok</span></span>

<span data-ttu-id="12a7a-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="12a7a-120">**Remarks**</span></span>

<span data-ttu-id="12a7a-121">Если задано **значение false**, то путь не будет иметь стрелок.</span><span class="sxs-lookup"><span data-stu-id="12a7a-121">If **False**, the path will not have arrowheads.</span></span> <span data-ttu-id="12a7a-122">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="12a7a-122">The default is **False**.</span></span> <span data-ttu-id="12a7a-123">Этот атрибут переопределяет все остальные атрибуты наконечника в родительском элементе или элементе **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="12a7a-123">This attribute overrides all other arrowhead attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="12a7a-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="12a7a-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="12a7a-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="12a7a-125">**Example**</span></span>

<span data-ttu-id="12a7a-126">У пути не будет стрелки.</span><span class="sxs-lookup"><span data-stu-id="12a7a-126">The path will not have an arrowhead.</span></span>


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 