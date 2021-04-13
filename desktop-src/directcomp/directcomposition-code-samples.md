---
title: Примеры DirectComposition
description: В следующих примерах приложений показано, как использовать Microsoft DirectComposition \ 32; API и демонстрируют его возможности.
ms.assetid: E2794CE7-20A3-4388-B1DC-D9822C970774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889ceb9a6f9383930b9231c9c19a2b610fba2815
ms.sourcegitcommit: 38c86be0218ed38d0f14db3df107db29827b6269
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412783"
---
# <a name="directcomposition-samples"></a><span data-ttu-id="8b91f-103">Примеры DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8b91f-103">DirectComposition samples</span></span>

> [!NOTE]
> <span data-ttu-id="8b91f-104">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="8b91f-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="8b91f-105">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="8b91f-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="8b91f-106">В следующих примерах приложений показано, как использовать API Microsoft DirectComposition и продемонстрировать его возможности.</span><span class="sxs-lookup"><span data-stu-id="8b91f-106">The following sample applications show how to use the Microsoft DirectComposition API and demonstrate its capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8b91f-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="8b91f-107">In this section</span></span>



| <span data-ttu-id="8b91f-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="8b91f-108">Topic</span></span>                                                                                                                                 | <span data-ttu-id="8b91f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8b91f-109">Description</span></span>                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b91f-110">Пример дочернего окна многоуровневого DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8b91f-110">DirectComposition layered child window sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionLayeredChildWindow)<br/>                           | <span data-ttu-id="8b91f-111">Демонстрирует, как использовать DirectComposition для анимации растрового элемента в слоеное дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="8b91f-111">Demonstrates how to use DirectComposition to animate the bitmap of a layered child window.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="8b91f-112">Пример управления анимацией DirectComposition с помощью Windows Animation Manager V2</span><span class="sxs-lookup"><span data-stu-id="8b91f-112">Managing DirectComposition animation with Windows Animation Manager v2 sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)<br/> | <span data-ttu-id="8b91f-113">Демонстрируется использование Windows Animation Manager V2 для создания кривых эффектов анимации (функций), которые могут использоваться DirectComposition? для создания анимированных переходов в классическом приложении.</span><span class="sxs-lookup"><span data-stu-id="8b91f-113">Demonstrates how Windows Animation Manager v2 can be used to generate animation curves (functions) that can be consumed by DirectComposition? to create animated transitions in a desktop application.</span></span> <br/>                                                            |
| [<span data-ttu-id="8b91f-114">Пример DirectComposition эффектов с Direct2D содержимым битовой карты</span><span class="sxs-lookup"><span data-stu-id="8b91f-114">DirectComposition effects with Direct2D bitmap content sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionEffects)<br/>                                                     | <span data-ttu-id="8b91f-115">Демонстрирует использование DirectComposition для применения эффектов анимации и эффектов к визуальным элементам, имеющим Direct2D содержимое растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="8b91f-115">Demonstrates how to use DirectComposition to apply animations and effects to visuals that have Direct2D bitmap content.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="8b91f-116">Пример пакетной обработки DirectComposition и D2D</span><span class="sxs-lookup"><span data-stu-id="8b91f-116">DirectComposition Backface and D2D Batching sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DCompV2BackfaceandD2DBatching)<br/>                  | <span data-ttu-id="8b91f-117">Демонстрирует использование API DirectComposition для применения отображения обратной стороны к визуальному элементу для отображения и скрытия задней стороны визуального элемента DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="8b91f-117">Demonstrates how to use the DirectComposition API to apply backface visibility to a visual element to show and hide the back side of a DirectComposition visual.</span></span> <span data-ttu-id="8b91f-118">В этом примере также демонстрируется оптимизация производительности для пакетирования вызовов Бегиндрав/EndDraw D2D.</span><span class="sxs-lookup"><span data-stu-id="8b91f-118">This sample also demonstrates a performance optimization of batching D2D BeginDraw/EndDraw calls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8b91f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8b91f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b91f-120">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8b91f-120">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





