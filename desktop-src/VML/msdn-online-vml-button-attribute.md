---
title: Атрибут кнопки VML
description: Атрибут кнопки VML
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2760fceaf52e3f9ee217d4c3d249fb670a845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672323"
---
# <a name="vml-button-attribute"></a><span data-ttu-id="b6a83-103">Атрибут кнопки VML</span><span class="sxs-lookup"><span data-stu-id="b6a83-103">VML Button Attribute</span></span>

<span data-ttu-id="b6a83-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b6a83-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b6a83-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b6a83-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b6a83-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b6a83-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b6a83-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b6a83-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b6a83-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b6a83-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b6a83-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b6a83-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b6a83-110">Определяет, будет ли фигура обработана как кнопка.</span><span class="sxs-lookup"><span data-stu-id="b6a83-110">Determines whether a shape will be processed as a button.</span></span> <span data-ttu-id="b6a83-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b6a83-111">Read/write.</span></span> <span data-ttu-id="b6a83-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="b6a83-112">**VgTriState**.</span></span>

<span data-ttu-id="b6a83-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b6a83-113">**Applies To**</span></span>

[<span data-ttu-id="b6a83-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="b6a83-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b6a83-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b6a83-115">**Tag Syntax**</span></span>

<span data-ttu-id="b6a83-116"><v: *element* о:буттон = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b6a83-116"><v: *element* o:button=" *expression* "></span></span>

<span data-ttu-id="b6a83-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b6a83-117">**Remarks**</span></span>

<span data-ttu-id="b6a83-118">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="b6a83-118">The default is **False**.</span></span> <span data-ttu-id="b6a83-119">Если **значение равно true**, фигура обрабатывается как кнопка.</span><span class="sxs-lookup"><span data-stu-id="b6a83-119">If **True**, the shape is processed as a button.</span></span>

<span data-ttu-id="b6a83-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="b6a83-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="b6a83-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="b6a83-121">**Example**</span></span>

<span data-ttu-id="b6a83-122">Фигура является кнопкой.</span><span class="sxs-lookup"><span data-stu-id="b6a83-122">The shape is a button.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 