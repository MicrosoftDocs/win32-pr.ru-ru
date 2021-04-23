---
description: '\_Класс стойки CIM представляет стойку (физическую рамку или корпус), в котором хранятся шасси. Как правило, стойка представляет корпус; все действующие компоненты упаковываются в корпус.'
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: Класс CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807325"
---
# <a name="cim_rack-class"></a><span data-ttu-id="ca2e6-104">\_Класс стойки CIM</span><span class="sxs-lookup"><span data-stu-id="ca2e6-104">CIM\_Rack class</span></span>

<span data-ttu-id="ca2e6-105">Класс **\_ стойки CIM** представляет стойку (физическую рамку или корпус), в котором хранятся шасси.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-105">The **CIM\_Rack** class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="ca2e6-106">Как правило, стойка представляет корпус; все действующие компоненты упаковываются в корпус.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-106">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca2e6-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ca2e6-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ca2e6-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ca2e6-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2e6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca2e6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="ca2e6-112">Члены</span><span class="sxs-lookup"><span data-stu-id="ca2e6-112">Members</span></span>

<span data-ttu-id="ca2e6-113">Класс **\_ стойки CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ca2e6-113">The **CIM\_Rack** class has these types of members:</span></span>

-   [<span data-ttu-id="ca2e6-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ca2e6-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca2e6-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca2e6-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca2e6-116">Методы</span><span class="sxs-lookup"><span data-stu-id="ca2e6-116">Methods</span></span>

<span data-ttu-id="ca2e6-117">Класс **\_ стойки CIM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-117">The **CIM\_Rack** class has these methods.</span></span>



| <span data-ttu-id="ca2e6-118">Метод</span><span class="sxs-lookup"><span data-stu-id="ca2e6-118">Method</span></span>                                                        | <span data-ttu-id="ca2e6-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ca2e6-119">Description</span></span>                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca2e6-120">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-rack.md) | <span data-ttu-id="ca2e6-121">Проверяет, может ли связанный физический элемент быть включен в физический пакет или вставлен в него.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="ca2e6-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ca2e6-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca2e6-123">Properties</span></span>

<span data-ttu-id="ca2e6-124">Класс **\_ стойки CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-124">The **CIM\_Rack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca2e6-125">**аудиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-125">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-128">Если **значение равно true**, кадр оснащен звуковым сигналом.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-128">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="ca2e6-129">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-129">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-130">**бреачдескриптион**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-130">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-133">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Секуритибреач**")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-133">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-134">Произвольная строка, которая предоставляет сведения, если свойство **секуритибреач** указывает, что произошло нарушение или какое-либо другое событие, связанное с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-134">Free-form string that provides information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="ca2e6-135">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-135">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-136">**каблеманажементстратеги**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-136">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-139">Произвольная строка, содержащая сведения о соединении различных кабелей и их объединении в пакеты.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-139">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="ca2e6-140">Благодаря многим сетям, связанным с хранилищем и кабелям питания Управление кабелями может быть сложной и сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-140">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="ca2e6-141">Это строковое свойство содержит сведения, помогающие в сборке и службе фрейма.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-141">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="ca2e6-142">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-142">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-143">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-146">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-147">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-147">Short textual description of the object.</span></span>

<span data-ttu-id="ca2e6-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-149">**каунтридесигнатион**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-149">**CountryDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-152">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ стойка CIM**.**Типеофракк**")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**TypeOfRack**")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-153">Страна или регион, для которых предназначена стойка.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-153">Country or region for which the rack is designed.</span></span> <span data-ttu-id="ca2e6-154">Строки кода страны или региона определяются в стандарте ISO/IEC 3166.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-154">Country or region code strings are as defined by ISO/IEC 3166.</span></span> <span data-ttu-id="ca2e6-155">Тип стойки указывается в свойстве **типеофракк** .</span><span class="sxs-lookup"><span data-stu-id="ca2e6-155">The rack type is specified in the **TypeOfRack** property.</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-159">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-159">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-160">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-160">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ca2e6-161">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-161">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ca2e6-162">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-162">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-163">**Depth**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-163">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-164">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-164">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-166">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-166">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-167">Глубина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-167">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="ca2e6-168">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-169">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-172">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-172">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-173">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-173">Textual description of the object.</span></span>

<span data-ttu-id="ca2e6-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-175">**Height**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-175">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-176">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-176">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-178">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-178">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-179">Высота физического пакета с использованием единицы измерения "U".</span><span class="sxs-lookup"><span data-stu-id="ca2e6-179">Height of the physical package, using the "U" unit of measure.</span></span> <span data-ttu-id="ca2e6-180">"U" — это стандартная единица измерения для высоты стойки или компонента, монтируемого в стойку, которая равна 1,75 дюйма или 4,445 сантиметров.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-180">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

