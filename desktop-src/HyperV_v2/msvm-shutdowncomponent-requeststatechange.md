---
description: Метод RequestStateChange класса Msvm_ShutdownComponent — запрашивает изменение состояния.
ms.assetid: bb1dea51-f9d6-4edc-8044-53380cc4d32e
title: Метод RequestStateChange класса Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 71237715f08e3775ff4c61660a789e000e4f5a5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109612"
---
# <a name="requeststatechange-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="260e8-103">Метод RequestStateChange \_ класса мсвм шутдовнкомпонент</span><span class="sxs-lookup"><span data-stu-id="260e8-103">RequestStateChange method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="260e8-104">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="260e8-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="260e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="260e8-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="260e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="260e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="260e8-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="260e8-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="260e8-108">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="260e8-108">The new state.</span></span> <span data-ttu-id="260e8-109">Сведения помещаются в свойство **RequestedState** экземпляра, если код возврата метода **RequestStateChange** равен 0 или 4096.</span><span class="sxs-lookup"><span data-stu-id="260e8-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="260e8-110">Дополнительные сведения см. в описании свойств **EnabledState** и **RequestedState** для элемента.</span><span class="sxs-lookup"><span data-stu-id="260e8-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="260e8-111">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="260e8-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="260e8-112">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="260e8-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="260e8-113">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="260e8-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="260e8-114">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="260e8-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="260e8-115">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="260e8-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="260e8-116">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="260e8-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="260e8-117">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="260e8-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="260e8-118">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="260e8-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="260e8-119">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="260e8-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="260e8-120">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="260e8-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="260e8-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="260e8-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="260e8-122">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="260e8-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="260e8-123">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="260e8-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="260e8-124">Может содержать ссылку на Конкретежоб, созданную для отслеживания перехода состояния, инициированного вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="260e8-124">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="260e8-125">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="260e8-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="260e8-126">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="260e8-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="260e8-127">Для указания Тимеаутпериод необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="260e8-127">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="260e8-128">Значение 0 или параметр NULL указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="260e8-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="260e8-129">Если это свойство не содержит значений 0 или null и реализация не поддерживает этот параметр, будет возвращен код возврата "использование параметра времени ожидания не поддерживается".</span><span class="sxs-lookup"><span data-stu-id="260e8-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="260e8-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="260e8-130">Return value</span></span>

<span data-ttu-id="260e8-131">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="260e8-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="260e8-132">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="260e8-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="260e8-133">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="260e8-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="260e8-134">Требования</span><span class="sxs-lookup"><span data-stu-id="260e8-134">Requirements</span></span>



| <span data-ttu-id="260e8-135">Требование</span><span class="sxs-lookup"><span data-stu-id="260e8-135">Requirement</span></span> | <span data-ttu-id="260e8-136">Значение</span><span class="sxs-lookup"><span data-stu-id="260e8-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="260e8-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="260e8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="260e8-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="260e8-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="260e8-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="260e8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="260e8-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="260e8-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="260e8-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="260e8-141">Namespace</span></span><br/>                | <span data-ttu-id="260e8-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="260e8-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="260e8-143">MOF</span><span class="sxs-lookup"><span data-stu-id="260e8-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="260e8-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="260e8-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="260e8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="260e8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="260e8-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="260e8-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="260e8-147">См. также</span><span class="sxs-lookup"><span data-stu-id="260e8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260e8-148">**Мсвм \_ шутдовнкомпонент**</span><span class="sxs-lookup"><span data-stu-id="260e8-148">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




