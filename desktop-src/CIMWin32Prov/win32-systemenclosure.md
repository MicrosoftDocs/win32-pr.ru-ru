---
description: Представляет свойства, связанные с физическим системным корпусом.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Класс Win32_SystemEnclosure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990761"
---
# <a name="win32_systemenclosure-class"></a><span data-ttu-id="6cd08-103">\_Класс Win32 системенклосуре</span><span class="sxs-lookup"><span data-stu-id="6cd08-103">Win32\_SystemEnclosure class</span></span>

<span data-ttu-id="6cd08-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ системенклосуре для Win32** представляет свойства, связанные с физическим системным корпусом.</span><span class="sxs-lookup"><span data-stu-id="6cd08-104">The **Win32\_SystemEnclosure** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties that are associated with a physical system enclosure.</span></span>

<span data-ttu-id="6cd08-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6cd08-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6cd08-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6cd08-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd08-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cd08-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="6cd08-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6cd08-108">Members</span></span>

<span data-ttu-id="6cd08-109">Класс **Win32 \_ системенклосуре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6cd08-109">The **Win32\_SystemEnclosure** class has these types of members:</span></span>

-   [<span data-ttu-id="6cd08-110">Методы</span><span class="sxs-lookup"><span data-stu-id="6cd08-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6cd08-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="6cd08-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6cd08-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6cd08-112">Methods</span></span>

<span data-ttu-id="6cd08-113">Класс **Win32 \_ системенклосуре** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6cd08-113">The **Win32\_SystemEnclosure** class has these methods.</span></span>



| <span data-ttu-id="6cd08-114">Метод</span><span class="sxs-lookup"><span data-stu-id="6cd08-114">Method</span></span>           | <span data-ttu-id="6cd08-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6cd08-115">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="6cd08-116">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="6cd08-116">**IsCompatible**</span></span> | <span data-ttu-id="6cd08-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="6cd08-117">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6cd08-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="6cd08-118">Properties</span></span>

<span data-ttu-id="6cd08-119">Класс **Win32 \_ системенклосуре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6cd08-119">The **Win32\_SystemEnclosure** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6cd08-120">**аудиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="6cd08-120">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-121">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6cd08-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-123">Если **значение равно true**, кадр оснащен звуковым сигналом.</span><span class="sxs-lookup"><span data-stu-id="6cd08-123">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="6cd08-124">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-124">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-125">**бреачдескриптион**</span><span class="sxs-lookup"><span data-stu-id="6cd08-125">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-128">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Секуритибреач**")</span><span class="sxs-lookup"><span data-stu-id="6cd08-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-129">Произвольная строка, которая предоставляет дополнительные сведения, если свойство **секуритибреач** указывает, что произошло событие, связанное с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="6cd08-129">Free-form string that provides more information if the **SecurityBreach** property indicates that a security-related event occurred.</span></span>

<span data-ttu-id="6cd08-130">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-130">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-131">**каблеманажементстратеги**</span><span class="sxs-lookup"><span data-stu-id="6cd08-131">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-134">Произвольная строка, содержащая сведения о соединении различных кабелей и их объединении в пакет.</span><span class="sxs-lookup"><span data-stu-id="6cd08-134">Free-form string that contains information about how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="6cd08-135">Благодаря многим сетям, связанным с хранилищем и кабелям питания Управление кабелями может быть сложной и сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="6cd08-135">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="6cd08-136">Это свойство содержит сведения, помогающие в сборке и службе фрейма.</span><span class="sxs-lookup"><span data-stu-id="6cd08-136">This property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="6cd08-137">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-137">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6cd08-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-141">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6cd08-141">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-142">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="6cd08-142">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="6cd08-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-144">**чассистипес**</span><span class="sxs-lookup"><span data-stu-id="6cd08-144">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-145">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="6cd08-145">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-147">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Глобальная таблица физического контейнера DMTF \| 002,1 "), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ шасси CIM**](cim-chassis.md).**Типедескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="6cd08-147">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-148">Массив типов корпуса.</span><span class="sxs-lookup"><span data-stu-id="6cd08-148">Array of chassis types.</span></span>

