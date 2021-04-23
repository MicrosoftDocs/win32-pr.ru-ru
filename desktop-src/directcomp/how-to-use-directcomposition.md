---
title: Как использовать DirectComposition
description: В этом разделе приводятся рекомендации по использованию Microsoft DirectComposition \ 32; API и демонстрирует использование API для выполнения нескольких распространенных задач.
ms.assetid: 49F6E356-90C7-423A-A31A-AEE41F882D3B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0658a9693567dfd88e9a986893048fa1d0fa1e5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105691404"
---
# <a name="how-to-use-directcomposition"></a><span data-ttu-id="9ccd9-103">Как использовать DirectComposition</span><span class="sxs-lookup"><span data-stu-id="9ccd9-103">How to use DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="9ccd9-104">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="9ccd9-105">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="9ccd9-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="9ccd9-106">В этом разделе описываются рекомендации по использованию API Microsoft DirectComposition и демонстрируется использование API для выполнения нескольких распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-106">This section describes best practices for using the Microsoft DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9ccd9-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9ccd9-107">In this section</span></span>



| <span data-ttu-id="9ccd9-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="9ccd9-108">Topic</span></span>                                                                                                                      | <span data-ttu-id="9ccd9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9ccd9-109">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ccd9-110">Рекомендации по DirectComposition</span><span class="sxs-lookup"><span data-stu-id="9ccd9-110">Best practices for DirectComposition</span></span>](best-practices-for-directcomposition.md)<br/>                                | <span data-ttu-id="9ccd9-111">В этом разделе описываются рекомендации по использованию DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-111">This topic describes best practices for using DirectComposition.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="9ccd9-112">Как инициализировать DirectComposition</span><span class="sxs-lookup"><span data-stu-id="9ccd9-112">How to initialize DirectComposition</span></span>](initialize-directcomposition.md)<br/>                                         | <span data-ttu-id="9ccd9-113">В этом разделе показано, как создать и инициализировать минимальный набор объектов DirectComposition, необходимых для создания простой композиции.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-113">This topic demonstrates how to create and initialize the minimum set of DirectComposition objects needed to create a simple composition.</span></span><br/>                                                          |
| [<span data-ttu-id="9ccd9-114">Создание простого визуального дерева</span><span class="sxs-lookup"><span data-stu-id="9ccd9-114">How to build a simple visual tree</span></span>](how-to--build-a-visual-tree.md)<br/>                                            | <span data-ttu-id="9ccd9-115">В этом разделе показано, как создать простое визуальное дерево DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-115">This topic demonstrates how to build a simple DirectComposition visual tree.</span></span> <span data-ttu-id="9ccd9-116">Пример в этом разделе создает и формирует визуальное дерево, состоящее из корневого визуального элемента и трех дочерних визуальных элементов.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-116">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <br/> |
| [<span data-ttu-id="9ccd9-117">Обрезка с помощью объекта прямоугольной обрезки</span><span class="sxs-lookup"><span data-stu-id="9ccd9-117">How to clip with a rectangle clip object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)<br/>                     | <span data-ttu-id="9ccd9-118">В этом разделе показано, как использовать объект прямоугольной картинки для обрезки визуального или визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-118">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="9ccd9-119">Как применять двумерные преобразования</span><span class="sxs-lookup"><span data-stu-id="9ccd9-119">How to apply 2D transforms</span></span>](apply-2d-transforms.md)<br/>                                                           | <span data-ttu-id="9ccd9-120">В этом разделе показано, как применять двумерные преобразования к визуальному элементу с помощью DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-120">This topic demonstrates how to apply 2D transforms to a visual by using DirectComposition.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="9ccd9-121">Как применять эффекты</span><span class="sxs-lookup"><span data-stu-id="9ccd9-121">How to apply effects</span></span>](how-to--apply-transforms-and-effects-to-a-visual.md)<br/>                                    | <span data-ttu-id="9ccd9-122">В этом разделе показано, как использовать DirectComposition для применения эффектов и трехмерных преобразований к визуальному элементу.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-122">This topic demonstrates how to use DirectComposition to apply effects and 3D transformations to a visual.</span></span><br/>                                                                                         |
| [<span data-ttu-id="9ccd9-123">Как применять анимацию</span><span class="sxs-lookup"><span data-stu-id="9ccd9-123">How to apply animations</span></span>](how-to--animate-a-visual.md)<br/>                                                         | <span data-ttu-id="9ccd9-124">В этом разделе показано, как анимировать свойства визуального элемента с помощью DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-124">This topic demonstrates how to animate the properties of a visual by using DirectComposition.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="9ccd9-125">Как анимировать растровое изображение для разслойного дочернего окна</span><span class="sxs-lookup"><span data-stu-id="9ccd9-125">How to animate the bitmap of a layered child window</span></span>](how-to--animate-the-bitmap-of-a-layered-child-window.md)<br/> | <span data-ttu-id="9ccd9-126">В этом разделе описывается создание и Анимация визуального элемента, который использует растровое изображение многоуровневого окна в качестве содержимого визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="9ccd9-126">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="9ccd9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9ccd9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ccd9-128">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="9ccd9-128">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





