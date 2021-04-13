---
description: Связывает виртуальную машину и ее устройства с экземплярами \_ SETTINGDATA CIM, представляющими текущие параметры, которые применяются к этим объектам.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Класс Msvm_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265243"
---
# <a name="msvm_settingsdefinestate-class"></a><span data-ttu-id="0e059-103">\_Класс мсвм сеттингсдефинестате</span><span class="sxs-lookup"><span data-stu-id="0e059-103">Msvm\_SettingsDefineState class</span></span>

<span data-ttu-id="0e059-104">Связывает виртуальную машину и ее устройства с экземплярами [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) , представляющими текущие параметры, которые применяются к этим объектам.</span><span class="sxs-lookup"><span data-stu-id="0e059-104">Associates a virtual machine and its devices with instances of [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that represent the current settings that apply to these objects.</span></span> <span data-ttu-id="0e059-105">В частности, он связывает [**мсвм \_ ComputerSystem**](msvm-computersystem.md) с экземплярами [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)и связывает \**\_ \* мсвм* _, производную от [_ *CIM \_* \*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , с \**мсвм \_ \** _, производными от [_ *CIM \_ ресаурцеаллокатионсеттингдата*. \*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)</span><span class="sxs-lookup"><span data-stu-id="0e059-105">More specifically, it associates [**Msvm\_ComputerSystem**](msvm-computersystem.md) with instances of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md), and it associates \**Msvm\_\** _ derivatives of [_ *CIM\_LogicalDevice*\*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) with \**Msvm\_\** _ derivatives of [_ *CIM\_ResourceAllocationSettingData*\*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0e059-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0e059-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e059-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e059-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="0e059-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0e059-108">Members</span></span>

<span data-ttu-id="0e059-109">Класс **мсвм \_ сеттингсдефинестате** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0e059-109">The **Msvm\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="0e059-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e059-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e059-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e059-111">Properties</span></span>

<span data-ttu-id="0e059-112">Класс **мсвм \_ сеттингсдефинестате** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0e059-112">The **Msvm\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e059-113">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="0e059-113">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e059-114">Тип данных: **[ **мсвм \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="0e059-114">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0e059-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e059-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e059-116">Ссылка на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0e059-116">A reference to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0e059-117">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="0e059-117">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e059-118">Тип данных: **[ **мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="0e059-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0e059-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e059-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e059-120">Ссылка на текущие активные параметры виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e059-120">A reference to the currently active settings for the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e059-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e059-121">Remarks</span></span>

<span data-ttu-id="0e059-122">Доступ к классу **\_ сеттингсдефинестате мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="0e059-122">Access to the **Msvm\_SettingsDefineState** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0e059-123">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0e059-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e059-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0e059-124">Requirements</span></span>



| <span data-ttu-id="0e059-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0e059-125">Requirement</span></span> | <span data-ttu-id="0e059-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0e059-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e059-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e059-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e059-128">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e059-128">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0e059-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e059-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e059-130">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e059-130">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0e059-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e059-131">Namespace</span></span><br/>                | <span data-ttu-id="0e059-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0e059-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0e059-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0e059-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e059-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e059-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e059-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0e059-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e059-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e059-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e059-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e059-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e059-138">**\_СЕТТИНГСДЕФИНЕСТАТЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="0e059-138">**CIM\_SettingsDefineState**</span></span>](cim-settingsdefinestate.md)
</dt> <dt>

[<span data-ttu-id="0e059-139">**\_СЕТТИНГСДЕФИНЕСТАТЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="0e059-139">**CIM\_SettingsDefineState**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[<span data-ttu-id="0e059-140">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="0e059-140">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