<span data-ttu-id="6cd08-149">Это значение берется из члена **типа** в структуре **System корпуса или корпуса** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6cd08-149">This value comes from the **Type** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="6cd08-150">Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-150">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6cd08-151">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6cd08-151">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6cd08-152">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="6cd08-152">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="6cd08-153">**Рабочий стол** (3)</span><span class="sxs-lookup"><span data-stu-id="6cd08-153">**Desktop** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="6cd08-154">**Настольный компьютер с низким уровнем профилирования** (4)</span><span class="sxs-lookup"><span data-stu-id="6cd08-154">**Low Profile Desktop** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="6cd08-155">**Поле пиццы** (5)</span><span class="sxs-lookup"><span data-stu-id="6cd08-155">**Pizza Box** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="6cd08-156">**Мини-башня** (6)</span><span class="sxs-lookup"><span data-stu-id="6cd08-156">**Mini Tower** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="6cd08-157">**Башня** (7)</span><span class="sxs-lookup"><span data-stu-id="6cd08-157">**Tower** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="6cd08-158">**Переносимый** (8)</span><span class="sxs-lookup"><span data-stu-id="6cd08-158">**Portable** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="6cd08-159">**Портативный компьютер** (9)</span><span class="sxs-lookup"><span data-stu-id="6cd08-159">**Laptop** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="6cd08-160">**Записная книжка** (10)</span><span class="sxs-lookup"><span data-stu-id="6cd08-160">**Notebook** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="6cd08-161">**Удержание** (11)</span><span class="sxs-lookup"><span data-stu-id="6cd08-161">**Hand Held** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="6cd08-162">**Стыковочный** стыковочный модуль (12)</span><span class="sxs-lookup"><span data-stu-id="6cd08-162">**Docking Station** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="6cd08-163">**Все в одном** (13)</span><span class="sxs-lookup"><span data-stu-id="6cd08-163">**All in One** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="6cd08-164">**Подзаписная книжка** (14)</span><span class="sxs-lookup"><span data-stu-id="6cd08-164">**Sub Notebook** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="6cd08-165">**Экономия пространства** (15)</span><span class="sxs-lookup"><span data-stu-id="6cd08-165">**Space-Saving** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="6cd08-166">**Поле обеда** (16)</span><span class="sxs-lookup"><span data-stu-id="6cd08-166">**Lunch Box** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="6cd08-167">**Основной системный корпус** (17)</span><span class="sxs-lookup"><span data-stu-id="6cd08-167">**Main System Chassis** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="6cd08-168">**Корпус расширения** (18)</span><span class="sxs-lookup"><span data-stu-id="6cd08-168">**Expansion Chassis** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="6cd08-169">**Корпус** (19)</span><span class="sxs-lookup"><span data-stu-id="6cd08-169">**SubChassis** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="6cd08-170">**Корпус расширения шины** (20)</span><span class="sxs-lookup"><span data-stu-id="6cd08-170">**Bus Expansion Chassis** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="6cd08-171">**Периферийный корпус** (21)</span><span class="sxs-lookup"><span data-stu-id="6cd08-171">**Peripheral Chassis** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="6cd08-172">**Корпус для хранения данных** (22)</span><span class="sxs-lookup"><span data-stu-id="6cd08-172">**Storage Chassis** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="6cd08-173">**Корпус для монтажа в стойку** (23)</span><span class="sxs-lookup"><span data-stu-id="6cd08-173">**Rack Mount Chassis** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="6cd08-174">**Компьютер с запечатанным корпусом** (24)</span><span class="sxs-lookup"><span data-stu-id="6cd08-174">**Sealed-Case PC** (24)</span></span>

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

<span data-ttu-id="6cd08-175">**Планшет** (30)</span><span class="sxs-lookup"><span data-stu-id="6cd08-175">**Tablet** (30)</span></span>

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

