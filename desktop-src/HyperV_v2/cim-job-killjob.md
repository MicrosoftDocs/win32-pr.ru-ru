---
description: Метод для уничтожения этого задания и всех базовых процессов, а также для удаления любых висячих ассоциаций. Этот метод является устаревшим; Вместо этого используйте Рекуестчанжестате.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Метод Киллжоб класса CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998322"
---
# <a name="killjob-method-of-the-cim_job-class"></a><span data-ttu-id="d68d9-104">Метод Киллжоб \_ класса заданий CIM</span><span class="sxs-lookup"><span data-stu-id="d68d9-104">KillJob method of the CIM\_Job class</span></span>

<span data-ttu-id="d68d9-105">Метод для уничтожения этого задания и всех базовых процессов, а также для удаления любых "висячих" сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="d68d9-105">A method to kill this job and any underlying processes, and to remove any 'dangling' associations.</span></span> <span data-ttu-id="d68d9-106">Этот метод является устаревшим; Вместо этого используйте **рекуестчанжестате** .</span><span class="sxs-lookup"><span data-stu-id="d68d9-106">This method is deprecated; use **RequestChangeState** instead.</span></span> <span data-ttu-id="d68d9-107">**Киллжоб** является устаревшим, так как нет различий между упорядоченным завершением работы и немедленной инструкцией Kill.</span><span class="sxs-lookup"><span data-stu-id="d68d9-107">**KillJob** is being deprecated because there is no distinction made between an orderly shutdown and an immediate kill.</span></span> <span data-ttu-id="d68d9-108">[**Модель CIM \_ Конкретежоб**](cim-concretejob.md). **RequestStateChange**() предоставляет параметры "Terminate" и "Kill", чтобы разрешить это различие.</span><span class="sxs-lookup"><span data-stu-id="d68d9-108">[**CIM\_ConcreteJob**](cim-concretejob.md).**RequestStateChange**() provides 'Terminate' and 'Kill' options to allow this distinction.</span></span>

## <a name="syntax"></a><span data-ttu-id="d68d9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d68d9-109">Syntax</span></span>


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a><span data-ttu-id="d68d9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d68d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d68d9-111">*Делетеонкилл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d68d9-111">*DeleteOnKill* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d68d9-112">Указывает, должно ли задание автоматически удаляться после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="d68d9-112">Indicates whether or not the Job should be automatically deleted upon termination.</span></span> <span data-ttu-id="d68d9-113">Этот параметр имеет приоритет над свойством **делетеонкомплетион** .</span><span class="sxs-lookup"><span data-stu-id="d68d9-113">This parameter takes precedence over the **DeleteOnCompletion** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d68d9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d68d9-114">Return value</span></span>

<span data-ttu-id="d68d9-115">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d68d9-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d68d9-116">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="d68d9-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d68d9-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-118">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d68d9-118">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="d68d9-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-120">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="d68d9-120">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-121">**Отказано в доступе** (6)</span><span class="sxs-lookup"><span data-stu-id="d68d9-121">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-122">**Не найдено** (7)</span><span class="sxs-lookup"><span data-stu-id="d68d9-122">**Not Found** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d68d9-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d68d9-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="d68d9-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d68d9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d68d9-125">Requirements</span></span>



| <span data-ttu-id="d68d9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d68d9-126">Requirement</span></span> | <span data-ttu-id="d68d9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d68d9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d68d9-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d68d9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d68d9-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d68d9-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d68d9-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d68d9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d68d9-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d68d9-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d68d9-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d68d9-132">Namespace</span></span><br/>                | <span data-ttu-id="d68d9-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d68d9-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d68d9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d68d9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d68d9-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d68d9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d68d9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d68d9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d68d9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d68d9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d68d9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d68d9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d68d9-139">**\_Задание CIM**</span><span class="sxs-lookup"><span data-stu-id="d68d9-139">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

 




