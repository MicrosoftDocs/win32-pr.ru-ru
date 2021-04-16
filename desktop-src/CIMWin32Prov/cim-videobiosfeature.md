---
description: Класс CIM \_ видеобиосфеатуре представляет возможности низкоуровневого программного обеспечения, используемого для настройки и доступа к видеоконтроллеру и экрану системы компьютера.
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: Класс CIM_VideoBIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45f9fd2feabdcd1f9e650e7e7a913a394e8ef67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655820"
---
# <a name="cim_videobiosfeature-class"></a><span data-ttu-id="3ebff-103">\_Класс CIM видеобиосфеатуре</span><span class="sxs-lookup"><span data-stu-id="3ebff-103">CIM\_VideoBIOSFeature class</span></span>

<span data-ttu-id="3ebff-104">Класс **CIM \_ видеобиосфеатуре** представляет возможности низкоуровневого программного обеспечения, используемого для настройки и доступа к видеоконтроллеру и экрану системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="3ebff-104">The **CIM\_VideoBIOSFeature** class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ebff-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="3ebff-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3ebff-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3ebff-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3ebff-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3ebff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3ebff-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3ebff-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebff-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ebff-109">Syntax</span></span>

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="3ebff-110">Члены</span><span class="sxs-lookup"><span data-stu-id="3ebff-110">Members</span></span>

<span data-ttu-id="3ebff-111">Класс **CIM \_ видеобиосфеатуре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3ebff-111">The **CIM\_VideoBIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="3ebff-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ebff-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ebff-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ebff-113">Properties</span></span>

<span data-ttu-id="3ebff-114">Класс **CIM \_ видеобиосфеатуре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3ebff-114">The **CIM\_VideoBIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ebff-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3ebff-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3ebff-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3ebff-119">Short textual description of the object.</span></span>

<span data-ttu-id="3ebff-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebff-121">**чарактеристикдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="3ebff-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-122">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3ebff-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-124">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Характеристики DMTF Video BIOS \| 001,4 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ видеобиосфеатуре**.**Характеристики**")</span><span class="sxs-lookup"><span data-stu-id="3ebff-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-125">Строки произвольной формы, содержащие подробные описания функций видео-BIOS, указанных в массиве **характеристик** .</span><span class="sxs-lookup"><span data-stu-id="3ebff-125">Free-form strings that provide detailed descriptions for the video BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="3ebff-126">Каждая запись этого массива связана с записью в массиве **характеристик** , расположенной в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="3ebff-126">Each entry of this array is related to the entry in the **Characteristics** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="3ebff-127">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="3ebff-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-128">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3ebff-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-130">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Характеристики DMTF Video BIOS \| 001,3 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ видеобиосфеатуре**.**Чарактеристикдескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="3ebff-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-131">Возможности, Поддерживаемые видео BIOS.</span><span class="sxs-lookup"><span data-stu-id="3ebff-131">Features supported by the video BIOS.</span></span> <span data-ttu-id="3ebff-132">Например, может быть указана поддержка теневой версии VESA для управления питанием или видео BIOS.</span><span class="sxs-lookup"><span data-stu-id="3ebff-132">For example, support for VESA power management or video BIOS shadowing could be indicated.</span></span> <span data-ttu-id="3ebff-133">Значение 3 ("Unknown") недопустимо в схеме CIM, так как оно представляет, что в DMI не поддерживаются функции BIOS.</span><span class="sxs-lookup"><span data-stu-id="3ebff-133">The value 3 ("Unknown") is not valid in the CIM schema since it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="3ebff-134">В этом случае объект не должен создаваться.</span><span class="sxs-lookup"><span data-stu-id="3ebff-134">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3ebff-135">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="3ebff-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3ebff-136">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="3ebff-136">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="3ebff-137">Не **определено** (3)</span><span class="sxs-lookup"><span data-stu-id="3ebff-137">**Undefined** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

<span data-ttu-id="3ebff-138">**Стандартная видео-BIOS** (4)</span><span class="sxs-lookup"><span data-stu-id="3ebff-138">**Standard Video BIOS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

<span data-ttu-id="3ebff-139">**Поддерживаемые расширения VESA для BIOS** (5)</span><span class="sxs-lookup"><span data-stu-id="3ebff-139">**VESA BIOS Extensions Supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

<span data-ttu-id="3ebff-140">**Поддерживаемые возможности управления питанием VESA** (6)</span><span class="sxs-lookup"><span data-stu-id="3ebff-140">**VESA Power Management Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

<span data-ttu-id="3ebff-141">**Поддерживается канал отображаемых данных VESA** (7)</span><span class="sxs-lookup"><span data-stu-id="3ebff-141">**VESA Display Data Channel Supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="3ebff-142">**Разрешена теневая версия Video BIOS** (8)</span><span class="sxs-lookup"><span data-stu-id="3ebff-142">**Video BIOS Shadowing Allowed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