<span data-ttu-id="6cd08-176">**Преобразуемый** (31)</span><span class="sxs-lookup"><span data-stu-id="6cd08-176">**Convertible** (31)</span></span>

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

<span data-ttu-id="6cd08-177">**Отсоединяемый** (32)</span><span class="sxs-lookup"><span data-stu-id="6cd08-177">**Detachable** (32)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6cd08-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6cd08-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-181">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6cd08-181">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-182">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6cd08-182">Name of the first concrete class that appears in the inheritance chain that is used in the creation of an instance.</span></span> <span data-ttu-id="6cd08-183">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="6cd08-183">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="6cd08-184">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-184">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-185">**куррентрекуиредорпродуцед**</span><span class="sxs-lookup"><span data-stu-id="6cd08-185">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-186">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="6cd08-186">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-188">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("ампер на 120 вольт")</span><span class="sxs-lookup"><span data-stu-id="6cd08-188">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-189">Ток, необходимый для шасси по адресу 120V.</span><span class="sxs-lookup"><span data-stu-id="6cd08-189">Current that is required by the chassis at 120V.</span></span> <span data-ttu-id="6cd08-190">Если питание обеспечивается корпусом, как в случае источника бесперебойного питания (ИБП), это свойство может указывать на ампераже, созданный (в виде отрицательного числа).</span><span class="sxs-lookup"><span data-stu-id="6cd08-190">If power is provided by the chassis—as in the case of an uninterruptible power supply (UPS)—this property may indicate the amperage produced (as a negative number).</span></span>

<span data-ttu-id="6cd08-191">Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-191">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-192">**Depth**</span><span class="sxs-lookup"><span data-stu-id="6cd08-192">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-193">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="6cd08-193">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-195">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="6cd08-195">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-196">Глубина физического пакета — в дюймах.</span><span class="sxs-lookup"><span data-stu-id="6cd08-196">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="6cd08-197">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-197">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-198">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6cd08-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-201">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6cd08-201">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-202">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6cd08-202">Description of the object.</span></span>

<span data-ttu-id="6cd08-203">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-204">**хеатженератион**</span><span class="sxs-lookup"><span data-stu-id="6cd08-204">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-205">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6cd08-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-207">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("БТУ в час")</span><span class="sxs-lookup"><span data-stu-id="6cd08-207">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-208">Объем тепла, формируемый шасси в БТУ/час.</span><span class="sxs-lookup"><span data-stu-id="6cd08-208">Amount of heat that is generated by the chassis in BTU/hour.</span></span>

<span data-ttu-id="6cd08-209">Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-209">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-210">**Height**</span><span class="sxs-lookup"><span data-stu-id="6cd08-210">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-211">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="6cd08-211">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-213">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="6cd08-213">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-214">Высота физического пакета — в дюймах.</span><span class="sxs-lookup"><span data-stu-id="6cd08-214">Height of the physical package—in inches.</span></span>

<span data-ttu-id="6cd08-215">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-215">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-216">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="6cd08-216">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-217">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6cd08-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-219">Если **значение — true**, физический пакет может быть горячим заменой (если можно заменить элемент физически отличающимся, но эквивалентным, пока содержащий его пакет применяет к нему питание).</span><span class="sxs-lookup"><span data-stu-id="6cd08-219">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="6cd08-220">Например, дисковый пакет, вставленный с помощью соединителей SCA, является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="6cd08-220">For example, a disk drive package that is inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="6cd08-221">Все пакеты, которые могут быть горячей заменой, по сути своей являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="6cd08-221">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="6cd08-222">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-222">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-223">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6cd08-223">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-224">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6cd08-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-226">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6cd08-226">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-227">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="6cd08-227">Date and time the object was installed.</span></span> <span data-ttu-id="6cd08-228">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="6cd08-228">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6cd08-229">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-230">**локкпресент**</span><span class="sxs-lookup"><span data-stu-id="6cd08-230">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6cd08-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-233">Если **значение равно true**, кадр защищен с блокировкой.</span><span class="sxs-lookup"><span data-stu-id="6cd08-233">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="6cd08-234">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-234">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-235">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="6cd08-235">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-238">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6cd08-238">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-239">Имя Организации, которая создает физический элемент.</span><span class="sxs-lookup"><span data-stu-id="6cd08-239">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="6cd08-240">Это значение поступает от **производителя** **системной корпуса или корпуса** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6cd08-240">This value comes from the **Manufacturer** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="6cd08-241">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-241">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-242">**Модель**</span><span class="sxs-lookup"><span data-stu-id="6cd08-242">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-245">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="6cd08-245">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-246">Имя, по которому известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="6cd08-246">Name by which the physical element is known.</span></span>

