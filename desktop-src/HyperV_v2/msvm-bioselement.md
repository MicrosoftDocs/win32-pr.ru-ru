---
description: Представляет программное обеспечение низкого уровня, которое загружается в ОЗУ для настройки и запуска системы.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Класс Msvm_BIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897882"
---
# <a name="msvm_bioselement-class"></a><span data-ttu-id="aa5b4-103">\_Класс мсвм биоселемент</span><span class="sxs-lookup"><span data-stu-id="aa5b4-103">Msvm\_BIOSElement class</span></span>

<span data-ttu-id="aa5b4-104">Представляет программное обеспечение низкого уровня, которое загружается в ОЗУ для настройки и запуска системы.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-104">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span> <span data-ttu-id="aa5b4-105">BIOS не является логическим устройством, поэтому виртуальная BIOS не должна рассматриваться как устройство виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-105">The BIOS is not a logical device, hence the virtual BIOS should not be thought of as a virtual machine device.</span></span> <span data-ttu-id="aa5b4-106">Так как устройство не является устройством, оно не имеет соответствующего пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-106">As it is not a device, it does not have a corresponding resource pool.</span></span> <span data-ttu-id="aa5b4-107">Объект BIOS связан с виртуальной машиной через ассоциацию [**мсвм \_ систембиос**](msvm-systembios.md) .</span><span class="sxs-lookup"><span data-stu-id="aa5b4-107">The BIOS object is associated with the virtual machine through the [**Msvm\_SystemBIOS**](msvm-systembios.md) association.</span></span>

<span data-ttu-id="aa5b4-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5b4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa5b4-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a><span data-ttu-id="aa5b4-110">Члены</span><span class="sxs-lookup"><span data-stu-id="aa5b4-110">Members</span></span>

<span data-ttu-id="aa5b4-111">Класс **мсвм \_ биоселемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aa5b4-111">The **Msvm\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="aa5b4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="aa5b4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa5b4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="aa5b4-113">Properties</span></span>

