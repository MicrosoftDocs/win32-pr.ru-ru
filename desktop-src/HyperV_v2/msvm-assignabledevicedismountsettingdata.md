---
description: Представляет параметры виртуальной системы для импорта. Используется методом Dismount \_ класса мсвм ассигнабледевицесервице.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Класс Msvm_AssignableDeviceDismountSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663736"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a><span data-ttu-id="3ef82-104">\_Класс мсвм ассигнабледевицедисмаунтсеттингдата</span><span class="sxs-lookup"><span data-stu-id="3ef82-104">Msvm\_AssignableDeviceDismountSettingData class</span></span>

<span data-ttu-id="3ef82-105">Представляет параметры виртуальной системы для импорта.</span><span class="sxs-lookup"><span data-stu-id="3ef82-105">Represents the settings of a virtual system to import.</span></span> <span data-ttu-id="3ef82-106">Используется методом [**dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) класса [**мсвм \_ ассигнабледевицесервице**](msvm-assignabledeviceservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ef82-106">Used by the [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) method of the [**Msvm\_AssignableDeviceService**](msvm-assignabledeviceservice.md) class.</span></span>

<span data-ttu-id="3ef82-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3ef82-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ef82-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a><span data-ttu-id="3ef82-109">Члены</span><span class="sxs-lookup"><span data-stu-id="3ef82-109">Members</span></span>

<span data-ttu-id="3ef82-110">Класс **мсвм \_ ассигнабледевицедисмаунтсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3ef82-110">The **Msvm\_AssignableDeviceDismountSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3ef82-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ef82-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ef82-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ef82-112">Properties</span></span>

<span data-ttu-id="3ef82-113">Класс **мсвм \_ ассигнабледевицедисмаунтсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3ef82-113">The **Msvm\_AssignableDeviceDismountSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ef82-114">**девицеинстанцепас**</span><span class="sxs-lookup"><span data-stu-id="3ef82-114">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ef82-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ef82-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ef82-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3ef82-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ef82-117">Идентификатор экземпляра устройства PNP.</span><span class="sxs-lookup"><span data-stu-id="3ef82-117">PNP device instance ID.</span></span>

</dd> <dt>

<span data-ttu-id="3ef82-118">**девицелокатионпас**</span><span class="sxs-lookup"><span data-stu-id="3ef82-118">**DeviceLocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ef82-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ef82-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ef82-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3ef82-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ef82-121">Путь расположения устройства PNP.</span><span class="sxs-lookup"><span data-stu-id="3ef82-121">PNP device location path.</span></span>

</dd> <dt>

<span data-ttu-id="3ef82-122">**рекуиреакссуппорт**</span><span class="sxs-lookup"><span data-stu-id="3ef82-122">**RequireAcsSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ef82-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3ef82-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ef82-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3ef82-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ef82-125">Указывает, должна ли обязательная поддержка ACS быть выполнена перед отключением.</span><span class="sxs-lookup"><span data-stu-id="3ef82-125">Indicates if the requisite ACS support should be in place before permitting the dismount.</span></span>

</dd> <dt>

<span data-ttu-id="3ef82-126">**рекуиредевицемитигатионс**</span><span class="sxs-lookup"><span data-stu-id="3ef82-126">**RequireDeviceMitigations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ef82-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3ef82-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ef82-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3ef82-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3ef82-129">Указывает, должны ли быть решены устройства перед отключением.</span><span class="sxs-lookup"><span data-stu-id="3ef82-129">Indicates if device mitigations should be in place before permitting the dismount.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ef82-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3ef82-130">Requirements</span></span>



| <span data-ttu-id="3ef82-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3ef82-131">Requirement</span></span> | <span data-ttu-id="3ef82-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3ef82-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef82-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ef82-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef82-134">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="3ef82-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3ef82-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ef82-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef82-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3ef82-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3ef82-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3ef82-137">Namespace</span></span><br/>                | <span data-ttu-id="3ef82-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3ef82-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ef82-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3ef82-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ef82-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ef82-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ef82-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3ef82-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ef82-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ef82-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ef82-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ef82-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef82-144">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3ef82-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