<span data-ttu-id="6cd08-247">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-247">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-248">**Name**</span><span class="sxs-lookup"><span data-stu-id="6cd08-248">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-251">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="6cd08-251">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-252">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="6cd08-252">Label by which the object is known.</span></span> <span data-ttu-id="6cd08-253">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="6cd08-253">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="6cd08-254">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-255">**нумберофповеркордс**</span><span class="sxs-lookup"><span data-stu-id="6cd08-255">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-256">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6cd08-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-258">Количество кабелей питания, которые должны быть подключены к корпусу для работы всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="6cd08-258">Number of power cords that must be connected to the chassis for all of the components to operate.</span></span>

<span data-ttu-id="6cd08-259">Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-259">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-260">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6cd08-260">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-263">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6cd08-263">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="6cd08-264">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="6cd08-264">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="6cd08-265">Имейте в виду, что если доступны только данные штрих-кода и они уникальны или могут использоваться в качестве ключа элемента, это свойство будет иметь **значение NULL** и данные штрих-кода, используемые в качестве ключа класса, в свойстве Tag.</span><span class="sxs-lookup"><span data-stu-id="6cd08-265">Be aware that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="6cd08-266">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-266">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-267">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="6cd08-267">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-270">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6cd08-270">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-271">Номер части, назначаемый Организацией, которая создает или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6cd08-271">Part number that is assigned by the organization that produces or manufacturing the physical element.</span></span>

<span data-ttu-id="6cd08-272">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-272">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-273">**повередон**</span><span class="sxs-lookup"><span data-stu-id="6cd08-273">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-274">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6cd08-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-276">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="6cd08-276">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="6cd08-277">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-277">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-278">**Службе**</span><span class="sxs-lookup"><span data-stu-id="6cd08-278">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-279">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6cd08-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-281">Если **значение равно true**, физический пакет является съемным (если он предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается, без нарушения функции общей упаковки).</span><span class="sxs-lookup"><span data-stu-id="6cd08-281">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="6cd08-282">Пакет по-прежнему может быть съемным, если для удаления требуется электропитание.</span><span class="sxs-lookup"><span data-stu-id="6cd08-282">A package can still be removable if the power must be "OFF" to perform the removal.</span></span> <span data-ttu-id="6cd08-283">Если пакет может быть удален при включенном питании, элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="6cd08-283">If the package can be removed while the power is ON, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="6cd08-284">Например, дополнительный аккумулятор ноутбука является съемным, как и дисковый пакет, вставленный с помощью соединителей приложения конфигурации сервера (SCA).</span><span class="sxs-lookup"><span data-stu-id="6cd08-284">For example, an extra battery in a laptop is removable, as is a disk drive package that is inserted using Server Configuration Application (SCA) connectors.</span></span> <span data-ttu-id="6cd08-285">Однако последняя может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="6cd08-285">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="6cd08-286">Экран ноутбука не является съемным или не является избыточным источником питания.</span><span class="sxs-lookup"><span data-stu-id="6cd08-286">A laptop display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="6cd08-287">Удаление этих компонентов повлияет на функцию общей упаковки или невозможно из-за тесной интеграции пакета.</span><span class="sxs-lookup"><span data-stu-id="6cd08-287">Removing these components would affect the function of the overall packaging or is impossible because of the tight integration of the package.</span></span>

