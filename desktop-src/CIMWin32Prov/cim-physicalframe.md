---
description: Класс CIM \_ фисикалфраме является родительским классом стойки, корпуса и других корпусов, так как они определены в классах расширения.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: Класс CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142349"
---
# <a name="cim_physicalframe-class"></a><span data-ttu-id="872a9-103">\_Класс CIM фисикалфраме</span><span class="sxs-lookup"><span data-stu-id="872a9-103">CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="872a9-104">Класс **CIM \_ фисикалфраме** является родительским классом стойки, корпуса и других корпусов, так как они определены в классах расширения.</span><span class="sxs-lookup"><span data-stu-id="872a9-104">The **CIM\_PhysicalFrame** class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="872a9-105">Такие свойства, как **висиблеаларм** и **аудиблеаларм**, и данные, связанные с нарушениями безопасности, включены в этот родительский класс.</span><span class="sxs-lookup"><span data-stu-id="872a9-105">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="872a9-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="872a9-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="872a9-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="872a9-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="872a9-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="872a9-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="872a9-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="872a9-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="872a9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="872a9-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
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
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="872a9-111">Члены</span><span class="sxs-lookup"><span data-stu-id="872a9-111">Members</span></span>

<span data-ttu-id="872a9-112">Класс **CIM \_ фисикалфраме** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="872a9-112">The **CIM\_PhysicalFrame** class has these types of members:</span></span>

-   [<span data-ttu-id="872a9-113">Методы</span><span class="sxs-lookup"><span data-stu-id="872a9-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="872a9-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="872a9-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="872a9-115">Методы</span><span class="sxs-lookup"><span data-stu-id="872a9-115">Methods</span></span>

<span data-ttu-id="872a9-116">Класс **CIM \_ фисикалфраме** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="872a9-116">The **CIM\_PhysicalFrame** class has these methods.</span></span>



| <span data-ttu-id="872a9-117">Метод</span><span class="sxs-lookup"><span data-stu-id="872a9-117">Method</span></span>                                                                 | <span data-ttu-id="872a9-118">Описание</span><span class="sxs-lookup"><span data-stu-id="872a9-118">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="872a9-119">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="872a9-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalframe.md) | <span data-ttu-id="872a9-120">Проверяет, может ли связанный физический элемент быть включен в физический пакет или вставлен в него.</span><span class="sxs-lookup"><span data-stu-id="872a9-120">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="872a9-121">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="872a9-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="872a9-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="872a9-122">Properties</span></span>

<span data-ttu-id="872a9-123">Класс **CIM \_ фисикалфраме** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="872a9-123">The **CIM\_PhysicalFrame** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="872a9-124">**аудиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="872a9-124">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-125">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872a9-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-127">Если **значение равно true**, кадр оснащен звуковым сигналом.</span><span class="sxs-lookup"><span data-stu-id="872a9-127">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="872a9-128">**бреачдескриптион**</span><span class="sxs-lookup"><span data-stu-id="872a9-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фисикалфраме**.**Секуритибреач**")</span><span class="sxs-lookup"><span data-stu-id="872a9-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-132">Произвольная строка, которая предоставляет дополнительные сведения, если свойство **секуритибреач** указывает на то, что произошло нарушение или какое-либо другое событие, связанное с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="872a9-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="872a9-133">**каблеманажементстратеги**</span><span class="sxs-lookup"><span data-stu-id="872a9-133">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-136">Произвольная строка, содержащая сведения о соединении различных кабелей и их объединении в пакеты.</span><span class="sxs-lookup"><span data-stu-id="872a9-136">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="872a9-137">Благодаря многим сетям, связанным с хранилищем и кабелям питания Управление кабелями может быть сложной и сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="872a9-137">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="872a9-138">Это строковое свойство содержит сведения, помогающие в сборке и службе фрейма.</span><span class="sxs-lookup"><span data-stu-id="872a9-138">This string property contains information to aid in assembly and service of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="872a9-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="872a9-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-142">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="872a9-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-143">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="872a9-143">Short textual description of the object.</span></span>

<span data-ttu-id="872a9-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="872a9-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-148">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="872a9-148">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-149">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="872a9-149">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="872a9-150">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="872a9-150">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="872a9-151">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-151">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-152">**Depth**</span><span class="sxs-lookup"><span data-stu-id="872a9-152">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-153">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="872a9-153">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-155">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="872a9-155">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-156">Глубина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="872a9-156">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="872a9-157">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-157">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-158">**Описание**</span><span class="sxs-lookup"><span data-stu-id="872a9-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-161">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="872a9-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-162">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="872a9-162">Textual description of the object.</span></span>

<span data-ttu-id="872a9-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-164">**Height**</span><span class="sxs-lookup"><span data-stu-id="872a9-164">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-165">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="872a9-165">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-167">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="872a9-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-168">Высота физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="872a9-168">Height of the physical package, in inches.</span></span>

