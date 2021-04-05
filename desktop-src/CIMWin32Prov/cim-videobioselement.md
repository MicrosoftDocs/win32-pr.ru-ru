---
description: Класс CIM \_ видеобиоселемент представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для настройки и доступа к видеоконтроллеру и экрану системы компьютера.
ms.assetid: f23d411f-4781-4727-abd1-61fe1a366bf0
ms.tgt_platform: multiple
title: Класс CIM_VideoBIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSElement
- CIM_VideoBIOSElement.BuildNumber
- CIM_VideoBIOSElement.Caption
- CIM_VideoBIOSElement.CodeSet
- CIM_VideoBIOSElement.Description
- CIM_VideoBIOSElement.IdentificationCode
- CIM_VideoBIOSElement.InstallDate
- CIM_VideoBIOSElement.IsShadowed
- CIM_VideoBIOSElement.LanguageEdition
- CIM_VideoBIOSElement.Manufacturer
- CIM_VideoBIOSElement.Name
- CIM_VideoBIOSElement.OtherTargetOS
- CIM_VideoBIOSElement.SerialNumber
- CIM_VideoBIOSElement.SoftwareElementID
- CIM_VideoBIOSElement.SoftwareElementState
- CIM_VideoBIOSElement.Status
- CIM_VideoBIOSElement.TargetOperatingSystem
- CIM_VideoBIOSElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d873b17f0bf0ea123d988d281c0cab728dd50f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990525"
---
# <a name="cim_videobioselement-class"></a><span data-ttu-id="67940-103">\_Класс CIM видеобиоселемент</span><span class="sxs-lookup"><span data-stu-id="67940-103">CIM\_VideoBIOSElement class</span></span>

<span data-ttu-id="67940-104">Класс **CIM \_ видеобиоселемент** представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для настройки и доступа к видеоконтроллеру и экрану системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="67940-104">The **CIM\_VideoBIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67940-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="67940-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="67940-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="67940-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="67940-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="67940-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="67940-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="67940-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67940-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67940-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{76148BF6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VideoBIOSElement : CIM_SoftwareElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  boolean  IsShadowed;
  string   LanguageEdition;
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="67940-110">Члены</span><span class="sxs-lookup"><span data-stu-id="67940-110">Members</span></span>

<span data-ttu-id="67940-111">Класс **CIM \_ видеобиоселемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="67940-111">The **CIM\_VideoBIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="67940-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="67940-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67940-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="67940-113">Properties</span></span>

<span data-ttu-id="67940-114">Класс **CIM \_ видеобиоселемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="67940-114">The **CIM\_VideoBIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67940-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="67940-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="67940-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="67940-119">Внутренний идентификатор компиляции этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="67940-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="67940-120">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="67940-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-124">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="67940-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="67940-125">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="67940-125">Short textual description of the object.</span></span>

<span data-ttu-id="67940-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-127">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="67940-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-130">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="67940-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="67940-131">Набор кодов, используемый программным элементом.</span><span class="sxs-lookup"><span data-stu-id="67940-131">Code set used by the software element.</span></span>

<span data-ttu-id="67940-132">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-133">**Описание**</span><span class="sxs-lookup"><span data-stu-id="67940-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-136">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="67940-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="67940-137">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="67940-137">Textual description of the object.</span></span>

<span data-ttu-id="67940-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-139">**идентификатионкоде**</span><span class="sxs-lookup"><span data-stu-id="67940-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-142">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="67940-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="67940-143">Идентификатор производителя программного элемента, например единицы складского учета (SKU) или номер детали.</span><span class="sxs-lookup"><span data-stu-id="67940-143">Manufacturer's identifier for the software element, such as a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="67940-144">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="67940-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-146">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67940-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67940-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="67940-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="67940-149">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="67940-149">Date and time the object was installed.</span></span> <span data-ttu-id="67940-150">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="67940-150">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="67940-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-152">**С тенью**</span><span class="sxs-lookup"><span data-stu-id="67940-152">**IsShadowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-153">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="67940-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67940-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-155">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video BIOS \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="67940-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="67940-156">**Значение true** показывает, что видео-BIOS является теневой.</span><span class="sxs-lookup"><span data-stu-id="67940-156">If **TRUE**, the video BIOS is shadowed.</span></span>

</dd> <dt>

