---
description: Связывает виртуальную машину и данные параметров экспорта.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Класс Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650487"
---
# <a name="msvm_systemexportsettingdata-class"></a><span data-ttu-id="e3dc8-103">\_Класс мсвм системекспортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="e3dc8-103">Msvm\_SystemExportSettingData class</span></span>

<span data-ttu-id="e3dc8-104">Связывает виртуальную машину и данные параметров экспорта.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-104">Associates a virtual machine and its export setting data.</span></span> <span data-ttu-id="e3dc8-105">Перед вызовом метода [**експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ Виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) можно получить экземпляр [**мсвм \_ виртуалсистемекспортсеттингдата**](msvm-virtualsystemexportsettingdata.md) , используя эту ассоциацию.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-105">Before calling the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class, an instance of [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) can be retrieved using this association.</span></span>

<span data-ttu-id="e3dc8-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dc8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3dc8-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="e3dc8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e3dc8-108">Members</span></span>

<span data-ttu-id="e3dc8-109">Класс **мсвм \_ системекспортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e3dc8-109">The **Msvm\_SystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e3dc8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3dc8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3dc8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3dc8-111">Properties</span></span>

<span data-ttu-id="e3dc8-112">Класс **мсвм \_ системекспортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-112">The **Msvm\_SystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3dc8-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dc8-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dc8-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3dc8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dc8-116">Указывает, используется ли на данный момент параметр, на который указывает ссылка, в операции элемента или что эта информация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-116">Indicates if the referenced setting is currently being used in the operation of the element, or that this information is unknown.</span></span> <span data-ttu-id="e3dc8-117">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e3dc8-117">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="e3dc8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc8-118">Value</span></span>                                                                        | <span data-ttu-id="e3dc8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc8-119">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="e3dc8-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-120"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e3dc8-121">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="e3dc8-121">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="e3dc8-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e3dc8-123">Текущий</span><span class="sxs-lookup"><span data-stu-id="e3dc8-123">Current</span></span><br/>     |
| <dl> <span data-ttu-id="e3dc8-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e3dc8-125">Не текущий</span><span class="sxs-lookup"><span data-stu-id="e3dc8-125">Not Current</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e3dc8-126">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-126">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dc8-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dc8-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3dc8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dc8-129">Указывает, является ли параметр, на который указывает ссылка, параметром по умолчанию для элемента или что эта информация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-129">Indicates if the referenced setting is a default setting for the element, or that this information is unknown.</span></span> <span data-ttu-id="e3dc8-130">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e3dc8-130">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="e3dc8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc8-131">Value</span></span>                                                                        | <span data-ttu-id="e3dc8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc8-132">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="e3dc8-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e3dc8-134">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="e3dc8-134">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="e3dc8-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e3dc8-136">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e3dc8-136">Default</span></span><br/>     |
| <dl> <span data-ttu-id="e3dc8-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e3dc8-138">Не по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e3dc8-138">Not Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e3dc8-139">**По подследу**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-139">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dc8-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dc8-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3dc8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dc8-142">Указывает, является ли параметр, на который указывает ссылка, следующим параметром, который должен быть применен.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-142">Indicates whether or not the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="e3dc8-143">Например, приложение может выполняться при повторной инициализации, сбросе и перенастройке запроса.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-143">For example, the application could take place on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="e3dc8-144">Это может быть постоянный параметр или параметр, используемый только один раз, как указано в флаге.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-144">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="e3dc8-145">Если это постоянный параметр, параметр применяется каждый раз при повторной инициализации управляемого элемента до тех пор, пока этот флаг не будет сброшен вручную.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-145">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="e3dc8-146">Однако при использовании одного из них флажок автоматически снимается после применения параметров.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-146">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="e3dc8-147">Кроме того, если этот флаг задан (т. е. задано значение, отличное от 0 (неизвестно)), то он имеет приоритет над всеми параметрами, которые могли быть указаны по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-147">Also, if this flag is specified (i.e. set to value other than 0 (Unknown)), then this takes precedence over any setting data that may have been specified as default.</span></span> <span data-ttu-id="e3dc8-148">Например, если управляемый элемент является компьютерной системой, а значение этого флага равно 1 (далее), этот параметр вступит в силу при следующем сбросе системы.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-148">For example: If the managed element is a computer system, and the value of this flag is 1 (Is Next), then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="e3dc8-149">И, если этот флаг не изменится, он будет сохранен при последующих сбросах системы.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-149">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="e3dc8-150">Однако если для этого флага задано значение 3 (для отдельного использования), этот параметр будет использоваться только один раз, а флаг будет сброшен после этого до 2 (не далее).</span><span class="sxs-lookup"><span data-stu-id="e3dc8-150">However, if this flag is set to 3 (Is Next For Single Use), then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="e3dc8-151">Таким образом, в приведенном выше примере, если система перезагружается, параметр не будет использоваться при второй перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-151">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<span data-ttu-id="e3dc8-152">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e3dc8-152">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="e3dc8-153">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc8-153">Value</span></span>                                                                        | <span data-ttu-id="e3dc8-154">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc8-154">Meaning</span></span>                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="e3dc8-155"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-155"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e3dc8-156">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="e3dc8-156">Unknown</span></span><br/>                |
| <dl> <span data-ttu-id="e3dc8-157"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-157"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e3dc8-158">Далее</span><span class="sxs-lookup"><span data-stu-id="e3dc8-158">Is Next</span></span><br/>                |
| <dl> <span data-ttu-id="e3dc8-159"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-159"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e3dc8-160">Не далее</span><span class="sxs-lookup"><span data-stu-id="e3dc8-160">Is Not Next</span></span><br/>            |
| <dl> <span data-ttu-id="e3dc8-161"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-161"><dt>3</dt></span></span> </dl> | <span data-ttu-id="e3dc8-162">Для одного использования</span><span class="sxs-lookup"><span data-stu-id="e3dc8-162">Is Next For Single Use</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e3dc8-163">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-163">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dc8-164">Тип данных: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-164">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e3dc8-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3dc8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3dc8-166">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ елементсеттингдата. манажеделемент")</span><span class="sxs-lookup"><span data-stu-id="e3dc8-166">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="e3dc8-167">Ссылка на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-167">Reference to the virtual machine.</span></span> <span data-ttu-id="e3dc8-168">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e3dc8-168">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="e3dc8-169">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-169">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dc8-170">Тип данных: **[ **мсвм \_ виртуалсистемекспортсеттингдата**](msvm-virtualsystemexportsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="e3dc8-170">Data type: **[**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="e3dc8-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e3dc8-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3dc8-172">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ елементсеттингдата. SettingData")</span><span class="sxs-lookup"><span data-stu-id="e3dc8-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.SettingData")</span></span>
</dt> </dl>

