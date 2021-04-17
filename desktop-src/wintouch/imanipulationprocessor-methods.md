---
title: Методы (IInertiaProcessor)
description: В этом разделе содержатся методы для интерфейса IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, интерфейс IInertiaProcessor
- Касание Windows, методы интерфейса
- инерция, интерфейс IInertiaProcessor
- Интерфейс IInertiaProcessor, методы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710435"
---
# <a name="methods-iinertiaprocessor"></a><span data-ttu-id="e2938-107">Методы (IInertiaProcessor)</span><span class="sxs-lookup"><span data-stu-id="e2938-107">Methods (IInertiaProcessor)</span></span>

<span data-ttu-id="e2938-108">В этом разделе содержатся методы для интерфейса [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="e2938-108">This section contains the methods for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="e2938-109">Метод</span><span class="sxs-lookup"><span data-stu-id="e2938-109">Method</span></span>                                                 | <span data-ttu-id="e2938-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e2938-110">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2938-111">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="e2938-111">**Reset**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | <span data-ttu-id="e2938-112">Инициализирует процессор с начальной меткой времени и перезапускает инерцию.</span><span class="sxs-lookup"><span data-stu-id="e2938-112">Initializes the processor with initial time stamp and restarts inertia.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="e2938-113">**Процесс**</span><span class="sxs-lookup"><span data-stu-id="e2938-113">**Process**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | <span data-ttu-id="e2938-114">Выполняет вычисления для текущего такта и может вызвать событие **Дельта** или **Completed** в зависимости от того, завершено ли экстраполяция.</span><span class="sxs-lookup"><span data-stu-id="e2938-114">Performs calculations for the current tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span> <span data-ttu-id="e2938-115">Если экстраполяция завершается в предыдущем такте, метод является оператором No-Op.</span><span class="sxs-lookup"><span data-stu-id="e2938-115">If extrapolation finished at the previous tick, the method is no-op.</span></span> |
| [<span data-ttu-id="e2938-116">**процесстиме**</span><span class="sxs-lookup"><span data-stu-id="e2938-116">**ProcessTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | <span data-ttu-id="e2938-117">Выполняет вычисления для заданного такта и может вызвать событие **Дельта** или **Completed** в зависимости от того, завершено ли экстраполяция.</span><span class="sxs-lookup"><span data-stu-id="e2938-117">Performs calculations for the given tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span>                                                                        |
| [<span data-ttu-id="e2938-118">**Завершить**</span><span class="sxs-lookup"><span data-stu-id="e2938-118">**Complete**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | <span data-ttu-id="e2938-119">Завершает текущую манипуляцию и останавливает инерцию в обработчике инерции.</span><span class="sxs-lookup"><span data-stu-id="e2938-119">Finishes the current manipulation and stops inertia on the inertia processor.</span></span>                                                                                                                                              |
| [<span data-ttu-id="e2938-120">**комплететиме**</span><span class="sxs-lookup"><span data-stu-id="e2938-120">**CompleteTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | <span data-ttu-id="e2938-121">Завершает текущую обработку в заданном такте, останавливает инерцию в обработчике инерции и создает событие ManipulationCompleted.</span><span class="sxs-lookup"><span data-stu-id="e2938-121">Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.</span></span>                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="e2938-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e2938-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2938-123">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="e2938-123">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




