---
description: Отключает указанное устройство PCI, чтобы его можно было назначить.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Метод Дисмаунтассигнабледевице класса Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683756"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="4686c-103">Метод Дисмаунтассигнабледевице \_ класса Ассигнабледевицесервице мсвм</span><span class="sxs-lookup"><span data-stu-id="4686c-103">DismountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="4686c-104">Отключает указанное устройство PCI, чтобы его можно было назначить.</span><span class="sxs-lookup"><span data-stu-id="4686c-104">Dismounts the specified PCI device so that it can be assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="4686c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4686c-105">Syntax</span></span>


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4686c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4686c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4686c-107">*Дисмаунтсеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4686c-107">*DismountSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-108">Внедренный экземпляр объекта данных параметра, указывающий устройство PCI для отключения.</span><span class="sxs-lookup"><span data-stu-id="4686c-108">Embedded instance of a setting data object that specifies the PCI device to dismount.</span></span>

</dd> <dt>

<span data-ttu-id="4686c-109">*Дисмаунтеддевицеинстанцепас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4686c-109">*DismountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-110">Строка, содержащая путь к экземпляру устройства для отключенного устройства.</span><span class="sxs-lookup"><span data-stu-id="4686c-110">String containing the device instance path to the dismounted device.</span></span>

</dd> <dt>

<span data-ttu-id="4686c-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4686c-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-112">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="4686c-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4686c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4686c-113">Return value</span></span>

<span data-ttu-id="4686c-114">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4686c-114">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4686c-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="4686c-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="4686c-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="4686c-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="4686c-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="4686c-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="4686c-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="4686c-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="4686c-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="4686c-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="4686c-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="4686c-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="4686c-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="4686c-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4686c-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="4686c-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4686c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4686c-129">Requirements</span></span>



| <span data-ttu-id="4686c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4686c-130">Requirement</span></span> | <span data-ttu-id="4686c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4686c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4686c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4686c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4686c-133">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="4686c-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4686c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4686c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4686c-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4686c-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4686c-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4686c-136">Namespace</span></span><br/>                | <span data-ttu-id="4686c-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4686c-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4686c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4686c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4686c-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4686c-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4686c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4686c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4686c-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4686c-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4686c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4686c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4686c-143">**Мсвм \_ ассигнабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="4686c-143">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




