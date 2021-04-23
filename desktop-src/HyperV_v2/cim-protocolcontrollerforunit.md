---
description: Представляет связь между контроллером протокола и доступным логическим устройством.
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: Класс CIM_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 26020745057d5963ed4a892ba8639ac078aaa20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663858"
---
# <a name="cim_protocolcontrollerforunit-class"></a><span data-ttu-id="0168c-103">\_Класс CIM протоколконтроллерфорунит</span><span class="sxs-lookup"><span data-stu-id="0168c-103">CIM\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="0168c-104">Представляет связь между контроллером протокола и доступным логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="0168c-104">Represents an association between a protocol controller and an exposed logical unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="0168c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0168c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="0168c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0168c-106">Members</span></span>

<span data-ttu-id="0168c-107">Класс **CIM \_ протоколконтроллерфорунит** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0168c-107">The **CIM\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="0168c-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0168c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0168c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0168c-109">Properties</span></span>

<span data-ttu-id="0168c-110">Класс **CIM \_ протоколконтроллерфорунит** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0168c-110">The **CIM\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0168c-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0168c-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0168c-112">Тип данных: **CIM \_ протоколконтроллер**</span><span class="sxs-lookup"><span data-stu-id="0168c-112">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="0168c-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0168c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0168c-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0168c-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0168c-115">Контроллер протокола.</span><span class="sxs-lookup"><span data-stu-id="0168c-115">The protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="0168c-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="0168c-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0168c-117">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="0168c-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0168c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0168c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0168c-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="0168c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0168c-120">Логическое устройство, связанное с контроллером протокола.</span><span class="sxs-lookup"><span data-stu-id="0168c-120">The logical unit associated with the protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="0168c-121">**девицеакцесс**</span><span class="sxs-lookup"><span data-stu-id="0168c-121">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0168c-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0168c-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0168c-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0168c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0168c-124">Права доступа, предоставленные логической единице через контроллер протокола.</span><span class="sxs-lookup"><span data-stu-id="0168c-124">The access rights granted to the logical unit through the protocol controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0168c-125">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0168c-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="0168c-126">**Чтение и запись** (2)</span><span class="sxs-lookup"><span data-stu-id="0168c-126">**Read Write** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="0168c-127">**Только для чтения** (3)</span><span class="sxs-lookup"><span data-stu-id="0168c-127">**Read-Only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

<span data-ttu-id="0168c-128">**Нет доступа** (4)</span><span class="sxs-lookup"><span data-stu-id="0168c-128">**No Access** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0168c-129">**Зарезервировано DMTF** (5.. 15999)</span><span class="sxs-lookup"><span data-stu-id="0168c-129">**DMTF Reserved** (5..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0168c-130">**Поставщик зарезервирован** (16000...)</span><span class="sxs-lookup"><span data-stu-id="0168c-130">**Vendor Reserved** (16000..)</span></span>


<span data-ttu-id="0168c-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0168c-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0168c-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0168c-132">Requirements</span></span>



| <span data-ttu-id="0168c-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0168c-133">Requirement</span></span> | <span data-ttu-id="0168c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0168c-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0168c-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0168c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0168c-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0168c-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0168c-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0168c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0168c-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0168c-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0168c-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0168c-139">Namespace</span></span><br/>                | <span data-ttu-id="0168c-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0168c-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0168c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="0168c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0168c-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0168c-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0168c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0168c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0168c-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0168c-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0168c-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0168c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0168c-146">**\_ПРОТОКОЛКОНТРОЛЛЕРФОРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="0168c-146">**CIM\_ProtocolControllerForDevice**</span></span>](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

