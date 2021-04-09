---
description: '\_Класс шасси CIM представляет физические элементы, охватывающие другие элементы, и предоставляет определяемые функциональные возможности, такие как рабочий стол, обрабатывающий узел, ИБП, диск или ленточное хранилище или их сочетание.'
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: Класс CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141950"
---
# <a name="cim_chassis-class"></a><span data-ttu-id="9a969-103">\_Класс шасси CIM</span><span class="sxs-lookup"><span data-stu-id="9a969-103">CIM\_Chassis class</span></span>

<span data-ttu-id="9a969-104">Класс **\_ шасси CIM** представляет физические элементы, охватывающие другие элементы, и предоставляет определяемые функциональные возможности, такие как рабочий стол, обрабатывающий узел, ИБП, диск или ленточное хранилище или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="9a969-104">The **CIM\_Chassis** class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a969-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9a969-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9a969-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9a969-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9a969-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9a969-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9a969-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="9a969-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a969-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a969-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="9a969-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9a969-110">Members</span></span>

<span data-ttu-id="9a969-111">Класс **\_ шасси CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9a969-111">The **CIM\_Chassis** class has these types of members:</span></span>

-   [<span data-ttu-id="9a969-112">Методы</span><span class="sxs-lookup"><span data-stu-id="9a969-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9a969-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a969-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9a969-114">Методы</span><span class="sxs-lookup"><span data-stu-id="9a969-114">Methods</span></span>

<span data-ttu-id="9a969-115">Класс **\_ шасси CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9a969-115">The **CIM\_Chassis** class has these methods.</span></span>



| <span data-ttu-id="9a969-116">Метод</span><span class="sxs-lookup"><span data-stu-id="9a969-116">Method</span></span>                                                           | <span data-ttu-id="9a969-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9a969-117">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a969-118">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="9a969-118">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-chassis.md) | <span data-ttu-id="9a969-119">Проверяет, может ли связанный физический элемент быть включен в физический пакет или вставлен в него.</span><span class="sxs-lookup"><span data-stu-id="9a969-119">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="9a969-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9a969-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9a969-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a969-121">Properties</span></span>

<span data-ttu-id="9a969-122">Класс **\_ шасси CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9a969-122">The **CIM\_Chassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a969-123">**аудиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="9a969-123">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a969-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-126">Если **значение равно true**, кадр оснащен звуковым сигналом.</span><span class="sxs-lookup"><span data-stu-id="9a969-126">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="9a969-127">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-127">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-128">**бреачдескриптион**</span><span class="sxs-lookup"><span data-stu-id="9a969-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Секуритибреач**")</span><span class="sxs-lookup"><span data-stu-id="9a969-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-132">Произвольная строка, которая предоставляет дополнительные сведения, если свойство **секуритибреач** указывает на то, что произошло нарушение или какое-либо другое событие, связанное с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="9a969-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="9a969-133">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-133">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-134">**каблеманажементстратеги**</span><span class="sxs-lookup"><span data-stu-id="9a969-134">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-137">Произвольная строка, содержащая сведения о соединении различных кабелей и их объединении в пакеты.</span><span class="sxs-lookup"><span data-stu-id="9a969-137">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="9a969-138">Благодаря многим сетям, связанным с хранилищем и кабелям питания Управление кабелями может быть сложной и сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="9a969-138">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="9a969-139">Это строковое свойство содержит сведения, помогающие в сборке и службе фрейма.</span><span class="sxs-lookup"><span data-stu-id="9a969-139">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="9a969-140">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-140">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-141">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9a969-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-144">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9a969-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-145">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9a969-145">A short textual description of the object.</span></span>

<span data-ttu-id="9a969-146">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-147">**чассистипес**</span><span class="sxs-lookup"><span data-stu-id="9a969-147">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9a969-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9a969-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-150">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Глобальная таблица физического контейнера DMTF \| 002,1 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ шасси CIM**.**Типедескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="9a969-150">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-151">Пронумерованный массив целочисленных значений, указывающий тип корпуса.</span><span class="sxs-lookup"><span data-stu-id="9a969-151">Enumerated, integer-valued array that indicates the type of chassis.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9a969-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9a969-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-153">Другое</span><span class="sxs-lookup"><span data-stu-id="9a969-153">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a969-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="9a969-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-155">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="9a969-155">Unknown.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="9a969-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Рабочий стол** (3)</span><span class="sxs-lookup"><span data-stu-id="9a969-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-157">Настольные ПК.</span><span class="sxs-lookup"><span data-stu-id="9a969-157">Desktop.</span></span>

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="9a969-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Настольный компьютер с низким уровнем профилирования** (4)</span><span class="sxs-lookup"><span data-stu-id="9a969-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Low Profile Desktop** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-159">Настольный компьютер с низким уровнем профилирования.</span><span class="sxs-lookup"><span data-stu-id="9a969-159">Low-profile desktop.</span></span>

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="9a969-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Поле пиццы** (5)</span><span class="sxs-lookup"><span data-stu-id="9a969-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-161">Поле пиццы.</span><span class="sxs-lookup"><span data-stu-id="9a969-161">Pizza box.</span></span>

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="9a969-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Мини-башня** (6)</span><span class="sxs-lookup"><span data-stu-id="9a969-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Tower** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-163">Мини-башня.</span><span class="sxs-lookup"><span data-stu-id="9a969-163">Mini tower.</span></span>

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="9a969-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Башня** (7)</span><span class="sxs-lookup"><span data-stu-id="9a969-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-165">Башня.</span><span class="sxs-lookup"><span data-stu-id="9a969-165">Tower.</span></span>

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="9a969-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Переносимый** (8)</span><span class="sxs-lookup"><span data-stu-id="9a969-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-167">Устройств.</span><span class="sxs-lookup"><span data-stu-id="9a969-167">Portable.</span></span>

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="9a969-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Портативный компьютер** (9)</span><span class="sxs-lookup"><span data-stu-id="9a969-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-169">Ноутбук.</span><span class="sxs-lookup"><span data-stu-id="9a969-169">Laptop.</span></span>

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="9a969-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Записная книжка** (10)</span><span class="sxs-lookup"><span data-stu-id="9a969-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-171">Занятий.</span><span class="sxs-lookup"><span data-stu-id="9a969-171">Notebook.</span></span>

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="9a969-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Удержание** (11)</span><span class="sxs-lookup"><span data-stu-id="9a969-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-173">С удержанием вручную.</span><span class="sxs-lookup"><span data-stu-id="9a969-173">Hand-held.</span></span>

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="9a969-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Стыковочный** стыковочный модуль (12)</span><span class="sxs-lookup"><span data-stu-id="9a969-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-175">Станция стыковки.</span><span class="sxs-lookup"><span data-stu-id="9a969-175">Docking station.</span></span>

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="9a969-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Все в одном** (13)</span><span class="sxs-lookup"><span data-stu-id="9a969-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**All in One** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-177">Все-в одном.</span><span class="sxs-lookup"><span data-stu-id="9a969-177">All-in-one.</span></span>

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="9a969-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Подзаписная книжка** (14)</span><span class="sxs-lookup"><span data-stu-id="9a969-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-179">Подзаписная книжка.</span><span class="sxs-lookup"><span data-stu-id="9a969-179">Subnotebook.</span></span>

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="9a969-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Экономия пространства** (15)</span><span class="sxs-lookup"><span data-stu-id="9a969-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Space-Saving** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-181">Сохранение пробелов.</span><span class="sxs-lookup"><span data-stu-id="9a969-181">Space-saving.</span></span>

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="9a969-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Поле обеда** (16)</span><span class="sxs-lookup"><span data-stu-id="9a969-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-183">Поле обеда.</span><span class="sxs-lookup"><span data-stu-id="9a969-183">Lunch box.</span></span>

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="9a969-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Основной системный корпус** (17)</span><span class="sxs-lookup"><span data-stu-id="9a969-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Main System Chassis** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-185">Основной системный корпус.</span><span class="sxs-lookup"><span data-stu-id="9a969-185">Main system chassis.</span></span>

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="9a969-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Корпус расширения** (18)</span><span class="sxs-lookup"><span data-stu-id="9a969-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Expansion Chassis** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-187">Корпус расширения.</span><span class="sxs-lookup"><span data-stu-id="9a969-187">Expansion chassis.</span></span>

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="9a969-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**Корпус** (19)</span><span class="sxs-lookup"><span data-stu-id="9a969-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-189">Подшасси.</span><span class="sxs-lookup"><span data-stu-id="9a969-189">Subchassis.</span></span>

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="9a969-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Корпус расширения шины** (20)</span><span class="sxs-lookup"><span data-stu-id="9a969-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Bus Expansion Chassis** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-191">Шасси расширения шины.</span><span class="sxs-lookup"><span data-stu-id="9a969-191">Bus-expansion chassis.</span></span>

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="9a969-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Периферийный корпус** (21)</span><span class="sxs-lookup"><span data-stu-id="9a969-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripheral Chassis** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-193">Периферийный корпус.</span><span class="sxs-lookup"><span data-stu-id="9a969-193">Peripheral chassis.</span></span>

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="9a969-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Корпус для хранения данных** (22)</span><span class="sxs-lookup"><span data-stu-id="9a969-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage Chassis** (22)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-195">Корпус хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a969-195">Storage chassis.</span></span>

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="9a969-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Корпус для монтажа в стойку** (23)</span><span class="sxs-lookup"><span data-stu-id="9a969-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-197">Корпус для монтажа в стойку.</span><span class="sxs-lookup"><span data-stu-id="9a969-197">Rack-mount chassis.</span></span>

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="9a969-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Компьютер с запечатанным корпусом** (24)</span><span class="sxs-lookup"><span data-stu-id="9a969-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case PC** (24)</span></span>


</dt> <dd>

<span data-ttu-id="9a969-199">Компьютер с запечатанным корпусом.</span><span class="sxs-lookup"><span data-stu-id="9a969-199">Sealed-case computer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a969-200">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9a969-200">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-203">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a969-203">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-204">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9a969-204">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9a969-205">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="9a969-205">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9a969-206">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-207">**куррентрекуиредорпродуцед**</span><span class="sxs-lookup"><span data-stu-id="9a969-207">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-208">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="9a969-208">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-210">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("ампер на 120 вольт")</span><span class="sxs-lookup"><span data-stu-id="9a969-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-211">В настоящее время требуется для корпуса с частотой 120 вольт.</span><span class="sxs-lookup"><span data-stu-id="9a969-211">Currently required by the chassis at 120 volts.</span></span> <span data-ttu-id="9a969-212">Если питание обеспечивается шасси (как в случае с ИБП), это свойство может указывать на ампераже, полученное в виде отрицательного числа.</span><span class="sxs-lookup"><span data-stu-id="9a969-212">If power is provided by the chassis (as in the case of a UPS), this property can indicate the amperage produced, as a negative number.</span></span>

</dd> <dt>

<span data-ttu-id="9a969-213">**Depth**</span><span class="sxs-lookup"><span data-stu-id="9a969-213">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-214">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a969-214">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-216">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="9a969-216">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-217">Глубина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="9a969-217">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="9a969-218">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-218">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-219">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9a969-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-222">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="9a969-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-223">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9a969-223">A textual description of the object.</span></span>

<span data-ttu-id="9a969-224">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-225">**хеатженератион**</span><span class="sxs-lookup"><span data-stu-id="9a969-225">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-226">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9a969-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-228">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("БТУ в час")</span><span class="sxs-lookup"><span data-stu-id="9a969-228">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-229">Объем тепла, создаваемый шасси в БТУ/час.</span><span class="sxs-lookup"><span data-stu-id="9a969-229">Amount of heat generated by the chassis in Btu/hour.</span></span>

</dd> <dt>

<span data-ttu-id="9a969-230">**Height**</span><span class="sxs-lookup"><span data-stu-id="9a969-230">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-231">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a969-231">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-233">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="9a969-233">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-234">Высота физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="9a969-234">Height of the physical package, in inches.</span></span>

<span data-ttu-id="9a969-235">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-235">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-236">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="9a969-236">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-237">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a969-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-239">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="9a969-239">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="9a969-240">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="9a969-240">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="9a969-241">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="9a969-241">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="9a969-242">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="9a969-242">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="9a969-243">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-243">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-244">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9a969-244">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-245">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9a969-245">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-247">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="9a969-247">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-248">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="9a969-248">Indicates when the object was installed.</span></span> <span data-ttu-id="9a969-249">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="9a969-249">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9a969-250">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-250">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-251">**локкпресент**</span><span class="sxs-lookup"><span data-stu-id="9a969-251">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-252">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a969-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-254">Если **значение равно true**, кадр защищен с блокировкой.</span><span class="sxs-lookup"><span data-stu-id="9a969-254">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="9a969-255">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-255">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-256">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="9a969-256">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-259">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a969-259">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-260">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="9a969-260">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="9a969-261">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-261">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="9a969-262">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-263">**Модель**</span><span class="sxs-lookup"><span data-stu-id="9a969-263">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-266">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a969-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-267">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="9a969-267">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="9a969-268">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-269">**Name**</span><span class="sxs-lookup"><span data-stu-id="9a969-269">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-272">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="9a969-272">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-273">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="9a969-273">Label by which the object is known.</span></span> <span data-ttu-id="9a969-274">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="9a969-274">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9a969-275">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-276">**нумберофповеркордс**</span><span class="sxs-lookup"><span data-stu-id="9a969-276">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-277">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9a969-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-279">Количество кабелей питания, которые должны быть подключены к корпусу, чтобы все компоненты могли работать.</span><span class="sxs-lookup"><span data-stu-id="9a969-279">Number of power cords that must be connected to the chassis so that all of the components can operate.</span></span>

</dd> <dt>

<span data-ttu-id="9a969-280">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9a969-280">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-283">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="9a969-283">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="9a969-284">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="9a969-284">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="9a969-285">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="9a969-285">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="9a969-286">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-287">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="9a969-287">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-290">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a969-290">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-291">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="9a969-291">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="9a969-292">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-293">**повередон**</span><span class="sxs-lookup"><span data-stu-id="9a969-293">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-294">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a969-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-296">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="9a969-296">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="9a969-297">В противном случае в данный момент он отключен.</span><span class="sxs-lookup"><span data-stu-id="9a969-297">Otherwise, it is currently off.</span></span>

<span data-ttu-id="9a969-298">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-299">**Службе**</span><span class="sxs-lookup"><span data-stu-id="9a969-299">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-300">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a969-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-302">Если **значение — true**, пакет предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="9a969-302">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="9a969-303">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="9a969-303">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="9a969-304">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="9a969-304">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="9a969-305">Например, обновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="9a969-305">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="9a969-306">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-306">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-307">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="9a969-307">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-308">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a969-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-310">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="9a969-310">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="9a969-311">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="9a969-311">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="9a969-312">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="9a969-312">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="9a969-313">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="9a969-313">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="9a969-314">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-314">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-315">**секуритибреач**</span><span class="sxs-lookup"><span data-stu-id="9a969-315">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-316">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9a969-316">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-318">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Глобальный контейнер DMTF \| 002,12 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Бреачдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="9a969-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-319">Указывает, была ли попытка физического нарушения кадра неудачной, неуспешной или попыток выполнить ее успешно.</span><span class="sxs-lookup"><span data-stu-id="9a969-319">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<span data-ttu-id="9a969-320">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-320">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9a969-321">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9a969-321">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a969-322">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="9a969-322">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="9a969-323">**Нет нарушений** (3)</span><span class="sxs-lookup"><span data-stu-id="9a969-323">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="9a969-324">**Попытки нарушения** (4)</span><span class="sxs-lookup"><span data-stu-id="9a969-324">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="9a969-325">**Успешное нарушение** (5)</span><span class="sxs-lookup"><span data-stu-id="9a969-325">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a969-326">**Номер**</span><span class="sxs-lookup"><span data-stu-id="9a969-326">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-327">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-329">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a969-329">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-330">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="9a969-330">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="9a969-331">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-331">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-332">**сервицедескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9a969-332">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-333">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9a969-333">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9a969-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-335">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицефилософи**")</span><span class="sxs-lookup"><span data-stu-id="9a969-335">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-336">Строки произвольной формы, содержащие подробные пояснения для записей в массиве **сервицефилософи** .</span><span class="sxs-lookup"><span data-stu-id="9a969-336">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="9a969-337">Каждая запись этого массива связана с записью в массиве **сервицефилософи** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="9a969-337">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

