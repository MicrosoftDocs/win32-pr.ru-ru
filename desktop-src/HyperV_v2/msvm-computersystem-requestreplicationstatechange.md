---
description: Запрашивает изменение состояния репликации виртуальной машины на указанное значение и действует в отношении первичной репликации виртуальной машины.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Метод Рекуестрепликатионстатечанже класса Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544735"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="db75d-103">Метод Рекуестрепликатионстатечанже \_ класса ComputerSystem мсвм</span><span class="sxs-lookup"><span data-stu-id="db75d-103">RequestReplicationStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="db75d-104">Запрашивает изменение состояния репликации виртуальной машины на указанное значение и действует в отношении первичной репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="db75d-104">Requests that the replication state of the virtual machine be changed to the specified value and acts on the primary replication relationship of the virtual machine.</span></span> <span data-ttu-id="db75d-105">Пока изменение состояния выполняется, свойство **ReplicationState** изменяется на значение параметра *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="db75d-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="db75d-106">Этот метод поддерживается только для экземпляров класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющих виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="db75d-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="db75d-107">Начиная с Windows 8.1 мы рекомендуем не использовать **рекуестрепликатионстатечанже** для запроса изменения состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="db75d-107">Starting with Windows 8.1, we recommend not to use **RequestReplicationStateChange** anymore to request changing of replication state.</span></span> <span data-ttu-id="db75d-108">Вместо этого используйте [**рекуестрепликатионстатечанжеекс**](msvm-requestreplicationstatechangeex-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="db75d-108">Instead, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="db75d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db75d-109">Syntax</span></span>


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="db75d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="db75d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db75d-111">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db75d-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db75d-112">Новое состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="db75d-112">The new replication state.</span></span> <span data-ttu-id="db75d-113">Параметр должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="db75d-113">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="db75d-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Все готово для запуска начальной репликации** (1)</span><span class="sxs-lookup"><span data-stu-id="db75d-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="db75d-115">Все готово для запуска начальной репликации.</span><span class="sxs-lookup"><span data-stu-id="db75d-115">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="db75d-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Ожидание завершения начальной репликации** (2)</span><span class="sxs-lookup"><span data-stu-id="db75d-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db75d-117">Ожидание завершения начальной репликации.</span><span class="sxs-lookup"><span data-stu-id="db75d-117">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="db75d-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Репликация** (3)</span><span class="sxs-lookup"><span data-stu-id="db75d-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db75d-119">репликация.</span><span class="sxs-lookup"><span data-stu-id="db75d-119">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="db75d-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Синхронизированная репликация завершена** (4)</span><span class="sxs-lookup"><span data-stu-id="db75d-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db75d-121">Синхронизированная репликация завершена.</span><span class="sxs-lookup"><span data-stu-id="db75d-121">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="db75d-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановка** (7)</span><span class="sxs-lookup"><span data-stu-id="db75d-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="db75d-123">Приостановить репликацию.</span><span class="sxs-lookup"><span data-stu-id="db75d-123">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="db75d-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Отменить повторную синхронизацию** (9)</span><span class="sxs-lookup"><span data-stu-id="db75d-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="db75d-125">Отменить повторную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="db75d-125">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="db75d-126">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db75d-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db75d-127">Необязательная ссылка на объект [**мсвм \_ конкретежоб**](msvm-concretejob.md) , который возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="db75d-127">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="db75d-128">При наличии возвращаемой ссылки можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="db75d-128">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="db75d-129">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db75d-129">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db75d-130">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="db75d-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db75d-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db75d-131">Return value</span></span>

<span data-ttu-id="db75d-132">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="db75d-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="db75d-133">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="db75d-133">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="db75d-134">Описание</span><span class="sxs-lookup"><span data-stu-id="db75d-134">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db75d-135"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="db75d-136">Успешно</span><span class="sxs-lookup"><span data-stu-id="db75d-136">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="db75d-137"><dt>**Параметры метода проверены — задание запущено**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-137"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="db75d-138">Переход является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="db75d-138">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="db75d-139"><dt>**Сбой**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-139"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-140"><dt>**Отказано в доступе**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-140"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-141"><dt>**Не поддерживается**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-141"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-142"><dt>**Состояние неизвестно**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-142"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-143"><dt>**Время ожидания**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-143"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-144"><dt>**Недопустимый параметр**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-144"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="db75d-145">Значение, указанное в одном из параметров, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="db75d-145">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="db75d-146"><dt>**Система используется**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-146"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-147"><dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-147"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="db75d-148">Значение, указанное в параметре *RequestedState* , не поддерживается в текущем режиме репликации или состоянии.</span><span class="sxs-lookup"><span data-stu-id="db75d-148">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="db75d-149"><dt>**Недопустимый тип данных**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-149"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-150"><dt>**Система недоступна**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-150"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-151"><dt>**Недостаточно памяти**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-151"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="db75d-152"><dt>**Файл не найден**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-152"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="db75d-153">Требования</span><span class="sxs-lookup"><span data-stu-id="db75d-153">Requirements</span></span>



| <span data-ttu-id="db75d-154">Требование</span><span class="sxs-lookup"><span data-stu-id="db75d-154">Requirement</span></span> | <span data-ttu-id="db75d-155">Значение</span><span class="sxs-lookup"><span data-stu-id="db75d-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db75d-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db75d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="db75d-157">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="db75d-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="db75d-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db75d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="db75d-159">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="db75d-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db75d-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db75d-160">Namespace</span></span><br/>                | <span data-ttu-id="db75d-161">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="db75d-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="db75d-162">MOF</span><span class="sxs-lookup"><span data-stu-id="db75d-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db75d-163"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="db75d-164">DLL</span><span class="sxs-lookup"><span data-stu-id="db75d-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db75d-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="db75d-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="db75d-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db75d-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db75d-167">**Мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="db75d-167">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




