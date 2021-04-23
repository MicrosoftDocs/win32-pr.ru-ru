---
title: Типы данных VML
description: Типы данных VML
ms.assetid: A71C9691-BDE9-4455-A2DC-2C67CF5FEF77
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f625999d2abc90cee4e645df2a012ebadfbbcccc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792108"
---
# <a name="vml-data-types"></a><span data-ttu-id="6416f-103">Типы данных VML</span><span class="sxs-lookup"><span data-stu-id="6416f-103">VML Data Types</span></span>

<span data-ttu-id="6416f-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="6416f-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6416f-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="6416f-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6416f-106">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6416f-106">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6416f-107">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6416f-107">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6416f-108">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6416f-108">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6416f-109">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6416f-109">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6416f-110">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6416f-110">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6416f-111">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6416f-111">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6416f-112">В этом разделе описываются типы данных VML.</span><span class="sxs-lookup"><span data-stu-id="6416f-112">This section describes VML data types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6416f-113">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="6416f-113">In this section</span></span>

-   [<span data-ttu-id="6416f-114">Тип данных Ивгаджустментс</span><span class="sxs-lookup"><span data-stu-id="6416f-114">IVgAdjustments Data Type</span></span>](msdn-online-vml-ivgadjustments-data-type.md)
-   [<span data-ttu-id="6416f-115">ивгколор</span><span class="sxs-lookup"><span data-stu-id="6416f-115">IVgColor</span></span>](msdn-online-vml-ivgcolor.md)
-   [<span data-ttu-id="6416f-116">Тип данных Ивгпоинтс</span><span class="sxs-lookup"><span data-stu-id="6416f-116">IVgPoints Data Type</span></span>](msdn-online-vml-ivgpoints-data-type.md)
-   [<span data-ttu-id="6416f-117">Тип данных IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="6416f-117">IVgVector2D Data Type</span></span>](msdn-online-vml-ivgvector2d-data-type.md)
-   [<span data-ttu-id="6416f-118">Тип данных Вганглеиндегрис</span><span class="sxs-lookup"><span data-stu-id="6416f-118">VgAngleInDegrees Data Type</span></span>](msdn-online-vml-vgangleindegrees-data-type.md)
-   [<span data-ttu-id="6416f-119">вгблакквхитемоде</span><span class="sxs-lookup"><span data-stu-id="6416f-119">VgBlackWhiteMode</span></span>](msdn-online-vml-vgblackwhitemode.md)
-   [<span data-ttu-id="6416f-120">Тип данных Вгфрактион</span><span class="sxs-lookup"><span data-stu-id="6416f-120">VgFraction Data Type</span></span>](msdn-online-vml-vgfraction-data-type.md)
-   [<span data-ttu-id="6416f-121">вгленгс</span><span class="sxs-lookup"><span data-stu-id="6416f-121">VGLength</span></span>](msdn-online-vml-vglength.md)
-   [<span data-ttu-id="6416f-122">вгтристате</span><span class="sxs-lookup"><span data-stu-id="6416f-122">VgTriState</span></span>](msdn-online-vml-vgtristate.md)

 

 