<span data-ttu-id="9a969-338">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-338">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-339">**сервицефилософи**</span><span class="sxs-lookup"><span data-stu-id="9a969-339">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-340">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9a969-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9a969-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-342">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицедескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="9a969-342">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-343">Указывает, обслуживается ли кадр сверху, спереди, сзади или сбоку; и содержит ли он скользящие лотки или съемные части, а также указывает, является ли кадр перемещаемым (например, у вас есть).</span><span class="sxs-lookup"><span data-stu-id="9a969-343">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="9a969-344">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-344">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a969-345">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9a969-345">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9a969-346">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9a969-346">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="9a969-347">**Служба из верхнего уровня** (2)</span><span class="sxs-lookup"><span data-stu-id="9a969-347">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="9a969-348">**Служба с передней части** (3)</span><span class="sxs-lookup"><span data-stu-id="9a969-348">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="9a969-349">**Со стороны службы** (4)</span><span class="sxs-lookup"><span data-stu-id="9a969-349">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="9a969-350">**Служба со стороны** (5)</span><span class="sxs-lookup"><span data-stu-id="9a969-350">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="9a969-351">**Скользящие лотки** (6)</span><span class="sxs-lookup"><span data-stu-id="9a969-351">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="9a969-352">**Съемные стороны** (7)</span><span class="sxs-lookup"><span data-stu-id="9a969-352">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="9a969-353">**Перемещаемый** (8)</span><span class="sxs-lookup"><span data-stu-id="9a969-353">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a969-354">**SKU**</span><span class="sxs-lookup"><span data-stu-id="9a969-354">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-357">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a969-357">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-358">Номер единицы складского учета для этого физического элемента.</span><span class="sxs-lookup"><span data-stu-id="9a969-358">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="9a969-359">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-359">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-360">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9a969-360">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-363">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="9a969-363">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-364">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9a969-364">String that indicates the current status of the object.</span></span> <span data-ttu-id="9a969-365">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="9a969-365">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9a969-366">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="9a969-366">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9a969-367">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="9a969-367">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9a969-368">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="9a969-368">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9a969-369">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="9a969-369">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9a969-370">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="9a969-370">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9a969-371">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9a969-372">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="9a969-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9a969-373">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="9a969-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9a969-374">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="9a969-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9a969-375">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="9a969-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a969-376">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="9a969-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9a969-377">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="9a969-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9a969-378">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="9a969-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9a969-379">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="9a969-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9a969-380">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="9a969-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9a969-381">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="9a969-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9a969-382">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="9a969-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9a969-383">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="9a969-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9a969-384">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="9a969-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a969-385">**Тег**</span><span class="sxs-lookup"><span data-stu-id="9a969-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-386">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-388">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9a969-388">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-389">Однозначно идентифицирует физический элемент и служит ключом элемента.</span><span class="sxs-lookup"><span data-stu-id="9a969-389">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="9a969-390">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="9a969-390">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="9a969-391">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="9a969-391">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="9a969-392">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="9a969-392">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="9a969-393">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="9a969-393">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="9a969-394">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="9a969-394">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="9a969-395">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-395">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-396">**типедескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9a969-396">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-397">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9a969-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9a969-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-399">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ шасси CIM**".**Чассистипес**")</span><span class="sxs-lookup"><span data-stu-id="9a969-399">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-400">Массив строк произвольной формы, предоставляющий сведения о записях массива **чассистипес** .</span><span class="sxs-lookup"><span data-stu-id="9a969-400">Array of free-form strings that provides information about the **ChassisTypes** array entries.</span></span>

