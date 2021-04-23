---
description: Представляет связь между управляемым элементом и связанными с ним данными параметров. Эта Ассоциация также описывает, является ли этот параметр стандартным или текущим.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Класс CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663482"
---
# <a name="cim_elementsettingdata-class"></a><span data-ttu-id="18b19-104">\_Класс CIM елементсеттингдата</span><span class="sxs-lookup"><span data-stu-id="18b19-104">CIM\_ElementSettingData class</span></span>

<span data-ttu-id="18b19-105">Представляет связь между управляемым элементом и связанными с ним данными параметров.</span><span class="sxs-lookup"><span data-stu-id="18b19-105">Represents an association between a managed element and its associated setting data.</span></span> <span data-ttu-id="18b19-106">Эта Ассоциация также описывает, является ли этот параметр стандартным или текущим.</span><span class="sxs-lookup"><span data-stu-id="18b19-106">This association also describes whether this is a default or current setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b19-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18b19-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a><span data-ttu-id="18b19-108">Члены</span><span class="sxs-lookup"><span data-stu-id="18b19-108">Members</span></span>

<span data-ttu-id="18b19-109">Класс **CIM \_ елементсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18b19-109">The **CIM\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="18b19-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="18b19-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18b19-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="18b19-111">Properties</span></span>

<span data-ttu-id="18b19-112">Класс **CIM \_ елементсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18b19-112">The **CIM\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18b19-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="18b19-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b19-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18b19-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18b19-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18b19-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b19-116">Указывает, используется ли в данный момент параметр, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="18b19-116">Indicates whether the referenced setting is currently being used by the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18b19-117">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="18b19-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

<span data-ttu-id="18b19-118">**Является текущим** (1)</span><span class="sxs-lookup"><span data-stu-id="18b19-118">**Is Current** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

<span data-ttu-id="18b19-119">**Не является текущим** (2)</span><span class="sxs-lookup"><span data-stu-id="18b19-119">**Is Not Current** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18b19-120">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="18b19-120">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b19-121">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18b19-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18b19-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18b19-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b19-123">Указывает, является ли параметр параметром по умолчанию для элемента.</span><span class="sxs-lookup"><span data-stu-id="18b19-123">Indicating whether the setting is a default setting for the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18b19-124">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="18b19-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

<span data-ttu-id="18b19-125">Значение **по умолчанию** (1)</span><span class="sxs-lookup"><span data-stu-id="18b19-125">**Is Default** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

<span data-ttu-id="18b19-126">**Не является значением по умолчанию** (2)</span><span class="sxs-lookup"><span data-stu-id="18b19-126">**Is Not Default** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18b19-127">**По подследу**</span><span class="sxs-lookup"><span data-stu-id="18b19-127">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b19-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18b19-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18b19-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18b19-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b19-130">Флаг, указывающий, когда и как часто следует применять этот параметр.</span><span class="sxs-lookup"><span data-stu-id="18b19-130">A flag that indicates when and how often to apply the setting.</span></span>

<span data-ttu-id="18b19-131">Например, параметр можно применить к запросу повторной инициализации, сброса и перенастройки.</span><span class="sxs-lookup"><span data-stu-id="18b19-131">For example, the setting could be applied on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="18b19-132">Это может быть постоянный параметр или параметр, используемый только один раз, как указано в флаге.</span><span class="sxs-lookup"><span data-stu-id="18b19-132">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="18b19-133">Если это постоянный параметр, параметр применяется каждый раз при повторной инициализации управляемого элемента до тех пор, пока этот флаг не будет сброшен вручную.</span><span class="sxs-lookup"><span data-stu-id="18b19-133">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="18b19-134">Однако при использовании одного из них флажок автоматически снимается после применения параметров.</span><span class="sxs-lookup"><span data-stu-id="18b19-134">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="18b19-135">Кроме того, если для этого флага задано значение, отличное от 0 (неизвестно), то это имеет приоритет над свойством **SettingData** , для которого задано "default".</span><span class="sxs-lookup"><span data-stu-id="18b19-135">In addition, if this flag is set to value other than 0 (Unknown), then this takes precedence over a **SettingData** property that is set to "Default".</span></span>

<span data-ttu-id="18b19-136">Если управляемый элемент является компьютерной системой, а значение этого флага — «далее», то параметр вступит в силу при следующем сбросе системы.</span><span class="sxs-lookup"><span data-stu-id="18b19-136">If the managed element is a computer system, and the value of this flag is "Is Next", then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="18b19-137">И, если этот флаг не изменится, он будет сохранен при последующих сбросах системы.</span><span class="sxs-lookup"><span data-stu-id="18b19-137">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="18b19-138">Однако если этот флаг имеет значение "Далее для отдельного использования", этот параметр будет использоваться только один раз, а флаг будет сброшен после этого до 2 (не далее).</span><span class="sxs-lookup"><span data-stu-id="18b19-138">However, if this flag is set to "Is Next For Single Use", then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="18b19-139">Таким образом, в приведенном выше примере, если система перезагружается, параметр не будет использоваться при второй перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="18b19-139">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18b19-140">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="18b19-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

<span data-ttu-id="18b19-141">**Следующий** (1)</span><span class="sxs-lookup"><span data-stu-id="18b19-141">**Is Next** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

<span data-ttu-id="18b19-142">**Не далее** (2)</span><span class="sxs-lookup"><span data-stu-id="18b19-142">**Is Not Next** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

<span data-ttu-id="18b19-143">**Следующее для отдельного использования** (3)</span><span class="sxs-lookup"><span data-stu-id="18b19-143">**Is Next For Single Use** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18b19-144">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="18b19-144">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b19-145">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="18b19-145">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="18b19-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18b19-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18b19-147">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18b19-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18b19-148">Управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="18b19-148">The managed element.</span></span>

</dd> <dt>

<span data-ttu-id="18b19-149">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="18b19-149">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b19-150">Тип данных: **\_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="18b19-150">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="18b19-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18b19-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18b19-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18b19-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18b19-153">Данные параметра, связанные с элементом.</span><span class="sxs-lookup"><span data-stu-id="18b19-153">The setting data associated with the element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18b19-154">Требования</span><span class="sxs-lookup"><span data-stu-id="18b19-154">Requirements</span></span>



| <span data-ttu-id="18b19-155">Требование</span><span class="sxs-lookup"><span data-stu-id="18b19-155">Requirement</span></span> | <span data-ttu-id="18b19-156">Значение</span><span class="sxs-lookup"><span data-stu-id="18b19-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b19-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18b19-157">Minimum supported client</span></span><br/> | <span data-ttu-id="18b19-158">Windows 8</span><span class="sxs-lookup"><span data-stu-id="18b19-158">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="18b19-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18b19-159">Minimum supported server</span></span><br/> | <span data-ttu-id="18b19-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18b19-160">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="18b19-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18b19-161">Namespace</span></span><br/>                | <span data-ttu-id="18b19-162">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="18b19-162">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18b19-163">MOF</span><span class="sxs-lookup"><span data-stu-id="18b19-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18b19-164"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18b19-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18b19-165">DLL</span><span class="sxs-lookup"><span data-stu-id="18b19-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18b19-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18b19-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

