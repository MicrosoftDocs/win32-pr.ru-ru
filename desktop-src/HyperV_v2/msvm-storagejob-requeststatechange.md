---
description: Запрашивает изменение состояния.
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: Метод RequestStateChange класса Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1ce563fdae2e73ba2e6994afc3d70c8d4d6fe34a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911012"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="0e5a5-103">Метод RequestStateChange \_ класса мсвм сторажежоб</span><span class="sxs-lookup"><span data-stu-id="0e5a5-103">RequestStateChange method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="0e5a5-104">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e5a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e5a5-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="0e5a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e5a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e5a5-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e5a5-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e5a5-108">RequestStateChange изменяет состояние задания.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="0e5a5-109">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0e5a5-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="0e5a5-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e5a5-111">Изменяет состояние на "работает".</span><span class="sxs-lookup"><span data-stu-id="0e5a5-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="0e5a5-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e5a5-113">Временно останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-113">Stops the job temporarily.</span></span> <span data-ttu-id="0e5a5-114">Цель — последующее перезапустить задание с помощью "Start".</span><span class="sxs-lookup"><span data-stu-id="0e5a5-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="0e5a5-115">В приостановленном состоянии можно ввести состояние службы.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="0e5a5-116">(Это зависит от задания.)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="0e5a5-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e5a5-118">Останавливает задание в чистом виде, сохраняет данные, сохраняет состояние и завершает все базовые процессы упорядоченным образом.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="0e5a5-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0e5a5-120">Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0e5a5-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0e5a5-122">Помещает задание в состояние службы, зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="0e5a5-123">Может быть возможным перезапуск задания.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e5a5-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0e5a5-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="0e5a5-126">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e5a5-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e5a5-127">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="0e5a5-128">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="0e5a5-129">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="0e5a5-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="0e5a5-130">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="0e5a5-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e5a5-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e5a5-131">Return value</span></span>

<span data-ttu-id="0e5a5-132">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0e5a5-132">This method returns one of the following values:</span></span>

<dl> <dt>

 <span data-ttu-id="0e5a5-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="0e5a5-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="0e5a5-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0e5a5-145">Требования</span><span class="sxs-lookup"><span data-stu-id="0e5a5-145">Requirements</span></span>



| <span data-ttu-id="0e5a5-146">Требование</span><span class="sxs-lookup"><span data-stu-id="0e5a5-146">Requirement</span></span> | <span data-ttu-id="0e5a5-147">Значение</span><span class="sxs-lookup"><span data-stu-id="0e5a5-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e5a5-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e5a5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0e5a5-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0e5a5-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0e5a5-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e5a5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0e5a5-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0e5a5-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0e5a5-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e5a5-152">Namespace</span></span><br/>                | <span data-ttu-id="0e5a5-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0e5a5-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e5a5-154">MOF</span><span class="sxs-lookup"><span data-stu-id="0e5a5-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e5a5-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e5a5-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e5a5-156">DLL</span><span class="sxs-lookup"><span data-stu-id="0e5a5-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e5a5-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e5a5-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e5a5-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e5a5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e5a5-159">**Мсвм \_ сторажежоб**</span><span class="sxs-lookup"><span data-stu-id="0e5a5-159">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




