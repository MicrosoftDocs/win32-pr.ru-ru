---
description: Метод RequestStateChange класса Msvm_Memory — запрашивает изменение состояния.
ms.assetid: 836ee3a1-e28e-4f84-8e1c-09f4a2ff0a25
title: Метод RequestStateChange класса Msvm_Memory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c168e3be7350b1422edd9ac87556aab886daf49c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118862"
---
# <a name="requeststatechange-method-of-the-msvm_memory-class"></a><span data-ttu-id="df172-103">Метод RequestStateChange \_ класса памяти мсвм</span><span class="sxs-lookup"><span data-stu-id="df172-103">RequestStateChange method of the Msvm\_Memory class</span></span>

<span data-ttu-id="df172-104">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="df172-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="df172-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df172-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="df172-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df172-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df172-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df172-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df172-108">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="df172-108">The new state.</span></span> <span data-ttu-id="df172-109">Сведения помещаются в свойство **RequestedState** экземпляра, если код возврата метода **RequestStateChange** равен 0 или 4096.</span><span class="sxs-lookup"><span data-stu-id="df172-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="df172-110">Дополнительные сведения см. в описании свойств **EnabledState** и **RequestedState** для элемента.</span><span class="sxs-lookup"><span data-stu-id="df172-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="df172-111">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="df172-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="df172-112">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="df172-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="df172-113">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="df172-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="df172-114">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="df172-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="df172-115">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="df172-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="df172-116">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="df172-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="df172-117">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="df172-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="df172-118">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="df172-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="df172-119">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="df172-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="df172-120">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="df172-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="df172-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="df172-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="df172-122">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="df172-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="df172-123">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="df172-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df172-124">Может содержать ссылку на [**\_ конкретежоб CIM**](cim-concretejob.md) , созданную для отслеживания перехода состояния, инициированного вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="df172-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="df172-125">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df172-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df172-126">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="df172-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="df172-127">Для указания Тимеаутпериод необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="df172-127">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="df172-128">Значение 0 или параметр NULL указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="df172-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="df172-129">Если это свойство не содержит значений 0 или null и реализация не поддерживает этот параметр, будет возвращен код возврата "использование параметра времени ожидания не поддерживается".</span><span class="sxs-lookup"><span data-stu-id="df172-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df172-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df172-130">Return value</span></span>

<span data-ttu-id="df172-131">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="df172-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="df172-132">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="df172-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df172-133">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="df172-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="df172-134">Требования</span><span class="sxs-lookup"><span data-stu-id="df172-134">Requirements</span></span>



| <span data-ttu-id="df172-135">Требование</span><span class="sxs-lookup"><span data-stu-id="df172-135">Requirement</span></span> | <span data-ttu-id="df172-136">Значение</span><span class="sxs-lookup"><span data-stu-id="df172-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df172-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df172-137">Minimum supported client</span></span><br/> | <span data-ttu-id="df172-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="df172-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="df172-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df172-139">Minimum supported server</span></span><br/> | <span data-ttu-id="df172-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="df172-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="df172-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="df172-141">Namespace</span></span><br/>                | <span data-ttu-id="df172-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="df172-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="df172-143">MOF</span><span class="sxs-lookup"><span data-stu-id="df172-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df172-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df172-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df172-145">DLL</span><span class="sxs-lookup"><span data-stu-id="df172-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df172-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df172-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df172-147">См. также</span><span class="sxs-lookup"><span data-stu-id="df172-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df172-148">**\_Память мсвм**</span><span class="sxs-lookup"><span data-stu-id="df172-148">**Msvm\_Memory**</span></span>](msvm-memory.md)
</dt> </dl>

 

 




