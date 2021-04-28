---
description: Метод RequestStateChange класса Msvm_SyntheticMouse — запрашивает изменение состояния.
ms.assetid: 6c29dc19-0e5a-48cc-ae4a-f7cf127678b2
title: Метод RequestStateChange класса Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 427dc0176856389f2eab2ae0c002c522f81048f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111212"
---
# <a name="requeststatechange-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="bfc5d-103">Метод RequestStateChange \_ класса мсвм синсетикмаусе</span><span class="sxs-lookup"><span data-stu-id="bfc5d-103">RequestStateChange method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="bfc5d-104">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="bfc5d-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc5d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfc5d-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="bfc5d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfc5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc5d-107">*RequestedState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfc5d-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc5d-108">Состояние, запрошенное для элемента.</span><span class="sxs-lookup"><span data-stu-id="bfc5d-108">The state requested for the element.</span></span> <span data-ttu-id="bfc5d-109">Эти сведения будут помещены в свойство RequestedState экземпляра, если код возврата метода RequestStateChange равен 0 ("завершено без ошибок") или 4096 (0x1000) ("задание запущено").</span><span class="sxs-lookup"><span data-stu-id="bfc5d-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="bfc5d-110">Подробные объяснения значений RequestedState см. в описании свойств EnabledState и RequestedState.</span><span class="sxs-lookup"><span data-stu-id="bfc5d-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bfc5d-111">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bfc5d-112">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="bfc5d-113">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="bfc5d-114">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="bfc5d-115">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="bfc5d-116">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="bfc5d-117">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="bfc5d-118">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="bfc5d-119">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bfc5d-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="bfc5d-121">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="bfc5d-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bfc5d-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc5d-123">Может содержать ссылку на Конкретежоб, созданную для отслеживания перехода состояния, инициированного вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="bfc5d-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="bfc5d-124">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfc5d-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc5d-125">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="bfc5d-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="bfc5d-126">Для указания Тимеаутпериод необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="bfc5d-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="bfc5d-127">Значение 0 или параметр NULL указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="bfc5d-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="bfc5d-128">Если это свойство не содержит значений 0 или null и реализация не поддерживает этот параметр, будет возвращен код возврата "использование параметра времени ожидания не поддерживается".</span><span class="sxs-lookup"><span data-stu-id="bfc5d-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc5d-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfc5d-129">Return value</span></span>

<span data-ttu-id="bfc5d-130">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bfc5d-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bfc5d-131">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bfc5d-132">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="bfc5d-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bfc5d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="bfc5d-133">Requirements</span></span>



| <span data-ttu-id="bfc5d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="bfc5d-134">Requirement</span></span> | <span data-ttu-id="bfc5d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="bfc5d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc5d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfc5d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc5d-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bfc5d-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bfc5d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfc5d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc5d-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bfc5d-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bfc5d-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bfc5d-140">Namespace</span></span><br/>                | <span data-ttu-id="bfc5d-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bfc5d-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bfc5d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="bfc5d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfc5d-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfc5d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfc5d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bfc5d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfc5d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfc5d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bfc5d-146">См. также</span><span class="sxs-lookup"><span data-stu-id="bfc5d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc5d-147">**Мсвм \_ синсетикмаусе**</span><span class="sxs-lookup"><span data-stu-id="bfc5d-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

 




