---
description: Диагностика сетевого подключения виртуальной машины в среде виртуализации сети Windows.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Метод Диагносенетворкконнектион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682497"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="857be-103">Метод Диагносенетворкконнектион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="857be-103">DiagnoseNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="857be-104">Диагностика сетевого подключения виртуальной машины в среде виртуализации сети Windows.</span><span class="sxs-lookup"><span data-stu-id="857be-104">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="857be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="857be-105">Syntax</span></span>


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="857be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="857be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="857be-107">*Таржетнетворкадаптер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="857be-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="857be-108">Ссылка на [**\_ есернетпорталлокатионсеттингдата мсвм**](msvm-ethernetportallocationsettingdata.md) , описывающая целевой сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="857be-108">Reference to an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) that describes the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="857be-109">*DiagnosticSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="857be-109">*DiagnosticSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="857be-110">Используемые параметры диагностики.</span><span class="sxs-lookup"><span data-stu-id="857be-110">The diagnostic settings to use.</span></span>

</dd> <dt>

<span data-ttu-id="857be-111">*DiagnosticInformation* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="857be-111">*DiagnosticInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="857be-112">При успешном выполнении возвращает диагностическую информацию.</span><span class="sxs-lookup"><span data-stu-id="857be-112">On success, returns the diagnostic information.</span></span>

</dd> <dt>

<span data-ttu-id="857be-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="857be-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="857be-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="857be-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="857be-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="857be-115">Return value</span></span>

<span data-ttu-id="857be-116">Возвращает значение 0 или 4096 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="857be-116">Returns a 0 or 4096 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="857be-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="857be-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="857be-118">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="857be-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="857be-119">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="857be-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="857be-120">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="857be-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="857be-121">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="857be-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="857be-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="857be-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="857be-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="857be-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="857be-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="857be-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="857be-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="857be-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="857be-126">Требования</span><span class="sxs-lookup"><span data-stu-id="857be-126">Requirements</span></span>



| <span data-ttu-id="857be-127">Требование</span><span class="sxs-lookup"><span data-stu-id="857be-127">Requirement</span></span> | <span data-ttu-id="857be-128">Значение</span><span class="sxs-lookup"><span data-stu-id="857be-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="857be-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="857be-129">Minimum supported client</span></span><br/> | <span data-ttu-id="857be-130">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="857be-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="857be-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="857be-131">Minimum supported server</span></span><br/> | <span data-ttu-id="857be-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="857be-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="857be-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="857be-133">Namespace</span></span><br/>                | <span data-ttu-id="857be-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="857be-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="857be-135">MOF</span><span class="sxs-lookup"><span data-stu-id="857be-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="857be-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="857be-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="857be-137">DLL</span><span class="sxs-lookup"><span data-stu-id="857be-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857be-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="857be-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="857be-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="857be-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857be-140">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="857be-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

