---
description: Запрашивает изменение состояния компонента интерфейса гостевой службы на указанное значение.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Метод Msvm_GuestServiceInterfaceComponent:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683378"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a><span data-ttu-id="8c8a1-103">Мсвм \_ гуестсервицеинтерфацекомпонент:: RequestStateChange, метод</span><span class="sxs-lookup"><span data-stu-id="8c8a1-103">Msvm\_GuestServiceInterfaceComponent::RequestStateChange method</span></span>

<span data-ttu-id="8c8a1-104">Запрашивает изменение состояния компонента интерфейса гостевой службы на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-104">Requests that the state of the guest service interface component be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c8a1-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="8c8a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c8a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c8a1-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c8a1-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8a1-108">Тип: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c8a1-108">Type: **uint16**</span></span>

<span data-ttu-id="8c8a1-109">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-109">The new state.</span></span> <span data-ttu-id="8c8a1-110">Сведения помещаются в свойство **RequestedState** экземпляра, если код возврата метода **RequestStateChange** равен 0 или 4096.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-110">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="8c8a1-111">Дополнительные сведения см. в описании свойств **EnabledState** и **RequestedState** для элемента.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-111">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="8c8a1-112">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-112">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8c8a1-113">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-113">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8c8a1-114">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-114">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8c8a1-115">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-115">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8c8a1-116">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-116">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8c8a1-117">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-117">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8c8a1-118">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-118">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8c8a1-119">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-119">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8c8a1-120">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-120">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8c8a1-121">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-121">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8c8a1-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8c8a1-123">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8c8a1-123">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8c8a1-124">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8c8a1-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8a1-125">Тип: **[ **CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="8c8a1-125">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="8c8a1-126">Необязательная ссылка на объект [**мсвм \_ конкретежоб**](msvm-concretejob.md) , который возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-126">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="8c8a1-127">При наличии возвращаемой ссылки можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-127">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="8c8a1-128">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c8a1-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c8a1-129">Тип: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c8a1-129">Type: **datetime**</span></span>

<span data-ttu-id="8c8a1-130">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-130">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="8c8a1-131">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-131">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="8c8a1-132">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-132">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="8c8a1-133">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="8c8a1-133">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c8a1-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c8a1-134">Return value</span></span>

<span data-ttu-id="8c8a1-135">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c8a1-135">Type: **uint32**</span></span>

<span data-ttu-id="8c8a1-136">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-136">This method returns one of the following values.</span></span>



| <span data-ttu-id="8c8a1-137">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="8c8a1-137">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="8c8a1-138">Описание</span><span class="sxs-lookup"><span data-stu-id="8c8a1-138">Description</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="8c8a1-139"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-139"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="8c8a1-140">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8c8a1-140">Success.</span></span><br/> |
| <dl> <span data-ttu-id="8c8a1-141"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-141"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                     |
| <dl> <span data-ttu-id="8c8a1-142"><dt>**Неизвестная или Неуказанная ошибка**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-142"><dt>**Unknown/Unspecified Error**</dt> <dt>2</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="8c8a1-143"><dt>**Не удается завершить в течение времени ожидания**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-143"><dt>**Can NOT complete within Timeout Period**</dt> <dt>3</dt></span></span> </dl>            |                     |
| <dl> <span data-ttu-id="8c8a1-144"><dt>**Сбой**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-144"><dt>**Failed**</dt> <dt>4</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="8c8a1-145"><dt>**Недопустимый параметр**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-145"><dt>**Invalid Parameter**</dt> <dt>5</dt></span></span> </dl>                                 |                     |
| <dl> <span data-ttu-id="8c8a1-146"><dt>**Используется**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-146"><dt>**In Use**</dt> <dt>6</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="8c8a1-147"><dt>**Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-147"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                    |                     |
| <dl> <span data-ttu-id="8c8a1-148"><dt>**Параметры метода проверены — переход запущен**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-148"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> |                     |
| <dl> <span data-ttu-id="8c8a1-149"><dt>**Недопустимая смена состояния**</dt> <dt>4097</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-149"><dt>**Invalid State Transition**</dt> <dt>4097</dt></span></span> </dl>                       |                     |
| <dl> <span data-ttu-id="8c8a1-150"><dt>**Использование параметра времени ожидания не поддерживается**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-150"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                     |
| <dl> <span data-ttu-id="8c8a1-151"><dt>**Занято**</dt> <dt>4099</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-151"><dt>**Busy**</dt> <dt>4099</dt></span></span> </dl>                                           |                     |
| <dl> <span data-ttu-id="8c8a1-152"><dt>**Метод зарезервирован**</dt> <dt>4100.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-152"><dt>**Method Reserved**</dt> <dt>4100..32767</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="8c8a1-153"><dt>**Независимый от поставщика**</dt> <dt>32768.65 535</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-153"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                        |                     |



 

## <a name="requirements"></a><span data-ttu-id="8c8a1-154">Требования</span><span class="sxs-lookup"><span data-stu-id="8c8a1-154">Requirements</span></span>



| <span data-ttu-id="8c8a1-155">Требование</span><span class="sxs-lookup"><span data-stu-id="8c8a1-155">Requirement</span></span> | <span data-ttu-id="8c8a1-156">Значение</span><span class="sxs-lookup"><span data-stu-id="8c8a1-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8a1-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c8a1-157">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8a1-158">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c8a1-158">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8c8a1-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c8a1-159">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8a1-160">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c8a1-160">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8c8a1-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8c8a1-161">Namespace</span></span><br/>                | <span data-ttu-id="8c8a1-162">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8c8a1-162">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="8c8a1-163">MOF</span><span class="sxs-lookup"><span data-stu-id="8c8a1-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c8a1-164"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c8a1-165">DLL</span><span class="sxs-lookup"><span data-stu-id="8c8a1-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c8a1-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8c8a1-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8c8a1-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c8a1-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c8a1-168">**Мсвм \_ гуестсервицеинтерфацекомпонент**</span><span class="sxs-lookup"><span data-stu-id="8c8a1-168">**Msvm\_GuestServiceInterfaceComponent**</span></span>](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