<span data-ttu-id="67940-157">**лангуажеедитион**</span><span class="sxs-lookup"><span data-stu-id="67940-157">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-160">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="67940-160">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="67940-161">Языковой выпуск программного элемента.</span><span class="sxs-lookup"><span data-stu-id="67940-161">Language edition of the software element.</span></span> <span data-ttu-id="67940-162">Следует использовать коды языков, определенные в стандарте ISO 639.</span><span class="sxs-lookup"><span data-stu-id="67940-162">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="67940-163">Если программный элемент представляет многоязычную или международную версию продукта, следует использовать строку "многоязычный".</span><span class="sxs-lookup"><span data-stu-id="67940-163">When the software element represents a multilingual or international version of a product, the string "Multilingual" should be used.</span></span>

<span data-ttu-id="67940-164">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-164">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-165">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="67940-165">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-168">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,1 в DMTF</span><span class="sxs-lookup"><span data-stu-id="67940-168">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="67940-169">Производитель программного элемента это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-169">Manufacturer of the software element This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-170">**Name**</span><span class="sxs-lookup"><span data-stu-id="67940-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-173">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="67940-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67940-174">Имя, используемое для распознавания элемента программного обеспечения, унаследованного от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-174">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-175">**осертаржетос**</span><span class="sxs-lookup"><span data-stu-id="67940-175">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-178">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель \_ CIM**](cim-operatingsystem.md).**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="67940-178">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="67940-179">Изготовитель и тип операционной системы для программного элемента, если свойство **таржетоператингсистем** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="67940-179">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="67940-180">Если свойство **таржетоператингсистем** имеет значение 1, это свойство должно иметь значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="67940-180">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="67940-181">Для всех остальных значений **таржетоператингсистем** это свойство имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="67940-181">For all other **TargetOperatingSystem** values, this property is null.</span></span> <span data-ttu-id="67940-182">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-182">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-183">**Номер**</span><span class="sxs-lookup"><span data-stu-id="67940-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-186">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,4 в DMTF</span><span class="sxs-lookup"><span data-stu-id="67940-186">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="67940-187">Назначенный серийный номер программного элемента.</span><span class="sxs-lookup"><span data-stu-id="67940-187">Assigned serial number of the software element.</span></span>