<span data-ttu-id="6cd08-288">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-288">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-289">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="6cd08-289">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-290">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6cd08-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-292">Если **значение — true**, этот компонент физического носителя можно заменить физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="6cd08-292">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="6cd08-293">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="6cd08-293">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="6cd08-294">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="6cd08-294">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="6cd08-295">Еще один пример — это пакет источника питания, подключенный к скользящим шинам.</span><span class="sxs-lookup"><span data-stu-id="6cd08-295">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="6cd08-296">Все съемные пакеты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="6cd08-296">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="6cd08-297">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-297">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-298">**секуритибреач**</span><span class="sxs-lookup"><span data-stu-id="6cd08-298">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-299">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6cd08-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-301">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Глобальный контейнер DMTF \| 002,12 "), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Бреачдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="6cd08-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-302">Состояние физического нарушения рамки.</span><span class="sxs-lookup"><span data-stu-id="6cd08-302">Status of a physical breach of the frame.</span></span>

<span data-ttu-id="6cd08-303">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-303">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6cd08-304">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6cd08-304">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6cd08-305">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="6cd08-305">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="6cd08-306">**Нет нарушений** (3)</span><span class="sxs-lookup"><span data-stu-id="6cd08-306">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="6cd08-307">**Попытки нарушения** (4)</span><span class="sxs-lookup"><span data-stu-id="6cd08-307">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="6cd08-308">**Успешное нарушение** (5)</span><span class="sxs-lookup"><span data-stu-id="6cd08-308">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6cd08-309">**секуритистатус**</span><span class="sxs-lookup"><span data-stu-id="6cd08-309">**SecurityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-310">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6cd08-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-312">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 3, \| состояние безопасности")</span><span class="sxs-lookup"><span data-stu-id="6cd08-312">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Security Status")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-313">Параметр безопасности для внешних входных данных, например клавиатура, на компьютер.</span><span class="sxs-lookup"><span data-stu-id="6cd08-313">Security setting for external input, for example, a keyboard, to a computer.</span></span>

<span data-ttu-id="6cd08-314">Это значение берется из элемента **состояние безопасности** в структуре **корпус или корпуса** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6cd08-314">This value comes from the **Security Status** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6cd08-315">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6cd08-315">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6cd08-316">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="6cd08-316">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="6cd08-317">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="6cd08-317">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="6cd08-318">**Внешний интерфейс заблокирован** (4)</span><span class="sxs-lookup"><span data-stu-id="6cd08-318">**External interface locked out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="6cd08-319">**Включен внешний интерфейс** (5)</span><span class="sxs-lookup"><span data-stu-id="6cd08-319">**External interface enabled** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6cd08-320">**Номер**</span><span class="sxs-lookup"><span data-stu-id="6cd08-320">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-323">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="6cd08-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-324">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6cd08-324">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="6cd08-325">Это значение берется из **серийного номера** , входящего в структуру **системы или корпуса** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6cd08-325">This value comes from the **Serial Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="6cd08-326">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-327">**сервицедескриптионс**</span><span class="sxs-lookup"><span data-stu-id="6cd08-327">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-328">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6cd08-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-330">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицефилософи**")</span><span class="sxs-lookup"><span data-stu-id="6cd08-330">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-331">Массив более подробных объяснений для любой записи в массиве **сервицефилософи** .</span><span class="sxs-lookup"><span data-stu-id="6cd08-331">Array of more detailed explanations for any of the entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="6cd08-332">Имейте в виду, что каждая запись этого массива связана с записью в **сервицефилософи** , расположенной в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="6cd08-332">Be aware that each entry of this array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="6cd08-333">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-333">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-334">**сервицефилософи**</span><span class="sxs-lookup"><span data-stu-id="6cd08-334">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-335">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="6cd08-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-337">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицедескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="6cd08-337">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-338">Массив, который содержит сведения о том, будет ли кадр обслуживаться сверху, спереди, сзади или сбоку, независимо от того, есть ли в кадре скользящие лотки или съемные части, а также находится ли кадр в процессе перемещения, например при наличии подвижек.</span><span class="sxs-lookup"><span data-stu-id="6cd08-338">Array that includes whether the frame is serviced from the top, front, back, or side, whether the frame has sliding trays or removable sides, and whether the frame is moveable—for example, having rollers.</span></span>

