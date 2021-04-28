---
description: Метод RequestStateChange класса Msvm_VirtualSystemMigrationService — запрашивает изменение состояния.
ms.assetid: 8355f2d8-d6d1-4bfa-b404-91376c2e2bdd
title: Метод RequestStateChange класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55679bf176fc0a8386ef3179a77d91245b5c9abc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109372"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="7f76a-103">Метод RequestStateChange \_ класса мсвм виртуалсистеммигратионсервице</span><span class="sxs-lookup"><span data-stu-id="7f76a-103">RequestStateChange method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="7f76a-104">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="7f76a-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f76a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f76a-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="7f76a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f76a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f76a-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f76a-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f76a-108">Новое состояние.</span><span class="sxs-lookup"><span data-stu-id="7f76a-108">The new state.</span></span> <span data-ttu-id="7f76a-109">Сведения помещаются в свойство **RequestedState** экземпляра, если код возврата метода **RequestStateChange** равен 0 (задание завершено без ошибок) или 4096 (задание запущено).</span><span class="sxs-lookup"><span data-stu-id="7f76a-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 (Job complete without error) or 4096 (Job started).</span></span> <span data-ttu-id="7f76a-110">Дополнительные сведения см. в описании свойств **EnabledState** и **RequestedState** для элемента.</span><span class="sxs-lookup"><span data-stu-id="7f76a-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="7f76a-111">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7f76a-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7f76a-112">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="7f76a-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7f76a-113">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="7f76a-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="7f76a-114">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="7f76a-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="7f76a-115">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="7f76a-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="7f76a-116">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="7f76a-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="7f76a-117">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="7f76a-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="7f76a-118">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="7f76a-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="7f76a-119">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="7f76a-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="7f76a-120">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="7f76a-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7f76a-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7f76a-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7f76a-122">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7f76a-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="7f76a-123">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f76a-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f76a-124">Может содержать ссылку на [**\_ конкретежоб CIM**](cim-concretejob.md) , созданную для отслеживания перехода состояния, инициированного вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="7f76a-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="7f76a-125">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f76a-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f76a-126">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="7f76a-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="7f76a-127">Для указания времени ожидания необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="7f76a-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="7f76a-128">Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="7f76a-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="7f76a-129">Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (**Использование параметра времени ожидания не поддерживается**).</span><span class="sxs-lookup"><span data-stu-id="7f76a-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f76a-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f76a-130">Return value</span></span>

<span data-ttu-id="7f76a-131">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7f76a-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="7f76a-132">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7f76a-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f76a-133">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7f76a-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7f76a-134">Требования</span><span class="sxs-lookup"><span data-stu-id="7f76a-134">Requirements</span></span>



| <span data-ttu-id="7f76a-135">Требование</span><span class="sxs-lookup"><span data-stu-id="7f76a-135">Requirement</span></span> | <span data-ttu-id="7f76a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7f76a-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f76a-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f76a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7f76a-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7f76a-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7f76a-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f76a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7f76a-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7f76a-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7f76a-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7f76a-141">Namespace</span></span><br/>                | <span data-ttu-id="7f76a-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7f76a-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7f76a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7f76a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f76a-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f76a-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f76a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7f76a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f76a-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f76a-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7f76a-147">См. также</span><span class="sxs-lookup"><span data-stu-id="7f76a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f76a-148">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="7f76a-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




