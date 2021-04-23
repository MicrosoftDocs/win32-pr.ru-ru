---
title: Атрибут маркера VML
description: Атрибут маркера VML
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413184"
---
# <a name="vml-bullet-attribute"></a><span data-ttu-id="e5236-103">Атрибут маркера VML</span><span class="sxs-lookup"><span data-stu-id="e5236-103">VML Bullet Attribute</span></span>

<span data-ttu-id="e5236-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e5236-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e5236-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e5236-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e5236-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e5236-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e5236-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5236-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e5236-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e5236-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e5236-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e5236-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e5236-110">Определяет, является ли фигура графическим маркером.</span><span class="sxs-lookup"><span data-stu-id="e5236-110">Determines whether a shape is a graphical bullet.</span></span> <span data-ttu-id="e5236-111">Чтение и запись **вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="e5236-111">Read/write **VgTriState**.</span></span>

<span data-ttu-id="e5236-112">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e5236-112">**Applies To**</span></span>

[<span data-ttu-id="e5236-113">Фигурная</span><span class="sxs-lookup"><span data-stu-id="e5236-113">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e5236-114">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e5236-114">**Tag Syntax**</span></span>

<span data-ttu-id="e5236-115"><v: *element* о:буллет = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="e5236-115"><v: *element* o:bullet=" *expression* "></span></span>

<span data-ttu-id="e5236-116">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e5236-116">**Remarks**</span></span>

<span data-ttu-id="e5236-117">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="e5236-117">The default is **False**.</span></span> <span data-ttu-id="e5236-118">Если **значение равно true**, то фигура является графическим маркером.</span><span class="sxs-lookup"><span data-stu-id="e5236-118">If **True**, the shape is a graphical bullet.</span></span>

<span data-ttu-id="e5236-119">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="e5236-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="e5236-120">**Пример**</span><span class="sxs-lookup"><span data-stu-id="e5236-120">**Example**</span></span>

<span data-ttu-id="e5236-121">Фигура является маркером.</span><span class="sxs-lookup"><span data-stu-id="e5236-121">The shape is a bullet.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 