<span data-ttu-id="ca2e6-181">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-181">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-182">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-182">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-183">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-185">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-185">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="ca2e6-186">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-186">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="ca2e6-187">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-187">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="ca2e6-188">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-188">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="ca2e6-189">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-189">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-190">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-190">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-191">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-193">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-193">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-194">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-194">Date and time the object was installed.</span></span> <span data-ttu-id="ca2e6-195">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-195">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ca2e6-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-197">**локкпресент**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-197">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-198">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-200">Если **значение равно true**, кадр защищен с блокировкой.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-200">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="ca2e6-201">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-201">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-202">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-202">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-205">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-206">Имя Организации, которая создала физический элемент.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-206">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="ca2e6-207">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-207">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="ca2e6-208">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-208">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-209">**Модель**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-209">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-212">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-213">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-213">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="ca2e6-214">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-214">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-215">**Name**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-218">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-218">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-219">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-219">Label by which the object is known.</span></span> <span data-ttu-id="ca2e6-220">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-220">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ca2e6-221">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-222">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-222">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-225">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для обнаружения физического элемента.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-225">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="ca2e6-226">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-226">One example is bar-code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="ca2e6-227">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="ca2e6-228">Если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="ca2e6-228">If only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="ca2e6-229">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-229">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-232">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-233">Номер детали, назначенный Организацией, которая создала или изготовлена физический элемент.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-233">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="ca2e6-234">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-234">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-235">**повередон**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-235">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-236">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-238">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-238">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="ca2e6-239">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-240">**Службе**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-240">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-241">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-243">Если **значение — true**, этот элемент предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-243">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="ca2e6-244">Пакет считается съемным, даже если для его удаления требуется выключить питание.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-244">A package is considered removable even if the power must be "off" to perform the removal.</span></span> <span data-ttu-id="ca2e6-245">Если мощность может быть "on", а пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-245">If the power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="ca2e6-246">Например, дополнительный аккумулятор ноутбука является съемным, как и дисковый пакет, вставленный с помощью соединителей SCA. Однако последняя может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-246">For example, an extra battery in a laptop is removable, as is a disk-drive package inserted using SCA connectors; however, the latter can be hot-swapped.</span></span> <span data-ttu-id="ca2e6-247">Дисплей ноутбука не является съемным и не является избыточным источником питания.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-247">A laptop's display is not removable, nor is a non-redundant power supply.</span></span> <span data-ttu-id="ca2e6-248">Удаление этих компонентов влияет на функцию общей упаковки или невозможно из-за тесной интеграции пакета.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-248">Removing these components impacts the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="ca2e6-249">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-249">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-250">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-250">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-251">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-253">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-253">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="ca2e6-254">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-254">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="ca2e6-255">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-255">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="ca2e6-256">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-256">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="ca2e6-257">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-257">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-258">**секуритибреач**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-258">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-259">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-261">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Глобальный контейнер DMTF \| 002,12 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Бреачдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-261">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-262">Указывает, была ли попытка физического нарушения кадра неудачной, неуспешной или попыток выполнить ее успешно.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-262">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span> <span data-ttu-id="ca2e6-263">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-263">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca2e6-264">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-264">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca2e6-265">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-265">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="ca2e6-266">**Нет нарушений** (3)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-266">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="ca2e6-267">**Попытки нарушения** (4)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-267">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="ca2e6-268">**Успешное нарушение** (5)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-268">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca2e6-269">**Номер**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-269">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-272">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-272">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-273">Номер, выделенный изготовителем, используемый для распознавания стойки.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-273">Manufacturer-allocated number used to identify the rack.</span></span>

