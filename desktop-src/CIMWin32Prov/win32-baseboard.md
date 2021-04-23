---
description: Представляет основную плату, которая также называется материнской платой или системной платой.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Класс Win32_BaseBoard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072532"
---
# <a name="win32_baseboard-class"></a><span data-ttu-id="1fd4e-103">\_Класс основной платы Win32</span><span class="sxs-lookup"><span data-stu-id="1fd4e-103">Win32\_BaseBoard class</span></span>

<span data-ttu-id="1fd4e-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ основной платы Win32** представляет основную плату, которая также называется материнской платой или системной платой.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-104">The **Win32\_BaseBoard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a baseboard, which is also known as a motherboard or system board.</span></span>

<span data-ttu-id="1fd4e-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd4e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fd4e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="1fd4e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1fd4e-107">Members</span></span>

<span data-ttu-id="1fd4e-108">Класс **\_ основной платы Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1fd4e-108">The **Win32\_BaseBoard** class has these types of members:</span></span>

-   [<span data-ttu-id="1fd4e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="1fd4e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1fd4e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fd4e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1fd4e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1fd4e-111">Methods</span></span>

<span data-ttu-id="1fd4e-112">Класс **\_ основной платы Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-112">The **Win32\_BaseBoard** class has these methods.</span></span>



| <span data-ttu-id="1fd4e-113">Метод</span><span class="sxs-lookup"><span data-stu-id="1fd4e-113">Method</span></span>           | <span data-ttu-id="1fd4e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1fd4e-114">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="1fd4e-115">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-115">**IsCompatible**</span></span> | <span data-ttu-id="1fd4e-116">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-116">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1fd4e-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="1fd4e-117">Properties</span></span>

<span data-ttu-id="1fd4e-118">Класс **\_ основной платы Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-118">The **Win32\_BaseBoard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fd4e-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-123">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-123">Short description of the object a one-line string.</span></span>

<span data-ttu-id="1fd4e-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-125">**конфигоптионс**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-125">**ConfigOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-126">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 12 \| строки параметров конфигурации")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 12\|Configuration Options Strings")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-129">Массив, представляющий конфигурацию переключателей и коммутаторов, расположенных на основной плате.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-129">Array that represents the configuration of the jumpers and switches located on the baseboard.</span></span>

<span data-ttu-id="1fd4e-130">Пример: "JP2: размер кэша 1-2 — 256 КБ, размер кэша 2-3 — 512 КБ, SW1-1: закрыть для отключения на платном видео"</span><span class="sxs-lookup"><span data-stu-id="1fd4e-130">Example: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-134">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-135">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-135">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1fd4e-136">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-136">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="1fd4e-137">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-138">**Depth**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-139">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-141">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-142">Глубина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-142">Depth of the physical package in inches.</span></span>

<span data-ttu-id="1fd4e-143">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-143">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-147">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-148">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-148">Description of the object.</span></span>

<span data-ttu-id="1fd4e-149">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-150">**Height**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-150">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-151">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-151">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-153">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-154">Высота физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-154">Height of the physical package in inches.</span></span>

<span data-ttu-id="1fd4e-155">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-155">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-156">**хостингбоард**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-156">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-157">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-159">Если **значение равно true**, плата является материнской платой или основной платой в корпусе.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-159">If **TRUE**, the card is a motherboard, or a baseboard in a chassis.</span></span>

