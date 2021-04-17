---
description: Подключает указанное устройство PCI, чтобы его можно было использовать в системе главного компьютера.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Метод Маунтассигнабледевице класса Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: df5f8a337fbf4baf47a4f695322944ed0b97e82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663735"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="6cfc0-103">Метод Маунтассигнабледевице \_ класса Ассигнабледевицесервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6cfc0-103">MountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="6cfc0-104">Подключает указанное устройство PCI, чтобы его можно было использовать в системе главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="6cfc0-104">Mounts the specified PCI device so that it can be used by the host computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cfc0-105">Syntax</span></span>


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6cfc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cfc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cfc0-107">*Девицеинстанцепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cfc0-107">*DeviceInstancePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfc0-108">Строка, содержащая путь к экземпляру устройства для устройства.</span><span class="sxs-lookup"><span data-stu-id="6cfc0-108">String containing the device instance path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="6cfc0-109">*Девицелокатионпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cfc0-109">*DeviceLocationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfc0-110">Строка, содержащая путь расположения устройства к устройству.</span><span class="sxs-lookup"><span data-stu-id="6cfc0-110">String containing the device location path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="6cfc0-111">*Маунтеддевицеинстанцепас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6cfc0-111">*MountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfc0-112">Строка, содержащая путь к экземпляру устройства для подключенного устройства.</span><span class="sxs-lookup"><span data-stu-id="6cfc0-112">String containing the device instance path to the mounted device.</span></span>

</dd> <dt>

<span data-ttu-id="6cfc0-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6cfc0-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfc0-114">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="6cfc0-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cfc0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cfc0-115">Return value</span></span>

<span data-ttu-id="6cfc0-116">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6cfc0-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6cfc0-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc0-130">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="6cfc0-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6cfc0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6cfc0-131">Requirements</span></span>



| <span data-ttu-id="6cfc0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6cfc0-132">Requirement</span></span> | <span data-ttu-id="6cfc0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6cfc0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfc0-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cfc0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6cfc0-135">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="6cfc0-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6cfc0-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cfc0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6cfc0-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6cfc0-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6cfc0-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6cfc0-138">Namespace</span></span><br/>                | <span data-ttu-id="6cfc0-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6cfc0-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6cfc0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6cfc0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cfc0-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cfc0-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cfc0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6cfc0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cfc0-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6cfc0-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6cfc0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cfc0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cfc0-145">**Мсвм \_ ассигнабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="6cfc0-145">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




