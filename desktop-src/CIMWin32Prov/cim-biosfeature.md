---
description: Представляет возможности низкоуровневого программного обеспечения, используемого для запуска и настройки компьютерной системы.
ms.assetid: 54d03539-d908-4571-b8fd-934b972e8d84
ms.tgt_platform: multiple
title: Класс CIM_BIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeature
- CIM_BIOSFeature.Caption
- CIM_BIOSFeature.Description
- CIM_BIOSFeature.InstallDate
- CIM_BIOSFeature.Status
- CIM_BIOSFeature.IdentifyingNumber
- CIM_BIOSFeature.ProductName
- CIM_BIOSFeature.Vendor
- CIM_BIOSFeature.Version
- CIM_BIOSFeature.Name
- CIM_BIOSFeature.CharacteristicDescriptions
- CIM_BIOSFeature.Characteristics
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 538dc9e4c18d976901519ae0e2d6f5249fd25c35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896185"
---
# <a name="cim_biosfeature-class"></a><span data-ttu-id="093aa-103">\_Класс CIM биосфеатуре</span><span class="sxs-lookup"><span data-stu-id="093aa-103">CIM\_BIOSFeature class</span></span>

<span data-ttu-id="093aa-104">Класс **CIM \_ биосфеатуре** представляет возможности низкоуровневого программного обеспечения, используемого для запуска и настройки компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="093aa-104">The **CIM\_BIOSFeature** class represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="093aa-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="093aa-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="093aa-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="093aa-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="093aa-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="093aa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="093aa-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="093aa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="093aa-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="093aa-109">Syntax</span></span>