<span data-ttu-id="1fd4e-160">Это свойство наследуется [**от \_ карты CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-160">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-161">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-161">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-162">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-164">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-164">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="1fd4e-165">Физический пакет может быть горячим заменой, если можно заменить элемент физически отличающимся, но эквивалентным элементом, пока содержащий его пакет применяет к нему питание, когда он включен.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-165">A physical package can be hot-swapped if it is possible to replace the element with a physically different but equivalent element while the containing package has power applied to it that is, while it is ON.</span></span> <span data-ttu-id="1fd4e-166">Например, пакет диска, вставленный с помощью соединителей SCA, является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-166">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="1fd4e-167">Все пакеты, которые могут быть горячей заменой, по сути своей являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-167">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="1fd4e-168">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-169">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-169">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-170">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-170">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-172">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-173">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-173">Date and time the object was installed.</span></span> <span data-ttu-id="1fd4e-174">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-174">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1fd4e-175">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-175">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-176">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-176">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-179">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-180">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-180">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="1fd4e-181">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-181">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-182">**Модель**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-182">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-185">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-186">Имя, по которому известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-186">Name by which the physical element is known.</span></span>

<span data-ttu-id="1fd4e-187">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-187">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-188">**Name**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-191">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-191">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-192">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-192">Label by which the object is known.</span></span> <span data-ttu-id="1fd4e-193">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-193">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1fd4e-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-195">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-195">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-198">Захватывает дополнительные данные, помимо сведений о тегах актива, которые можно использовать для обнаружения физического элемента.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-198">Captures additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="1fd4e-199">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-199">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="1fd4e-200">Обратите внимание, что если только данные штрих-кода доступны и уникальны или могут использоваться в качестве ключа элемента, значение свойства будет **равно NULL** , а данные штрих-кода будут использоваться в качестве ключа класса в свойстве Tag.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-200">Note that if only bar code data is available and unique or able to be used as an element key, the property value would be **NULL** and the bar code data would be used as the class key, in the tag property.</span></span>

<span data-ttu-id="1fd4e-201">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-202">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-202">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-205">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-206">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-206">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="1fd4e-207">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-207">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-208">**повередон**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-208">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-209">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-211">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-211">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="1fd4e-212">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-213">**Продукт**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-213">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-216">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 2 \| продукта")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 2\|Product")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-217">Номер части основной платы, определяемый производителем.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-217">Baseboard part number defined by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-218">**Службе**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-221">**Значение true**, если пакет является съемным.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-221">If **TRUE**, a package is removable.</span></span> <span data-ttu-id="1fd4e-222">Физический пакет является съемным, если он предназначен для извлечения и выхода из физического контейнера, в котором он обычно обнаруживается без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-222">A physical package is removable if it is designed to be taken in and out of the physical container in which it is normally found without impairing the function of the overall packaging.</span></span> <span data-ttu-id="1fd4e-223">Пакет по-прежнему может быть съемным, если необходимо отключить питание для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-223">A package can still be removable if the power must be OFF to perform the removal.</span></span> <span data-ttu-id="1fd4e-224">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-224">If the power can be ON and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="1fd4e-225">Например, дополнительный аккумулятор ноутбука является съемным, как и дисковый пакет, вставленный с помощью соединителей SCA.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-225">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="1fd4e-226">Однако последняя может также быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-226">However, the latter can also be hot-swapped.</span></span> <span data-ttu-id="1fd4e-227">Дисплей ноутбука не является съемным или не является избыточным источником питания.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-227">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="1fd4e-228">Удаление этих компонентов повлияет на функцию общей упаковки или невозможно из-за тесной интеграции пакета.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-228">Removing these components would impact the function of the overall packaging, or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="1fd4e-229">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-229">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-230">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-230">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-233">**Значение true**, если пакет является заменяемым.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-233">If **TRUE**, a package is replaceable.</span></span> <span data-ttu-id="1fd4e-234">Физический пакет может быть заменяемым, если можно заменить (FRU или обновить) элемент физически другой.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-234">A physical package is replaceable if it is possible to replace (FRU or upgrade) the element with a physically different one.</span></span> <span data-ttu-id="1fd4e-235">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-235">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="1fd4e-236">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-236">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="1fd4e-237">Еще один пример — это пакет источника питания, подключенный к скользящим шинам.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-237">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="1fd4e-238">Все съемные пакеты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-238">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="1fd4e-239">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-239">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-240">**рекуирементсдескриптион**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-240">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-243">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ карта CIM**](cim-card.md)".**СпеЦиалрекуирементс**")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-244">Произвольная строка, которая описывает способ физического уникальности этой карточки с других карточек.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-244">Free-form string that describes the way in which this card is physically unique from other cards.</span></span> <span data-ttu-id="1fd4e-245">Свойство имеет значение только в том случае, если соответствующее свойство логического свойства **спеЦиалрекуирементс** имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-245">The property only has meaning when the corresponding Boolean property **SpecialRequirements** is set to **TRUE**.</span></span>

