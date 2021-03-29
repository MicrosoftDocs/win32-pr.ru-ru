---
description: Определяет запланированную виртуальную систему.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Метод Дефинепланнедсистем класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540298"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="fd933-103">Метод Дефинепланнедсистем \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="fd933-103">DefinePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="fd933-104">Определяет запланированную виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="fd933-104">Defines a planned virtual system.</span></span>

<span data-ttu-id="fd933-105">Входные данные, которые указаны не полностью, могут быть заполнены значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fd933-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd933-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd933-106">Syntax</span></span>


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fd933-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd933-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd933-108">*SystemSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd933-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd933-109">Параметры системы для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="fd933-109">The system settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="fd933-110">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd933-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd933-111">Параметры ресурсов для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="fd933-111">The resource settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="fd933-112">*Референцеконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd933-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd933-113">[**\_ Виртуалсистемсеттингдата CIM**](cim-virtualsystemsettingdata.md) , содержащий конфигурацию ссылки.</span><span class="sxs-lookup"><span data-stu-id="fd933-113">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the reference configuration.</span></span>

</dd> <dt>

<span data-ttu-id="fd933-114">*Ресултингсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fd933-114">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd933-115">Объект [**\_ ComputerSystem CIM**](cim-computersystem.md) , содержащий результирующую систему.</span><span class="sxs-lookup"><span data-stu-id="fd933-115">A [**CIM\_ComputerSystem**](cim-computersystem.md) containing the resulting system.</span></span>

</dd> <dt>

<span data-ttu-id="fd933-116">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fd933-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd933-117">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fd933-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd933-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd933-118">Return value</span></span>

<span data-ttu-id="fd933-119">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fd933-119">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="fd933-120">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="fd933-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-121">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="fd933-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-122">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="fd933-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-123">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="fd933-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-124">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="fd933-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-125">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="fd933-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-126">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="fd933-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-127">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fd933-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fd933-128">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="fd933-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fd933-129">Требования</span><span class="sxs-lookup"><span data-stu-id="fd933-129">Requirements</span></span>



| <span data-ttu-id="fd933-130">Требование</span><span class="sxs-lookup"><span data-stu-id="fd933-130">Requirement</span></span> | <span data-ttu-id="fd933-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fd933-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd933-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd933-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fd933-133">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fd933-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fd933-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd933-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fd933-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fd933-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fd933-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fd933-136">Namespace</span></span><br/>                | <span data-ttu-id="fd933-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fd933-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fd933-138">MOF</span><span class="sxs-lookup"><span data-stu-id="fd933-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd933-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd933-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd933-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fd933-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd933-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd933-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd933-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd933-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd933-143">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="fd933-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

