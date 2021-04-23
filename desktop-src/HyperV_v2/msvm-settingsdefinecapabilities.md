---
description: Предоставляет связь между экземпляром возможностей и минимальными, максимальными, добавочными и параметрами по умолчанию для ресурса.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Класс Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682911"
---
# <a name="msvm_settingsdefinecapabilities-class"></a><span data-ttu-id="64615-103">\_Класс мсвм сеттингсдефинекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="64615-103">Msvm\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="64615-104">Предоставляет связь между экземпляром возможностей и минимальными, максимальными, добавочными и параметрами по умолчанию для ресурса.</span><span class="sxs-lookup"><span data-stu-id="64615-104">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="64615-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="64615-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="64615-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64615-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="64615-107">Члены</span><span class="sxs-lookup"><span data-stu-id="64615-107">Members</span></span>

<span data-ttu-id="64615-108">Класс **мсвм \_ сеттингсдефинекапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="64615-108">The **Msvm\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="64615-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="64615-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64615-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="64615-110">Properties</span></span>

<span data-ttu-id="64615-111">Класс **мсвм \_ сеттингсдефинекапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="64615-111">The **Msvm\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64615-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="64615-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64615-113">Тип данных: **[ **\_ возможности CIM**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="64615-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="64615-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64615-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64615-115">Экземпляр возможностей.</span><span class="sxs-lookup"><span data-stu-id="64615-115">The capabilities instance.</span></span> <span data-ttu-id="64615-116">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64615-116">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="64615-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="64615-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64615-118">Тип данных: **[ **\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="64615-118">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="64615-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64615-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64615-120">Параметр, используемый для определения связанного экземпляра возможностей.</span><span class="sxs-lookup"><span data-stu-id="64615-120">A setting used to define the associated capabilities instance.</span></span> <span data-ttu-id="64615-121">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64615-121">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="64615-122">**пропертиполици**</span><span class="sxs-lookup"><span data-stu-id="64615-122">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64615-123">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64615-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64615-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64615-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64615-125">Указывает, обрабатываются ли непустые, ненулевые свойства экземпляра данных связанных параметров, независимо друг от друга или как коррелированный набор.</span><span class="sxs-lookup"><span data-stu-id="64615-125">Indicates whether the non-null, non-key properties of the associated setting data instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="64615-126">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)) и всегда имеет значение 0 (независимо от него).</span><span class="sxs-lookup"><span data-stu-id="64615-126">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) and it is always set to 0 (Independent).</span></span>

</dd> <dt>

<span data-ttu-id="64615-127">**суппортстатемент**</span><span class="sxs-lookup"><span data-stu-id="64615-127">**SupportStatement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64615-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64615-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64615-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64615-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64615-130">Идентифицирует инструкцию поддержки.</span><span class="sxs-lookup"><span data-stu-id="64615-130">Identifies the support statement.</span></span>

> [!Note]  
> <span data-ttu-id="64615-131">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="64615-131">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span data-ttu-id="64615-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Рабочая среда** (0)</span><span class="sxs-lookup"><span data-stu-id="64615-132"><span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Production** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span data-ttu-id="64615-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Предварительный выпуск** (1)</span><span class="sxs-lookup"><span data-stu-id="64615-133"><span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Prerelease** (1)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="64615-134">Было **Непроизводствым** в Windows 10, версия 1703.</span><span class="sxs-lookup"><span data-stu-id="64615-134">Was **NonProduction** in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="64615-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (..)</span><span class="sxs-lookup"><span data-stu-id="64615-135"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="64615-136">**валуеранже**</span><span class="sxs-lookup"><span data-stu-id="64615-136">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64615-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64615-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64615-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64615-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64615-139">Любая дальнейшая семантика для интерпретации всех ненулевых неключевых свойств данных параметров.</span><span class="sxs-lookup"><span data-stu-id="64615-139">Any further semantics on the interpretation of all non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="64615-140">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64615-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="64615-141">**валуероле**</span><span class="sxs-lookup"><span data-stu-id="64615-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64615-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="64615-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64615-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64615-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64615-144">Любая дальнейшая семантика интерпретации ненулевых неключевых свойств данных параметров.</span><span class="sxs-lookup"><span data-stu-id="64615-144">Any further semantics on the interpretation of the non-null, non-key properties of the setting data.</span></span> <span data-ttu-id="64615-145">Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64615-145">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64615-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64615-146">Remarks</span></span>