<span data-ttu-id="67940-188">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-188">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-189">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="67940-189">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-192">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="67940-192">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67940-193">Идентификатор программного элемента, предназначенного для использования вместе с другими ключами для создания уникального представления класса [**CIM \_ софтварилемент**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="67940-193">Identifier for the software element that is designed to be used in conjunction with other keys to create a unique representation of the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

<span data-ttu-id="67940-194">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-194">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67940-195">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="67940-195">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67940-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67940-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-198">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67940-198">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67940-199">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="67940-199">State of a software element.</span></span>

<span data-ttu-id="67940-200">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-200">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="67940-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="67940-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="67940-202">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="67940-202">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="67940-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="67940-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="67940-204">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="67940-204">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="67940-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="67940-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="67940-206">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="67940-206">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="67940-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="67940-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67940-208">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="67940-208">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67940-209">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="67940-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-212">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="67940-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="67940-213">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="67940-213">Current status of the object.</span></span> <span data-ttu-id="67940-214">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="67940-215">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="67940-215">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="67940-216">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="67940-216">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="67940-217">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="67940-217">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="67940-218">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="67940-218">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67940-219">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="67940-219">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="67940-220">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="67940-220">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="67940-221">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="67940-221">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="67940-222">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="67940-222">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="67940-223">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="67940-223">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="67940-224">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="67940-224">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="67940-225">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="67940-225">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="67940-226">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="67940-226">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="67940-227">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="67940-227">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67940-228">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="67940-228">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-229">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67940-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67940-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-231">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о программном компоненте DMTF \| 002,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель CIM \_**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="67940-231">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="67940-232">Среда операционной системы.</span><span class="sxs-lookup"><span data-stu-id="67940-232">Operating system environment.</span></span> <span data-ttu-id="67940-233">Значение этого свойства не гарантирует двоичного выполнения.</span><span class="sxs-lookup"><span data-stu-id="67940-233">The value of this property does not ensure binary execution.</span></span> <span data-ttu-id="67940-234">Версию операционной системы необходимо указать с помощью проверки версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="67940-234">The version of the operating system must be specified using the operating system version check.</span></span> <span data-ttu-id="67940-235">Также требуется архитектура, на которой выполняется операционная система.</span><span class="sxs-lookup"><span data-stu-id="67940-235">Also required is the architecture on which the operating system runs.</span></span> <span data-ttu-id="67940-236">Сочетание этих конструкций позволяет поставщику четко определить уровень операционной системы, необходимый для конкретного программного элемента.</span><span class="sxs-lookup"><span data-stu-id="67940-236">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="67940-237">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-237">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67940-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="67940-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67940-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="67940-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="67940-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="67940-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="67940-241">MacOS</span><span class="sxs-lookup"><span data-stu-id="67940-241">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="67940-242"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="67940-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67940-243">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="67940-243">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="67940-244"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="67940-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="67940-245"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="67940-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="67940-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="67940-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="67940-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="67940-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="67940-248">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="67940-248">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="67940-249"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="67940-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="67940-250">HP-UX</span><span class="sxs-lookup"><span data-stu-id="67940-250">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="67940-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="67940-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="67940-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="67940-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="67940-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="67940-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="67940-254"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="67940-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="67940-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="67940-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="67940-256">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="67940-256">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="67940-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="67940-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="67940-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="67940-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="67940-259">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="67940-259">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="67940-260"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="67940-260"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="67940-261">Windows 95</span><span class="sxs-lookup"><span data-stu-id="67940-261">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="67940-262"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="67940-262"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="67940-263">Windows 98</span><span class="sxs-lookup"><span data-stu-id="67940-263">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="67940-264"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="67940-264"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="67940-265">Windows NT</span><span class="sxs-lookup"><span data-stu-id="67940-265">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="67940-266"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="67940-266"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="67940-267">Windows CE</span><span class="sxs-lookup"><span data-stu-id="67940-267">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="67940-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="67940-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="67940-269">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="67940-269">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="67940-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="67940-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="67940-271"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="67940-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="67940-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="67940-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="67940-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="67940-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="67940-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="67940-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="67940-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="67940-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="67940-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="67940-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="67940-277"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="67940-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="67940-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="67940-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="67940-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="67940-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="67940-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="67940-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="67940-281"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="67940-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="67940-282">Серия</span><span class="sxs-lookup"><span data-stu-id="67940-282">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="67940-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="67940-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="67940-284">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="67940-284">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="67940-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="67940-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="67940-286">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="67940-286">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="67940-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="67940-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="67940-288">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="67940-288">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="67940-289"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="67940-289"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="67940-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="67940-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="67940-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="67940-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="67940-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="67940-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="67940-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="67940-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="67940-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="67940-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="67940-295">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="67940-295">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="67940-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="67940-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="67940-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="67940-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="67940-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="67940-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="67940-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="67940-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="67940-300">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="67940-300">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="67940-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="67940-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="67940-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="67940-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="67940-303"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="67940-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="67940-304"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="67940-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="67940-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="67940-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="67940-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="67940-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="67940-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="67940-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="67940-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="67940-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="67940-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="67940-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="67940-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="67940-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="67940-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="67940-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="67940-312">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="67940-312">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="67940-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="67940-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="67940-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="67940-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="67940-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="67940-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="67940-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="67940-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="67940-317"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="67940-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67940-318">**Version**</span><span class="sxs-lookup"><span data-stu-id="67940-318">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67940-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67940-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67940-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67940-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67940-321">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="67940-321">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="67940-322">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="67940-322">Version of the operation.</span></span>

<span data-ttu-id="67940-323">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="67940-323">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="67940-324"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="67940-324"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="67940-325"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="67940-325"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="67940-326">Это свойство наследуется от класса [**CIM \_ софтварилемент**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="67940-326">This property is inherited from the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67940-327">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67940-327">Remarks</span></span>

<span data-ttu-id="67940-328">Класс **CIM \_ видеобиоселемент** является производным от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67940-328">The **CIM\_VideoBIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="67940-329">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="67940-329">WMI does not implement this class.</span></span>

<span data-ttu-id="67940-330">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="67940-330">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="67940-331">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="67940-331">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="67940-332">Требования</span><span class="sxs-lookup"><span data-stu-id="67940-332">Requirements</span></span>



| <span data-ttu-id="67940-333">Требование</span><span class="sxs-lookup"><span data-stu-id="67940-333">Requirement</span></span> | <span data-ttu-id="67940-334">Значение</span><span class="sxs-lookup"><span data-stu-id="67940-334">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67940-335">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67940-335">Minimum supported client</span></span><br/> | <span data-ttu-id="67940-336">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67940-336">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67940-337">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67940-337">Minimum supported server</span></span><br/> | <span data-ttu-id="67940-338">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67940-338">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67940-339">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="67940-339">Namespace</span></span><br/>                | <span data-ttu-id="67940-340">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="67940-340">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67940-341">MOF</span><span class="sxs-lookup"><span data-stu-id="67940-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67940-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67940-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67940-343">DLL</span><span class="sxs-lookup"><span data-stu-id="67940-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67940-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67940-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67940-345">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67940-345">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67940-346">**\_СОФТВАРИЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="67940-346">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