<span data-ttu-id="ca2e6-274">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-274">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-275">**сервицедескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-275">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-276">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-276">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-278">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицефилософи**")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-278">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-279">Строки произвольной формы, содержащие подробные пояснения для записей в массиве **сервицефилософи** .</span><span class="sxs-lookup"><span data-stu-id="ca2e6-279">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="ca2e6-280">Обратите внимание, что каждая запись массива связана с записью в **сервицефилософи** , расположенной в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-280">Note, each entry of the array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="ca2e6-281">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-281">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-282">**сервицефилософи**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-282">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-283">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ca2e6-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-285">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицедескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-285">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-286">Указывает, обслуживается ли кадр сверху, спереди, сзади или сбоку; и содержит ли он скользящие лотки или съемные части, а также указывает, является ли кадр перемещаемым (например, у вас есть).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-286">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="ca2e6-287">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-287">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca2e6-288">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-288">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca2e6-289">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-289">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="ca2e6-290">**Служба из верхнего уровня** (2)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-290">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="ca2e6-291">**Служба с передней части** (3)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-291">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="ca2e6-292">**Со стороны службы** (4)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-292">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="ca2e6-293">**Служба со стороны** (5)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-293">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="ca2e6-294">**Скользящие лотки** (6)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-294">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="ca2e6-295">**Съемные стороны** (7)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-295">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="ca2e6-296">**Перемещаемый** (8)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-296">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca2e6-297">**SKU**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-297">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-300">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-300">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-301">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-301">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="ca2e6-302">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-303">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-303">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-306">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-307">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-307">Current status of the object.</span></span> <span data-ttu-id="ca2e6-308">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ca2e6-309">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="ca2e6-309">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ca2e6-310">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-310">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ca2e6-311">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-311">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ca2e6-312">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-312">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca2e6-313">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-313">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ca2e6-314">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-314">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ca2e6-315">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-315">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ca2e6-316">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-316">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ca2e6-317">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-317">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ca2e6-318">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-318">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ca2e6-319">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-319">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ca2e6-320">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-320">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ca2e6-321">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-321">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca2e6-322">**Тег**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-322">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-325">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-325">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-326">Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-326">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="ca2e6-327">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-327">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="ca2e6-328">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-328">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="ca2e6-329">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-329">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="ca2e6-330">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-330">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="ca2e6-331">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-331">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="ca2e6-332">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-332">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-333">**типеофракк**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-333">**TypeOfRack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-334">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-336">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ стойка CIM**.**Каунтридесигнатион**")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-336">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**CountryDesignation**")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-337">Тип стойки.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-337">Type of rack.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca2e6-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span data-ttu-id="ca2e6-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Стандартный 19 дюймов** (1)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Inch** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ca2e6-340">Стандартный 19-дюймовый</span><span class="sxs-lookup"><span data-stu-id="ca2e6-340">Standard 19-inch</span></span>

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span data-ttu-id="ca2e6-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span data-ttu-id="ca2e6-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Полка оборудования** (3)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Equipment Shelf** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span data-ttu-id="ca2e6-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Не стандартный** (4)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non-Standard** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca2e6-344">**Version**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-344">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-347">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ca2e6-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-348">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-348">Version of the physical element.</span></span>

<span data-ttu-id="ca2e6-349">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-349">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-350">**висиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-350">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-351">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-351">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-353">Если **true**, оборудование включает видимый сигнал.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-353">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="ca2e6-354">Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-354">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-355">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-355">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-356">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-356">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-358">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-358">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-359">Вес физического пакета (в фунтах).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-359">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="ca2e6-360">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-360">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca2e6-361">**Width**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-361">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2e6-362">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-362">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca2e6-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2e6-364">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="ca2e6-364">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="ca2e6-365">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-365">Width of the physical package, in inches.</span></span>

<span data-ttu-id="ca2e6-366">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-366">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca2e6-367">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca2e6-367">Remarks</span></span>

<span data-ttu-id="ca2e6-368">Класс **\_ стойки CIM** является производным от [**CIM \_ фисикалфраме**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="ca2e6-368">The **CIM\_Rack** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="ca2e6-369">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-369">WMI does not implement this class.</span></span>

<span data-ttu-id="ca2e6-370">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-370">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ca2e6-371">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ca2e6-371">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2e6-372">Требования</span><span class="sxs-lookup"><span data-stu-id="ca2e6-372">Requirements</span></span>



| <span data-ttu-id="ca2e6-373">Требование</span><span class="sxs-lookup"><span data-stu-id="ca2e6-373">Requirement</span></span> | <span data-ttu-id="ca2e6-374">Значение</span><span class="sxs-lookup"><span data-stu-id="ca2e6-374">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2e6-375">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca2e6-375">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2e6-376">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca2e6-376">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca2e6-377">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca2e6-377">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2e6-378">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca2e6-378">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca2e6-379">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca2e6-379">Namespace</span></span><br/>                | <span data-ttu-id="ca2e6-380">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ca2e6-380">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca2e6-381">MOF</span><span class="sxs-lookup"><span data-stu-id="ca2e6-381">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca2e6-382"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e6-382"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca2e6-383">DLL</span><span class="sxs-lookup"><span data-stu-id="ca2e6-383">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca2e6-384"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e6-384"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2e6-385">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca2e6-385">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2e6-386">**\_ФИСИКАЛФРАМЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ca2e6-386">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

