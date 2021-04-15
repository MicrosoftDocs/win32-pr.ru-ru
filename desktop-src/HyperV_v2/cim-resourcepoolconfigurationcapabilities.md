---
description: Управляет возможностями \_ экземпляра CIM ресаурцепулконфигуратионсервице для \_ объекта ResourcePool CIM.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: Класс CIM_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682816"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="70004-103">\_Класс CIM ресаурцепулконфигуратионкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="70004-103">CIM\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="70004-104">Управляет возможностями экземпляра [**CIM \_ ресаурцепулконфигуратионсервице**](cim-resourcepoolconfigurationservice.md) для объекта [**\_ ResourcePool CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="70004-104">Manages the capabilities of the [**CIM\_ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) instance for a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="70004-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70004-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="70004-106">Члены</span><span class="sxs-lookup"><span data-stu-id="70004-106">Members</span></span>

<span data-ttu-id="70004-107">Класс **CIM \_ ресаурцепулконфигуратионкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70004-107">The **CIM\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="70004-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="70004-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70004-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="70004-109">Properties</span></span>

<span data-ttu-id="70004-110">Класс **CIM \_ ресаурцепулконфигуратионкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70004-110">The **CIM\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70004-111">**асинчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="70004-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-112">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70004-112">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="70004-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70004-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70004-114">Методы службы настройки, поддерживаемые асинхронными операциями.</span><span class="sxs-lookup"><span data-stu-id="70004-114">The methods of the configuration service that are supported for asynchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-115">**CreateResourcePool поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="70004-115">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-116">**Поддерживается CreateChild ResourcePool** (3)</span><span class="sxs-lookup"><span data-stu-id="70004-116">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-117">**Делетересаурцепул поддерживается** (4)</span><span class="sxs-lookup"><span data-stu-id="70004-117">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-118">**Аддресаурцесторесаурцепул поддерживается** (5)</span><span class="sxs-lookup"><span data-stu-id="70004-118">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-119">**Ремовересаурцесфромресаурцепул поддерживается** (6)</span><span class="sxs-lookup"><span data-stu-id="70004-119">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-120">**Чанжепарентресаурцепул поддерживается** (7)</span><span class="sxs-lookup"><span data-stu-id="70004-120">**ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="70004-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="70004-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="70004-122">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="70004-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="70004-123">**синчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="70004-123">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-124">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70004-124">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="70004-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70004-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70004-126">Методы службы настройки, поддерживаемые для синхронных операций.</span><span class="sxs-lookup"><span data-stu-id="70004-126">The methods of the configuration service that are supported for synchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-127">**CreateResourcePool поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="70004-127">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-128">**Поддерживается CreateChild ResourcePool** (3)</span><span class="sxs-lookup"><span data-stu-id="70004-128">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-129">**Делетересаурцепул поддерживается** (4)</span><span class="sxs-lookup"><span data-stu-id="70004-129">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-130">**Аддресаурцесторесаурцепул поддерживается** (5)</span><span class="sxs-lookup"><span data-stu-id="70004-130">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-131">**Ремовересаурцесфромресаурцепул поддерживается** (6)</span><span class="sxs-lookup"><span data-stu-id="70004-131">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="70004-132">**Модель CIM \_ Чанжепарентресаурцепул поддерживается** (7)</span><span class="sxs-lookup"><span data-stu-id="70004-132">**CIM\_ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="70004-133">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="70004-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="70004-134">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="70004-134">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="70004-135"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="70004-135"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="70004-136">Требования</span><span class="sxs-lookup"><span data-stu-id="70004-136">Requirements</span></span>



| <span data-ttu-id="70004-137">Требование</span><span class="sxs-lookup"><span data-stu-id="70004-137">Requirement</span></span> | <span data-ttu-id="70004-138">Значение</span><span class="sxs-lookup"><span data-stu-id="70004-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70004-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70004-139">Minimum supported client</span></span><br/> | <span data-ttu-id="70004-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="70004-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="70004-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70004-141">Minimum supported server</span></span><br/> | <span data-ttu-id="70004-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="70004-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="70004-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70004-143">Namespace</span></span><br/>                | <span data-ttu-id="70004-144">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="70004-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="70004-145">MOF</span><span class="sxs-lookup"><span data-stu-id="70004-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70004-146"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70004-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70004-147">DLL</span><span class="sxs-lookup"><span data-stu-id="70004-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70004-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70004-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70004-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70004-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70004-150">**\_Возможности CIM**</span><span class="sxs-lookup"><span data-stu-id="70004-150">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

 




