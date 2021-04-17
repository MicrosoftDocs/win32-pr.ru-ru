---
description: Запрашивает изменение состояния репликации отношения репликации виртуальной машины на указанное значение.
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: 'Метод Msvm_ComputerSystem:: Рекуестрепликатионстатечанжеекс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650916"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a><span data-ttu-id="c2806-103">Мсвм \_ ComputerSystem:: рекуестрепликатионстатечанжеекс, метод</span><span class="sxs-lookup"><span data-stu-id="c2806-103">Msvm\_ComputerSystem::RequestReplicationStateChangeEx method</span></span>

<span data-ttu-id="c2806-104">Запрашивает изменение состояния репликации отношения репликации виртуальной машины на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="c2806-104">Requests that the replication state of the replication relationship of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="c2806-105">Пока изменение состояния выполняется, свойство **ReplicationState** изменяется на значение параметра *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="c2806-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="c2806-106">Этот метод поддерживается только для экземпляров класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющих виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="c2806-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2806-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2806-107">Syntax</span></span>


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c2806-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2806-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2806-109">*Репликатионрелатионшип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2806-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2806-110">Строковое представление внедренного экземпляра класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , определяющего отношение репликации для запроса на изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="c2806-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for state change request.</span></span> <span data-ttu-id="c2806-111">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c2806-111">This parameter is optional.</span></span> <span data-ttu-id="c2806-112">Если он не указан, запрос выполняется в отношении первичной репликации.</span><span class="sxs-lookup"><span data-stu-id="c2806-112">When it's unspecified, the request runs on the primary replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="c2806-113">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2806-113">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2806-114">Новое состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="c2806-114">The new replication state.</span></span> <span data-ttu-id="c2806-115">Параметр должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c2806-115">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="c2806-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Все готово для запуска начальной репликации** (1)</span><span class="sxs-lookup"><span data-stu-id="c2806-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c2806-117">Все готово для запуска начальной репликации.</span><span class="sxs-lookup"><span data-stu-id="c2806-117">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="c2806-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Ожидание завершения начальной репликации** (2)</span><span class="sxs-lookup"><span data-stu-id="c2806-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c2806-119">Ожидание завершения начальной репликации.</span><span class="sxs-lookup"><span data-stu-id="c2806-119">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="c2806-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Репликация** (3)</span><span class="sxs-lookup"><span data-stu-id="c2806-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c2806-121">репликация.</span><span class="sxs-lookup"><span data-stu-id="c2806-121">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="c2806-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Синхронизированная репликация завершена** (4)</span><span class="sxs-lookup"><span data-stu-id="c2806-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c2806-123">Синхронизированная репликация завершена.</span><span class="sxs-lookup"><span data-stu-id="c2806-123">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="c2806-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановка** (7)</span><span class="sxs-lookup"><span data-stu-id="c2806-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c2806-125">Приостановить репликацию.</span><span class="sxs-lookup"><span data-stu-id="c2806-125">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="c2806-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Отменить повторную синхронизацию** (9)</span><span class="sxs-lookup"><span data-stu-id="c2806-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c2806-127">Отменить повторную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="c2806-127">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c2806-128">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c2806-128">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2806-129">Необязательная ссылка на объект [**мсвм \_ конкретежоб**](msvm-concretejob.md) , который возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="c2806-129">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="c2806-130">При наличии возвращаемой ссылки можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="c2806-130">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="c2806-131">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2806-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2806-132">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c2806-132">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2806-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2806-133">Return value</span></span>

<span data-ttu-id="c2806-134">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c2806-134">This method returns one of the following values.</span></span>



| <span data-ttu-id="c2806-135">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c2806-135">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="c2806-136">Описание</span><span class="sxs-lookup"><span data-stu-id="c2806-136">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2806-137"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-137"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="c2806-138">Успешно</span><span class="sxs-lookup"><span data-stu-id="c2806-138">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="c2806-139"><dt>**Параметры метода проверены — задание запущено**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-139"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="c2806-140">Переход является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="c2806-140">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="c2806-141"><dt>**Сбой**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-141"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-142"><dt>**Отказано в доступе**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-142"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-143"><dt>**Не поддерживается**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-143"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-144"><dt>**Состояние неизвестно**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-144"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-145"><dt>**Время ожидания**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-145"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-146"><dt>**Недопустимый параметр**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-146"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="c2806-147">Значение, указанное в одном из параметров, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2806-147">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="c2806-148"><dt>**Система используется**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-148"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-149"><dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-149"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="c2806-150">Значение, указанное в параметре *RequestedState* , не поддерживается в текущем режиме репликации или состоянии.</span><span class="sxs-lookup"><span data-stu-id="c2806-150">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="c2806-151"><dt>**Недопустимый тип данных**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-151"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-152"><dt>**Система недоступна**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-152"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-153"><dt>**Недостаточно памяти**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-153"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="c2806-154"><dt>**Файл не найден**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-154"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="c2806-155">Требования</span><span class="sxs-lookup"><span data-stu-id="c2806-155">Requirements</span></span>



| <span data-ttu-id="c2806-156">Требование</span><span class="sxs-lookup"><span data-stu-id="c2806-156">Requirement</span></span> | <span data-ttu-id="c2806-157">Значение</span><span class="sxs-lookup"><span data-stu-id="c2806-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2806-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2806-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c2806-159">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2806-159">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c2806-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2806-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c2806-161">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c2806-161">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2806-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c2806-162">Namespace</span></span><br/>                | <span data-ttu-id="c2806-163">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c2806-163">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="c2806-164">MOF</span><span class="sxs-lookup"><span data-stu-id="c2806-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2806-165"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2806-166">DLL</span><span class="sxs-lookup"><span data-stu-id="c2806-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2806-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2806-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c2806-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2806-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2806-169">**Мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="c2806-169">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




