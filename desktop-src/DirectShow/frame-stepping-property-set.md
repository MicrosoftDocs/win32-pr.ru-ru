---
description: Набор свойств пошагового выполнения кадра
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Набор свойств пошагового выполнения кадра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806130"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="3b3c3-103">Набор свойств пошагового выполнения кадра</span><span class="sxs-lookup"><span data-stu-id="3b3c3-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="3b3c3-104">Декодеры, которые реализуют точное Поиск в виде кадров в Microsoft DirectShow, должны реализовать \_ \_ набор свойств AM кспропсетид фраместеп, который используется совместно с интерфейсом [**ивидеофраместеп**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .</span><span class="sxs-lookup"><span data-stu-id="3b3c3-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="3b3c3-105">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="3b3c3-105">Property Set GUID</span></span> | <span data-ttu-id="3b3c3-106">\_Кспропсетид \_ фраместеп</span><span class="sxs-lookup"><span data-stu-id="3b3c3-106">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="3b3c3-107">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="3b3c3-107">Property ID</span></span>                              | <span data-ttu-id="3b3c3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3b3c3-108">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3c3-109">\_шаг свойства \_ фраместеп \_</span><span class="sxs-lookup"><span data-stu-id="3b3c3-109">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="3b3c3-110">Предписывает декодеру начать пошаговую операцию и передать структуру [**\_ Свойства AM \_ фраместеп**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) , указывающую количество шагов.</span><span class="sxs-lookup"><span data-stu-id="3b3c3-110">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="3b3c3-111">\_свойство AM \_ фраместеп \_ Cancel</span><span class="sxs-lookup"><span data-stu-id="3b3c3-111">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="3b3c3-112">Предписывает декодеру отменить текущую операцию шага.</span><span class="sxs-lookup"><span data-stu-id="3b3c3-112">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="3b3c3-113">С этим свойством не связаны данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3b3c3-113">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="3b3c3-114">\_свойство AM \_ фраместеп \_ канстеп</span><span class="sxs-lookup"><span data-stu-id="3b3c3-114">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="3b3c3-115">Декодер возвращает \_ ОК в этой инструкции, чтобы указать, что она может выполнять пошаговое выполнение \_ . в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="3b3c3-115">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="3b3c3-116">Если это свойство задано, данные экземпляра не передаются.</span><span class="sxs-lookup"><span data-stu-id="3b3c3-116">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="3b3c3-117">\_свойство AM \_ фраместеп \_ канстепмултипле</span><span class="sxs-lookup"><span data-stu-id="3b3c3-117">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="3b3c3-118">Декодер возвращает \_ ОК в этой инструкции, чтобы указать, что он может пошагово выполнить несколько кадров за раз \_ . в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="3b3c3-118">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="3b3c3-119">Если это свойство задано, данные экземпляра не передаются.</span><span class="sxs-lookup"><span data-stu-id="3b3c3-119">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3b3c3-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3b3c3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b3c3-121">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="3b3c3-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



