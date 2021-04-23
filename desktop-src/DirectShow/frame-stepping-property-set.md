---
description: Набор свойств пошагового выполнения кадра
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Набор свойств пошагового выполнения кадра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908452"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="cb79e-103">Набор свойств пошагового выполнения кадра</span><span class="sxs-lookup"><span data-stu-id="cb79e-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="cb79e-104">Декодеры, которые реализуют точное Поиск в виде кадров в Microsoft DirectShow, должны реализовать \_ \_ набор свойств AM кспропсетид фраместеп, который используется совместно с интерфейсом [**ивидеофраместеп**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .</span><span class="sxs-lookup"><span data-stu-id="cb79e-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



| <span data-ttu-id="cb79e-105">Метка</span><span class="sxs-lookup"><span data-stu-id="cb79e-105">Label</span></span> | <span data-ttu-id="cb79e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="cb79e-106">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="cb79e-107">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="cb79e-107">Property Set GUID</span></span> | <span data-ttu-id="cb79e-108">\_Кспропсетид \_ фраместеп</span><span class="sxs-lookup"><span data-stu-id="cb79e-108">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="cb79e-109">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="cb79e-109">Property ID</span></span>                              | <span data-ttu-id="cb79e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cb79e-110">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb79e-111">\_шаг свойства \_ фраместеп \_</span><span class="sxs-lookup"><span data-stu-id="cb79e-111">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="cb79e-112">Предписывает декодеру начать пошаговую операцию и передать структуру [**\_ Свойства AM \_ фраместеп**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) , указывающую количество шагов.</span><span class="sxs-lookup"><span data-stu-id="cb79e-112">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="cb79e-113">\_свойство AM \_ фраместеп \_ Cancel</span><span class="sxs-lookup"><span data-stu-id="cb79e-113">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="cb79e-114">Предписывает декодеру отменить текущую операцию шага.</span><span class="sxs-lookup"><span data-stu-id="cb79e-114">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="cb79e-115">С этим свойством не связаны данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cb79e-115">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="cb79e-116">\_свойство AM \_ фраместеп \_ канстеп</span><span class="sxs-lookup"><span data-stu-id="cb79e-116">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="cb79e-117">Декодер возвращает \_ ОК в этой инструкции, чтобы указать, что она может выполнять пошаговое выполнение \_ . в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="cb79e-117">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="cb79e-118">Если это свойство задано, данные экземпляра не передаются.</span><span class="sxs-lookup"><span data-stu-id="cb79e-118">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="cb79e-119">\_свойство AM \_ фраместеп \_ канстепмултипле</span><span class="sxs-lookup"><span data-stu-id="cb79e-119">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="cb79e-120">Декодер возвращает \_ ОК в этой инструкции, чтобы указать, что он может пошагово выполнить несколько кадров за раз \_ . в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="cb79e-120">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="cb79e-121">Если это свойство задано, данные экземпляра не передаются.</span><span class="sxs-lookup"><span data-stu-id="cb79e-121">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cb79e-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cb79e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb79e-123">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="cb79e-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



