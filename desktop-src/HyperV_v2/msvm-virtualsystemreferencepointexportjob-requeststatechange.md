---
description: Запрашивает изменение состояния.
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: Метод RequestStateChange класса Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5612371738915b5e38657eca0773a88e31e3b0d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664828"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="42f96-103">Метод RequestStateChange \_ класса мсвм виртуалсистемреференцепоинтекспортжоб</span><span class="sxs-lookup"><span data-stu-id="42f96-103">RequestStateChange method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="42f96-104">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="42f96-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42f96-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="42f96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42f96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f96-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42f96-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f96-108">Изменяет состояние задания.</span><span class="sxs-lookup"><span data-stu-id="42f96-108">Changes the state of a job.</span></span> <span data-ttu-id="42f96-109">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="42f96-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="42f96-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)</span><span class="sxs-lookup"><span data-stu-id="42f96-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="42f96-111">Изменяет состояние на "работает".</span><span class="sxs-lookup"><span data-stu-id="42f96-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="42f96-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)</span><span class="sxs-lookup"><span data-stu-id="42f96-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="42f96-113">Временно останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="42f96-113">Stops the job temporarily.</span></span> <span data-ttu-id="42f96-114">Цель — последующее перезапустить задание с помощью "Start".</span><span class="sxs-lookup"><span data-stu-id="42f96-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="42f96-115">В приостановленном состоянии можно ввести состояние службы.</span><span class="sxs-lookup"><span data-stu-id="42f96-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="42f96-116">(Это зависит от задания.)</span><span class="sxs-lookup"><span data-stu-id="42f96-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="42f96-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)</span><span class="sxs-lookup"><span data-stu-id="42f96-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="42f96-118">Останавливает задание в чистом виде, сохраняет данные, сохраняет состояние и завершает все базовые процессы упорядоченным образом.</span><span class="sxs-lookup"><span data-stu-id="42f96-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="42f96-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="42f96-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="42f96-120">Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.</span><span class="sxs-lookup"><span data-stu-id="42f96-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="42f96-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)</span><span class="sxs-lookup"><span data-stu-id="42f96-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="42f96-122">Помещает задание в состояние службы, зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="42f96-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="42f96-123">Может быть возможным перезапуск задания.</span><span class="sxs-lookup"><span data-stu-id="42f96-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="42f96-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="42f96-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="42f96-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="42f96-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="42f96-126">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="42f96-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f96-127">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="42f96-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="42f96-128">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="42f96-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="42f96-129">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="42f96-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="42f96-130">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="42f96-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f96-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42f96-131">Return value</span></span>

<span data-ttu-id="42f96-132">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="42f96-132">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

 <span data-ttu-id="42f96-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="42f96-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="42f96-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="42f96-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="42f96-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="42f96-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="42f96-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="42f96-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="42f96-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="42f96-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="42f96-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="42f96-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="42f96-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="42f96-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="42f96-145">Требования</span><span class="sxs-lookup"><span data-stu-id="42f96-145">Requirements</span></span>



| <span data-ttu-id="42f96-146">Требование</span><span class="sxs-lookup"><span data-stu-id="42f96-146">Requirement</span></span> | <span data-ttu-id="42f96-147">Значение</span><span class="sxs-lookup"><span data-stu-id="42f96-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f96-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42f96-148">Minimum supported client</span></span><br/> | <span data-ttu-id="42f96-149">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="42f96-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="42f96-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42f96-150">Minimum supported server</span></span><br/> | <span data-ttu-id="42f96-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="42f96-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="42f96-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="42f96-152">Namespace</span></span><br/>                | <span data-ttu-id="42f96-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="42f96-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="42f96-154">MOF</span><span class="sxs-lookup"><span data-stu-id="42f96-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42f96-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42f96-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42f96-156">DLL</span><span class="sxs-lookup"><span data-stu-id="42f96-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42f96-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42f96-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42f96-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42f96-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f96-159">**Мсвм \_ виртуалсистемреференцепоинтекспортжоб**</span><span class="sxs-lookup"><span data-stu-id="42f96-159">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




