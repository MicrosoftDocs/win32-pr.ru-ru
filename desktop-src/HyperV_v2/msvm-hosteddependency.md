---
description: Связывает экземпляр виртуальной машины с объектом компьютерной системы, представляющим физическую систему размещения.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Класс Msvm_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ce580e6b478dbdf320377c2738708d0eb7689fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896841"
---
# <a name="msvm_hosteddependency-class"></a><span data-ttu-id="0803c-103">\_Класс мсвм хостеддепенденци</span><span class="sxs-lookup"><span data-stu-id="0803c-103">Msvm\_HostedDependency class</span></span>

<span data-ttu-id="0803c-104">Связывает экземпляр виртуальной машины с объектом компьютерной системы, представляющим физическую систему размещения.</span><span class="sxs-lookup"><span data-stu-id="0803c-104">Associates a virtual machine instance with the computer system object that represents the physical, hosting system.</span></span>

<span data-ttu-id="0803c-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0803c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0803c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0803c-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0803c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0803c-107">Members</span></span>

<span data-ttu-id="0803c-108">Класс **мсвм \_ хостеддепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0803c-108">The **Msvm\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="0803c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0803c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0803c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0803c-110">Properties</span></span>

<span data-ttu-id="0803c-111">Класс **мсвм \_ хостеддепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0803c-111">The **Msvm\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0803c-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0803c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0803c-113">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0803c-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0803c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0803c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0803c-115">Ссылка на систему компьютера размещения.</span><span class="sxs-lookup"><span data-stu-id="0803c-115">A reference to the hosting computer system.</span></span> <span data-ttu-id="0803c-116">Это свойство наследуется от [**CIM \_ хостеддепенденци**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0803c-116">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0803c-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="0803c-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0803c-118">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0803c-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0803c-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0803c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0803c-120">Ссылка на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0803c-120">A reference to the virtual machine.</span></span> <span data-ttu-id="0803c-121">Это свойство наследуется от [**CIM \_ хостеддепенденци**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0803c-121">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0803c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0803c-122">Remarks</span></span>

<span data-ttu-id="0803c-123">Доступ к классу **\_ хостеддепенденци мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="0803c-123">Access to the **Msvm\_HostedDependency** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0803c-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0803c-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0803c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0803c-125">Requirements</span></span>



| <span data-ttu-id="0803c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0803c-126">Requirement</span></span> | <span data-ttu-id="0803c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0803c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0803c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0803c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0803c-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0803c-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0803c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0803c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0803c-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0803c-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0803c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0803c-132">Namespace</span></span><br/>                | <span data-ttu-id="0803c-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0803c-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0803c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0803c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0803c-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0803c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0803c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0803c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0803c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0803c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0803c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0803c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0803c-139">**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="0803c-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="0803c-140">[**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0803c-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0803c-141">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="0803c-141">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

