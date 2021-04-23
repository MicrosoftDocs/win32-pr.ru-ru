---
title: Вложенные элементы формы
description: Вложенные элементы формы
ms.assetid: 85E36F7B-25FA-4032-B4BE-DD95EBACDB14
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 40b8f1fef957040c15bd622f20bf596e8b5f85d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890688"
---
# <a name="subelements-of-shape"></a><span data-ttu-id="1a481-103">Вложенные элементы формы</span><span class="sxs-lookup"><span data-stu-id="1a481-103">Subelements of Shape</span></span>

<span data-ttu-id="1a481-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1a481-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1a481-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1a481-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1a481-106">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1a481-106">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1a481-107">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="1a481-107">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1a481-108">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="1a481-108">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1a481-109">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1a481-109">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1a481-110">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1a481-110">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1a481-111">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1a481-111">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1a481-112">В этом разделе описываются элементы, являющиеся дочерними элементами (или вложенными *элементами*) элемента Shape.</span><span class="sxs-lookup"><span data-stu-id="1a481-112">This section describes elements that are child elements (or *subelements*) of the Shape element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a481-113">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="1a481-113">In this section</span></span>

-   [<span data-ttu-id="1a481-114">Элемент выноски</span><span class="sxs-lookup"><span data-stu-id="1a481-114">Callout Element</span></span>](msdn-online-vml-callout-element.md)
-   [<span data-ttu-id="1a481-115">Элемент объемной фигуры</span><span class="sxs-lookup"><span data-stu-id="1a481-115">Extrusion Element</span></span>](msdn-online-vml-extrusion-element.md)
-   [<span data-ttu-id="1a481-116">Fill, элемент</span><span class="sxs-lookup"><span data-stu-id="1a481-116">Fill Element</span></span>](msdn-online-vml-fill-element.md)
-   [<span data-ttu-id="1a481-117">Элемент формул</span><span class="sxs-lookup"><span data-stu-id="1a481-117">Formulas Element</span></span>](msdn-online-vml-formulas-element.md)
-   [<span data-ttu-id="1a481-118">Обрабатывает элемент</span><span class="sxs-lookup"><span data-stu-id="1a481-118">Handles Element</span></span>](msdn-online-vml-handles-element.md)
-   [<span data-ttu-id="1a481-119">Имажедата, элемент</span><span class="sxs-lookup"><span data-stu-id="1a481-119">Imagedata Element</span></span>](msdn-online-vml-imagedata-element.md)
-   [<span data-ttu-id="1a481-120">Locks, элемент</span><span class="sxs-lookup"><span data-stu-id="1a481-120">Locks Element</span></span>](msdn-online-vml-locks-element.md)
-   [<span data-ttu-id="1a481-121">Элемент Path</span><span class="sxs-lookup"><span data-stu-id="1a481-121">Path Element</span></span>](msdn-online-vml-path-element.md)
-   [<span data-ttu-id="1a481-122">Элемент Shadow</span><span class="sxs-lookup"><span data-stu-id="1a481-122">Shadow Element</span></span>](msdn-online-vml-shadow-element.md)
-   [<span data-ttu-id="1a481-123">Элемент асимметрии</span><span class="sxs-lookup"><span data-stu-id="1a481-123">Skew Element</span></span>](msdn-online-vml-skew-element.md)
-   [<span data-ttu-id="1a481-124">Элемент Stroke</span><span class="sxs-lookup"><span data-stu-id="1a481-124">Stroke Element</span></span>](msdn-online-vml-stroke-element.md)
-   [<span data-ttu-id="1a481-125">TextBox, элемент</span><span class="sxs-lookup"><span data-stu-id="1a481-125">TextBox Element</span></span>](msdn-online-vml-textbox-element.md)
-   [<span data-ttu-id="1a481-126">Текстпас, элемент</span><span class="sxs-lookup"><span data-stu-id="1a481-126">TextPath Element</span></span>](msdn-online-vml-textpath-element.md)

 

 