> [!Note]  
> <span data-ttu-id="9a969-401">Каждая запись массива связана с записью в свойстве **чассистипес** , которая находится в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="9a969-401">Each array entry is related to the entry in the **ChassisTypes** property, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="9a969-402">**Version**</span><span class="sxs-lookup"><span data-stu-id="9a969-402">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9a969-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-405">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a969-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a969-406">Указывает версию физического элемента.</span><span class="sxs-lookup"><span data-stu-id="9a969-406">Indicates the version of the physical element.</span></span>

<span data-ttu-id="9a969-407">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-407">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-408">**висиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="9a969-408">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-409">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9a969-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a969-411">Если **true**, оборудование включает видимый сигнал.</span><span class="sxs-lookup"><span data-stu-id="9a969-411">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="9a969-412">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-412">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-413">**Weight**</span><span class="sxs-lookup"><span data-stu-id="9a969-413">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-414">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a969-414">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-416">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="9a969-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-417">Вес физического пакета (в фунтах).</span><span class="sxs-lookup"><span data-stu-id="9a969-417">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="9a969-418">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-418">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a969-419">**Width**</span><span class="sxs-lookup"><span data-stu-id="9a969-419">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a969-420">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="9a969-420">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="9a969-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a969-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a969-422">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="9a969-422">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="9a969-423">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="9a969-423">Width of the physical package, in inches.</span></span>