<span data-ttu-id="6cd08-339">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-339">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6cd08-340">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6cd08-340">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6cd08-341">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6cd08-341">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="6cd08-342">**Служба из верхнего уровня** (2)</span><span class="sxs-lookup"><span data-stu-id="6cd08-342">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="6cd08-343">**Служба с передней части** (3)</span><span class="sxs-lookup"><span data-stu-id="6cd08-343">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="6cd08-344">**Со стороны службы** (4)</span><span class="sxs-lookup"><span data-stu-id="6cd08-344">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="6cd08-345">**Служба со стороны** (5)</span><span class="sxs-lookup"><span data-stu-id="6cd08-345">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="6cd08-346">**Скользящие лотки** (6)</span><span class="sxs-lookup"><span data-stu-id="6cd08-346">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="6cd08-347">**Съемные стороны** (7)</span><span class="sxs-lookup"><span data-stu-id="6cd08-347">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="6cd08-348">**Перемещаемый** (8)</span><span class="sxs-lookup"><span data-stu-id="6cd08-348">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6cd08-349">**SKU**</span><span class="sxs-lookup"><span data-stu-id="6cd08-349">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-352">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="6cd08-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-353">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6cd08-353">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="6cd08-354">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-355">**SMBIOSAssetTag**</span><span class="sxs-lookup"><span data-stu-id="6cd08-355">**SMBIOSAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-356">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-358">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 3, \| тег ресурса")</span><span class="sxs-lookup"><span data-stu-id="6cd08-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Asset Tag")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-359">Номер тега ресурса системного корпуса.</span><span class="sxs-lookup"><span data-stu-id="6cd08-359">Asset tag number of the system enclosure.</span></span>

<span data-ttu-id="6cd08-360">Это значение берется из раздела **номер тега актива** в структуре **корпус или корпуса** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6cd08-360">This value comes from the **Asset Tag Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-361">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6cd08-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-362">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-364">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6cd08-364">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-365">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6cd08-365">Current status of the object.</span></span> <span data-ttu-id="6cd08-366">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="6cd08-366">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6cd08-367">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="6cd08-367">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6cd08-368">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="6cd08-368">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6cd08-369">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="6cd08-369">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6cd08-370">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6cd08-370">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6cd08-371">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6cd08-372">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="6cd08-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6cd08-373">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6cd08-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6cd08-374">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6cd08-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6cd08-375">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6cd08-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6cd08-376">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6cd08-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6cd08-377">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6cd08-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6cd08-378">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6cd08-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6cd08-379">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6cd08-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6cd08-380">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6cd08-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6cd08-381">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6cd08-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6cd08-382">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6cd08-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6cd08-383">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6cd08-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6cd08-384">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6cd08-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6cd08-385">**Тег**</span><span class="sxs-lookup"><span data-stu-id="6cd08-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-386">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-388">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**reoverride**](../wmisdk/standard-qualifiers.md) ("тег"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="6cd08-388">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-389">Уникальный идентификатор системного корпуса.</span><span class="sxs-lookup"><span data-stu-id="6cd08-389">Unique identifier of the system enclosure.</span></span>

