---
description: Связывает управляемый элемент с его данными конфигурации.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Класс Msvm_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682870"
---
# <a name="msvm_elementsettingdata-class"></a><span data-ttu-id="9c879-103">\_Класс мсвм елементсеттингдата</span><span class="sxs-lookup"><span data-stu-id="9c879-103">Msvm\_ElementSettingData class</span></span>

<span data-ttu-id="9c879-104">Связывает управляемый элемент с его данными конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9c879-104">Associates a managed element with its configuration data.</span></span> <span data-ttu-id="9c879-105">Некоторые из наиболее важных приложений этой ассоциации используются при связывании виртуальной машины и логических устройств, назначенных этой системе, со сведениями о конфигурации моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="9c879-105">Some of the more notable applications of this association are its use in linking a virtual machine and the logical devices that have been assigned to that system with their snapshot configuration information.</span></span> <span data-ttu-id="9c879-106">Текущие сведения о конфигурации связаны с виртуальной машиной и ее устройствами через ассоциацию [**мсвм \_ сеттингсдефинестате**](msvm-settingsdefinestate.md) .</span><span class="sxs-lookup"><span data-stu-id="9c879-106">Current configuration information is associated with the virtual machine and its devices through the [**Msvm\_SettingsDefineState**](msvm-settingsdefinestate.md) association.</span></span>

<span data-ttu-id="9c879-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9c879-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c879-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c879-108">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="9c879-109">Члены</span><span class="sxs-lookup"><span data-stu-id="9c879-109">Members</span></span>

<span data-ttu-id="9c879-110">Класс **мсвм \_ елементсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c879-110">The **Msvm\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9c879-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c879-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c879-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c879-112">Properties</span></span>

<span data-ttu-id="9c879-113">Класс **мсвм \_ елементсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c879-113">The **Msvm\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c879-114">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="9c879-114">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c879-115">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c879-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c879-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c879-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c879-117">Указывает, что параметр, на который указывает ссылка, в данный момент используется в операции элемента или что эти сведения неизвестны.</span><span class="sxs-lookup"><span data-stu-id="9c879-117">Indicates that the referenced setting is currently being used in the operation of the element or that this information is unknown.</span></span> <span data-ttu-id="9c879-118">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9c879-118">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="9c879-119">Значение по умолчанию — 0 (неизвестно).</span><span class="sxs-lookup"><span data-stu-id="9c879-119">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="9c879-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c879-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c879-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Является текущим** (1)</span><span class="sxs-lookup"><span data-stu-id="9c879-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Is Current** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c879-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Не является текущим** (2)</span><span class="sxs-lookup"><span data-stu-id="9c879-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Is Not Current** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c879-123">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="9c879-123">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c879-124">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c879-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c879-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c879-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c879-126">Указывает, что параметр, на который указывает ссылка, является значением по умолчанию для элемента или что эта информация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="9c879-126">Indicates that the referenced setting is a default setting for the element or that this information is unknown.</span></span> <span data-ttu-id="9c879-127">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9c879-127">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="9c879-128">Значение по умолчанию — 0 (неизвестно).</span><span class="sxs-lookup"><span data-stu-id="9c879-128">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="9c879-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c879-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c879-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>Значение **по умолчанию** (1)</span><span class="sxs-lookup"><span data-stu-id="9c879-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Is Default** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c879-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Не является значением по умолчанию** (2)</span><span class="sxs-lookup"><span data-stu-id="9c879-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Is Not Default** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c879-132">**По подследу**</span><span class="sxs-lookup"><span data-stu-id="9c879-132">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c879-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c879-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c879-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c879-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c879-135">Указывает, является ли параметр, на который указывает ссылка, следующим параметром, который должен быть применен.</span><span class="sxs-lookup"><span data-stu-id="9c879-135">Indicates whether the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="9c879-136">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9c879-136">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="9c879-137">Значение по умолчанию — 0 (неизвестно).</span><span class="sxs-lookup"><span data-stu-id="9c879-137">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="9c879-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c879-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c879-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Следующий** (1)</span><span class="sxs-lookup"><span data-stu-id="9c879-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Is Next** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c879-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Не далее** (2)</span><span class="sxs-lookup"><span data-stu-id="9c879-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Is Not Next** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c879-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Следующее для отдельного использования** (3)</span><span class="sxs-lookup"><span data-stu-id="9c879-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Is Next For Single Use** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c879-142">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="9c879-142">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c879-143">Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="9c879-143">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="9c879-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c879-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c879-145">Ссылка на виртуальную машину или виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="9c879-145">Reference to the virtual machine or virtual device.</span></span> <span data-ttu-id="9c879-146">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9c879-146">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9c879-147">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="9c879-147">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c879-148">Тип данных: **[ **\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9c879-148">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="9c879-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c879-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c879-150">Ссылка на параметры снапшоттед для виртуальной машины или виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="9c879-150">Reference to the snapshotted settings for the virtual machine or virtual device.</span></span> <span data-ttu-id="9c879-151">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9c879-151">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c879-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c879-152">Remarks</span></span>

<span data-ttu-id="9c879-153">Доступ к классу **\_ елементсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="9c879-153">Access to the **Msvm\_ElementSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9c879-154">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9c879-154">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9c879-155">Примеры</span><span class="sxs-lookup"><span data-stu-id="9c879-155">Examples</span></span>

<span data-ttu-id="9c879-156">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9c879-156">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c879-157">Требования</span><span class="sxs-lookup"><span data-stu-id="9c879-157">Requirements</span></span>



| <span data-ttu-id="9c879-158">Требование</span><span class="sxs-lookup"><span data-stu-id="9c879-158">Requirement</span></span> | <span data-ttu-id="9c879-159">Значение</span><span class="sxs-lookup"><span data-stu-id="9c879-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c879-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c879-160">Minimum supported client</span></span><br/> | <span data-ttu-id="9c879-161">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9c879-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c879-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c879-162">Minimum supported server</span></span><br/> | <span data-ttu-id="9c879-163">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9c879-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c879-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c879-164">Namespace</span></span><br/>                | <span data-ttu-id="9c879-165">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9c879-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c879-166">MOF</span><span class="sxs-lookup"><span data-stu-id="9c879-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c879-167"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c879-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c879-168">DLL</span><span class="sxs-lookup"><span data-stu-id="9c879-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c879-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c879-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c879-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c879-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c879-171">**\_ЕЛЕМЕНТСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="9c879-171">**CIM\_ElementSettingData**</span></span>](cim-elementsettingdata.md)
</dt> <dt>

[<span data-ttu-id="9c879-172">**\_ЕЛЕМЕНТСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="9c879-172">**CIM\_ElementSettingData**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[<span data-ttu-id="9c879-173">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="9c879-173">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