<span data-ttu-id="9a969-424">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-424">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a969-425">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a969-425">Remarks</span></span>

<span data-ttu-id="9a969-426">Класс **\_ шасси CIM** является производным от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="9a969-426">The **CIM\_Chassis** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="9a969-427">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="9a969-427">WMI does not implement this class.</span></span> <span data-ttu-id="9a969-428">Дополнительные сведения о классах, производных от CIM, см. в разделе [Классы Win32](win32-provider.md). **\_**</span><span class="sxs-lookup"><span data-stu-id="9a969-428">For more information about classes derived from **CIM\_Chassis**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9a969-429">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9a969-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9a969-430">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9a969-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a969-431">Требования</span><span class="sxs-lookup"><span data-stu-id="9a969-431">Requirements</span></span>



| <span data-ttu-id="9a969-432">Требование</span><span class="sxs-lookup"><span data-stu-id="9a969-432">Requirement</span></span> | <span data-ttu-id="9a969-433">Значение</span><span class="sxs-lookup"><span data-stu-id="9a969-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a969-434">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a969-434">Minimum supported client</span></span><br/> | <span data-ttu-id="9a969-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a969-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a969-436">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a969-436">Minimum supported server</span></span><br/> | <span data-ttu-id="9a969-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a969-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a969-438">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9a969-438">Namespace</span></span><br/>                | <span data-ttu-id="9a969-439">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9a969-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a969-440">MOF</span><span class="sxs-lookup"><span data-stu-id="9a969-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a969-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a969-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a969-442">DLL</span><span class="sxs-lookup"><span data-stu-id="9a969-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a969-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a969-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a969-444">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a969-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a969-445">**\_ФИСИКАЛФРАМЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="9a969-445">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