<span data-ttu-id="64615-147">Значения для свойств **валуероле** и **валуеранже** используются в следующих парах:</span><span class="sxs-lookup"><span data-stu-id="64615-147">The values for the **ValueRole** and **ValueRange** properties are used in the following pairs:</span></span>

-   <span data-ttu-id="64615-148">Точка или значение по умолчанию (0/0)</span><span class="sxs-lookup"><span data-stu-id="64615-148">Point/Default (0/0)</span></span>
-   <span data-ttu-id="64615-149">Минимум/поддерживается (1/3)</span><span class="sxs-lookup"><span data-stu-id="64615-149">Minimums/Supported (1/3)</span></span>
-   <span data-ttu-id="64615-150">Максимум/поддерживается (2/3)</span><span class="sxs-lookup"><span data-stu-id="64615-150">Maximums/Supported (2/3)</span></span>
-   <span data-ttu-id="64615-151">Инкременты и поддерживаются (3/3).</span><span class="sxs-lookup"><span data-stu-id="64615-151">Increments/Supported (3/3).</span></span>

<span data-ttu-id="64615-152">"Точка" означает, что каждое из свойств объекта **PartComponent** представляет платформу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64615-152">"Point" means that each of the properties on the **PartComponent** object represents the platform default.</span></span>

<span data-ttu-id="64615-153">"Минимум" и "максимум" означают, что каждое из свойств объекта **PartComponent** представляет наименьшее и наибольшее возможное значение для этих свойств, поддерживаемое платформой на основе текущей конфигурации компьютера.</span><span class="sxs-lookup"><span data-stu-id="64615-153">"Minimums" and "Maximums" mean that each of the properties on the **PartComponent** object represent the smallest and largest possible values for these properties that are supported by the platform based on your current machine configuration.</span></span>

<span data-ttu-id="64615-154">«Приращения» обозначает гранулярность, с которой можно увеличить или уменьшить параметры.</span><span class="sxs-lookup"><span data-stu-id="64615-154">"Increments" indicates the granularity at which you can increase or decrease the settings.</span></span>

<span data-ttu-id="64615-155">Доступ к классу **\_ сеттингсдефинекапабилитиес мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="64615-155">Access to the **Msvm\_SettingsDefineCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="64615-156">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="64615-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="64615-157">Требования</span><span class="sxs-lookup"><span data-stu-id="64615-157">Requirements</span></span>



| <span data-ttu-id="64615-158">Требование</span><span class="sxs-lookup"><span data-stu-id="64615-158">Requirement</span></span> | <span data-ttu-id="64615-159">Значение</span><span class="sxs-lookup"><span data-stu-id="64615-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64615-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64615-160">Minimum supported client</span></span><br/> | <span data-ttu-id="64615-161">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="64615-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="64615-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64615-162">Minimum supported server</span></span><br/> | <span data-ttu-id="64615-163">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="64615-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64615-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="64615-164">Namespace</span></span><br/>                | <span data-ttu-id="64615-165">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="64615-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="64615-166">MOF</span><span class="sxs-lookup"><span data-stu-id="64615-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64615-167"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64615-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64615-168">DLL</span><span class="sxs-lookup"><span data-stu-id="64615-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64615-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64615-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64615-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64615-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64615-171">**\_СЕТТИНГСДЕФИНЕКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="64615-171">**CIM\_SettingsDefineCapabilities**</span></span>](cim-settingsdefinecapabilities.md)
</dt> <dt>

<span data-ttu-id="64615-172">[**\_СЕТТИНГСДЕФИНЕКАПАБИЛИТИЕС CIM**](/previous-versions//cc136913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64615-172">[**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="64615-173">**Мсвм \_ сеттингсдефинекапабилитиес (v1)**</span><span class="sxs-lookup"><span data-stu-id="64615-173">**Msvm\_SettingsDefineCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[<span data-ttu-id="64615-174">Классы управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="64615-174">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

