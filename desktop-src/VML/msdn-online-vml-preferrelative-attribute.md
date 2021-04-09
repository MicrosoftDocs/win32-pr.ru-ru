---
title: Атрибут Преферрелативе VML
description: Атрибут Преферрелативе VML
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070098"
---
# <a name="vml-preferrelative-attribute"></a><span data-ttu-id="3bef4-103">Атрибут Преферрелативе VML</span><span class="sxs-lookup"><span data-stu-id="3bef4-103">VML PreferRelative Attribute</span></span>

<span data-ttu-id="3bef4-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3bef4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3bef4-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="3bef4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3bef4-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="3bef4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3bef4-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3bef4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3bef4-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3bef4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3bef4-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3bef4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3bef4-110">Определяет, сохраняется ли исходный размер объекта после переформатирования.</span><span class="sxs-lookup"><span data-stu-id="3bef4-110">Determines whether the original size of an object is saved after reformatting.</span></span> <span data-ttu-id="3bef4-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="3bef4-111">Read/write.</span></span> <span data-ttu-id="3bef4-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="3bef4-112">**VgTriState**.</span></span>

<span data-ttu-id="3bef4-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="3bef4-113">**Applies To**</span></span>

[<span data-ttu-id="3bef4-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="3bef4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3bef4-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="3bef4-115">**Tag Syntax**</span></span>

<span data-ttu-id="3bef4-116"><v: *element* о:преферрелативе = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="3bef4-116"><v: *element* o:preferrelative=" *expression* "></span></span>

<span data-ttu-id="3bef4-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3bef4-117">**Remarks**</span></span>

<span data-ttu-id="3bef4-118">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="3bef4-118">The default is **False**.</span></span> <span data-ttu-id="3bef4-119">Если **значение — true**, будет сохранен исходный размер объекта, а изменение размера будет основано на проценте от этого исходного размера.</span><span class="sxs-lookup"><span data-stu-id="3bef4-119">If **True**, the original size of the object will be stored and all resizing will be based on a percentage of that original size.</span></span> <span data-ttu-id="3bef4-120">В противном случае при каждом изменении размера будет сброшен масштаб в 100%.</span><span class="sxs-lookup"><span data-stu-id="3bef4-120">Otherwise, each resizing will reset the scale to 100%.</span></span>

<span data-ttu-id="3bef4-121">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="3bef4-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="3bef4-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="3bef4-122">**Example**</span></span>

<span data-ttu-id="3bef4-123">При изменении размера фигуры исходный размер не будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="3bef4-123">If the shape is resized, the original size will not be stored.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 