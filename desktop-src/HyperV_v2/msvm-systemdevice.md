---
description: Связывает логическое устройство с родительской системой.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Класс Msvm_SystemDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650486"
---
# <a name="msvm_systemdevice-class"></a><span data-ttu-id="2f645-103">\_Класс мсвм системдевице</span><span class="sxs-lookup"><span data-stu-id="2f645-103">Msvm\_SystemDevice class</span></span>

<span data-ttu-id="2f645-104">Логические устройства могут быть агрегированы системой.</span><span class="sxs-lookup"><span data-stu-id="2f645-104">Logical devices can be aggregated by a system.</span></span> <span data-ttu-id="2f645-105">Эта связь делается явной в связи с системным устройством.</span><span class="sxs-lookup"><span data-stu-id="2f645-105">This relationship is made explicit by the system device association.</span></span>

<span data-ttu-id="2f645-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2f645-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f645-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f645-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2f645-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2f645-108">Members</span></span>

<span data-ttu-id="2f645-109">Класс **мсвм \_ системдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2f645-109">The **Msvm\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2f645-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2f645-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f645-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2f645-111">Properties</span></span>

<span data-ttu-id="2f645-112">Класс **мсвм \_ системдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2f645-112">The **Msvm\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f645-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="2f645-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f645-114">Тип данных: **[ **\_ система CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="2f645-114">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="2f645-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f645-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f645-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2f645-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="2f645-117">Родительская система в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="2f645-117">The parent system in the association.</span></span> <span data-ttu-id="2f645-118">Это свойство наследуется [**от \_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="2f645-118">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="2f645-119">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2f645-119">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f645-120">Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="2f645-120">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="2f645-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f645-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f645-122">Логическое устройство, которое является элементом системы.</span><span class="sxs-lookup"><span data-stu-id="2f645-122">The logical device that is an element of a system.</span></span> <span data-ttu-id="2f645-123">Это свойство наследуется [**от \_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="2f645-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f645-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f645-124">Remarks</span></span>

<span data-ttu-id="2f645-125">Доступ к классу **\_ системдевице мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="2f645-125">Access to the **Msvm\_SystemDevice** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2f645-126">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2f645-126">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f645-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2f645-127">Requirements</span></span>



| <span data-ttu-id="2f645-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2f645-128">Requirement</span></span> | <span data-ttu-id="2f645-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2f645-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f645-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f645-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2f645-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2f645-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f645-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f645-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2f645-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2f645-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f645-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2f645-134">Namespace</span></span><br/>                | <span data-ttu-id="2f645-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2f645-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f645-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2f645-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f645-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f645-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f645-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2f645-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f645-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f645-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f645-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f645-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f645-141">**\_СИСТЕМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="2f645-141">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="2f645-142">**\_СИСТЕМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="2f645-142">**CIM\_SystemDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[<span data-ttu-id="2f645-143">Классы виртуальных систем</span><span class="sxs-lookup"><span data-stu-id="2f645-143">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