<span data-ttu-id="1fd4e-246">Это свойство наследуется [**от \_ карты CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-246">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-247">**рекуиресдаугхтербоард**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-247">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-248">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-250">Если задано **значение true**, для правильной работы требуется по крайней мере одна даугхтербоард или вспомогательная карта.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-250">If **TRUE**, at least one daughterboard or auxiliary card is required to function properly.</span></span>

<span data-ttu-id="1fd4e-251">Это свойство наследуется [**от \_ карты CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-251">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-252">**Номер**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-252">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-255">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-256">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-256">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="1fd4e-257">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-258">**SKU**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-258">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-259">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-261">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-262">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-262">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="1fd4e-263">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-264">**слотлайаут**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-264">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-265">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-267">Произвольная строка, описывающая расположение слота, типичное использование, ограничения, отдельные интервалы между гнездами и другие сведения, относящиеся к слотам на карте.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-267">Free-form string that describes the slot position, typical usage, restrictions, individual slot spacing or any other pertinent information for the slots on a card.</span></span>

<span data-ttu-id="1fd4e-268">Это свойство наследуется [**от \_ карты CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-268">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-269">**спеЦиалрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-269">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-270">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-272">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ карта CIM**](cim-card.md)".**Рекуирементсдескриптион**")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-272">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-273">Если **значение — true**, эта карта физически уникальна по отношению к другим картам того же типа, поэтому для нее требуется специальный слот.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-273">If **TRUE**, this card is physically unique from other cards of the same type and therefore requires a special slot.</span></span> <span data-ttu-id="1fd4e-274">Например, для двойной широкой карты требуется два слота.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-274">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="1fd4e-275">Другим примером является то, что определенная карта может использоваться для одной и той же общей функции с другими картами, но для нее требуется специальный слот (например, очень длинный), тогда как другие карты можно разместить в любом доступном слоте.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-275">Another example is where a certain card may be used for the same general function as other cards but requires a special slot (for example, extra long), whereas the other cards can be placed in any available slot.</span></span> <span data-ttu-id="1fd4e-276">Если задано значение **true**, то соответствующее свойство, **рекуирементсдескриптион**, должно задавать природу уникальности или назначения карты.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-276">If set to **TRUE**, then the corresponding property, **RequirementsDescription**, should specify the nature of the uniqueness or purpose of the card.</span></span>

<span data-ttu-id="1fd4e-277">Это свойство наследуется [**от \_ карты CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-277">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-278">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-278">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-281">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-281">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-282">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-282">Current status of the object.</span></span> <span data-ttu-id="1fd4e-283">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-283">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1fd4e-284">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-284">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1fd4e-285">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="1fd4e-285">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1fd4e-286">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-286">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1fd4e-287">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-287">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1fd4e-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1fd4e-289">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="1fd4e-289">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1fd4e-290">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-290">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1fd4e-291">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-291">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1fd4e-292">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-292">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1fd4e-293">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-293">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1fd4e-294">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-294">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1fd4e-295">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-295">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1fd4e-296">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-296">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1fd4e-297">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-297">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1fd4e-298">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-298">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1fd4e-299">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-299">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1fd4e-300">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-300">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1fd4e-301">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-301">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1fd4e-302">**Тег**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-302">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-305">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("тег"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-305">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-306">Уникальный идентификатор основной платы системы.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-306">Unique identifier of the baseboard of the system.</span></span>

<span data-ttu-id="1fd4e-307">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-307">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="1fd4e-308">Пример: "Основная плата"</span><span class="sxs-lookup"><span data-stu-id="1fd4e-308">Example: "Base Board"</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-309">**Version**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-309">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-312">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1fd4e-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-313">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-313">Version of the physical element.</span></span>

<span data-ttu-id="1fd4e-314">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-315">**Weight**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-315">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-316">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-316">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-318">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-318">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-319">Вес физического пакета в фунтах.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-319">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="1fd4e-320">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-320">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1fd4e-321">**Width**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-321">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fd4e-322">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-322">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1fd4e-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fd4e-324">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="1fd4e-324">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="1fd4e-325">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-325">Width of the physical package in inches.</span></span>

<span data-ttu-id="1fd4e-326">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-326">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fd4e-327">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fd4e-327">Remarks</span></span>

<span data-ttu-id="1fd4e-328">Класс **\_ основной платы Win32** является производным [**от \_ карты CIM**](cim-card.md) , которая является производной от [**CIM \_ фисикалпаккаже**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1fd4e-328">The **Win32\_BaseBoard** class is derived from [**CIM\_Card**](cim-card.md) which derives from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1fd4e-329">Примеры</span><span class="sxs-lookup"><span data-stu-id="1fd4e-329">Examples</span></span>

<span data-ttu-id="1fd4e-330">Образец [свойства основной платы компьютера](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) на Perl возвращает сведения о компьютерной плате.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-330">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="1fd4e-331">Пример " [свойства платы компьютера](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) " в примере PowerShell возвращает сведения о компьютерной плате.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-331">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) PowerShell sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="1fd4e-332">Следующий пример VBScript также возвращает сведения о компьютерной плате.</span><span class="sxs-lookup"><span data-stu-id="1fd4e-332">The following VBScript sample also returns information about the computer baseboard.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a><span data-ttu-id="1fd4e-333">Требования</span><span class="sxs-lookup"><span data-stu-id="1fd4e-333">Requirements</span></span>



| <span data-ttu-id="1fd4e-334">Требование</span><span class="sxs-lookup"><span data-stu-id="1fd4e-334">Requirement</span></span> | <span data-ttu-id="1fd4e-335">Значение</span><span class="sxs-lookup"><span data-stu-id="1fd4e-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd4e-336">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fd4e-336">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd4e-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fd4e-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1fd4e-338">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fd4e-338">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd4e-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fd4e-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1fd4e-340">MOF</span><span class="sxs-lookup"><span data-stu-id="1fd4e-340">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fd4e-341"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fd4e-341"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fd4e-342">DLL</span><span class="sxs-lookup"><span data-stu-id="1fd4e-342">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fd4e-343"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fd4e-343"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd4e-344">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fd4e-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd4e-345">**\_Карта CIM**</span><span class="sxs-lookup"><span data-stu-id="1fd4e-345">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dt>

[<span data-ttu-id="1fd4e-346">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1fd4e-346">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

