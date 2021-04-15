---
description: Универсальная ассоциация, используемая для установления части отношений между одним экземпляром CIM \_ виртуалсистемсеттингдата и одним или несколькими экземплярами CIM \_ ресаурцеаллокатионсеттингдата.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Класс Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662227"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="7a330-103">\_Класс мсвм виртуалсистемсеттингдатакомпонент</span><span class="sxs-lookup"><span data-stu-id="7a330-103">Msvm\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="7a330-104">Универсальная ассоциация, используемая для установления отношений "часть" между одним экземпляром [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) и одним или несколькими экземплярами [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7a330-104">A generic association used to establish 'part of' relationships between one instance of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) and one or more instances of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="7a330-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7a330-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a330-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a330-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="7a330-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7a330-107">Members</span></span>

<span data-ttu-id="7a330-108">Класс **мсвм \_ виртуалсистемсеттингдатакомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7a330-108">The **Msvm\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="7a330-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a330-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a330-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a330-110">Properties</span></span>

<span data-ttu-id="7a330-111">Класс **мсвм \_ виртуалсистемсеттингдатакомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7a330-111">The **Msvm\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a330-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="7a330-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a330-113">Тип данных: **[ **CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="7a330-113">Data type: **[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="7a330-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a330-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a330-115">Квалификаторы: **override**, **min** (1), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="7a330-115">Qualifiers: **Override**, **Min** (1), **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="7a330-116">Родительский элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="7a330-116">The parent element in the association.</span></span> <span data-ttu-id="7a330-117">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдатакомпонент**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7a330-117">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7a330-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7a330-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a330-119">Тип данных: **[ **CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="7a330-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="7a330-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a330-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a330-121">Дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="7a330-121">The child element in the association.</span></span> <span data-ttu-id="7a330-122">Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдатакомпонент**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7a330-122">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a330-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a330-123">Remarks</span></span>

<span data-ttu-id="7a330-124">Доступ к классу **\_ виртуалсистемсеттингдатакомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7a330-124">Access to the **Msvm\_VirtualSystemSettingDataComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7a330-125">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7a330-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a330-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7a330-126">Requirements</span></span>



| <span data-ttu-id="7a330-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7a330-127">Requirement</span></span> | <span data-ttu-id="7a330-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7a330-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a330-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a330-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7a330-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7a330-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7a330-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a330-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7a330-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7a330-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a330-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a330-133">Namespace</span></span><br/>                | <span data-ttu-id="7a330-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7a330-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7a330-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7a330-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a330-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a330-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a330-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7a330-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a330-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a330-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7a330-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a330-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a330-140">**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТАКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="7a330-140">**CIM\_VirtualSystemSettingDataComponent**</span></span>](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

<span data-ttu-id="7a330-141">[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТАКОМПОНЕНТ CIM**](/previous-versions//cc150674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7a330-141">[**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7a330-142">Классы виртуальных систем</span><span class="sxs-lookup"><span data-stu-id="7a330-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