<span data-ttu-id="e3dc8-173">Ссылка на данные настройки экспорта для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-173">Reference to the export setting data for the virtual machine.</span></span> <span data-ttu-id="e3dc8-174">Это свойство наследуется от [**CIM \_ елементсеттингдата**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e3dc8-174">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3dc8-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3dc8-175">Remarks</span></span>

<span data-ttu-id="e3dc8-176">Доступ к классу **\_ системекспортсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e3dc8-176">Access to the **Msvm\_SystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e3dc8-177">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e3dc8-177">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3dc8-178">Требования</span><span class="sxs-lookup"><span data-stu-id="e3dc8-178">Requirements</span></span>



| <span data-ttu-id="e3dc8-179">Требование</span><span class="sxs-lookup"><span data-stu-id="e3dc8-179">Requirement</span></span> | <span data-ttu-id="e3dc8-180">Значение</span><span class="sxs-lookup"><span data-stu-id="e3dc8-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dc8-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3dc8-181">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dc8-182">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e3dc8-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e3dc8-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3dc8-183">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dc8-184">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e3dc8-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3dc8-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3dc8-185">Namespace</span></span><br/>                | <span data-ttu-id="e3dc8-186">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e3dc8-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e3dc8-187">MOF</span><span class="sxs-lookup"><span data-stu-id="e3dc8-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3dc8-188"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3dc8-189">DLL</span><span class="sxs-lookup"><span data-stu-id="e3dc8-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3dc8-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3dc8-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

