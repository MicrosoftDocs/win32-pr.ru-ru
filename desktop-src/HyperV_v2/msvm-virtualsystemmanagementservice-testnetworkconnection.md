---
description: Проверяет сетевое подключение виртуальной машины в среде виртуализации сети Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Метод Тестнетворкконнектион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143876"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="36d3f-103">Метод Тестнетворкконнектион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="36d3f-103">TestNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="36d3f-104">Проверяет сетевое подключение виртуальной машины в среде виртуализации сети Windows.</span><span class="sxs-lookup"><span data-stu-id="36d3f-104">Tests the network connectivity of a VM in a Windows network virtualization environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d3f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36d3f-105">Syntax</span></span>


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="36d3f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36d3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d3f-107">*Таржетнетворкадаптер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-108">Ссылка на [**мсвм \_ есернетпорталлокатионсеттингдата**](msvm-ethernetportallocationsettingdata.md) , описывающий целевой сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="36d3f-108">Reference to a [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) describing the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-109">*Отправители* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-109">*IsSender* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-110">Указывает, вызывается ли этот метод у отправителя или получателя.</span><span class="sxs-lookup"><span data-stu-id="36d3f-110">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-111">*Сендерип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-111">*SenderIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-112">IP-адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="36d3f-112">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-113">*Рецеиверип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-113">*ReceiverIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-114">Mac-адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="36d3f-114">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-115">*Рецеивермак* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-115">*ReceiverMac* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-116">Mac-адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="36d3f-116">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-117">*Исолатионид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-117">*IsolationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-118">Идентификатор изоляции.</span><span class="sxs-lookup"><span data-stu-id="36d3f-118">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-119">*SequenceNumber* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-119">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-120">Идентификатор изоляции.</span><span class="sxs-lookup"><span data-stu-id="36d3f-120">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-121">*Раундтриптиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-121">*RoundTripTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-122">Время кругового пути.</span><span class="sxs-lookup"><span data-stu-id="36d3f-122">The round trip time.</span></span>

</dd> <dt>

<span data-ttu-id="36d3f-123">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="36d3f-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36d3f-124">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="36d3f-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d3f-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36d3f-125">Return value</span></span>

<span data-ttu-id="36d3f-126">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="36d3f-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="36d3f-127">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="36d3f-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-128">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="36d3f-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-129">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="36d3f-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-130">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="36d3f-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-131">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="36d3f-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-132">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="36d3f-132">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-133">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="36d3f-133">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-134">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="36d3f-134">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="36d3f-135">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="36d3f-135">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="36d3f-136">Требования</span><span class="sxs-lookup"><span data-stu-id="36d3f-136">Requirements</span></span>



| <span data-ttu-id="36d3f-137">Требование</span><span class="sxs-lookup"><span data-stu-id="36d3f-137">Requirement</span></span> | <span data-ttu-id="36d3f-138">Значение</span><span class="sxs-lookup"><span data-stu-id="36d3f-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d3f-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36d3f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="36d3f-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36d3f-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="36d3f-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36d3f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="36d3f-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="36d3f-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="36d3f-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="36d3f-143">Namespace</span></span><br/>                | <span data-ttu-id="36d3f-144">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="36d3f-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36d3f-145">MOF</span><span class="sxs-lookup"><span data-stu-id="36d3f-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36d3f-146"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36d3f-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36d3f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="36d3f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d3f-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36d3f-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36d3f-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36d3f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d3f-150">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="36d3f-150">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