<span data-ttu-id="6cd08-390">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-390">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="6cd08-391">Пример: "Системный корпус 1"</span><span class="sxs-lookup"><span data-stu-id="6cd08-391">Example: "System Enclosure 1"</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-392">**типедескриптионс**</span><span class="sxs-lookup"><span data-stu-id="6cd08-392">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-393">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6cd08-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-395">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ шасси CIM**](cim-chassis.md)".**Чассистипес**")</span><span class="sxs-lookup"><span data-stu-id="6cd08-395">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-396">Массив дополнительных сведений о записях массива **чассистипес** .</span><span class="sxs-lookup"><span data-stu-id="6cd08-396">Array of more information about the **ChassisTypes** array entries.</span></span> <span data-ttu-id="6cd08-397">Имейте в виду, что каждая запись этого массива связана с записью в **чассистипес** , расположенной в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="6cd08-397">Be aware that each entry of this array is related to the entry in **ChassisTypes** that is located at the same index.</span></span>

<span data-ttu-id="6cd08-398">Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-398">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-399">**Version**</span><span class="sxs-lookup"><span data-stu-id="6cd08-399">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6cd08-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-402">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="6cd08-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-403">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="6cd08-403">Version of the physical element.</span></span>

<span data-ttu-id="6cd08-404">Это значение берется из элемента **Version** корпуса или структуры **корпуса** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6cd08-404">This value comes from the **Version** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="6cd08-405">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-405">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-406">**висиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="6cd08-406">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-407">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6cd08-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-409">Если **true**, оборудование включает видимый сигнал.</span><span class="sxs-lookup"><span data-stu-id="6cd08-409">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="6cd08-410">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-410">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-411">**Weight**</span><span class="sxs-lookup"><span data-stu-id="6cd08-411">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-412">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="6cd08-412">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-414">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="6cd08-414">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-415">Вес физического пакета в фунтах.</span><span class="sxs-lookup"><span data-stu-id="6cd08-415">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="6cd08-416">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-416">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cd08-417">**Width**</span><span class="sxs-lookup"><span data-stu-id="6cd08-417">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cd08-418">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="6cd08-418">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6cd08-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cd08-420">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="6cd08-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="6cd08-421">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="6cd08-421">Width of the physical package in inches.</span></span>

<span data-ttu-id="6cd08-422">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-422">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cd08-423">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cd08-423">Remarks</span></span>

<span data-ttu-id="6cd08-424">Класс **Win32 \_ системенклосуре** является производным от [**CIM- \_ корпуса**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="6cd08-424">The **Win32\_SystemEnclosure** class is derived from [**CIM\_Chassis**](cim-chassis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6cd08-425">Примеры</span><span class="sxs-lookup"><span data-stu-id="6cd08-425">Examples</span></span>

<span data-ttu-id="6cd08-426">При [сборе многопоточных системных ресурсов с помощью PowerShell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell в коллекции TechNet используется ряд классов, включая **Win32 \_ системенклосуре**, для получения данных из системы.</span><span class="sxs-lookup"><span data-stu-id="6cd08-426">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell example on TechNet gallery uses a number of classes, including **Win32\_SystemEnclosure**, to retrieve data from a system.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd08-427">Требования</span><span class="sxs-lookup"><span data-stu-id="6cd08-427">Requirements</span></span>



| <span data-ttu-id="6cd08-428">Требование</span><span class="sxs-lookup"><span data-stu-id="6cd08-428">Requirement</span></span> | <span data-ttu-id="6cd08-429">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd08-429">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd08-430">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cd08-430">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd08-431">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cd08-431">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6cd08-432">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cd08-432">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd08-433">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cd08-433">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6cd08-434">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6cd08-434">Namespace</span></span><br/>                | <span data-ttu-id="6cd08-435">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6cd08-435">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6cd08-436">MOF</span><span class="sxs-lookup"><span data-stu-id="6cd08-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cd08-437"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cd08-437"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cd08-438">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd08-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd08-439"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cd08-439"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd08-440">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cd08-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd08-441">**\_Корпус CIM**</span><span class="sxs-lookup"><span data-stu-id="6cd08-441">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="6cd08-442">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="6cd08-442">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="6cd08-443">Задачи WMI: оборудование компьютера</span><span class="sxs-lookup"><span data-stu-id="6cd08-443">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
