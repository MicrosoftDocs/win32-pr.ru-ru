---
title: Перечисление задач
description: Планировщик задач 1,0 предоставляет объект перечисления для перечисления задач в папке «Назначенные задания».
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- Перечисление задач планировщик задач
- Перечисление задач планировщик задач, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068269"
---
# <a name="enumerating-tasks"></a><span data-ttu-id="df349-105">Перечисление задач</span><span class="sxs-lookup"><span data-stu-id="df349-105">Enumerating Tasks</span></span>

<span data-ttu-id="df349-106">Планировщик задач 1,0 предоставляет объект перечисления для перечисления задач в [*папке «Назначенные задания*](s.md)».</span><span class="sxs-lookup"><span data-stu-id="df349-106">Task Scheduler 1.0 provides an enumeration object for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>

> [!Note]  
> <span data-ttu-id="df349-107">Для компьютера под управлением Windows Server 2003, Windows XP или Windows 2000 для создания, мониторинга и управления задачами на компьютере с Windows Vista некоторые операции должны быть выполнены на компьютере под управлением Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df349-107">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="df349-108">Дополнительные сведения см. в разделе [Задачи](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="df349-108">For more information, see [Tasks](tasks.md).</span></span>

 

## <a name="using-the-enumeration-object"></a><span data-ttu-id="df349-109">Использование объекта перечисления</span><span class="sxs-lookup"><span data-stu-id="df349-109">Using the Enumeration Object</span></span>

<span data-ttu-id="df349-110">Интерфейс [**иенумворкитемс**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) этого объекта предоставляет методы для перечисления задач в папке, сброса последовательности перечисления до начала списка, пропуска задач и создания копии текущего объекта перечисления для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="df349-110">The [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface of this object provides methods for enumerating the tasks in the folder, resetting the enumeration sequence to the start of the list, skipping tasks, and making a copy of the current enumeration object for later use.</span></span>

<span data-ttu-id="df349-111">Сведения о перечислении задач в папке «запланированные задания» см. в разделе [**иенумворкитемс:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span><span class="sxs-lookup"><span data-stu-id="df349-111">For information about enumerating the tasks in the Scheduled tasks folder, see [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span></span>

<span data-ttu-id="df349-112">Дополнительные сведения о сбросе перечисления в начало списка см. в разделе [**иенумворкитемс:: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span><span class="sxs-lookup"><span data-stu-id="df349-112">For information about resetting the enumeration to the start of the list, see [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span></span>

<span data-ttu-id="df349-113">Дополнительные сведения о пропуске задач см. в разделе [**иенумворкитемс:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span><span class="sxs-lookup"><span data-stu-id="df349-113">For information about skipping tasks, see [**IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span></span>

<span data-ttu-id="df349-114">Сведения о создании копии текущего объекта перечисления см. в разделе [**иенумворкитемс:: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span><span class="sxs-lookup"><span data-stu-id="df349-114">For information about making a copy of the current enumeration object, see [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span></span>

<span data-ttu-id="df349-115">Пример перечисления задач в папке «запланированные задания» см. в разделе [Пример перечисления задач](enumerating-tasks-example.md).</span><span class="sxs-lookup"><span data-stu-id="df349-115">For an example of enumerating the tasks in the Scheduled Tasks folder, see [Enumerating Tasks Example](enumerating-tasks-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df349-116">См. также</span><span class="sxs-lookup"><span data-stu-id="df349-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="df349-117">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="df349-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="df349-118">Сведения о задаче планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="df349-118">Task Scheduler 1.0 Task Information</span></span>](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




