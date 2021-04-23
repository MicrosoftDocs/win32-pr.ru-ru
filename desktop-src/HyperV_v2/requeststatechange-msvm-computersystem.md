---
description: Запрашивает изменение состояния виртуальной машины на указанное значение.
ms.assetid: 87BE4C7D-604B-4F8D-B4DC-89BD563E3999
title: Метод RequestStateChange класса Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 291d72797b1ee765507a3d23921cd518cf605354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273119"
---
# <a name="requeststatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="d7234-103">Метод RequestStateChange \_ класса ComputerSystem мсвм</span><span class="sxs-lookup"><span data-stu-id="d7234-103">RequestStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="d7234-104">Запрашивает изменение состояния виртуальной машины на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="d7234-104">Requests that the state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="d7234-105">Вызов метода **RequestStateChange** несколько раз может привести к перезаписанию или потере предыдущих запросов.</span><span class="sxs-lookup"><span data-stu-id="d7234-105">Invoking the **RequestStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="d7234-106">Этот метод поддерживается только для экземпляров класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющих виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d7234-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

<span data-ttu-id="d7234-107">Пока выполняется изменение состояния, свойство **requestedstate** изменяется на значение параметра *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="d7234-107">While the state change is in progress, the **RequestedState** property is changed to the value of the *RequestedState* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7234-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7234-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="d7234-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7234-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7234-110">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7234-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7234-111">Тип: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d7234-111">Type: **uint16**</span></span>

<span data-ttu-id="d7234-112">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="d7234-112">The new state.</span></span> <span data-ttu-id="d7234-113">Значения, превышающие 32767, являются предложенными значениями в **DMTF** и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="d7234-113">Values that are greater than 32767 are **DMTF** proposed values and are subject to change.</span></span>

