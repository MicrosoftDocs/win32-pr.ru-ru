---
title: Ирдвтаскплугиннотифисинк ScheduleTask, метод
description: Вызывается агентом задачи для планирования задачи.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ScheduleTask
- Службы удаленных рабочих столов метода ScheduleTask, интерфейс Ирдвтаскплугиннотифисинк
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк, метод ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892630"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a><span data-ttu-id="5db16-106">Метод Ирдвтаскплугиннотифисинк:: ScheduleTask</span><span class="sxs-lookup"><span data-stu-id="5db16-106">IRDVTaskPluginNotifySink::ScheduleTask method</span></span>

<span data-ttu-id="5db16-107">Вызывается агентом задачи для планирования задачи.</span><span class="sxs-lookup"><span data-stu-id="5db16-107">Called by the task agent to schedule a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db16-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5db16-108">Syntax</span></span>


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a><span data-ttu-id="5db16-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5db16-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db16-110">*фтстарттиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5db16-110">*ftStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db16-111">Тип: **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="5db16-111">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="5db16-112">Самое раннее время запуска задачи в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="5db16-112">The earliest task start time, in UTC.</span></span>

</dd> <dt>

<span data-ttu-id="5db16-113">*фтендтиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5db16-113">*ftEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db16-114">Тип: **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="5db16-114">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="5db16-115">Время окончания задачи в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="5db16-115">The task end time, in UTC.</span></span> <span data-ttu-id="5db16-116">Передайте значение [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , равное всем нулям, если время окончания не указано.</span><span class="sxs-lookup"><span data-stu-id="5db16-116">Pass a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) set to all zeros if no end time is specified.</span></span>

</dd> <dt>

<span data-ttu-id="5db16-117">*фтдеадлине* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5db16-117">*ftDeadline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db16-118">Тип: **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="5db16-118">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="5db16-119">Крайний срок задачи в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="5db16-119">The task deadline, in UTC.</span></span> <span data-ttu-id="5db16-120">Используется для задания приоритета для нескольких задач, находящихся в начальном окне.</span><span class="sxs-lookup"><span data-stu-id="5db16-120">This is used to set priority for multiple tasks that are within their start window.</span></span> <span data-ttu-id="5db16-121">Если необходимо запустить более одной задачи, сначала начнется одна из них с самым ранним сроком.</span><span class="sxs-lookup"><span data-stu-id="5db16-121">If more than one task should be started, the one with the earliest deadline will be started first.</span></span>

</dd> <dt>

<span data-ttu-id="5db16-122">*бстрлабел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5db16-122">*bstrLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db16-123">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5db16-123">Type: **BSTR**</span></span>

<span data-ttu-id="5db16-124">Метка для задачи.</span><span class="sxs-lookup"><span data-stu-id="5db16-124">The label for the task.</span></span> <span data-ttu-id="5db16-125">Передается методу [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="5db16-125">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5db16-126">*bstrIdentifier* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5db16-126">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db16-127">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5db16-127">Type: **BSTR**</span></span>

<span data-ttu-id="5db16-128">Идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="5db16-128">The identifier of the task.</span></span> <span data-ttu-id="5db16-129">Передается методу [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="5db16-129">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5db16-130">*саконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5db16-130">*saContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db16-131">Тип: **SAFEARRAY (Byte)**</span><span class="sxs-lookup"><span data-stu-id="5db16-131">Type: **SAFEARRAY(BYTE)**</span></span>

<span data-ttu-id="5db16-132">Необязательные данные для задачи.</span><span class="sxs-lookup"><span data-stu-id="5db16-132">Optional data for the task.</span></span> <span data-ttu-id="5db16-133">Передается методу [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="5db16-133">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db16-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5db16-134">Return value</span></span>

<span data-ttu-id="5db16-135">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5db16-135">Type: **HRESULT**</span></span>

<span data-ttu-id="5db16-136">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5db16-136">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5db16-137">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5db16-137">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5db16-138">Требования</span><span class="sxs-lookup"><span data-stu-id="5db16-138">Requirements</span></span>



| <span data-ttu-id="5db16-139">Требование</span><span class="sxs-lookup"><span data-stu-id="5db16-139">Requirement</span></span> | <span data-ttu-id="5db16-140">Значение</span><span class="sxs-lookup"><span data-stu-id="5db16-140">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="5db16-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5db16-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5db16-142">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="5db16-142">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="5db16-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5db16-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5db16-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5db16-144">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5db16-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5db16-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db16-146">**ирдвтаскплугиннотифисинк**</span><span class="sxs-lookup"><span data-stu-id="5db16-146">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