<span data-ttu-id="aa5b4-114">Класс **мсвм \_ биоселемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-114">The **Msvm\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa5b4-115">**басебоардсериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-115">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-118">Серийный номер для основной платы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-118">The serial number for the base board on the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-119">**биосгуид**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-119">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-122">Уникальный идентификатор BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-122">The unique identifier for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-123">**биоснумлокк**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-123">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-126">Включенное состояние NUM LOCK в BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-126">The enabled state of the Num Lock in the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-127">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-127">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-130">Серийный номер BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-130">The serial number for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-131">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-131">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-132">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="aa5b4-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-134">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-134">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-135">Порядок, в котором устройства будут искать загрузочный сектор при запуске.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-135">The order in which devices will be searched for a boot sector at startup.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-136">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-136">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-139">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-139">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-140">Внутренний идентификатор для этой компиляции программного элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-140">The internal identifier for this compilation of software element.</span></span> <span data-ttu-id="aa5b4-141">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение 14.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-141">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 14.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-142">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-145">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-145">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-146">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-146">A short description of the object.</span></span> <span data-ttu-id="aa5b4-147">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-148">**чассисассеттаг**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-148">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-151">Автоматически заполняется BIOS при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-151">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-152">**чассиссериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-152">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-155">Автоматически заполняется BIOS при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-155">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-156">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-156">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-159">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-159">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-160">Набор кодов, используемый программным элементом.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-160">The code set used by the software element.</span></span> <span data-ttu-id="aa5b4-161">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-161">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-162">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-165">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="aa5b4-166">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="aa5b4-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-168">**куррентлангуаже**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-168">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-171">Выбранный в данный момент язык для BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-171">The currently selected language for the BIOS.</span></span> <span data-ttu-id="aa5b4-172">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="aa5b4-172">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-173">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-176">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-176">A description of the object.</span></span> <span data-ttu-id="aa5b4-177">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-181">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-181">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="aa5b4-182">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="aa5b4-183">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-187">Отображаемое имя элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-187">A display name for the element.</span></span> <span data-ttu-id="aa5b4-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-192">Указывает текущую работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-192">Specifies the current health of the element.</span></span> <span data-ttu-id="aa5b4-193">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="aa5b4-194">При возникновении критической ошибки просмотрите подробные сведения в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-194">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="aa5b4-195">Свойство **EnabledState** также может содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-195">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="aa5b4-196">Например, если место на диске критически низкий, значение **HealthState** равно 25, виртуальная машина будет приостановлена, а параметру **EnabledState** будет присвоено значение 32768 (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-196">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="aa5b4-197">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="aa5b4-198">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5b4-198">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="aa5b4-199">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5b4-199">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="aa5b4-200"><dt>**ОК**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-200"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="aa5b4-201">Виртуальная машина полностью работоспособна и работает в нормальных рабочих параметрах и без ошибок.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-201">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="aa5b4-202"><dt>**Серьезный сбой**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-202"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="aa5b4-203">Произошла серьезная ошибка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-203">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="aa5b4-204">Это значение используется, когда на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске, а виртуальная машина приостановлена.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-204">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="aa5b4-205"><dt>**Критический сбой**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-205"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="aa5b4-206">Элемент нефункциональный, и восстановление может быть невозможным.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-206">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="aa5b4-207">Это может означать, что рабочий процесс для виртуальной машины (Vmwp.exe) не отвечает на запросы контроля или информации или что на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-207">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aa5b4-208">**идентификатионкоде**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-208">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-211">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-211">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-212">Идентификатор изготовителя для этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-212">The manufacturer's identifier for this software element.</span></span> <span data-ttu-id="aa5b4-213">Часто это будет единицей складского учета (SKU) или номером части.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-213">Often this will be a stock keeping unit (SKU) or a part number.</span></span> <span data-ttu-id="aa5b4-214">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-214">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-216">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-218">Автоматически заполняется BIOS при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-218">Automatically populated by the BIOS when the virtual machine is created.</span></span> <span data-ttu-id="aa5b4-219">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-220">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-220">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-223">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-223">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-224">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-224">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="aa5b4-225">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-226">**лангуажеедитион**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-226">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-229">Квалификаторы: **maxlen** (32)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-229">Qualifiers: **MaxLen** (32)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-230">Языковой выпуск этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-230">The language edition of this software element.</span></span> <span data-ttu-id="aa5b4-231">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-231">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-232">**листофлангуажес**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-232">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-233">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-233">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-235">Список устанавливаемых языков для BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-235">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="aa5b4-236">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="aa5b4-236">THIS property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-237">**лоадедендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-237">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-238">Тип данных: **unit64**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-238">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-240">Конечный адрес памяти, которую занимает эта BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-240">The ending address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="aa5b4-241">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-241">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-242">**лоадедстартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-242">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-243">Тип данных: **unit64**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-243">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-245">Начальный адрес памяти, которую занимает эта BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-245">The starting address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="aa5b4-246">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение 0xE0000.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-246">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xE0000.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-247">**лоадутилитинформатион**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-247">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-250">Строка, описывающая программу BIOS Flash/Load, необходимую для обновления элемента BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-250">A string that describes the BIOS flash/load utility that is required to update the BIOS element.</span></span> <span data-ttu-id="aa5b4-251">В этом свойстве могут быть указаны версия и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-251">Version and other information may be indicated in this property.</span></span> <span data-ttu-id="aa5b4-252">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-252">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-253">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-253">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-254">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-256">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-256">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-257">Производитель этой BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-257">The manufacturer of this BIOS.</span></span> <span data-ttu-id="aa5b4-258">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "Корпорация Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="aa5b4-258">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-259">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-259">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-262">Квалификаторы: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-262">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-263">Имя, используемое для обнаружения этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-263">The name used to identify this software element.</span></span> <span data-ttu-id="aa5b4-264">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-264">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="aa5b4-265">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение "BIOS".</span><span class="sxs-lookup"><span data-stu-id="aa5b4-265">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "BIOS".</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-266">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-269">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="aa5b4-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="aa5b4-270">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="aa5b4-271">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-273">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="aa5b4-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-275">Массив, содержащий текущие состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-275">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="aa5b4-276">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="aa5b4-277">Значение с нулевым индексом (0) является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-277">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="aa5b4-278">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5b4-278">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="aa5b4-279">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5b4-279">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="aa5b4-280"><dt>**ОК**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-280"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="aa5b4-281">Виртуальная машина работоспособна и работает нормально.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-281">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="aa5b4-282"><dt>**Снижение уровня работоспособности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-282"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="aa5b4-283">Виртуальная машина работает только частично.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-283">The virtual machine is only partially functional.</span></span> <span data-ttu-id="aa5b4-284">Это означает, что хранилище, которое содержит конфигурацию, недоступно.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-284">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="aa5b4-285">Виртуальная машина в этом состоянии может быть выключена или удалена.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-285">A virtual machine in this state may only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="aa5b4-286"><dt>**Прогнозный сбой**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-286"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="aa5b4-287">Виртуальная машина работоспособна, но может завершиться с ошибкой в будущем.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-287">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="aa5b4-288">Это означает, что недостаточно свободного места в хранилище, содержащем виртуальный жесткий диск виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-288">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="aa5b4-289">Виртуальная машина будет приостановлена, если свободное место на диске не станет доступным.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-289">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="aa5b4-290"><dt>**Остановлено**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-290"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="aa5b4-291">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-291">This value is not supported.</span></span> <span data-ttu-id="aa5b4-292">Если виртуальная машина остановлена, свойство **EnabledState** будет иметь значение 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-292">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="aa5b4-293"><dt>**В службе**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-293"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="aa5b4-294">Виртуальная машина обрабатывает запрос.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-294">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="aa5b4-295"><dt>**Неактивность**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-295"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="aa5b4-296">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-296">This value is not supported.</span></span> <span data-ttu-id="aa5b4-297">Если виртуальная машина приостановлена или приостановлена, свойство **EnabledState** будет иметь значение 32769 (приостановлено) или 32768 (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-297">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="aa5b4-298">Значение с индексом 1 является необязательным и содержит дополнительные сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-298">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="aa5b4-299">Клиент должен использовать первичное состояние из нулевого индекса (0), чтобы определить, может ли новый запрос выдаться виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-299">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="aa5b4-300">Если значение **OperationalStatus** \[ 0 \] равно 2 (ОК), операция, указанная в **OperationalStatus** \[ 1, \] может быть прервана.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-300">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="aa5b4-301">Значение в **OperationalStatus** \[ 1 \] имеет одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-301">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="aa5b4-302">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5b4-302">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="aa5b4-303">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5b4-303">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="aa5b4-304"><dt>**Создание моментального снимка**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-304"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="aa5b4-305">Моментальный снимок находится в процессе создания для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-305">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="aa5b4-306"><dt>**Применение моментального снимка**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-306"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="aa5b4-307">Моментальный снимок находится в процессе применения к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-307">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="aa5b4-308"><dt>**Удаление моментального снимка**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-308"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="aa5b4-309">Моментальный снимок находится в процессе удаления из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-309">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="aa5b4-310"><dt>**Ожидание запуска**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-310"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="aa5b4-311">Виртуальная машина будет запущена после истечения интервала автоматической загрузки.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-311">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="aa5b4-312"><dt>**Слияние дисков**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-312"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="aa5b4-313">Выполняется слияние виртуальных жестких дисков из ранее удаленных моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-313">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="aa5b4-314"><dt>**Экспорт виртуальной машины**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-314"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="aa5b4-315">Выполняется экспорт виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-315">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="aa5b4-316"><dt>**Миграция виртуальной машины**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-316"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="aa5b4-317">Виртуальная машина переносится с одного физического компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-317">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="aa5b4-318">**осертаржетос**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-318">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-321">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-321">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-322">Изготовитель и операционная система для программного элемента, если свойство **таржетоператингсистем** имеет значение 1 (другое), которое требует, чтобы свойство **осертаржетос** имело значение, отличное от **null** .</span><span class="sxs-lookup"><span data-stu-id="aa5b4-322">The manufacturer and operating system for a software element when the **TargetOperatingSystem** property has a value of 1 (Other), which requires the **OtherTargetOS** property to have a non-**Null** value.</span></span> <span data-ttu-id="aa5b4-323">Для всех остальных значений **таржетоператингсистем** свойство **Осертаржетос** должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-323">For all other values of **TargetOperatingSystem**, the **OtherTargetOS** property must be **Null**.</span></span> <span data-ttu-id="aa5b4-324">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-324">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-325">**примарибиос**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-325">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-326">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-328">Если значение равно true, это основная BIOS компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-328">If True, this is the primary BIOS of the computer system.</span></span> <span data-ttu-id="aa5b4-329">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-329">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-330">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-330">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-331">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-333">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-333">Provides high level status information.</span></span> <span data-ttu-id="aa5b4-334">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-334">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="aa5b4-335">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="aa5b4-336">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-337">**регистрюрис**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-337">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-338">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-340">Массив строк, представляющий расположение публикации реестра атрибутов BIOS или реестров, которым соответствует реализация.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-340">An array of strings representing the publication location of the BIOS attribute registry or registries the implementation complies to.</span></span> <span data-ttu-id="aa5b4-341">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-341">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-342">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-342">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-343">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-343">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-345">Дата выпуска BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-345">The date that the BIOS was released.</span></span> <span data-ttu-id="aa5b4-346">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-346">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-347">**Номер**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-347">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-348">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-350">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-350">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-351">Назначенный серийный номер BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-351">The assigned serial number of the BIOS.</span></span> <span data-ttu-id="aa5b4-352">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-352">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-353">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-353">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-354">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-356">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-356">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-357">Идентификатор программного элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-357">An identifier for the software element.</span></span> <span data-ttu-id="aa5b4-358">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение "Microsoft:*GUID* \\ *, зависящие от устройства*".</span><span class="sxs-lookup"><span data-stu-id="aa5b4-358">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-359">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-359">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-360">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-362">Состояние жизненного цикла программного элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-362">The state of a software element's life cycle.</span></span> <span data-ttu-id="aa5b4-363">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение 2 (исполняемый объект).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-363">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 2 (Executable).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-364">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-365">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-367">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-368">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-368">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-369">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-371">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="aa5b4-371">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-372">Массив, содержащий строки, описывающие соответствующие значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="aa5b4-372">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="aa5b4-373">Например, если 11 (в службе) — значение, назначенное для **OperationalStatus** \[ 0 \] , то **статусдескриптионс** \[ 0 \] может содержать объяснение, почему виртуальная машина обрабатывает запрос.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-373">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="aa5b4-374">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-375">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-375">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-376">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-378">Среда операционной системы элемента.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-378">The element's operating system environment.</span></span> <span data-ttu-id="aa5b4-379">Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение 0 (неизвестно).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-379">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 0 (Unknown).</span></span>

