---
description: Запрашивает изменение состояния задания на значение, указанное в параметре RequestedState. Вызов метода RequestStateChange несколько раз может привести к перезаписанию или потере предыдущих запросов.
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: Метод RequestStateChange класса CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344132"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a><span data-ttu-id="19b61-104">Метод RequestStateChange \_ класса CIM конкретежоб</span><span class="sxs-lookup"><span data-stu-id="19b61-104">RequestStateChange method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="19b61-105">Запрашивает изменение состояния задания на значение, указанное в параметре RequestedState.</span><span class="sxs-lookup"><span data-stu-id="19b61-105">Requests that the state of the job be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="19b61-106">Вызов метода RequestStateChange несколько раз может привести к перезаписанию или потере предыдущих запросов.</span><span class="sxs-lookup"><span data-stu-id="19b61-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

<span data-ttu-id="19b61-107">Если возвращается значение 0, задача выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="19b61-107">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="19b61-108">Любой другой код возврата указывает на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="19b61-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b61-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19b61-109">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="19b61-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="19b61-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19b61-111">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19b61-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19b61-112">Состояние запроса задания.</span><span class="sxs-lookup"><span data-stu-id="19b61-112">The state to request for a job.</span></span> <span data-ttu-id="19b61-113">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="19b61-113">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="19b61-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)</span><span class="sxs-lookup"><span data-stu-id="19b61-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19b61-115">Изменяет состояние на "работает".</span><span class="sxs-lookup"><span data-stu-id="19b61-115">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="19b61-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)</span><span class="sxs-lookup"><span data-stu-id="19b61-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="19b61-117">Временно останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="19b61-117">Stops the job temporarily.</span></span> <span data-ttu-id="19b61-118">Цель — последующее перезапустить задание с помощью "Start".</span><span class="sxs-lookup"><span data-stu-id="19b61-118">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="19b61-119">В приостановленном состоянии можно ввести состояние службы.</span><span class="sxs-lookup"><span data-stu-id="19b61-119">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="19b61-120">(Это зависит от задания.)</span><span class="sxs-lookup"><span data-stu-id="19b61-120">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="19b61-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)</span><span class="sxs-lookup"><span data-stu-id="19b61-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="19b61-122">Останавливает задание в чистом виде, сохраняет данные, сохраняет состояние и завершает все базовые процессы упорядоченным образом.</span><span class="sxs-lookup"><span data-stu-id="19b61-122">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="19b61-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="19b61-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="19b61-124">Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.</span><span class="sxs-lookup"><span data-stu-id="19b61-124">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="19b61-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)</span><span class="sxs-lookup"><span data-stu-id="19b61-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="19b61-126">Помещает задание в состояние службы, зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="19b61-126">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="19b61-127">Может быть возможным перезапуск задания.</span><span class="sxs-lookup"><span data-stu-id="19b61-127">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="19b61-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="19b61-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="19b61-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="19b61-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="19b61-130">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19b61-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19b61-131">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="19b61-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="19b61-132">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="19b61-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="19b61-133">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="19b61-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="19b61-134">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="19b61-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19b61-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19b61-135">Return value</span></span>

<span data-ttu-id="19b61-136">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="19b61-136">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="19b61-137">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="19b61-137">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-138">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="19b61-138">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-139">**Неизвестная или Неуказанная ошибка** (2)</span><span class="sxs-lookup"><span data-stu-id="19b61-139">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-140">**Не удается завершить в течение времени ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="19b61-140">**Can NOT complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-141">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="19b61-141">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-142">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="19b61-142">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-143">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="19b61-143">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-144">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="19b61-144">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-145">**Параметры метода проверены — начато переход** (4096)</span><span class="sxs-lookup"><span data-stu-id="19b61-145">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-146">**Недопустимая смена состояния** (4097)</span><span class="sxs-lookup"><span data-stu-id="19b61-146">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-147">**Использование параметра времени ожидания не поддерживается** (4098)</span><span class="sxs-lookup"><span data-stu-id="19b61-147">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-148">**Занято** (4099)</span><span class="sxs-lookup"><span data-stu-id="19b61-148">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-149">**Метод зарезервирован** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="19b61-149">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="19b61-150">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="19b61-150">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="19b61-151">Требования</span><span class="sxs-lookup"><span data-stu-id="19b61-151">Requirements</span></span>



| <span data-ttu-id="19b61-152">Требование</span><span class="sxs-lookup"><span data-stu-id="19b61-152">Requirement</span></span> | <span data-ttu-id="19b61-153">Значение</span><span class="sxs-lookup"><span data-stu-id="19b61-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b61-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19b61-154">Minimum supported client</span></span><br/> | <span data-ttu-id="19b61-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="19b61-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="19b61-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19b61-156">Minimum supported server</span></span><br/> | <span data-ttu-id="19b61-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="19b61-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="19b61-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="19b61-158">Namespace</span></span><br/>                | <span data-ttu-id="19b61-159">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="19b61-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19b61-160">MOF</span><span class="sxs-lookup"><span data-stu-id="19b61-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19b61-161"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19b61-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19b61-162">DLL</span><span class="sxs-lookup"><span data-stu-id="19b61-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b61-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19b61-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19b61-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19b61-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b61-165">**\_КОНКРЕТЕЖОБ CIM**</span><span class="sxs-lookup"><span data-stu-id="19b61-165">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