<span data-ttu-id="d7234-114">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="d7234-114">Here are possible values:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d7234-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d7234-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-116">Соответствует [**CIM \_ Енабледлогикалелемент. EnabledState**](/previous-versions//cc136818(v=vs.85)) = other.</span><span class="sxs-lookup"><span data-stu-id="d7234-116">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Other.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d7234-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="d7234-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-118">Соответствует [**CIM \_ Енабледлогикалелемент. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span><span class="sxs-lookup"><span data-stu-id="d7234-118">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d7234-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="d7234-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-120">Соответствует [**CIM \_ Енабледлогикалелемент. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span><span class="sxs-lookup"><span data-stu-id="d7234-120">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="d7234-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="d7234-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-122">Допустим только в версии 1 (v1) только для Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d7234-122">Valid in version 1 (V1) of Hyper-V only.</span></span> <span data-ttu-id="d7234-123">Работа виртуальной машины завершается через службу завершения работы.</span><span class="sxs-lookup"><span data-stu-id="d7234-123">The virtual machine is shutting down via the shutdown service.</span></span> <span data-ttu-id="d7234-124">Соответствует [**CIM \_ Енабледлогикалелемент. EnabledState**](/previous-versions//cc136818(v=vs.85)) = шуттингдовн.</span><span class="sxs-lookup"><span data-stu-id="d7234-124">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="d7234-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="d7234-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-126">Соответствует [**CIM \_ Енабледлогикалелемент. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled, но в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="d7234-126">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled but offline.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="d7234-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="d7234-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="d7234-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="d7234-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="d7234-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="d7234-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-130">Соответствует [**CIM \_ Енабледлогикалелемент. EnabledState**](/previous-versions//cc136818(v=vs.85)) = замораживание, включено, но приостановлено.</span><span class="sxs-lookup"><span data-stu-id="d7234-130">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Quiesce, Enabled but paused.</span></span>

</dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="d7234-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="d7234-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-132">Переход состояния с **Off** или **сохранен** в состояние **выполнения**.</span><span class="sxs-lookup"><span data-stu-id="d7234-132">State transition from **Off** or **Saved** to **Running**.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="d7234-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="d7234-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-134">Сбросьте виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d7234-134">Reset the virtual machine.</span></span> <span data-ttu-id="d7234-135">Соответствует [**CIM \_ Енабледлогикалелемент. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span><span class="sxs-lookup"><span data-stu-id="d7234-135">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="d7234-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Сохранение** (32773)</span><span class="sxs-lookup"><span data-stu-id="d7234-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-137">В версии 1 (v1) Hyper-V соответствует **енабледстатесавинг**.</span><span class="sxs-lookup"><span data-stu-id="d7234-137">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateSaving**.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="d7234-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Приостановка** (32776)</span><span class="sxs-lookup"><span data-stu-id="d7234-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-139">В версии 1 (v1) Hyper-V соответствует **енабледстатепаусинг**.</span><span class="sxs-lookup"><span data-stu-id="d7234-139">In version 1 (V1) of Hyper-V, corresponds to **EnabledStatePausing**.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="d7234-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Возобновление** (32777)</span><span class="sxs-lookup"><span data-stu-id="d7234-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-141">В версии 1 (v1) Hyper-V соответствует **енабледстатересуминг**.</span><span class="sxs-lookup"><span data-stu-id="d7234-141">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateResuming**.</span></span> <span data-ttu-id="d7234-142">Переход состояния от **приостановленного** к **выполнению**.</span><span class="sxs-lookup"><span data-stu-id="d7234-142">State transition from **Paused** to **Running**.</span></span>

</dd> <dt>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>

<span data-ttu-id="d7234-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**Фастсавед** (32779)</span><span class="sxs-lookup"><span data-stu-id="d7234-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-144">Соответствует **енабледстатефастсуспенд**.</span><span class="sxs-lookup"><span data-stu-id="d7234-144">Corresponds to **EnabledStateFastSuspend**.</span></span>

</dd> <dt>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>

<span data-ttu-id="d7234-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**Фастсавинг** (32780)</span><span class="sxs-lookup"><span data-stu-id="d7234-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span></span>


</dt> <dd>

<span data-ttu-id="d7234-146">Соответствует **енабледстатефастсуспендинг**.</span><span class="sxs-lookup"><span data-stu-id="d7234-146">Corresponds to **EnabledStateFastSuspending**.</span></span> <span data-ttu-id="d7234-147">Переход состояния от **выполнения** к **фастсавед**.</span><span class="sxs-lookup"><span data-stu-id="d7234-147">State transition from **Running** to **FastSaved**.</span></span>

</dd> </dl>

<span data-ttu-id="d7234-148">Эти значения представляют критические состояния:</span><span class="sxs-lookup"><span data-stu-id="d7234-148">These values represent critical states:</span></span>

<dt>

<span id="RunningCritical"></span><span id="runningcritical"></span><span id="RUNNINGCRITICAL"></span>

<span data-ttu-id="d7234-149">**Руннингкритикал** (32781)</span><span class="sxs-lookup"><span data-stu-id="d7234-149">**RunningCritical** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="OffCritical"></span><span id="offcritical"></span><span id="OFFCRITICAL"></span>

<span data-ttu-id="d7234-150">**Оффкритикал** (32782)</span><span class="sxs-lookup"><span data-stu-id="d7234-150">**OffCritical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="StoppingCritical"></span><span id="stoppingcritical"></span><span id="STOPPINGCRITICAL"></span>

<span data-ttu-id="d7234-151">**Стоппингкритикал** (32783)</span><span class="sxs-lookup"><span data-stu-id="d7234-151">**StoppingCritical** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="SavedCritical"></span><span id="savedcritical"></span><span id="SAVEDCRITICAL"></span>

<span data-ttu-id="d7234-152">**Саведкритикал** (32784)</span><span class="sxs-lookup"><span data-stu-id="d7234-152">**SavedCritical** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="PausedCritical"></span><span id="pausedcritical"></span><span id="PAUSEDCRITICAL"></span>

<span data-ttu-id="d7234-153">**Пауседкритикал** (32785)</span><span class="sxs-lookup"><span data-stu-id="d7234-153">**PausedCritical** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="StartingCritical"></span><span id="startingcritical"></span><span id="STARTINGCRITICAL"></span>

<span data-ttu-id="d7234-154">**Стартингкритикал** (32786)</span><span class="sxs-lookup"><span data-stu-id="d7234-154">**StartingCritical** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="ResetCritical"></span><span id="resetcritical"></span><span id="RESETCRITICAL"></span>

<span data-ttu-id="d7234-155">**Ресеткритикал** (32787)</span><span class="sxs-lookup"><span data-stu-id="d7234-155">**ResetCritical** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="SavingCritical"></span><span id="savingcritical"></span><span id="SAVINGCRITICAL"></span>

<span data-ttu-id="d7234-156">**Савингкритикал** (32788)</span><span class="sxs-lookup"><span data-stu-id="d7234-156">**SavingCritical** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="PausingCritical"></span><span id="pausingcritical"></span><span id="PAUSINGCRITICAL"></span>

<span data-ttu-id="d7234-157">**Паусингкритикал** (32789)</span><span class="sxs-lookup"><span data-stu-id="d7234-157">**PausingCritical** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="ResumingCritical"></span><span id="resumingcritical"></span><span id="RESUMINGCRITICAL"></span>

<span data-ttu-id="d7234-158">**Ресумингкритикал** (32790)</span><span class="sxs-lookup"><span data-stu-id="d7234-158">**ResumingCritical** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavedCritical"></span><span id="fastsavedcritical"></span><span id="FASTSAVEDCRITICAL"></span>

<span data-ttu-id="d7234-159">**Фастсаведкритикал** (32791)</span><span class="sxs-lookup"><span data-stu-id="d7234-159">**FastSavedCritical** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavingCritical"></span><span id="fastsavingcritical"></span><span id="FASTSAVINGCRITICAL"></span>

<span data-ttu-id="d7234-160">**Фастсавингкритикал** (32792)</span><span class="sxs-lookup"><span data-stu-id="d7234-160">**FastSavingCritical** (32792)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d7234-161">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7234-161">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7234-162">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d7234-162">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="d7234-163">Необязательная ссылка на объект [**мсвм \_ конкретежоб**](msvm-concretejob.md) , который возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d7234-163">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="d7234-164">При наличии возвращаемой ссылки можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="d7234-164">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="d7234-165">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7234-165">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7234-166">Тип: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d7234-166">Type: **datetime**</span></span>

<span data-ttu-id="d7234-167">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="d7234-167">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7234-168">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7234-168">Return value</span></span>

<span data-ttu-id="d7234-169">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d7234-169">Type: **uint32**</span></span>

<span data-ttu-id="d7234-170">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d7234-170">This method returns one of the following values.</span></span>



| <span data-ttu-id="d7234-171">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d7234-171">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="d7234-172">Описание</span><span class="sxs-lookup"><span data-stu-id="d7234-172">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7234-173"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-173"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="d7234-174">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d7234-174">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="d7234-175"><dt>**Параметры метода проверены — переход запущен**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-175"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="d7234-176">Переход является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="d7234-176">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="d7234-177"><dt>**Отказано в доступе**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-177"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="d7234-178">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="d7234-178">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="d7234-179"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-179"><dt></dt> <dt>32768</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-180"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-180"><dt></dt> <dt>32770</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-181"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-181"><dt></dt> <dt>32771</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-182"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-182"><dt></dt> <dt>32772</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-183"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-183"><dt></dt> <dt>32773</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-184"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-184"><dt></dt> <dt>32774</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-185"><dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-185"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="d7234-186">Значение, указанное в параметре *RequestedState* , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d7234-186">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="d7234-187"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-187"><dt></dt> <dt>32776</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-188"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-188"><dt></dt> <dt>32777</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="d7234-189"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-189"><dt></dt> <dt>32778</dt></span></span> </dl>                                                  |                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d7234-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7234-190">Remarks</span></span>

<span data-ttu-id="d7234-191">Доступ к классу [**\_ ComputerSystem мсвм**](msvm-computersystem.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d7234-191">Access to the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d7234-192">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d7234-192">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d7234-193">Примеры</span><span class="sxs-lookup"><span data-stu-id="d7234-193">Examples</span></span>

<span data-ttu-id="d7234-194">В следующем примере C# запускается или отключается виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="d7234-194">The following C# example starts or disables a virtual machine.</span></span> <span data-ttu-id="d7234-195">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d7234-195">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7234-196">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="d7234-196">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    public class RequestStateChangeClass
    {
        public static void RequestStateChange(string vmName, string action)
        {
            ManagementScope scope = new ManagementScope(@"\\.\root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

            if (null == vm)
            {
                throw new ArgumentException(
                    string.Format(
                    "The virtual machine '{0}' could not be found.", 
                    vmName));
            }

            ManagementBaseObject inParams = vm.GetMethodParameters("RequestStateChange");

            const int Enabled = 2;
            const int Disabled = 3;

            if (action.ToLower() == "start")
            {
                inParams["RequestedState"] = Enabled;
            }
            else if (action.ToLower() == "stop")
            {
                inParams["RequestedState"] = Disabled;
            }
            else
            {
                throw new Exception("Wrong action is specified");
            }

            ManagementBaseObject outParams = vm.InvokeMethod(
                "RequestStateChange", 
                inParams, 
                null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine(
                        "{0} state was changed successfully.", 
                        vmName);
                }
                else
                {
                    Console.WriteLine("Failed to change virtual system state");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine(
                    "{0} state was changed successfully.", 
                    vmName);
            }
            else
            {
                Console.WriteLine(
                    "Change virtual system state failed with error {0}", 
                    outParams["ReturnValue"]);
            }

        }

        public static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: <application> vmName action");
                Console.WriteLine("action: start|stop");
                return;
            }

            RequestStateChange(args[0], args[1]);
        }

    }
}
```



<span data-ttu-id="d7234-197">Следующий пример сценария Visual Basic Scripting Edition (VBScript) запускает или отключает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d7234-197">The following Visual Basic Scripting Edition (VBScript) example starts or disables a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7234-198">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="d7234-198">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```VB
dim objWMIService
dim fileSystem

