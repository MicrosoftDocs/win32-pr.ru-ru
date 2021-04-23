---
title: Методы (IManipulationProcessor)
description: В этом разделе содержатся методы для интерфейса IManipulationProcessor.
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Windows Touch, интерфейс IManipulationProcessor
- Касание Windows, методы интерфейса
- манипуляции, интерфейс IManipulationProcessor
- Интерфейс IManipulationProcessor, методы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995a848e18b8308d46ceda717bf7eec291953505
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414564"
---
# <a name="methods-imanipulationprocessor"></a><span data-ttu-id="4ad5b-107">Методы (IManipulationProcessor)</span><span class="sxs-lookup"><span data-stu-id="4ad5b-107">Methods (IManipulationProcessor)</span></span>

<span data-ttu-id="4ad5b-108">В этом разделе содержатся методы для интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="4ad5b-108">This section contains the methods for the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>

<span data-ttu-id="4ad5b-109">Интерфейс [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) представляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-109">The following methods are exposed by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>



| <span data-ttu-id="4ad5b-110">Метод</span><span class="sxs-lookup"><span data-stu-id="4ad5b-110">Method</span></span>                                                                      | <span data-ttu-id="4ad5b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4ad5b-111">Description</span></span>                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ad5b-112">**комплетеманипулатион**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-112">**CompleteManipulation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | <span data-ttu-id="4ad5b-113">Этот метод вызывается, когда разработчик решает закончить манипуляцию.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-113">This method is called when the developer chooses to end the manipulation.</span></span>                |
| [<span data-ttu-id="4ad5b-114">**жетангуларвелоЦити**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-114">**GetAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | <span data-ttu-id="4ad5b-115">Вычисляет скорость вращения, в которую перемещается целевой объект.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-115">Calculates the rotational velocity that the target object is moving at.</span></span>                  |
| [<span data-ttu-id="4ad5b-116">**жетекспансионвелоЦити**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-116">**GetExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | <span data-ttu-id="4ad5b-117">Вычисляет частоту, с которой происходит расширение целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-117">Calculates the rate that the target object is expanding at.</span></span>                              |
| [<span data-ttu-id="4ad5b-118">**жетвелоЦитикс**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-118">**GetVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | <span data-ttu-id="4ad5b-119">Вычисляет и возвращает горизонтальную скорость для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-119">Calculates and returns the horizontal velocity for the target object.</span></span>                    |
| [<span data-ttu-id="4ad5b-120">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-120">**GetVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | <span data-ttu-id="4ad5b-121">Вычисляет и возвращает вертикальную скорость.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-121">Calculates and returns the vertical velocity.</span></span>                                            |
| [<span data-ttu-id="4ad5b-122">**процессдовн**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-122">**ProcessDown**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | <span data-ttu-id="4ad5b-123">Передает данные в обработчик манипуляции, связанный с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-123">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="4ad5b-124">**процессмове**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-124">**ProcessMove**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | <span data-ttu-id="4ad5b-125">Передает данные в обработчик манипуляции, связанный с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-125">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="4ad5b-126">**процессуп**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-126">**ProcessUp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | <span data-ttu-id="4ad5b-127">Передает данные в обработчик манипуляции, связанный с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-127">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="4ad5b-128">**процессдовнвистиме**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-128">**ProcessDownWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | <span data-ttu-id="4ad5b-129">Данные каналов, включая метку времени для обработчика манипуляций, связанного с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-129">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="4ad5b-130">**процессмовевистиме**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-130">**ProcessMoveWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | <span data-ttu-id="4ad5b-131">Данные каналов, включая метку времени для обработчика манипуляций, связанного с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-131">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="4ad5b-132">**процессупвистиме**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-132">**ProcessUpWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | <span data-ttu-id="4ad5b-133">Данные каналов, включая метку времени для обработчика манипуляций, связанного с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4ad5b-133">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4ad5b-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4ad5b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ad5b-135">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="4ad5b-135">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




