---
description: Представляет непрерывный диапазон логических блоков, идентифицируемый файловой системой с помощью поля DeviceID (ключ) дисков.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: Класс CIM_LogicalDisk (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999037"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a><span data-ttu-id="74298-103">Класс CIM_LogicalDisk (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="74298-103">CIM_LogicalDisk class (Hyper-V management)</span></span>

<span data-ttu-id="74298-104">Представляет непрерывный диапазон логических блоков, идентифицируемый файловой системой с помощью поля **DeviceID** диска (Key).</span><span class="sxs-lookup"><span data-stu-id="74298-104">Represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="74298-105">Например, в среде Windows поле **DeviceID** содержит букву диска; в среде UNIX она содержит путь доступа. и в среде NetWare он содержит имя тома.</span><span class="sxs-lookup"><span data-stu-id="74298-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

## <a name="syntax"></a><span data-ttu-id="74298-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74298-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a><span data-ttu-id="74298-107">Члены</span><span class="sxs-lookup"><span data-stu-id="74298-107">Members</span></span>

<span data-ttu-id="74298-108">Класс **CIM \_ LogicalDisk** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74298-108">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="74298-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="74298-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74298-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="74298-110">Properties</span></span>

<span data-ttu-id="74298-111">Класс логического логического класса **CIM \_** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="74298-111">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74298-112">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="74298-112">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74298-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74298-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74298-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74298-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74298-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("намеформат")</span><span class="sxs-lookup"><span data-stu-id="74298-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="74298-116">Указывает, использует ли логическое устройство формат имени операционной системы.</span><span class="sxs-lookup"><span data-stu-id="74298-116">Indicates whether the logical device uses the name format of the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74298-117">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="74298-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="74298-118">**Имя устройства ОС** (12)</span><span class="sxs-lookup"><span data-stu-id="74298-118">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74298-119">**наменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="74298-119">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74298-120">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74298-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74298-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74298-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74298-122">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("наменамеспаце")</span><span class="sxs-lookup"><span data-stu-id="74298-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span></span>
</dt> </dl>

<span data-ttu-id="74298-123">Указывает, имеет ли логическое устройство то же пространство имен, что и ОС.</span><span class="sxs-lookup"><span data-stu-id="74298-123">Indicates whether the logical device has the same namespace as the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74298-124">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="74298-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="74298-125">**Пространство имен устройств ОС** (8)</span><span class="sxs-lookup"><span data-stu-id="74298-125">**OS Device Namespace** (8)</span></span>


<span data-ttu-id="74298-126"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="74298-126"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="74298-127">Требования</span><span class="sxs-lookup"><span data-stu-id="74298-127">Requirements</span></span>



| <span data-ttu-id="74298-128">Требование</span><span class="sxs-lookup"><span data-stu-id="74298-128">Requirement</span></span> | <span data-ttu-id="74298-129">Значение</span><span class="sxs-lookup"><span data-stu-id="74298-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74298-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74298-130">Minimum supported client</span></span><br/> | <span data-ttu-id="74298-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="74298-131">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="74298-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74298-132">Minimum supported server</span></span><br/> | <span data-ttu-id="74298-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74298-133">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="74298-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="74298-134">Namespace</span></span><br/>                | <span data-ttu-id="74298-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="74298-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="74298-136">MOF</span><span class="sxs-lookup"><span data-stu-id="74298-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74298-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74298-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74298-138">DLL</span><span class="sxs-lookup"><span data-stu-id="74298-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74298-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74298-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74298-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74298-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74298-141">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="74298-141">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

