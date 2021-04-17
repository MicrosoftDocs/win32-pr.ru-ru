---
description: Изменяет состояние задания.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Метод Msvm_CopyFileToGuestJob:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683748"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a><span data-ttu-id="2d93e-103">Мсвм \_ копифилетогуестжоб:: RequestStateChange, метод</span><span class="sxs-lookup"><span data-stu-id="2d93e-103">Msvm\_CopyFileToGuestJob::RequestStateChange method</span></span>

<span data-ttu-id="2d93e-104">Изменяет состояние задания.</span><span class="sxs-lookup"><span data-stu-id="2d93e-104">Changes the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d93e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d93e-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="2d93e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d93e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d93e-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d93e-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d93e-108">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="2d93e-108">The new state.</span></span> <span data-ttu-id="2d93e-109">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="2d93e-109">These are the possible values:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="2d93e-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)</span><span class="sxs-lookup"><span data-stu-id="2d93e-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2d93e-111">Изменяет состояние на "работает".</span><span class="sxs-lookup"><span data-stu-id="2d93e-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="2d93e-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)</span><span class="sxs-lookup"><span data-stu-id="2d93e-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2d93e-113">Временно останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="2d93e-113">Stops the job temporarily.</span></span> <span data-ttu-id="2d93e-114">Затем клиент может впоследствии перезапустить задание с помощью "Start".</span><span class="sxs-lookup"><span data-stu-id="2d93e-114">The client can then subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="2d93e-115">Клиент может, возможно, войти в состояние "Service", когда приостановлено (это зависит от задания).</span><span class="sxs-lookup"><span data-stu-id="2d93e-115">The client can possibly enter the 'Service' state while suspended (this is job-specific).</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="2d93e-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)</span><span class="sxs-lookup"><span data-stu-id="2d93e-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2d93e-117">Выполнение задания в чистом виде, сохранение данных, сохранение состояния и завершение работы всех базовых процессов в порядке.</span><span class="sxs-lookup"><span data-stu-id="2d93e-117">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="2d93e-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="2d93e-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2d93e-119">Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.</span><span class="sxs-lookup"><span data-stu-id="2d93e-119">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2d93e-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)</span><span class="sxs-lookup"><span data-stu-id="2d93e-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2d93e-121">Помещает задание в состояние службы, зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="2d93e-121">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="2d93e-122">Клиент может, возможно, перезапустить задание.</span><span class="sxs-lookup"><span data-stu-id="2d93e-122">The client can possibly restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2d93e-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2d93e-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2d93e-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2d93e-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="2d93e-125">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d93e-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d93e-126">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="2d93e-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="2d93e-127">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="2d93e-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="2d93e-128">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="2d93e-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="2d93e-129">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="2d93e-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d93e-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d93e-130">Return value</span></span>

<span data-ttu-id="2d93e-131">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2d93e-131">This method returns one of the following values.</span></span>



| <span data-ttu-id="2d93e-132">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2d93e-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="2d93e-133">Описание</span><span class="sxs-lookup"><span data-stu-id="2d93e-133">Description</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d93e-134"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-134"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="2d93e-135">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2d93e-135">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="2d93e-136"><dt>**Использование параметра времени ожидания не поддерживается**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-136"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="2d93e-137"><dt>**Сбой**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-137"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                |                                                                                    |
| <dl> <span data-ttu-id="2d93e-138"><dt>**Отказано в доступе**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-138"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                         | <span data-ttu-id="2d93e-139">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2d93e-139">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="2d93e-140"><dt>**Не поддерживается**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-140"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                         |                                                                                    |
| <dl> <span data-ttu-id="2d93e-141"><dt>**Состояние неизвестно**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-141"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="2d93e-142"><dt>**Время ожидания**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-142"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                               |                                                                                    |
| <dl> <span data-ttu-id="2d93e-143"><dt>**Недопустимый параметр**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-143"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="2d93e-144"><dt>**Система используется**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-144"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                      |                                                                                    |
| <dl> <span data-ttu-id="2d93e-145"><dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-145"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>      | <span data-ttu-id="2d93e-146">Значение, указанное в параметре *RequestedState* , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2d93e-146">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="2d93e-147"><dt>**Недопустимый тип данных**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-147"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                   |                                                                                    |
| <dl> <span data-ttu-id="2d93e-148"><dt>**Система недоступна**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-148"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>               |                                                                                    |
| <dl> <span data-ttu-id="2d93e-149"><dt>**Недостаточно памяти**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-149"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                         |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="2d93e-150">Требования</span><span class="sxs-lookup"><span data-stu-id="2d93e-150">Requirements</span></span>



| <span data-ttu-id="2d93e-151">Требование</span><span class="sxs-lookup"><span data-stu-id="2d93e-151">Requirement</span></span> | <span data-ttu-id="2d93e-152">Значение</span><span class="sxs-lookup"><span data-stu-id="2d93e-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d93e-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d93e-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2d93e-154">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d93e-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2d93e-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d93e-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2d93e-156">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d93e-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d93e-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2d93e-157">Namespace</span></span><br/>                | <span data-ttu-id="2d93e-158">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2d93e-158">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="2d93e-159">MOF</span><span class="sxs-lookup"><span data-stu-id="2d93e-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d93e-160"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d93e-161">DLL</span><span class="sxs-lookup"><span data-stu-id="2d93e-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d93e-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d93e-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d93e-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d93e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d93e-164">**Мсвм \_ копифилетогуестжоб**</span><span class="sxs-lookup"><span data-stu-id="2d93e-164">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