<span data-ttu-id="872a9-169">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-169">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-170">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="872a9-170">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-171">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872a9-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-173">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="872a9-173">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="872a9-174">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="872a9-174">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="872a9-175">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="872a9-175">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="872a9-176">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="872a9-176">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="872a9-177">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-177">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-178">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="872a9-178">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-179">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="872a9-179">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-181">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="872a9-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-182">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="872a9-182">Date and time the object was installed.</span></span> <span data-ttu-id="872a9-183">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="872a9-183">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="872a9-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-185">**локкпресент**</span><span class="sxs-lookup"><span data-stu-id="872a9-185">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-186">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872a9-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-188">Если **значение равно true**, кадр защищен с блокировкой.</span><span class="sxs-lookup"><span data-stu-id="872a9-188">If **TRUE**, the frame is protected with a lock.</span></span>

</dd> <dt>

<span data-ttu-id="872a9-189">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="872a9-189">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-192">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="872a9-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-193">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="872a9-193">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="872a9-194">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-194">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="872a9-195">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-195">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-196">**Модель**</span><span class="sxs-lookup"><span data-stu-id="872a9-196">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-199">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="872a9-199">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-200">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="872a9-200">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="872a9-201">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-202">**Name**</span><span class="sxs-lookup"><span data-stu-id="872a9-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-205">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="872a9-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-206">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="872a9-206">Label by which the object is known.</span></span> <span data-ttu-id="872a9-207">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="872a9-207">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="872a9-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-209">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="872a9-209">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-212">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="872a9-212">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="872a9-213">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="872a9-213">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="872a9-214">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="872a9-214">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="872a9-215">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-216">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="872a9-216">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-219">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="872a9-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-220">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="872a9-220">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="872a9-221">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-222">**повередон**</span><span class="sxs-lookup"><span data-stu-id="872a9-222">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-223">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872a9-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-225">Если **значение равно true**, физический элемент включен; в противном случае в данный момент он отключен.</span><span class="sxs-lookup"><span data-stu-id="872a9-225">If **TRUE**, the physical element is powered on; otherwise, it is currently off.</span></span>

<span data-ttu-id="872a9-226">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-226">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-227">**Службе**</span><span class="sxs-lookup"><span data-stu-id="872a9-227">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-228">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872a9-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-230">Если **значение — true**, этот элемент предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="872a9-230">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="872a9-231">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="872a9-231">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="872a9-232">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="872a9-232">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="872a9-233">Например, обновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="872a9-233">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="872a9-234">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-234">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-235">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="872a9-235">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-236">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872a9-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-238">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="872a9-238">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="872a9-239">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="872a9-239">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="872a9-240">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="872a9-240">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="872a9-241">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="872a9-241">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="872a9-242">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-242">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-243">**секуритибреач**</span><span class="sxs-lookup"><span data-stu-id="872a9-243">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-244">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872a9-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-246">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Глобальный контейнер DMTF \| 002,12 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фисикалфраме**.**Бреачдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="872a9-246">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-247">Указывает, была ли попытка физического нарушения кадра неудачной, неуспешной или попыток выполнить ее успешно.</span><span class="sxs-lookup"><span data-stu-id="872a9-247">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="872a9-248">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="872a9-248">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="872a9-249">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="872a9-249">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="872a9-250">**Нет нарушений** (3)</span><span class="sxs-lookup"><span data-stu-id="872a9-250">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="872a9-251">**Попытки нарушения** (4)</span><span class="sxs-lookup"><span data-stu-id="872a9-251">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="872a9-252">**Успешное нарушение** (5)</span><span class="sxs-lookup"><span data-stu-id="872a9-252">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="872a9-253">**Номер**</span><span class="sxs-lookup"><span data-stu-id="872a9-253">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-254">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-256">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="872a9-256">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-257">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="872a9-257">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="872a9-258">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-258">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-259">**сервицедескриптионс**</span><span class="sxs-lookup"><span data-stu-id="872a9-259">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-260">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="872a9-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="872a9-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-262">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фисикалфраме**.**Сервицефилософи**")</span><span class="sxs-lookup"><span data-stu-id="872a9-262">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-263">Строки произвольной формы, содержащие подробные пояснения для записей в массиве **сервицефилософи** .</span><span class="sxs-lookup"><span data-stu-id="872a9-263">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="872a9-264">Каждая запись этого массива связана с записью в массиве **сервицефилософи** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="872a9-264">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="872a9-265">**сервицефилософи**</span><span class="sxs-lookup"><span data-stu-id="872a9-265">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-266">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="872a9-266">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="872a9-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-268">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ фисикалфраме**.**Сервицедескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="872a9-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-269">Указывает, обслуживается ли кадр сверху, спереди, сзади или сбоку; и содержит ли он скользящие лотки или съемные части, а также указывает, является ли кадр перемещаемым (например, у вас есть).</span><span class="sxs-lookup"><span data-stu-id="872a9-269">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="872a9-270">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="872a9-270">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="872a9-271">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="872a9-271">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="872a9-272">**Служба из верхнего уровня** (2)</span><span class="sxs-lookup"><span data-stu-id="872a9-272">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="872a9-273">**Служба с передней части** (3)</span><span class="sxs-lookup"><span data-stu-id="872a9-273">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="872a9-274">**Со стороны службы** (4)</span><span class="sxs-lookup"><span data-stu-id="872a9-274">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="872a9-275">**Служба со стороны** (5)</span><span class="sxs-lookup"><span data-stu-id="872a9-275">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="872a9-276">**Скользящие лотки** (6)</span><span class="sxs-lookup"><span data-stu-id="872a9-276">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="872a9-277">**Съемные стороны** (7)</span><span class="sxs-lookup"><span data-stu-id="872a9-277">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="872a9-278">**Перемещаемый** (8)</span><span class="sxs-lookup"><span data-stu-id="872a9-278">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="872a9-279">**SKU**</span><span class="sxs-lookup"><span data-stu-id="872a9-279">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-282">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="872a9-282">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-283">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="872a9-283">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="872a9-284">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-284">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-285">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="872a9-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-288">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="872a9-288">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-289">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="872a9-289">Current status of the object.</span></span>

