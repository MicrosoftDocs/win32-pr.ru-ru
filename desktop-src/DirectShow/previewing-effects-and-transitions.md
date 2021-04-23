---
description: Предварительный просмотр эффектов и переходов
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Предварительный просмотр эффектов и переходов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140371"
---
# <a name="previewing-effects-and-transitions"></a><span data-ttu-id="d850d-103">Предварительный просмотр эффектов и переходов</span><span class="sxs-lookup"><span data-stu-id="d850d-103">Previewing Effects and Transitions</span></span>

<span data-ttu-id="d850d-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="d850d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d850d-105">Отрисовка некоторых эффектов и переходов занимает довольно много времени.</span><span class="sxs-lookup"><span data-stu-id="d850d-105">Some effects and transitions take a relatively long time to render.</span></span> <span data-ttu-id="d850d-106">При предварительном просмотре это может привести к нестабильной или невозможности синхронизации видео с аудио.</span><span class="sxs-lookup"><span data-stu-id="d850d-106">During preview this can cause the video to become choppy or out of sync with the audio.</span></span> <span data-ttu-id="d850d-107">Вы можете увеличить скорость просмотра, отключив эффекты или переходы:</span><span class="sxs-lookup"><span data-stu-id="d850d-107">You can increase preview speed by disabling effects or transitions:</span></span>

-   <span data-ttu-id="d850d-108">Чтобы отключить все эффекты, вызовите метод [**иамтимелине:: енаблиффектс**](iamtimeline-enableeffects.md).</span><span class="sxs-lookup"><span data-stu-id="d850d-108">To disable all effects, call [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).</span></span>
-   <span data-ttu-id="d850d-109">Чтобы отключить все переходы, вызовите метод [**иамтимелине:: енаблетранситионс**](iamtimeline-enabletransitions.md).</span><span class="sxs-lookup"><span data-stu-id="d850d-109">To disable all transitions, call [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).</span></span>
-   <span data-ttu-id="d850d-110">Чтобы отключить определенный переход, вызовите метод [**иамтимелинетранс:: сеткутсонли**](iamtimelinetrans-setcutsonly.md).</span><span class="sxs-lookup"><span data-stu-id="d850d-110">To disable a particular transition, call [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span></span>

<span data-ttu-id="d850d-111">Если эффекты отключены, они не отображаются во время предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="d850d-111">When effects are disabled, they are not rendered during preview.</span></span> <span data-ttu-id="d850d-112">Если переход отключен, он готовится к просмотру при вырезании.</span><span class="sxs-lookup"><span data-stu-id="d850d-112">When a transition is disabled, it is rendered as a jump cut.</span></span> <span data-ttu-id="d850d-113">Перехода между дорожками все еще происходит, но визуальный элемент не визуализируется.</span><span class="sxs-lookup"><span data-stu-id="d850d-113">The segue between tracks still occurs, but the visual effect is not rendered.</span></span>

<span data-ttu-id="d850d-114">Если не удается подготовить к просмотру эффекты или переход, подсистема подготовки отчетов подставляет к нему эффекты по умолчанию или переход.</span><span class="sxs-lookup"><span data-stu-id="d850d-114">If an effect or transition cannot be rendered, the render engine substitutes a default effect or transition.</span></span> <span data-ttu-id="d850d-115">Вызовите метод [**иамтимелине:: сетдефаултеффект**](iamtimeline-setdefaulteffect.md) , чтобы задать результат по умолчанию, и метод [**Иамтимелине:: сетдефаулттранситион**](iamtimeline-setdefaulttransition.md) для установки перехода по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d850d-115">Call the [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) method to set the default effect, and the [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) method to set the default transition.</span></span> <span data-ttu-id="d850d-116">Если не указать значение по умолчанию или если указанное значение также вызывает ошибку, DES использует собственное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d850d-116">If you do not specify a default, or if the one you specify also causes an error, DES uses its own default.</span></span>

> [!Note]  
> <span data-ttu-id="d850d-117">Можно также повысить качество предварительного просмотра, увеличив объем буферизации кадров.</span><span class="sxs-lookup"><span data-stu-id="d850d-117">You can also improve preview quality by increasing the amount of frame buffering.</span></span> <span data-ttu-id="d850d-118">См. раздел [**иамтимелинеграуп:: сетаутпутбуфферинг**](iamtimelinegroup-setoutputbuffering.md).</span><span class="sxs-lookup"><span data-stu-id="d850d-118">See [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d850d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d850d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d850d-120">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="d850d-120">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



