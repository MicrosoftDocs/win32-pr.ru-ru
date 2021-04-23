---
title: Свойства Итссбтаскинфо
description: Интерфейс Итссбтаскинфо предоставляет следующие свойства.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783819"
---
# <a name="itssbtaskinfo-properties"></a><span data-ttu-id="3e21d-103">Свойства Итссбтаскинфо</span><span class="sxs-lookup"><span data-stu-id="3e21d-103">ITsSbTaskInfo Properties</span></span>

<span data-ttu-id="3e21d-104">Интерфейс [**итссбтаскинфо**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e21d-104">The [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e21d-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="3e21d-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3e21d-106">**Свойство Context**</span><span class="sxs-lookup"><span data-stu-id="3e21d-106">**Context property**</span></span>](itssbtaskinfo-context.md)
</dt> <dd>

<span data-ttu-id="3e21d-107">Извлекает байты контекста, связанные с задачей.</span><span class="sxs-lookup"><span data-stu-id="3e21d-107">Retrieves the context bytes associated with the task.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-108">**Свойство крайний срок**</span><span class="sxs-lookup"><span data-stu-id="3e21d-108">**Deadline property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

<span data-ttu-id="3e21d-109">Возвращает время, в которое должна быть инициирована задача.</span><span class="sxs-lookup"><span data-stu-id="3e21d-109">Retrieves the time by which the task must be initiated.</span></span> <span data-ttu-id="3e21d-110">Используется для определения приоритетов исправлений.</span><span class="sxs-lookup"><span data-stu-id="3e21d-110">This is used to prioritize patches.</span></span> <span data-ttu-id="3e21d-111">Сначала будет инициировано исправление с самым ранним сроком.</span><span class="sxs-lookup"><span data-stu-id="3e21d-111">The patch with the earliest deadline will get initiated first.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-112">**EndTime, свойство**</span><span class="sxs-lookup"><span data-stu-id="3e21d-112">**EndTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

<span data-ttu-id="3e21d-113">Возвращает последнее время, в течение которого агент задачи может запустить задачу.</span><span class="sxs-lookup"><span data-stu-id="3e21d-113">Retrieves the latest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-114">**Свойство идентификатора**</span><span class="sxs-lookup"><span data-stu-id="3e21d-114">**Identifier property**</span></span>](itssbtaskinfo-identifier.md)
</dt> <dd>

<span data-ttu-id="3e21d-115">Извлекает идентификатор GUID, используемый агентом задачи в качестве уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="3e21d-115">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-116">**Свойство Label**</span><span class="sxs-lookup"><span data-stu-id="3e21d-116">**Label property**</span></span>](itssbtaskinfo-label.md)
</dt> <dd>

<span data-ttu-id="3e21d-117">Извлекает метку, которая описывает назначение задачи.</span><span class="sxs-lookup"><span data-stu-id="3e21d-117">Retrieves the label that describes the purpose of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-118">**Свойство подключаемого модуля**</span><span class="sxs-lookup"><span data-stu-id="3e21d-118">**Plugin property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

<span data-ttu-id="3e21d-119">Возвращает отображаемое имя агента задачи.</span><span class="sxs-lookup"><span data-stu-id="3e21d-119">Retrieves the display name of the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-120">**StartTime, свойство**</span><span class="sxs-lookup"><span data-stu-id="3e21d-120">**StartTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

<span data-ttu-id="3e21d-121">Возвращает самое раннее время, в течение которого агент задачи может запустить задачу.</span><span class="sxs-lookup"><span data-stu-id="3e21d-121">Retrieves the earliest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-122">**Свойство Status**</span><span class="sxs-lookup"><span data-stu-id="3e21d-122">**Status property**</span></span>](itssbtaskinfo-status.md)
</dt> <dd>

<span data-ttu-id="3e21d-123">Извлекает значение [**перечисления \_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , представляющее состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="3e21d-123">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="3e21d-124">**TargetId, свойство**</span><span class="sxs-lookup"><span data-stu-id="3e21d-124">**TargetId property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

<span data-ttu-id="3e21d-125">Извлекает идентификатор целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3e21d-125">Retrieves the target identifier.</span></span>

</dd> </dl>

 

 




