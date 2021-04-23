---
description: Запрашивает изменение состояния элемента.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Метод RequestStateChange класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991223"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="ac143-103">Метод RequestStateChange \_ класса клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="ac143-103">RequestStateChange method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="ac143-104">Запрашивает изменение состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ac143-104">Requests that the state of the element be changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac143-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac143-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="ac143-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac143-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac143-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac143-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac143-108">Новое состояние, запрошенное для элемента.</span><span class="sxs-lookup"><span data-stu-id="ac143-108">The new state requested for the element.</span></span> <span data-ttu-id="ac143-109">Эти сведения будут помещены в свойство **RequestedState** экземпляра, если код возврата равен 0 ("завершено без ошибок"), 3 ("Timeout") или 4096 (0x1000) ("задание запущено").</span><span class="sxs-lookup"><span data-stu-id="ac143-109">This information will be placed into the **RequestedState** property of the instance if the return code is 0 ('Completed with No Error'), 3 ('Timeout'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="ac143-110">Подробные объяснения значений *RequestedState* см. в описании свойств **EnabledState** и **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="ac143-110">For detailed explanations of the *RequestedState* values, see the description of the **EnabledState** and **RequestedState** properties.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ac143-111">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="ac143-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ac143-112">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="ac143-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="ac143-113">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="ac143-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="ac143-114">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="ac143-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="ac143-115">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="ac143-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="ac143-116">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="ac143-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="ac143-117">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="ac143-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="ac143-118">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="ac143-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="ac143-119">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="ac143-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ac143-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ac143-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ac143-121">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ac143-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ac143-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac143-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac143-123">Ссылка на задание.</span><span class="sxs-lookup"><span data-stu-id="ac143-123">A reference to the job.</span></span> <span data-ttu-id="ac143-124">Если задача завершена, этот параметр может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ac143-124">This parameter can be **Null** if the task is completed.</span></span>

</dd> <dt>

<span data-ttu-id="ac143-125">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac143-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac143-126">Максимальное время, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="ac143-126">The maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="ac143-127">Для указания этого времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="ac143-127">The interval format must be used to specify this time-out period.</span></span> <span data-ttu-id="ac143-128">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="ac143-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="ac143-129">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, возвращается код возврата 4098 ("использование параметра времени ожидания не поддерживается").</span><span class="sxs-lookup"><span data-stu-id="ac143-129">If this property does not contain 0 or **Null**, and the implementation does not support this parameter, a return code of 4098 ("Use Of Timeout Parameter Not Supported") is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac143-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac143-130">Return value</span></span>

<dl> <dt>

<span data-ttu-id="ac143-131">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ac143-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-132">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ac143-132">**Not supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-133">**Неизвестная или Неуказанная ошибка** (2)</span><span class="sxs-lookup"><span data-stu-id="ac143-133">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-134">**Невозможно завершить в течение времени ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="ac143-134">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-135">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="ac143-135">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-136">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="ac143-136">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-137">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="ac143-137">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-138">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ac143-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-139">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ac143-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-140">**Недопустимая смена состояния** (4097)</span><span class="sxs-lookup"><span data-stu-id="ac143-140">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-141">**Использование параметра времени ожидания не поддерживается** (4098)</span><span class="sxs-lookup"><span data-stu-id="ac143-141">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-142">**Занято** (4099)</span><span class="sxs-lookup"><span data-stu-id="ac143-142">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-143">**Метод зарезервирован** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ac143-143">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ac143-144">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="ac143-144">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ac143-145">Требования</span><span class="sxs-lookup"><span data-stu-id="ac143-145">Requirements</span></span>



| <span data-ttu-id="ac143-146">Требование</span><span class="sxs-lookup"><span data-stu-id="ac143-146">Requirement</span></span> | <span data-ttu-id="ac143-147">Значение</span><span class="sxs-lookup"><span data-stu-id="ac143-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac143-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac143-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ac143-149">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac143-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ac143-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac143-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ac143-151">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac143-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ac143-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac143-152">Namespace</span></span><br/>                | <span data-ttu-id="ac143-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ac143-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ac143-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ac143-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac143-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac143-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac143-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ac143-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac143-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac143-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac143-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac143-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac143-159">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="ac143-159">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