<span data-ttu-id="3ebff-143">**Обновляемая видео BIOS** (9)</span><span class="sxs-lookup"><span data-stu-id="3ebff-143">**Video BIOS Upgradeable** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ebff-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ebff-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-147">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="3ebff-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-148">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3ebff-148">Textual description of the object.</span></span>

<span data-ttu-id="3ebff-149">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebff-150">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="3ebff-150">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-153">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="3ebff-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-154">Идентификация продукта, например серийный номер программного обеспечения или номер кристалла в микросхеме оборудования.</span><span class="sxs-lookup"><span data-stu-id="3ebff-154">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span> <span data-ttu-id="3ebff-155">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-155">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebff-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3ebff-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-157">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ebff-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-159">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="3ebff-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-160">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="3ebff-160">Date and time the object was installed.</span></span> <span data-ttu-id="3ebff-161">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="3ebff-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3ebff-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebff-163">**Name**</span><span class="sxs-lookup"><span data-stu-id="3ebff-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-166">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3ebff-166">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-167">Метка, по которой объект известен за пределами системы обработки данных.</span><span class="sxs-lookup"><span data-stu-id="3ebff-167">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="3ebff-168">Эта метка является именем, уникальным образом идентифицирующее элемент в контексте пространства имен элемента.</span><span class="sxs-lookup"><span data-stu-id="3ebff-168">This label is a name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="3ebff-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebff-170">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="3ebff-170">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-173">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="3ebff-173">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-174">Часто используемое название продукта.</span><span class="sxs-lookup"><span data-stu-id="3ebff-174">Commonly used product name.</span></span>

<span data-ttu-id="3ebff-175">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-175">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebff-176">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3ebff-176">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-179">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="3ebff-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-180">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="3ebff-180">Current status of the object.</span></span> <span data-ttu-id="3ebff-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3ebff-182">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="3ebff-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3ebff-183">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="3ebff-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3ebff-184">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="3ebff-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3ebff-185">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="3ebff-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3ebff-186">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3ebff-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3ebff-187">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="3ebff-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3ebff-188">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="3ebff-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3ebff-189">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="3ebff-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3ebff-190">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="3ebff-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3ebff-191">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="3ebff-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3ebff-192">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="3ebff-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3ebff-193">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="3ebff-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3ebff-194">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="3ebff-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ebff-195">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="3ebff-195">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-198">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Поставщик**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="3ebff-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-199">Название поставщика продукта, которое соответствует свойству **Vendor** объекта Product стандарта Exchange (SES) DMTF Solution Standard.</span><span class="sxs-lookup"><span data-stu-id="3ebff-199">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard (SES).</span></span>

<span data-ttu-id="3ebff-200">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-200">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ebff-201">**Version**</span><span class="sxs-lookup"><span data-stu-id="3ebff-201">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ebff-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3ebff-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ebff-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ebff-204">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Версия**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="3ebff-204">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="3ebff-205">Сведения о версии продукта, соответствующие свойству **Version** в объекте Product объекта SES DMTF.</span><span class="sxs-lookup"><span data-stu-id="3ebff-205">Product version information, which corresponds to the **Version** property in the product object of the DMTF SES.</span></span>

<span data-ttu-id="3ebff-206">Это свойство наследуется от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-206">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ebff-207">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ebff-207">Remarks</span></span>

<span data-ttu-id="3ebff-208">Класс **CIM \_ видеобиосфеатуре** является производным от [**CIM \_ софтварефеатуре**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="3ebff-208">The **CIM\_VideoBIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="3ebff-209">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="3ebff-209">WMI does not implement this class.</span></span>

<span data-ttu-id="3ebff-210">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="3ebff-210">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3ebff-211">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3ebff-211">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ebff-212">Требования</span><span class="sxs-lookup"><span data-stu-id="3ebff-212">Requirements</span></span>



| <span data-ttu-id="3ebff-213">Требование</span><span class="sxs-lookup"><span data-stu-id="3ebff-213">Requirement</span></span> | <span data-ttu-id="3ebff-214">Значение</span><span class="sxs-lookup"><span data-stu-id="3ebff-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebff-215">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ebff-215">Minimum supported client</span></span><br/> | <span data-ttu-id="3ebff-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ebff-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ebff-217">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ebff-217">Minimum supported server</span></span><br/> | <span data-ttu-id="3ebff-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ebff-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ebff-219">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3ebff-219">Namespace</span></span><br/>                | <span data-ttu-id="3ebff-220">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3ebff-220">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ebff-221">MOF</span><span class="sxs-lookup"><span data-stu-id="3ebff-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ebff-222"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ebff-222"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ebff-223">DLL</span><span class="sxs-lookup"><span data-stu-id="3ebff-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ebff-224"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ebff-224"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ebff-225">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ebff-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebff-226">**\_СОФТВАРЕФЕАТУРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="3ebff-226">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