<span data-ttu-id="872a9-290">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="872a9-291">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="872a9-291">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="872a9-292">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="872a9-292">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="872a9-293">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="872a9-293">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="872a9-294">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="872a9-294">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="872a9-295">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="872a9-295">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="872a9-296">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="872a9-296">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="872a9-297">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="872a9-297">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="872a9-298">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="872a9-298">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="872a9-299">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="872a9-299">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="872a9-300">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="872a9-300">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="872a9-301">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="872a9-301">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="872a9-302">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="872a9-302">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="872a9-303">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="872a9-303">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="872a9-304">**Тег**</span><span class="sxs-lookup"><span data-stu-id="872a9-304">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-307">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="872a9-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-308">Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента.</span><span class="sxs-lookup"><span data-stu-id="872a9-308">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="872a9-309">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="872a9-309">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="872a9-310">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="872a9-310">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="872a9-311">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="872a9-311">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="872a9-312">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="872a9-312">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="872a9-313">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="872a9-313">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="872a9-314">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-315">**Version**</span><span class="sxs-lookup"><span data-stu-id="872a9-315">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872a9-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-318">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="872a9-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="872a9-319">Строка, указывающая версию физического элемента.</span><span class="sxs-lookup"><span data-stu-id="872a9-319">String that indicates the version of the physical element.</span></span>

<span data-ttu-id="872a9-320">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-321">**висиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="872a9-321">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-322">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872a9-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872a9-324">Если **true**, оборудование включает видимый сигнал.</span><span class="sxs-lookup"><span data-stu-id="872a9-324">If **TRUE**, the equipment includes a visible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="872a9-325">**Weight**</span><span class="sxs-lookup"><span data-stu-id="872a9-325">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-326">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="872a9-326">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-328">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="872a9-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-329">Вес физического пакета (в фунтах).</span><span class="sxs-lookup"><span data-stu-id="872a9-329">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="872a9-330">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-330">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="872a9-331">**Width**</span><span class="sxs-lookup"><span data-stu-id="872a9-331">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872a9-332">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="872a9-332">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="872a9-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872a9-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872a9-334">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="872a9-334">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="872a9-335">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="872a9-335">Width of the physical package, in inches.</span></span>

<span data-ttu-id="872a9-336">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-336">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="872a9-337">Комментарии</span><span class="sxs-lookup"><span data-stu-id="872a9-337">Remarks</span></span>

<span data-ttu-id="872a9-338">Класс **CIM \_ фисикалфраме** является производным от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-338">The **CIM\_PhysicalFrame** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="872a9-339">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="872a9-339">WMI does not implement this class.</span></span> <span data-ttu-id="872a9-340">Классы WMI, производные от **CIM \_ фисикалфраме**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="872a9-340">For WMI classes derived from **CIM\_PhysicalFrame**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="872a9-341">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="872a9-341">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="872a9-342">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="872a9-342">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="872a9-343">Требования</span><span class="sxs-lookup"><span data-stu-id="872a9-343">Requirements</span></span>



| <span data-ttu-id="872a9-344">Требование</span><span class="sxs-lookup"><span data-stu-id="872a9-344">Requirement</span></span> | <span data-ttu-id="872a9-345">Значение</span><span class="sxs-lookup"><span data-stu-id="872a9-345">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="872a9-346">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="872a9-346">Minimum supported client</span></span><br/> | <span data-ttu-id="872a9-347">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="872a9-347">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="872a9-348">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="872a9-348">Minimum supported server</span></span><br/> | <span data-ttu-id="872a9-349">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="872a9-349">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="872a9-350">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="872a9-350">Namespace</span></span><br/>                | <span data-ttu-id="872a9-351">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="872a9-351">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="872a9-352">MOF</span><span class="sxs-lookup"><span data-stu-id="872a9-352">MOF</span></span><br/>                      | <dl> <span data-ttu-id="872a9-353"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="872a9-353"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="872a9-354">DLL</span><span class="sxs-lookup"><span data-stu-id="872a9-354">DLL</span></span><br/>                      | <dl> <span data-ttu-id="872a9-355"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872a9-355"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="872a9-356">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="872a9-356">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872a9-357">**\_ФИСИКАЛПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="872a9-357">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

