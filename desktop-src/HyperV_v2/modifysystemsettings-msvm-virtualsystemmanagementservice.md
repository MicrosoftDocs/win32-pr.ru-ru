---
description: Изменяет параметры виртуальной машины.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Метод Модифисистемсеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663983"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="4f48d-103">Метод Модифисистемсеттингс \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="4f48d-103">ModifySystemSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4f48d-104">Изменяет параметры виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f48d-104">Modifies virtual machine settings.</span></span> <span data-ttu-id="4f48d-105">При применении к параметрам системы "Текущая" Конфигурация виртуальной машины в качестве побочного результата можно изменить экземпляр виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f48d-105">When applied to the system settings of a "current" virtual machine configuration, as a side effect the virtual machine instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f48d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f48d-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4f48d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f48d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f48d-108">*SystemSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f48d-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f48d-109">Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , который содержит измененные аспекты виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f48d-109">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that contains the modified aspects of the virtual machine.</span></span> <span data-ttu-id="4f48d-110">Свойство **InstanceId** определяет изменяемый параметр виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f48d-110">The **InstanceID** property identifies the virtual machine setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="4f48d-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f48d-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f48d-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f48d-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f48d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f48d-113">Return value</span></span>

<span data-ttu-id="4f48d-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4f48d-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4f48d-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="4f48d-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="4f48d-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-117">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="4f48d-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="4f48d-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-119">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="4f48d-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-120">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="4f48d-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-121">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="4f48d-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4f48d-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="4f48d-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4f48d-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4f48d-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="4f48d-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4f48d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4f48d-126">Requirements</span></span>



| <span data-ttu-id="4f48d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4f48d-127">Requirement</span></span> | <span data-ttu-id="4f48d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4f48d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f48d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f48d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4f48d-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4f48d-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f48d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f48d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4f48d-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4f48d-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f48d-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f48d-133">Namespace</span></span><br/>                | <span data-ttu-id="4f48d-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4f48d-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f48d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4f48d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f48d-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f48d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f48d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4f48d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f48d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f48d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f48d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f48d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f48d-140">**Модифивиртуалсистем (v1)**</span><span class="sxs-lookup"><span data-stu-id="4f48d-140">**ModifyVirtualSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="4f48d-141">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="4f48d-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

