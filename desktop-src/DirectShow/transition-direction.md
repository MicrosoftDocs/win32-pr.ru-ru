---
description: Направление перехода
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Направление перехода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562483"
---
# <a name="transition-direction"></a><span data-ttu-id="cb616-103">Направление перехода</span><span class="sxs-lookup"><span data-stu-id="cb616-103">Transition Direction</span></span>

<span data-ttu-id="cb616-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="cb616-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="cb616-105">Переход проходит от входного типа A к входу B и от Time t ₀ к t ₁.</span><span class="sxs-lookup"><span data-stu-id="cb616-105">A transition goes from input A to input B, and from time t₀ to t₁.</span></span> <span data-ttu-id="cb616-106">Таким образом, *направление* перехода может означать одно из двух действий:</span><span class="sxs-lookup"><span data-stu-id="cb616-106">Therefore, the *direction* of a transition can mean one of two things:</span></span>

-   <span data-ttu-id="cb616-107">Сопоставление слоев временной шкалы с входными данными.</span><span class="sxs-lookup"><span data-stu-id="cb616-107">The mapping of timeline layers to inputs.</span></span>
-   <span data-ttu-id="cb616-108">Ход выполнения с течением времени.</span><span class="sxs-lookup"><span data-stu-id="cb616-108">The progression over time.</span></span>

<span data-ttu-id="cb616-109">Первый — *направление ввода*, а второй — *направление выполнения*.</span><span class="sxs-lookup"><span data-stu-id="cb616-109">The first is the *input direction*, and the second is the *progress direction*.</span></span> <span data-ttu-id="cb616-110">Вы можете управлять обоими направлениями.</span><span class="sxs-lookup"><span data-stu-id="cb616-110">You can control both directions.</span></span>

-   <span data-ttu-id="cb616-111">Направление ввода. по умолчанию переход проходит от состава слоев с низким приоритетом к слою, содержащему переход.</span><span class="sxs-lookup"><span data-stu-id="cb616-111">Input direction: By default, a transition goes from the composite of the lower-priority layers to the layer that contains the transition.</span></span> <span data-ttu-id="cb616-112">Чтобы отменить это направление, вызовите метод [**иамтимелинетранс:: сетсвапинпутс**](iamtimelinetrans-setswapinputs.md) .</span><span class="sxs-lookup"><span data-stu-id="cb616-112">To reverse this direction, call the [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md) method.</span></span>
-   <span data-ttu-id="cb616-113">Направление выполнения. Большинство переходов поддерживают стандартное свойство **Progress** , которое указывает, какой процент переходов отражается в выходных данных в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="cb616-113">Progress direction: Most transitions support a standard **Progress** property, which specifies what percentage of the transition is reflected in the output at a given moment.</span></span> <span data-ttu-id="cb616-114">По умолчанию значение свойства **Progress** переходит с 0,0 на 1,0 в течение периода перехода.</span><span class="sxs-lookup"><span data-stu-id="cb616-114">By default, the value of the **Progress** property goes from 0.0 to 1.0 over the duration of the transition.</span></span> <span data-ttu-id="cb616-115">Чтобы отменить ход выполнения, задайте для свойства **Progress** значение переход с 1,0 на 0,0.</span><span class="sxs-lookup"><span data-stu-id="cb616-115">To reverse the progress, set the **Progress** property to go from 1.0 to 0.0.</span></span>

<span data-ttu-id="cb616-116">На следующей схеме показана разница между направлением ввода и направлением хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="cb616-116">The following diagram illustrates the difference between input direction and progress direction.</span></span> <span data-ttu-id="cb616-117">В нем показаны четыре варианта стандартного перехода на [очистку SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="cb616-117">It shows four variations on a standard [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

![направления очистки](images/wipedirections.png)

<span data-ttu-id="cb616-119">Переход находится на дорожке 1.</span><span class="sxs-lookup"><span data-stu-id="cb616-119">The transition resides on track 1.</span></span> <span data-ttu-id="cb616-120">По умолчанию очистка выполняется слева направо и от контрольной записи 0 до значения 1.</span><span class="sxs-lookup"><span data-stu-id="cb616-120">By default, the wipe goes from left to right and from track 0 to track 1.</span></span> <span data-ttu-id="cb616-121">Переключение входных данных приводит к тому, что очистка будет переходить от Track 1 к отслеживанию 0, но по-прежнему слева направо.</span><span class="sxs-lookup"><span data-stu-id="cb616-121">Swapping inputs causes the wipe to go from track 1 to track 0, but still from left to right.</span></span> <span data-ttu-id="cb616-122">При обратном выполнении переход переходит справа налево.</span><span class="sxs-lookup"><span data-stu-id="cb616-122">Reversing the progress makes the transition go from right to left.</span></span> <span data-ttu-id="cb616-123">Можно объединить оба, как показано в левом углу.</span><span class="sxs-lookup"><span data-stu-id="cb616-123">You can combine both, as shown on the far left.</span></span>

<span data-ttu-id="cb616-124">Дополнительные сведения о отрисовке переходов DES см. [в разделе Модель временной шкалы](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="cb616-124">For more information about how DES renders transitions, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb616-125">См. также</span><span class="sxs-lookup"><span data-stu-id="cb616-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb616-126">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="cb616-126">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



