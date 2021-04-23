---
description: Запрашивает изменение состояния гостевой службы на указанное значение.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: 'Метод Msvm_GuestService:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815224"
---
# <a name="msvm_guestservicerequeststatechange-method"></a><span data-ttu-id="b5b64-103">Мсвм \_ гуестсервице:: RequestStateChange, метод</span><span class="sxs-lookup"><span data-stu-id="b5b64-103">Msvm\_GuestService::RequestStateChange method</span></span>

<span data-ttu-id="b5b64-104">Запрашивает изменение состояния гостевой службы на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="b5b64-104">Requests that the state of the guest service be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5b64-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="b5b64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5b64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5b64-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5b64-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5b64-108">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="b5b64-108">The new state.</span></span> <span data-ttu-id="b5b64-109">Сведения помещаются в свойство **RequestedState** экземпляра, если код возврата метода **RequestStateChange** равен 0 или 4096.</span><span class="sxs-lookup"><span data-stu-id="b5b64-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="b5b64-110">Дополнительные сведения см. в описании свойств **EnabledState** и **RequestedState** для элемента.</span><span class="sxs-lookup"><span data-stu-id="b5b64-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="b5b64-111">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b5b64-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b5b64-112">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="b5b64-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b5b64-113">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="b5b64-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="b5b64-114">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="b5b64-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="b5b64-115">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="b5b64-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="b5b64-116">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="b5b64-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="b5b64-117">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="b5b64-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="b5b64-118">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="b5b64-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="b5b64-119">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="b5b64-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="b5b64-120">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="b5b64-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b5b64-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="b5b64-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b5b64-122">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b5b64-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b5b64-123">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5b64-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5b64-124">Необязательная ссылка на объект [**CIM \_ конкретежоб**](cim-concretejob.md) , возвращаемый, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b5b64-124">An optional reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="b5b64-125">При наличии возвращаемой ссылки можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="b5b64-125">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="b5b64-126">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5b64-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5b64-127">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="b5b64-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="b5b64-128">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="b5b64-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="b5b64-129">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="b5b64-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="b5b64-130">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="b5b64-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5b64-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5b64-131">Return value</span></span>

<span data-ttu-id="b5b64-132">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b5b64-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="b5b64-133">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b5b64-133">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="b5b64-134">Описание</span><span class="sxs-lookup"><span data-stu-id="b5b64-134">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5b64-135"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="b5b64-136">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b5b64-136">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="b5b64-137"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-137"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                                                                                    |
| <dl> <span data-ttu-id="b5b64-138"><dt>**Параметры метода проверены — переход запущен**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-138"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="b5b64-139">Переход является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="b5b64-139">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="b5b64-140"><dt>**Использование параметра времени ожидания не поддерживается**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-140"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                                                                                    |
| <dl> <span data-ttu-id="b5b64-141"><dt>**Отказано в доступе**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-141"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="b5b64-142">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b5b64-142">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="b5b64-143"><dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-143"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="b5b64-144">Значение, указанное в параметре *RequestedState* , не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b5b64-144">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b5b64-145">Требования</span><span class="sxs-lookup"><span data-stu-id="b5b64-145">Requirements</span></span>



| <span data-ttu-id="b5b64-146">Требование</span><span class="sxs-lookup"><span data-stu-id="b5b64-146">Requirement</span></span> | <span data-ttu-id="b5b64-147">Значение</span><span class="sxs-lookup"><span data-stu-id="b5b64-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b64-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5b64-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b5b64-149">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b5b64-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b5b64-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5b64-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b5b64-151">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5b64-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5b64-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b5b64-152">Namespace</span></span><br/>                | <span data-ttu-id="b5b64-153">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b5b64-153">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="b5b64-154">MOF</span><span class="sxs-lookup"><span data-stu-id="b5b64-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5b64-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5b64-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b5b64-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5b64-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5b64-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5b64-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5b64-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b64-159">**Мсвм \_ гуестсервице**</span><span class="sxs-lookup"><span data-stu-id="b5b64-159">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