``` syntax
[UUID("{7D33100E-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   IdentifyingNumber;
  string   ProductName;
  string   Vendor;
  string   Version;
  string   Name;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="093aa-110">Члены</span><span class="sxs-lookup"><span data-stu-id="093aa-110">Members</span></span>

<span data-ttu-id="093aa-111">Класс **CIM \_ биосфеатуре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="093aa-111">The **CIM\_BIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="093aa-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="093aa-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="093aa-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="093aa-113">Properties</span></span>

<span data-ttu-id="093aa-114">Класс **CIM \_ биосфеатуре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="093aa-114">The **CIM\_BIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="093aa-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="093aa-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="093aa-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="093aa-119">A short textual description of the object.</span></span>

<span data-ttu-id="093aa-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="093aa-121">**чарактеристикдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="093aa-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-122">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="093aa-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="093aa-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-124">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Характеристика BIOS \| 003,4 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ биосфеатуре**.**Характеристики**")</span><span class="sxs-lookup"><span data-stu-id="093aa-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-125">Массив строк произвольной формы, предоставляющий подробные объяснения функций BIOS, указанных в массиве **характеристик** .</span><span class="sxs-lookup"><span data-stu-id="093aa-125">Array of free-form strings that provides detailed explanations of the BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="093aa-126">Каждая запись в этом массиве связана с записью в массиве **характеристик** , которая находится в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="093aa-126">Each entry in this array is related to the entry in the **Characteristics** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="093aa-127">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="093aa-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-128">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="093aa-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="093aa-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-130">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Характеристика BIOS \| 003,3 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ биосфеатуре**.**Чарактеристикдескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="093aa-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-131">Массив целых чисел, указывающий возможности, поддерживаемые BIOS.</span><span class="sxs-lookup"><span data-stu-id="093aa-131">Array of integers that specifies the features supported by the BIOS.</span></span> <span data-ttu-id="093aa-132">Значение 3 недопустимо в схеме CIM, так как оно представляет, что в DMI не поддерживаются функции BIOS.</span><span class="sxs-lookup"><span data-stu-id="093aa-132">The value 3 is not valid in the CIM schema because it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="093aa-133">В этом случае не следует создавать экземпляры этого объекта.</span><span class="sxs-lookup"><span data-stu-id="093aa-133">In which case, this object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="093aa-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="093aa-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-135">Другое</span><span class="sxs-lookup"><span data-stu-id="093aa-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="093aa-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="093aa-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-137">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="093aa-137">Unknown.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="093aa-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (3)</span><span class="sxs-lookup"><span data-stu-id="093aa-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-139">Не определено.</span><span class="sxs-lookup"><span data-stu-id="093aa-139">Undefined.</span></span>

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span data-ttu-id="093aa-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**Поддержка ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="093aa-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA Support** (4)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-141">Поддержка ISA.</span><span class="sxs-lookup"><span data-stu-id="093aa-141">ISA support.</span></span>

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span data-ttu-id="093aa-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**Поддержка MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="093aa-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA Support** (5)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-143">Поддержка MCA.</span><span class="sxs-lookup"><span data-stu-id="093aa-143">MCA support.</span></span>

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span data-ttu-id="093aa-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**Поддержка EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="093aa-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA Support** (6)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-145">Поддержка EISA.</span><span class="sxs-lookup"><span data-stu-id="093aa-145">EISA support.</span></span>

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span data-ttu-id="093aa-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**Поддержка PCI** (7)</span><span class="sxs-lookup"><span data-stu-id="093aa-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI Support** (7)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-147">Поддержка PCI.</span><span class="sxs-lookup"><span data-stu-id="093aa-147">PCI support.</span></span>

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span data-ttu-id="093aa-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**Поддержка PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="093aa-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA Support** (8)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-149">Поддержка PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="093aa-149">PCMCIA support.</span></span>

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span data-ttu-id="093aa-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**Поддержка PnP** (9)</span><span class="sxs-lookup"><span data-stu-id="093aa-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP Support** (9)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-151">Поддержка PnP.</span><span class="sxs-lookup"><span data-stu-id="093aa-151">PnP support.</span></span>

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span data-ttu-id="093aa-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**Поддержка APM** (10)</span><span class="sxs-lookup"><span data-stu-id="093aa-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM Support** (10)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-153">Поддержка APM.</span><span class="sxs-lookup"><span data-stu-id="093aa-153">APM support.</span></span>

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span data-ttu-id="093aa-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Обновляемая BIOS** (11)</span><span class="sxs-lookup"><span data-stu-id="093aa-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradeable BIOS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-155">Обновляемая BIOS.</span><span class="sxs-lookup"><span data-stu-id="093aa-155">Upgradeable BIOS.</span></span>

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="093aa-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**Разрешена теневая версия BIOS** (12)</span><span class="sxs-lookup"><span data-stu-id="093aa-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing Allowed** (12)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-157">Разрешена теневая версия BIOS.</span><span class="sxs-lookup"><span data-stu-id="093aa-157">BIOS shadowing allowed.</span></span>

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span data-ttu-id="093aa-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**Поддержка корпоративного протокола VESA** (13)</span><span class="sxs-lookup"><span data-stu-id="093aa-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA Support** (13)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-159">Поддержка корпоративного лицензирования VESA.</span><span class="sxs-lookup"><span data-stu-id="093aa-159">VL VESA support.</span></span>

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span data-ttu-id="093aa-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**Поддержка ESCD** (14)</span><span class="sxs-lookup"><span data-stu-id="093aa-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD Support** (14)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-161">Поддержка ESCD.</span><span class="sxs-lookup"><span data-stu-id="093aa-161">ESCD support.</span></span>

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span data-ttu-id="093aa-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**Поддержка Ls-120** (15)</span><span class="sxs-lookup"><span data-stu-id="093aa-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 Support** (15)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-163">Поддержка LS-120.</span><span class="sxs-lookup"><span data-stu-id="093aa-163">LS-120 support.</span></span>

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span data-ttu-id="093aa-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**Поддержка ACPI** (16)</span><span class="sxs-lookup"><span data-stu-id="093aa-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI Support** (16)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-165">Поддержка ACPI.</span><span class="sxs-lookup"><span data-stu-id="093aa-165">ACPI support.</span></span>

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span data-ttu-id="093aa-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**Поддержка загрузки I2O** (17)</span><span class="sxs-lookup"><span data-stu-id="093aa-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O Boot Support** (17)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-167">Поддержка загрузки I2O.</span><span class="sxs-lookup"><span data-stu-id="093aa-167">I2O boot support.</span></span>

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span data-ttu-id="093aa-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**Поддержка устаревших устройств USB** (18)</span><span class="sxs-lookup"><span data-stu-id="093aa-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy Support** (18)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-169">Поддержка устаревших устройств USB.</span><span class="sxs-lookup"><span data-stu-id="093aa-169">USB legacy support.</span></span>

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span data-ttu-id="093aa-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**Поддержка AGP** (19)</span><span class="sxs-lookup"><span data-stu-id="093aa-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP Support** (19)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-171">Поддержка AGP.</span><span class="sxs-lookup"><span data-stu-id="093aa-171">AGP support.</span></span>

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span data-ttu-id="093aa-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**Плата PC Card** (20)</span><span class="sxs-lookup"><span data-stu-id="093aa-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-173">PC Card.</span><span class="sxs-lookup"><span data-stu-id="093aa-173">PC card.</span></span>

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span data-ttu-id="093aa-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span><span class="sxs-lookup"><span data-stu-id="093aa-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-175">IR.</span><span class="sxs-lookup"><span data-stu-id="093aa-175">IR.</span></span>

</dd> <dt>

<span id="1394"></span>

<span data-ttu-id="093aa-176"><span id="1394"></span>**1394** (22)</span><span class="sxs-lookup"><span data-stu-id="093aa-176"><span id="1394"></span>**1394** (22)</span></span>


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="093aa-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span><span class="sxs-lookup"><span data-stu-id="093aa-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-178">Шины.</span><span class="sxs-lookup"><span data-stu-id="093aa-178">I2C.</span></span>

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span data-ttu-id="093aa-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Интеллектуальный аккумулятор** (24)</span><span class="sxs-lookup"><span data-stu-id="093aa-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-180">Интеллектуальный аккумулятор.</span><span class="sxs-lookup"><span data-stu-id="093aa-180">Smart battery.</span></span>

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="093aa-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="093aa-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>


</dt> <dd>

<span data-ttu-id="093aa-182">PC-98.</span><span class="sxs-lookup"><span data-stu-id="093aa-182">PC-98.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="093aa-183">**Описание**</span><span class="sxs-lookup"><span data-stu-id="093aa-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-186">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="093aa-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-187">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="093aa-187">A textual description of the object.</span></span>

<span data-ttu-id="093aa-188">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="093aa-189">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="093aa-189">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-192">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="093aa-192">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-193">Идентификация продукта, например серийный номер программного обеспечения или номер кристалла в микросхеме оборудования.</span><span class="sxs-lookup"><span data-stu-id="093aa-193">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

<span data-ttu-id="093aa-194">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-194">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="093aa-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="093aa-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-196">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="093aa-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-198">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="093aa-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-199">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="093aa-199">Indicates when the object was installed.</span></span> <span data-ttu-id="093aa-200">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="093aa-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="093aa-201">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="093aa-202">**Name**</span><span class="sxs-lookup"><span data-stu-id="093aa-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-205">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="093aa-205">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="093aa-206">Свойство Name определяет метку, по которой объект известен всему миру за пределами системы обработки данных.</span><span class="sxs-lookup"><span data-stu-id="093aa-206">The Name property defines the label by which the object is known to the world outside the data processing system.</span></span> <span data-ttu-id="093aa-207">Эта метка является понятным для человека именем, которое однозначно определяет элемент в контексте пространства имен элемента.</span><span class="sxs-lookup"><span data-stu-id="093aa-207">This label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="093aa-208">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-208">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="093aa-209">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="093aa-209">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-212">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="093aa-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-213">Часто используемое название продукта.</span><span class="sxs-lookup"><span data-stu-id="093aa-213">Commonly used product name.</span></span>

<span data-ttu-id="093aa-214">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-214">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="093aa-215">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="093aa-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-218">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="093aa-218">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-219">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="093aa-219">String that indicates the current status of the object.</span></span> <span data-ttu-id="093aa-220">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="093aa-220">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="093aa-221">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="093aa-221">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="093aa-222">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="093aa-222">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="093aa-223">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="093aa-223">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="093aa-224">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="093aa-224">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="093aa-225">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="093aa-225">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="093aa-226">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-226">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="093aa-227">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="093aa-227">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="093aa-228">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="093aa-228">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="093aa-229">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="093aa-229">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="093aa-230">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="093aa-230">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="093aa-231">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="093aa-231">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="093aa-232">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="093aa-232">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="093aa-233">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="093aa-233">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="093aa-234">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="093aa-234">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="093aa-235">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="093aa-235">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="093aa-236">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="093aa-236">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="093aa-237">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="093aa-237">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="093aa-238">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="093aa-238">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="093aa-239">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="093aa-239">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="093aa-240">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="093aa-240">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-243">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Поставщик**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="093aa-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-244">Название поставщика продукта, соответствующее свойству **Vendor** объекта Product стандарта Exchange решения DMTF Standard.</span><span class="sxs-lookup"><span data-stu-id="093aa-244">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="093aa-245">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-245">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="093aa-246">**Version**</span><span class="sxs-lookup"><span data-stu-id="093aa-246">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="093aa-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="093aa-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="093aa-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="093aa-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="093aa-249">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Версия**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="093aa-249">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="093aa-250">Сведения о версии продукта, которые соответствуют свойству **Version** объекта Product стандарта Exchange решения DMTF Standard.</span><span class="sxs-lookup"><span data-stu-id="093aa-250">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="093aa-251">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-251">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="093aa-252">Комментарии</span><span class="sxs-lookup"><span data-stu-id="093aa-252">Remarks</span></span>

<span data-ttu-id="093aa-253">Класс **CIM \_ биосфеатуре** является производным от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="093aa-253">The **CIM\_BIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="093aa-254">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="093aa-254">WMI does not implement this class.</span></span>

<span data-ttu-id="093aa-255">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="093aa-255">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="093aa-256">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="093aa-256">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="093aa-257">Требования</span><span class="sxs-lookup"><span data-stu-id="093aa-257">Requirements</span></span>



| <span data-ttu-id="093aa-258">Требование</span><span class="sxs-lookup"><span data-stu-id="093aa-258">Requirement</span></span> | <span data-ttu-id="093aa-259">Значение</span><span class="sxs-lookup"><span data-stu-id="093aa-259">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="093aa-260">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="093aa-260">Minimum supported client</span></span><br/> | <span data-ttu-id="093aa-261">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="093aa-261">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="093aa-262">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="093aa-262">Minimum supported server</span></span><br/> | <span data-ttu-id="093aa-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="093aa-263">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="093aa-264">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="093aa-264">Namespace</span></span><br/>                | <span data-ttu-id="093aa-265">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="093aa-265">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="093aa-266">MOF</span><span class="sxs-lookup"><span data-stu-id="093aa-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="093aa-267"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="093aa-267"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="093aa-268">DLL</span><span class="sxs-lookup"><span data-stu-id="093aa-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="093aa-269"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="093aa-269"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="093aa-270">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="093aa-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="093aa-271">**\_СОФТВАРЕФЕАТУРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="093aa-271">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

