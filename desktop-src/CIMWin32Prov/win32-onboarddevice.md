---
description: '\_Класс WMI онбоарддевице для Win32 представляет общие устройства адаптеров, встроенные в материнскую плату (системная плата).'
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Класс Win32_OnBoardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262750"
---
# <a name="win32_onboarddevice-class"></a><span data-ttu-id="cd2c3-103">\_Класс Win32 онбоарддевице</span><span class="sxs-lookup"><span data-stu-id="cd2c3-103">Win32\_OnBoardDevice class</span></span>

<span data-ttu-id="cd2c3-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ онбоарддевице для Win32** представляет общие устройства адаптеров, встроенные в материнскую плату (системная плата).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-104">The **Win32\_OnBoardDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents common adapter devices built into the motherboard (system board).</span></span>

<span data-ttu-id="cd2c3-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cd2c3-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd2c3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="cd2c3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="cd2c3-108">Members</span></span>

<span data-ttu-id="cd2c3-109">Класс **Win32 \_ онбоарддевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cd2c3-109">The **Win32\_OnBoardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="cd2c3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd2c3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd2c3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd2c3-111">Properties</span></span>

<span data-ttu-id="cd2c3-112">Класс **Win32 \_ онбоарддевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-112">The **Win32\_OnBoardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd2c3-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-116">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-117">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-117">Short description of the object.</span></span>

<span data-ttu-id="cd2c3-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-122">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-122">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-123">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-123">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="cd2c3-124">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cd2c3-125">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-125">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-129">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Описание"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 10 \| Description")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-129">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-130">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-130">Description of the object.</span></span>

<span data-ttu-id="cd2c3-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-132">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-132">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-135">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("тип SMBIOS \| 10 \| тип устройства n")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Type n")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-136">Тип представляемого устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-136">Type of device being represented.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cd2c3-137">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd2c3-138">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="cd2c3-139">**Видео** (3)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-139">**Video** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

<span data-ttu-id="cd2c3-140">**Контроллер SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-140">**SCSI Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="cd2c3-141">**Ethernet** (5)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-141">**Ethernet** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="cd2c3-142">**Token Ring** (6)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-142">**Token Ring** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