const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const Enabled = 2
const Disabled = 3



Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    strComputer = "."
    set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       action = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript StartVM.vbs vmName start|stop"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)

    if RequestStateChange(computerSystem, action) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "RequestStateChange failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Turn on a virtual machine
'-----------------------------------------------------------------
Function RequestStateChange(computerSystem, action)
    WriteLog Format2("RequestStateChange({0}, {1})", computerSystem.ElementName, action)

    RequestStateChange = false
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    
    if action = "start" then
        objInParam.RequestedState = Enabled
    else
        objInParam.RequestedState = Disabled
    end if

    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VM {0} was started successfully", computerSystem.ElementName)
            RequestStateChange = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)

    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        end if

    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    dim WMIJob

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting

        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState

    wend


    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\StartVM.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="d7234-199">Требования</span><span class="sxs-lookup"><span data-stu-id="d7234-199">Requirements</span></span>



| <span data-ttu-id="d7234-200">Требование</span><span class="sxs-lookup"><span data-stu-id="d7234-200">Requirement</span></span> | <span data-ttu-id="d7234-201">Значение</span><span class="sxs-lookup"><span data-stu-id="d7234-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7234-202">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7234-202">Minimum supported client</span></span><br/> | <span data-ttu-id="d7234-203">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d7234-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d7234-204">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7234-204">Minimum supported server</span></span><br/> | <span data-ttu-id="d7234-205">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d7234-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7234-206">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d7234-206">Namespace</span></span><br/>                | <span data-ttu-id="d7234-207">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d7234-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d7234-208">MOF</span><span class="sxs-lookup"><span data-stu-id="d7234-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7234-209"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7234-210">DLL</span><span class="sxs-lookup"><span data-stu-id="d7234-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7234-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7234-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d7234-212">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7234-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7234-213">**Мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="d7234-213">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

