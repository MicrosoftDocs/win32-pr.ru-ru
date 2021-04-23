---
description: Запрашивает изменение состояния элемента на значение, указанное в параметре RequestedState.
ms.assetid: 6d0061ad-ca14-400a-b813-af920f231eeb
title: Метод RequestStateChange класса CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5b28a2c33b61893be24eacc882b29b5a2be18b14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345795"
---
# <a name="requeststatechange-method-of-the-cim_enabledlogicalelement-class"></a><span data-ttu-id="214ae-103">Метод RequestStateChange \_ класса CIM енабледлогикалелемент</span><span class="sxs-lookup"><span data-stu-id="214ae-103">RequestStateChange method of the CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="214ae-104">Запрашивает изменение состояния элемента на значение, указанное в параметре RequestedState.</span><span class="sxs-lookup"><span data-stu-id="214ae-104">Requests that the state of the element be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="214ae-105">Когда происходит изменение запрошенного состояния, значение EnabledState и RequestedState элемента будут одинаковы.</span><span class="sxs-lookup"><span data-stu-id="214ae-105">When the requested state change takes place, the EnabledState and RequestedState of the element will be the same.</span></span> <span data-ttu-id="214ae-106">Вызов метода RequestStateChange несколько раз может привести к перезаписанию или потере предыдущих запросов.</span><span class="sxs-lookup"><span data-stu-id="214ae-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="214ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="214ae-107">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="214ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="214ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214ae-109">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="214ae-109">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="214ae-110">Состояние, запрошенное для элемента.</span><span class="sxs-lookup"><span data-stu-id="214ae-110">The state requested for the element.</span></span> <span data-ttu-id="214ae-111">Эти сведения будут помещены в свойство **RequestedState** экземпляра, если код возврата метода **RequestStateChange** равен 0 ("завершено без ошибок") или 4096 (0X1000) ("задание запущено").</span><span class="sxs-lookup"><span data-stu-id="214ae-111">This information will be placed into the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="214ae-112">Подробные объяснения значений **RequestedState** см. в описании свойств **EnabledState** и **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="214ae-112">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the **RequestedState** values.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="214ae-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)</span><span class="sxs-lookup"><span data-stu-id="214ae-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="214ae-114">Изменяет состояние на "работает".</span><span class="sxs-lookup"><span data-stu-id="214ae-114">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="214ae-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)</span><span class="sxs-lookup"><span data-stu-id="214ae-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="214ae-116">Временно останавливает задание.</span><span class="sxs-lookup"><span data-stu-id="214ae-116">Stops the job temporarily.</span></span> <span data-ttu-id="214ae-117">Цель — последующее перезапустить задание с помощью "Start".</span><span class="sxs-lookup"><span data-stu-id="214ae-117">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="214ae-118">В приостановленном состоянии можно ввести состояние службы.</span><span class="sxs-lookup"><span data-stu-id="214ae-118">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="214ae-119">(Это зависит от задания.)</span><span class="sxs-lookup"><span data-stu-id="214ae-119">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="214ae-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)</span><span class="sxs-lookup"><span data-stu-id="214ae-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="214ae-121">Останавливает задание в чистом виде, сохраняет данные, сохраняет состояние и завершает все базовые процессы упорядоченным образом.</span><span class="sxs-lookup"><span data-stu-id="214ae-121">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="214ae-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="214ae-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="214ae-123">Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.</span><span class="sxs-lookup"><span data-stu-id="214ae-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="214ae-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)</span><span class="sxs-lookup"><span data-stu-id="214ae-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="214ae-125">Помещает задание в состояние службы, зависящее от поставщика.</span><span class="sxs-lookup"><span data-stu-id="214ae-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="214ae-126">Может быть возможным перезапуск задания.</span><span class="sxs-lookup"><span data-stu-id="214ae-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="214ae-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="214ae-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="214ae-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="214ae-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="214ae-129">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="214ae-129">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214ae-130">Может содержать ссылку на [**\_ конкретежоб CIM**](cim-concretejob.md) , созданную для отслеживания перехода состояния, инициированного вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="214ae-130">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="214ae-131">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="214ae-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="214ae-132">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="214ae-132">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="214ae-133">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="214ae-133">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="214ae-134">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="214ae-134">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="214ae-135">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="214ae-135">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214ae-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="214ae-136">Return value</span></span>

<span data-ttu-id="214ae-137">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="214ae-137">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="214ae-138">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="214ae-138">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-139">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="214ae-139">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-140">**Неизвестная или Неуказанная ошибка** (2)</span><span class="sxs-lookup"><span data-stu-id="214ae-140">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-141">**Невозможно завершить в течение времени ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="214ae-141">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-142">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="214ae-142">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-143">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="214ae-143">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-144">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="214ae-144">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-145">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="214ae-145">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-146">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="214ae-146">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-147">**Недопустимая смена состояния** (4097)</span><span class="sxs-lookup"><span data-stu-id="214ae-147">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-148">**Использование параметра времени ожидания не поддерживается** (4098)</span><span class="sxs-lookup"><span data-stu-id="214ae-148">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-149">**Занято** (4099)</span><span class="sxs-lookup"><span data-stu-id="214ae-149">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-150">**Метод зарезервирован** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="214ae-150">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="214ae-151">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="214ae-151">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="214ae-152">Требования</span><span class="sxs-lookup"><span data-stu-id="214ae-152">Requirements</span></span>



| <span data-ttu-id="214ae-153">Требование</span><span class="sxs-lookup"><span data-stu-id="214ae-153">Requirement</span></span> | <span data-ttu-id="214ae-154">Значение</span><span class="sxs-lookup"><span data-stu-id="214ae-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="214ae-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="214ae-155">Minimum supported client</span></span><br/> | <span data-ttu-id="214ae-156">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="214ae-156">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="214ae-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="214ae-157">Minimum supported server</span></span><br/> | <span data-ttu-id="214ae-158">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="214ae-158">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="214ae-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="214ae-159">Namespace</span></span><br/>                | <span data-ttu-id="214ae-160">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="214ae-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="214ae-161">MOF</span><span class="sxs-lookup"><span data-stu-id="214ae-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="214ae-162"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="214ae-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="214ae-163">DLL</span><span class="sxs-lookup"><span data-stu-id="214ae-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="214ae-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="214ae-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="214ae-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="214ae-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214ae-166">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="214ae-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

 




