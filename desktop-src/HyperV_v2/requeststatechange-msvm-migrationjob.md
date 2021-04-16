---
description: Запрашивает изменение состояния задания миграции на указанное состояние.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Метод RequestStateChange класса Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31011de619780ae36f390ee87038300a3b42fef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663067"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="9c9ce-103">Метод RequestStateChange \_ класса мсвм мигратионжоб</span><span class="sxs-lookup"><span data-stu-id="9c9ce-103">RequestStateChange method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="9c9ce-104">Запрашивает изменение состояния задания миграции на указанное состояние.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-104">Requests that the state of the migration job be changed to the specified state.</span></span> <span data-ttu-id="9c9ce-105">Вызов метода **RequestStateChange** несколько раз может привести к перезаписанию или потере предыдущих запросов.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="9c9ce-106">Если возвращается значение 0, задача выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="9c9ce-107">Любой другой код возврата указывает на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9ce-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c9ce-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="9c9ce-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c9ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c9ce-110">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c9ce-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c9ce-111">Новое состояние задания.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-111">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="9c9ce-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9c9ce-113">Изменяет состояние на "работает".</span><span class="sxs-lookup"><span data-stu-id="9c9ce-113">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="9c9ce-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9c9ce-115">Временно останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-115">Stops the job temporarily.</span></span> <span data-ttu-id="9c9ce-116">Цель — последующее перезапустить задание с помощью "Start".</span><span class="sxs-lookup"><span data-stu-id="9c9ce-116">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="9c9ce-117">В приостановленном состоянии можно ввести состояние службы.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-117">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="9c9ce-118">(Это зависит от задания.)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-118">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="9c9ce-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9c9ce-120">Выполнение задания в чистом виде, сохранение данных, сохранение состояния и завершение работы всех базовых процессов в порядке.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-120">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="9c9ce-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9c9ce-122">Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-122">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9c9ce-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9c9ce-124">Помещает задание в состояние службы, зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-124">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="9c9ce-125">Может быть возможным перезапуск задания.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-125">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9c9ce-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF**</span><span class="sxs-lookup"><span data-stu-id="9c9ce-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="9c9ce-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-127">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9c9ce-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован**</span><span class="sxs-lookup"><span data-stu-id="9c9ce-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="9c9ce-129">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-129">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9c9ce-130">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c9ce-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c9ce-131">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="9c9ce-132">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="9c9ce-133">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="9c9ce-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="9c9ce-134">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (использование параметра времени ожидания не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="9c9ce-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c9ce-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c9ce-135">Return value</span></span>

<dl> <dt>

 <span data-ttu-id="9c9ce-136"> (0)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-136">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-137">(32768)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-137">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-138">(32769)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-138">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-139">(32770)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-139">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-140">(32771)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-140">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-141">(32772)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-141">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-142">(32773)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-142">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-143">(32774)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-143">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-144">(32775)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-144">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-145">(32776)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-145">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-146">(32777)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-146">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="9c9ce-147">(32778)</span><span class="sxs-lookup"><span data-stu-id="9c9ce-147">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9c9ce-148">Требования</span><span class="sxs-lookup"><span data-stu-id="9c9ce-148">Requirements</span></span>



| <span data-ttu-id="9c9ce-149">Требование</span><span class="sxs-lookup"><span data-stu-id="9c9ce-149">Requirement</span></span> | <span data-ttu-id="9c9ce-150">Значение</span><span class="sxs-lookup"><span data-stu-id="9c9ce-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9ce-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c9ce-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9c9ce-152">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9c9ce-152">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c9ce-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c9ce-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9c9ce-154">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9c9ce-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c9ce-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c9ce-155">Namespace</span></span><br/>                | <span data-ttu-id="9c9ce-156">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9c9ce-156">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c9ce-157">MOF</span><span class="sxs-lookup"><span data-stu-id="9c9ce-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c9ce-158"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ce-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c9ce-159">DLL</span><span class="sxs-lookup"><span data-stu-id="9c9ce-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c9ce-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ce-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c9ce-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c9ce-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c9ce-162">**Мсвм \_ мигратионжоб**</span><span class="sxs-lookup"><span data-stu-id="9c9ce-162">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