<span data-ttu-id="cd2c3-143">**Звук** (7)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-143">**Sound** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd2c3-144">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-144">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-147">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 10 \| устройства с состоянием n")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Status n")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-148">Если **значение — true**, встроенное устройство доступно для использования.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-148">If **TRUE**, the on-board device is available for use.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-149">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-150">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-152">Если **значение — true**, физический пакет может быть горячим заменой (если можно заменить элемент физически отличающимся, но эквивалентным, пока содержащий его пакет применяет к нему питание).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-152">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="cd2c3-153">Например, пакет диска, вставленный с помощью соединителей SCA, является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-153">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="cd2c3-154">Все пакеты, которые могут быть горячей заменой, по сути своей являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-154">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="cd2c3-155">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-155">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-157">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-159">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-160">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-160">Date and time the object was installed.</span></span> <span data-ttu-id="cd2c3-161">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cd2c3-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-163">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-163">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-166">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-166">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-167">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-167">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="cd2c3-168">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-168">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-169">**Модель**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-169">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-172">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-173">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-173">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="cd2c3-174">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-175">**Name**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-178">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-178">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-179">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-179">Label by which the object is known.</span></span> <span data-ttu-id="cd2c3-180">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-180">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="cd2c3-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-182">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-182">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-185">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для обнаружения физического элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-185">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="cd2c3-186">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-186">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="cd2c3-187">Обратите внимание, что если доступны только данные штрих-кода и они уникальны или могут использоваться в качестве ключа элемента, это свойство будет иметь **значение NULL** , а данные штрих-кода будут использоваться в качестве ключа класса в свойстве Tag.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-187">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="cd2c3-188">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-188">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-189">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-189">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-192">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-193">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-193">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="cd2c3-194">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-195">**повередон**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-195">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-198">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-198">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="cd2c3-199">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-199">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-200">**Службе**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-200">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-201">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-203">Если **значение равно true**, физический пакет является съемным (если он предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается, без нарушения функции общей упаковки).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-203">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="cd2c3-204">Пакет по-прежнему может быть съемным, если необходимо отключить питание, чтобы выполнить удаление.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-204">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="cd2c3-205">Если Power может быть "on", а пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-205">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="cd2c3-206">Например, дополнительный аккумулятор ноутбука является съемным, как и дисковый пакет, вставленный с помощью соединителей SCA.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-206">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="cd2c3-207">Однако последняя может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-207">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="cd2c3-208">Дисплей ноутбука не является съемным или не является избыточным источником питания.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-208">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="cd2c3-209">Удаление этих компонентов повлияет на функцию общей упаковки или невозможно из-за тесной интеграции пакета.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-209">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="cd2c3-210">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-210">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-211">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-211">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-212">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-214">Если **значение равно true**, физический пакет является заменяемым (если можно заменить, FRU или обновить, элемент с физически другой).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-214">If **TRUE**, a physical package is replaceable (if it is possible to replace, FRU or upgrade, the element with a physically different one).</span></span> <span data-ttu-id="cd2c3-215">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-215">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="cd2c3-216">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-216">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="cd2c3-217">Еще один пример — это пакет источника питания, подключенный к скользящим шинам.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-217">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="cd2c3-218">Все съемные пакеты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-218">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="cd2c3-219">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-219">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-220">**Номер**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-223">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-223">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-224">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="cd2c3-225">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-229">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-229">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-230">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="cd2c3-231">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-232">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-235">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-235">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-236">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-236">Current status of the object.</span></span> <span data-ttu-id="cd2c3-237">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-237">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="cd2c3-238">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-238">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="cd2c3-239">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="cd2c3-239">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cd2c3-240">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-240">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cd2c3-241">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-241">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cd2c3-242">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cd2c3-243">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="cd2c3-243">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cd2c3-244">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-244">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cd2c3-245">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-245">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cd2c3-246">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-246">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd2c3-247">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-247">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cd2c3-248">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-248">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cd2c3-249">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-249">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cd2c3-250">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-250">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cd2c3-251">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-251">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cd2c3-252">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-252">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cd2c3-253">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-253">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cd2c3-254">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-254">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cd2c3-255">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-255">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd2c3-256">**Тег**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-256">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-259">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**reoverride**](../wmisdk/standard-qualifiers.md) ("тег"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="cd2c3-259">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-260">Уникальный идентификатор встроенного устройства, подключенного к системе.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-260">Unique identifier of the on-board device connected to the system.</span></span>

<span data-ttu-id="cd2c3-261">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="cd2c3-262">Пример: "на платном устройстве 1"</span><span class="sxs-lookup"><span data-stu-id="cd2c3-262">Example: "On Board Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="cd2c3-263">**Version**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-263">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c3-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c3-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c3-266">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cd2c3-266">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd2c3-267">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c3-267">Version of the physical element.</span></span>

<span data-ttu-id="cd2c3-268">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd2c3-269">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd2c3-269">Remarks</span></span>

<span data-ttu-id="cd2c3-270">Класс **Win32 \_ онбоарддевице** является производным от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cd2c3-270">The **Win32\_OnBoardDevice** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2c3-271">Требования</span><span class="sxs-lookup"><span data-stu-id="cd2c3-271">Requirements</span></span>



| <span data-ttu-id="cd2c3-272">Требование</span><span class="sxs-lookup"><span data-stu-id="cd2c3-272">Requirement</span></span> | <span data-ttu-id="cd2c3-273">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c3-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2c3-274">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd2c3-274">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2c3-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd2c3-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd2c3-276">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd2c3-276">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2c3-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd2c3-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd2c3-278">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cd2c3-278">Namespace</span></span><br/>                | <span data-ttu-id="cd2c3-279">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cd2c3-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd2c3-280">MOF</span><span class="sxs-lookup"><span data-stu-id="cd2c3-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd2c3-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c3-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd2c3-282">DLL</span><span class="sxs-lookup"><span data-stu-id="cd2c3-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd2c3-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c3-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd2c3-284">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd2c3-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2c3-285">**\_ФИСИКАЛКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="cd2c3-285">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dt>

[<span data-ttu-id="cd2c3-286">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="cd2c3-286">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
