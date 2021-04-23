---
description: Обновляет виртуальную систему.
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Метод Упградесистемверсион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c34b33da14d8718f2c2414de3aea3079672bbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682487"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="5ca81-103">Метод Упградесистемверсион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="5ca81-103">UpgradeSystemVersion method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="5ca81-104">Обновляет виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="5ca81-104">Upgrades the virtual system.</span></span>

<span data-ttu-id="5ca81-105">При применении к параметрам системы "Текущая" Конфигурация виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="5ca81-105">When applied to the system settings of a "current" virtual system configuration</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca81-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ca81-106">Syntax</span></span>


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5ca81-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ca81-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca81-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ca81-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca81-109">Ссылка на объект [**CIM, \_**](cim-computersystem.md) представляющий систему обновляемого виртуального компьютера.</span><span class="sxs-lookup"><span data-stu-id="5ca81-109">A reference to a [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual computer system to be upgraded.</span></span>

</dd> <dt>

<span data-ttu-id="5ca81-110">*Упградесеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ca81-110">*UpgradeSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca81-111">Данные параметра обновления.</span><span class="sxs-lookup"><span data-stu-id="5ca81-111">The upgrade setting data.</span></span>

</dd> <dt>

<span data-ttu-id="5ca81-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5ca81-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca81-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5ca81-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca81-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ca81-114">Return value</span></span>

<span data-ttu-id="5ca81-115">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5ca81-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5ca81-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="5ca81-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="5ca81-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="5ca81-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="5ca81-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="5ca81-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-121">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="5ca81-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-122">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="5ca81-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5ca81-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="5ca81-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5ca81-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5ca81-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="5ca81-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5ca81-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5ca81-127">Requirements</span></span>



| <span data-ttu-id="5ca81-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5ca81-128">Requirement</span></span> | <span data-ttu-id="5ca81-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5ca81-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca81-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ca81-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca81-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5ca81-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5ca81-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ca81-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca81-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5ca81-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5ca81-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5ca81-134">Namespace</span></span><br/>                | <span data-ttu-id="5ca81-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5ca81-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ca81-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5ca81-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ca81-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ca81-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ca81-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5ca81-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca81-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ca81-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ca81-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ca81-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca81-141">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="5ca81-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