</dd> <dt>

<span data-ttu-id="aa5b4-380">**Version**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5b4-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa5b4-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa5b4-383">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="aa5b4-383">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa5b4-384">Версия BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-384">The version of the BIOS.</span></span> <span data-ttu-id="aa5b4-385">Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "8.02.00".</span><span class="sxs-lookup"><span data-stu-id="aa5b4-385">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "8.02.00".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa5b4-386">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa5b4-386">Remarks</span></span>

<span data-ttu-id="aa5b4-387">Доступ к классу **\_ биоселемент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="aa5b4-387">Access to the **Msvm\_BIOSElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="aa5b4-388">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="aa5b4-388">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5b4-389">Требования</span><span class="sxs-lookup"><span data-stu-id="aa5b4-389">Requirements</span></span>



| <span data-ttu-id="aa5b4-390">Требование</span><span class="sxs-lookup"><span data-stu-id="aa5b4-390">Requirement</span></span> | <span data-ttu-id="aa5b4-391">Значение</span><span class="sxs-lookup"><span data-stu-id="aa5b4-391">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5b4-392">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa5b4-392">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5b4-393">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="aa5b4-393">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aa5b4-394">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa5b4-394">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5b4-395">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="aa5b4-395">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa5b4-396">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aa5b4-396">Namespace</span></span><br/>                | <span data-ttu-id="aa5b4-397">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="aa5b4-397">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aa5b4-398">MOF</span><span class="sxs-lookup"><span data-stu-id="aa5b4-398">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa5b4-399"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-399"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa5b4-400">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5b4-400">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa5b4-401"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa5b4-401"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa5b4-402">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa5b4-402">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5b4-403">**\_БИОСЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-403">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="aa5b4-404">Классы BIOS</span><span class="sxs-lookup"><span data-stu-id="aa5b4-404">BIOS Classes</span></span>](bios-classes.md)
</dt> <dt>

[<span data-ttu-id="aa5b4-405">**\_БИОСЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="aa5b4-405">**CIM\_BIOSElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

