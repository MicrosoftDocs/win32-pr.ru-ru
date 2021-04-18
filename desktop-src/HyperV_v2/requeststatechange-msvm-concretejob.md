---
description: Запрашивает изменение состояния задания на указанное состояние.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Метод RequestStateChange класса Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663724"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="3c3e9-103">Метод RequestStateChange \_ класса мсвм конкретежоб</span><span class="sxs-lookup"><span data-stu-id="3c3e9-103">RequestStateChange method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="3c3e9-104">Запрашивает изменение состояния задания на указанное состояние.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-104">Requests that the state of the job be changed to the specified state.</span></span> <span data-ttu-id="3c3e9-105">Вызов метода **RequestStateChange** несколько раз может привести к перезаписанию или потере предыдущих запросов.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="3c3e9-106">Если возвращается значение 0, задача выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="3c3e9-107">Любой другой код возврата указывает на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3e9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c3e9-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3c3e9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c3e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c3e9-110">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c3e9-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3e9-111">Тип: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c3e9-111">Type: **uint16**</span></span>

<span data-ttu-id="3c3e9-112">Новое состояние задания.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-112">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="3c3e9-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3c3e9-114">Изменяет состояние на "работает".</span><span class="sxs-lookup"><span data-stu-id="3c3e9-114">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="3c3e9-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3c3e9-116">Временно останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-116">Stops the job temporarily.</span></span> <span data-ttu-id="3c3e9-117">Цель — последующее перезапустить задание с помощью "Start".</span><span class="sxs-lookup"><span data-stu-id="3c3e9-117">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="3c3e9-118">В приостановленном состоянии можно ввести состояние службы.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-118">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="3c3e9-119">(Это зависит от задания.)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-119">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="3c3e9-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3c3e9-121">Выполнение задания в чистом виде, сохранение данных, сохранение состояния и завершение работы всех базовых процессов в порядке.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-121">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="3c3e9-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3c3e9-123">Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3c3e9-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3c3e9-125">Помещает задание в состояние службы, зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="3c3e9-126">Может быть возможным перезапуск задания.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3c3e9-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF**</span><span class="sxs-lookup"><span data-stu-id="3c3e9-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="3c3e9-128">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-128">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3c3e9-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован**</span><span class="sxs-lookup"><span data-stu-id="3c3e9-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="3c3e9-130">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-130">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3c3e9-131">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c3e9-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c3e9-132">Тип: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3c3e9-132">Type: **datetime**</span></span>

<span data-ttu-id="3c3e9-133">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-133">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="3c3e9-134">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-134">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="3c3e9-135">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-135">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="3c3e9-136">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (использование параметра времени ожидания не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="3c3e9-136">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c3e9-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c3e9-137">Return value</span></span>

<span data-ttu-id="3c3e9-138">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c3e9-138">Type: **uint32**</span></span>

<span data-ttu-id="3c3e9-139">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-139">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3c3e9-140">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-140">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-141">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-141">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-142">**Неизвестная или Неуказанная ошибка** (2)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-142">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-143">**Невозможно завершить в течение времени ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-143">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-144">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-144">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-145">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-145">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-146">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-146">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-147">**Зарезервировано DMTF** (7 4095)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-147">**DMTF Reserved** (7 4095)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-148">**Параметры метода проверены — начато переход** (4096)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-148">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-149">**Недопустимая смена состояния** (4097)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-149">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-150">**Использование параметра времени ожидания не поддерживается** (4098)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-150">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-151">**Занято** (4099)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-151">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-152">**Метод зарезервирован** (4100 32767)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-152">**Method Reserved** (4100 32767)</span></span>
</dt> <dt>

<span data-ttu-id="3c3e9-153">**Зависит от поставщика** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="3c3e9-153">**Vendor Specific** (32768 65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3c3e9-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c3e9-154">Remarks</span></span>

<span data-ttu-id="3c3e9-155">Доступ к классу [**\_ конкретежоб мсвм**](msvm-concretejob.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3c3e9-155">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3c3e9-156">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3c3e9-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c3e9-157">Требования</span><span class="sxs-lookup"><span data-stu-id="3c3e9-157">Requirements</span></span>



| <span data-ttu-id="3c3e9-158">Требование</span><span class="sxs-lookup"><span data-stu-id="3c3e9-158">Requirement</span></span> | <span data-ttu-id="3c3e9-159">Значение</span><span class="sxs-lookup"><span data-stu-id="3c3e9-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3e9-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c3e9-160">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3e9-161">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3c3e9-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3c3e9-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c3e9-162">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3e9-163">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3c3e9-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c3e9-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c3e9-164">Namespace</span></span><br/>                | <span data-ttu-id="3c3e9-165">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3c3e9-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3c3e9-166">MOF</span><span class="sxs-lookup"><span data-stu-id="3c3e9-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c3e9-167"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c3e9-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c3e9-168">DLL</span><span class="sxs-lookup"><span data-stu-id="3c3e9-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c3e9-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c3e9-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c3e9-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c3e9-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3e9-171">**Мсвм \_ конкретежоб**</span><span class="sxs-lookup"><span data-stu-id="3c3e9-171">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

