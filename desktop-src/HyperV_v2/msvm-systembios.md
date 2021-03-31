---
description: Используется для связывания виртуальной машины с BIOS.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Класс Msvm_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143909"
---
# <a name="msvm_systembios-class"></a><span data-ttu-id="e8f89-103">\_Класс мсвм систембиос</span><span class="sxs-lookup"><span data-stu-id="e8f89-103">Msvm\_SystemBIOS class</span></span>

<span data-ttu-id="e8f89-104">Используется для связывания виртуальной машины с BIOS.</span><span class="sxs-lookup"><span data-stu-id="e8f89-104">Used to associate a virtual machine with its BIOS.</span></span>

<span data-ttu-id="e8f89-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e8f89-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8f89-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8f89-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e8f89-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e8f89-107">Members</span></span>

<span data-ttu-id="e8f89-108">Класс **мсвм \_ систембиос** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e8f89-108">The **Msvm\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="e8f89-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8f89-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8f89-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8f89-110">Properties</span></span>

<span data-ttu-id="e8f89-111">Класс **мсвм \_ систембиос** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e8f89-111">The **Msvm\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8f89-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="e8f89-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f89-113">Тип данных: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="e8f89-113">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e8f89-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8f89-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f89-115">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e8f89-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e8f89-116">Виртуальная машина, которая запускается из BIOS.</span><span class="sxs-lookup"><span data-stu-id="e8f89-116">The virtual machine that starts from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="e8f89-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e8f89-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f89-118">Тип данных: **[ **мсвм \_ биоселемент**](msvm-bioselement.md)**</span><span class="sxs-lookup"><span data-stu-id="e8f89-118">Data type: **[**Msvm\_BIOSElement**](msvm-bioselement.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e8f89-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8f89-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f89-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e8f89-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e8f89-121">BIOS, связанная с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="e8f89-121">The BIOS associated with the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8f89-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8f89-122">Remarks</span></span>

<span data-ttu-id="e8f89-123">Доступ к классу **\_ систембиос мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e8f89-123">Access to the **Msvm\_SystemBIOS** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e8f89-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e8f89-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8f89-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e8f89-125">Requirements</span></span>



| <span data-ttu-id="e8f89-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e8f89-126">Requirement</span></span> | <span data-ttu-id="e8f89-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e8f89-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f89-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8f89-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8f89-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e8f89-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e8f89-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8f89-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8f89-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e8f89-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8f89-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8f89-132">Namespace</span></span><br/>                | <span data-ttu-id="e8f89-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e8f89-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e8f89-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e8f89-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8f89-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8f89-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8f89-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e8f89-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8f89-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8f89-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8f89-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8f89-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f89-139">**\_СИСТЕМБИОС CIM**</span><span class="sxs-lookup"><span data-stu-id="e8f89-139">**CIM\_SystemBIOS**</span></span>](cim-systembios.md)
</dt> <dt>

[<span data-ttu-id="e8f89-140">Классы BIOS</span><span class="sxs-lookup"><span data-stu-id="e8f89-140">BIOS Classes</span></span>](bios-classes.md)
</dt> </dl>

 

