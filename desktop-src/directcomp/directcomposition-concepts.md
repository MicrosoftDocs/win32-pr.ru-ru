---
title: Основные понятия DirectComposition
description: Этот раздел содержит общие сведения о DirectComposition.
ms.assetid: 7839C264-C15F-4E89-82B6-2963A5C61CEC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea823d2edd27b2c725cefdd73cd053e94124d7f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068780"
---
# <a name="directcomposition-concepts"></a><span data-ttu-id="c4f96-103">Основные понятия DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c4f96-103">DirectComposition concepts</span></span>

> [!NOTE]
> <span data-ttu-id="c4f96-104">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="c4f96-105">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="c4f96-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="c4f96-106">Этот раздел содержит общие сведения о DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-106">This section provides a conceptual overview of DirectComposition.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4f96-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c4f96-107">In this section</span></span>



| <span data-ttu-id="c4f96-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="c4f96-108">Topic</span></span>                                                                     | <span data-ttu-id="c4f96-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c4f96-109">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4f96-110">Основные понятия</span><span class="sxs-lookup"><span data-stu-id="c4f96-110">Basic concepts</span></span>](basic-concepts.md)<br/>                           | <span data-ttu-id="c4f96-111">В этом разделе приводится обзор основных понятий Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-111">This topic provides an overview of the basic concepts of Microsoft DirectComposition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="c4f96-112">Растровые объекты</span><span class="sxs-lookup"><span data-stu-id="c4f96-112">Bitmap objects</span></span>](bitmap-surfaces.md)<br/>                          | <span data-ttu-id="c4f96-113">В этом разделе описываются типы растрового содержимого, которое поддерживает DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-113">This topic describes the types of bitmap content that DirectComposition supports.</span></span><br/>                                                                                           |
| [<span data-ttu-id="c4f96-114">Область композиции</span><span class="sxs-lookup"><span data-stu-id="c4f96-114">Composition surface</span></span>](composition-surface.md)<br/>                 | <span data-ttu-id="c4f96-115">В этом разделе описываются типы типов поверхностей, поддерживаемых DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-115">This topic describes the types of types of surfaces that DirectComposition supports.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c4f96-116">Преобразования</span><span class="sxs-lookup"><span data-stu-id="c4f96-116">Transforms</span></span>](transforms.md)<br/>                                   | <span data-ttu-id="c4f96-117">В этом разделе рассматривается поддержка DirectComposition преобразований двухмерной (линейная) и описание типов преобразований, поддерживаемых DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-117">This topic discusses DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span> <br/> |
| [<span data-ttu-id="c4f96-118">Эффекты</span><span class="sxs-lookup"><span data-stu-id="c4f96-118">Effects</span></span>](effects.md)<br/>                                         | <span data-ttu-id="c4f96-119">В этом разделе обсуждаются основы DirectComposition эффектов и описываются типы эффектов, поддерживаемых DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-119">This topic discusses the basics of DirectComposition effects, and describes the types of effects that DirectComposition supports.</span></span> <br/>                                          |
| [<span data-ttu-id="c4f96-120">Анимация</span><span class="sxs-lookup"><span data-stu-id="c4f96-120">Animation</span></span>](animation.md)<br/>                                     | <span data-ttu-id="c4f96-121">В этом разделе обсуждаются основы анимации DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-121">This topic discusses the basics of DirectComposition animation.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="c4f96-122">Вырезая</span><span class="sxs-lookup"><span data-stu-id="c4f96-122">Clipping</span></span>](clipping.md)<br/>                                       | <span data-ttu-id="c4f96-123">В этом разделе описывается поддержка DirectComposition для обрезки визуальных элементов.</span><span class="sxs-lookup"><span data-stu-id="c4f96-123">This topic describes DirectComposition support for clipping visuals.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="c4f96-124">Архитектура и компоненты</span><span class="sxs-lookup"><span data-stu-id="c4f96-124">Architecture and components</span></span>](architecture-and-components.md)<br/> | <span data-ttu-id="c4f96-125">В этом разделе описываются компоненты, составляющие DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c4f96-125">This topic describes the components that make up DirectComposition.</span></span><br/>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="c4f96-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c4f96-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f96-127">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c4f96-127">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





