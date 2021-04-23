---
description: Класс CIM \_ биоселемент представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для запуска и настройки компьютерной системы.
ms.assetid: c203244a-51e0-4733-a0bc-cf9b7957f364
ms.tgt_platform: multiple
title: Класс CIM_BIOSElement (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Caption
- CIM_BIOSElement.Description
- CIM_BIOSElement.InstallDate
- CIM_BIOSElement.Status
- CIM_BIOSElement.Name
- CIM_BIOSElement.BuildNumber
- CIM_BIOSElement.CodeSet
- CIM_BIOSElement.IdentificationCode
- CIM_BIOSElement.LanguageEdition
- CIM_BIOSElement.OtherTargetOS
- CIM_BIOSElement.SerialNumber
- CIM_BIOSElement.SoftwareElementID
- CIM_BIOSElement.SoftwareElementState
- CIM_BIOSElement.TargetOperatingSystem
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.Version
- CIM_BIOSElement.PrimaryBIOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21cd0d13d62f5cfa70f579110480b4c11c36b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072492"
---
# <a name="cim_bioselement-class-cimwin32-wmi-providers"></a><span data-ttu-id="58fc2-103">Класс CIM_BIOSElement (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="58fc2-103">CIM_BIOSElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="58fc2-104">Класс **CIM \_ биоселемент** представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для запуска и настройки компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="58fc2-104">The **CIM\_BIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58fc2-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="58fc2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58fc2-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58fc2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58fc2-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="58fc2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="58fc2-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="58fc2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58fc2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58fc2-109">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C562-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  string   BuildNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  uint16   TargetOperatingSystem;
  string   Manufacturer;
  string   Version;
  boolean  PrimaryBIOS;
};
```

## <a name="members"></a><span data-ttu-id="58fc2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="58fc2-110">Members</span></span>

<span data-ttu-id="58fc2-111">Класс **CIM \_ биоселемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="58fc2-111">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="58fc2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="58fc2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58fc2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="58fc2-113">Properties</span></span>

<span data-ttu-id="58fc2-114">Класс **CIM \_ биоселемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="58fc2-114">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58fc2-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="58fc2-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="58fc2-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-119">Внутренний идентификатор компиляции этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="58fc2-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="58fc2-120">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="58fc2-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-124">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="58fc2-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-125">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="58fc2-125">A short textual description of the object.</span></span>

<span data-ttu-id="58fc2-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-127">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="58fc2-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-130">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="58fc2-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-131">Набор кодов, используемый программным элементом.</span><span class="sxs-lookup"><span data-stu-id="58fc2-131">Code set used by the software element.</span></span>

<span data-ttu-id="58fc2-132">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-133">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58fc2-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-136">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="58fc2-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-137">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="58fc2-137">A textual description of the object.</span></span>

<span data-ttu-id="58fc2-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-139">**идентификатионкоде**</span><span class="sxs-lookup"><span data-stu-id="58fc2-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-142">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="58fc2-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-143">Идентификатор производителя программного элемента, который часто является единицей хранения (SKU) или номером части.</span><span class="sxs-lookup"><span data-stu-id="58fc2-143">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="58fc2-144">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="58fc2-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-146">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="58fc2-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="58fc2-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-149">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="58fc2-149">Indicates when the object was installed.</span></span> <span data-ttu-id="58fc2-150">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="58fc2-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="58fc2-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-152">**лангуажеедитион**</span><span class="sxs-lookup"><span data-stu-id="58fc2-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-155">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="58fc2-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-156">Языковой выпуск программного элемента.</span><span class="sxs-lookup"><span data-stu-id="58fc2-156">Language edition of the software element.</span></span> <span data-ttu-id="58fc2-157">Следует использовать коды языков, определенные в стандарте ISO 639.</span><span class="sxs-lookup"><span data-stu-id="58fc2-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="58fc2-158">Если программный элемент представляет многоязычные или международные версии продукта, следует использовать строку "многоязычный".</span><span class="sxs-lookup"><span data-stu-id="58fc2-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="58fc2-159">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-159">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-160">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="58fc2-160">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-163">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="58fc2-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-164">Производитель BIOS.</span><span class="sxs-lookup"><span data-stu-id="58fc2-164">The manufacturer of the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-165">**Name**</span><span class="sxs-lookup"><span data-stu-id="58fc2-165">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-168">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="58fc2-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-169">Имя, используемое для обнаружения этого программного элемента</span><span class="sxs-lookup"><span data-stu-id="58fc2-169">The name used to identify this software element</span></span>

<span data-ttu-id="58fc2-170">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-170">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-171">**осертаржетос**</span><span class="sxs-lookup"><span data-stu-id="58fc2-171">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-174">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель \_ CIM**](cim-operatingsystem.md).**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="58fc2-174">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-175">Изготовитель и тип операционной системы для программного элемента, если свойство **таржетоператингсистем** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="58fc2-175">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="58fc2-176">Если свойство **таржетоператингсистем** имеет значение 1, это свойство должно иметь значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="58fc2-176">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="58fc2-177">Для всех остальных значений **таржетоператингсистем** это свойство имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="58fc2-177">For all other **TargetOperatingSystem** values, this property is null.</span></span>

<span data-ttu-id="58fc2-178">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-178">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-179">**примарибиос**</span><span class="sxs-lookup"><span data-stu-id="58fc2-179">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="58fc2-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-182">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -система BIOS \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="58fc2-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-183">Если **значение равно true**, это основная BIOS компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="58fc2-183">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-184">**Номер**</span><span class="sxs-lookup"><span data-stu-id="58fc2-184">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-187">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,4 в DMTF</span><span class="sxs-lookup"><span data-stu-id="58fc2-187">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-188">Серийный номер программного элемента.</span><span class="sxs-lookup"><span data-stu-id="58fc2-188">Serial number of the software element.</span></span>

<span data-ttu-id="58fc2-189">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-189">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-190">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="58fc2-190">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-193">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="58fc2-193">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-194">Идентификатор программного элемента.</span><span class="sxs-lookup"><span data-stu-id="58fc2-194">Identifier for the software element.</span></span> <span data-ttu-id="58fc2-195">Он предназначен для использования совместно с другими ключами для создания уникального представления этой [**\_ софтварилемент CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-195">It is designed to be used in conjunction with other keys to create a unique representation of this [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="58fc2-196">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-196">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58fc2-197">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="58fc2-197">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58fc2-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-200">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58fc2-200">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-201">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="58fc2-201">State of a software element.</span></span>

<span data-ttu-id="58fc2-202">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-202">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="58fc2-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="58fc2-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-204">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="58fc2-204">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="58fc2-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="58fc2-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-206">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="58fc2-206">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="58fc2-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="58fc2-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-208">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="58fc2-208">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="58fc2-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="58fc2-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-210">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="58fc2-210">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="58fc2-211">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="58fc2-211">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-214">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="58fc2-214">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-215">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="58fc2-215">String that indicates the current status of the object.</span></span> <span data-ttu-id="58fc2-216">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="58fc2-216">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="58fc2-217">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="58fc2-217">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="58fc2-218">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="58fc2-218">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="58fc2-219">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="58fc2-219">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="58fc2-220">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="58fc2-220">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="58fc2-221">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="58fc2-221">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="58fc2-222">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="58fc2-223">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="58fc2-223">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="58fc2-224">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="58fc2-224">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="58fc2-225">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="58fc2-225">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="58fc2-226">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="58fc2-226">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58fc2-227">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="58fc2-227">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="58fc2-228">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="58fc2-228">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="58fc2-229">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="58fc2-229">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="58fc2-230">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="58fc2-230">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="58fc2-231">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="58fc2-231">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="58fc2-232">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="58fc2-232">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="58fc2-233">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="58fc2-233">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="58fc2-234">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="58fc2-234">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="58fc2-235">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="58fc2-235">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58fc2-236">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="58fc2-236">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58fc2-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-239">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о программном компоненте DMTF \| 002,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель CIM \_**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="58fc2-239">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-240">Среда операционной системы.</span><span class="sxs-lookup"><span data-stu-id="58fc2-240">Operating system environment.</span></span> <span data-ttu-id="58fc2-241">Значение этого свойства не гарантирует двоичного ексекутабилити, требуется дополнительная информация.</span><span class="sxs-lookup"><span data-stu-id="58fc2-241">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="58fc2-242">Версию операционной системы необходимо указать с помощью проверки версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="58fc2-242">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="58fc2-243">Также требуется архитектура, на которой выполняется операционная система.</span><span class="sxs-lookup"><span data-stu-id="58fc2-243">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="58fc2-244">Сочетание этих конструкций позволяет поставщику четко определить уровень операционной системы, необходимый для конкретного программного элемента.</span><span class="sxs-lookup"><span data-stu-id="58fc2-244">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="58fc2-245">Это свойство наследуется от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-245">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58fc2-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="58fc2-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="58fc2-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="58fc2-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="58fc2-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="58fc2-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-249">MacOS</span><span class="sxs-lookup"><span data-stu-id="58fc2-249">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="58fc2-250"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="58fc2-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-251">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="58fc2-251">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="58fc2-252"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="58fc2-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="58fc2-253"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="58fc2-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="58fc2-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="58fc2-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="58fc2-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="58fc2-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-256">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="58fc2-256">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="58fc2-257"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="58fc2-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-258">HP-UX</span><span class="sxs-lookup"><span data-stu-id="58fc2-258">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="58fc2-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="58fc2-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="58fc2-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="58fc2-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="58fc2-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="58fc2-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="58fc2-262"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="58fc2-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="58fc2-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="58fc2-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-264">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="58fc2-264">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="58fc2-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="58fc2-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="58fc2-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="58fc2-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-267">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="58fc2-267">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="58fc2-268"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="58fc2-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-269">Windows 95</span><span class="sxs-lookup"><span data-stu-id="58fc2-269">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="58fc2-270"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="58fc2-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-271">Windows 98</span><span class="sxs-lookup"><span data-stu-id="58fc2-271">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="58fc2-272"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="58fc2-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-273">Windows NT</span><span class="sxs-lookup"><span data-stu-id="58fc2-273">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="58fc2-274"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="58fc2-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-275">Windows CE</span><span class="sxs-lookup"><span data-stu-id="58fc2-275">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="58fc2-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="58fc2-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-277">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="58fc2-277">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="58fc2-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="58fc2-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="58fc2-279"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="58fc2-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="58fc2-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="58fc2-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="58fc2-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="58fc2-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="58fc2-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="58fc2-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="58fc2-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="58fc2-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="58fc2-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="58fc2-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="58fc2-285"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="58fc2-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="58fc2-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="58fc2-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="58fc2-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="58fc2-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="58fc2-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="58fc2-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="58fc2-289"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="58fc2-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-290">Серия</span><span class="sxs-lookup"><span data-stu-id="58fc2-290">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="58fc2-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="58fc2-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-292">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="58fc2-292">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="58fc2-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="58fc2-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-294">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="58fc2-294">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="58fc2-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="58fc2-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-296">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="58fc2-296">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="58fc2-297"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="58fc2-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="58fc2-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="58fc2-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="58fc2-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="58fc2-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="58fc2-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="58fc2-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="58fc2-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="58fc2-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="58fc2-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="58fc2-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-303">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="58fc2-303">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="58fc2-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="58fc2-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="58fc2-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="58fc2-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="58fc2-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="58fc2-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="58fc2-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="58fc2-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-308">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="58fc2-308">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="58fc2-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="58fc2-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="58fc2-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="58fc2-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="58fc2-311"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="58fc2-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="58fc2-312"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="58fc2-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="58fc2-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="58fc2-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="58fc2-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="58fc2-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="58fc2-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="58fc2-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="58fc2-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="58fc2-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="58fc2-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="58fc2-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="58fc2-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="58fc2-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="58fc2-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="58fc2-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="58fc2-320">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="58fc2-320">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="58fc2-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="58fc2-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="58fc2-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="58fc2-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="58fc2-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="58fc2-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="58fc2-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="58fc2-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="58fc2-325"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="58fc2-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58fc2-326">**Version**</span><span class="sxs-lookup"><span data-stu-id="58fc2-326">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58fc2-327">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58fc2-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58fc2-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58fc2-329">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("версия"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -система BIOS \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="58fc2-329">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="58fc2-330">Версия BIOS.</span><span class="sxs-lookup"><span data-stu-id="58fc2-330">The version of the BIOS.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58fc2-331">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58fc2-331">Remarks</span></span>

<span data-ttu-id="58fc2-332">Класс **CIM \_ биоселемент** является производным от [**CIM \_ софтварилемент**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-332">The **CIM\_BIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="58fc2-333">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="58fc2-333">WMI does not implement this class.</span></span> <span data-ttu-id="58fc2-334">Дополнительные сведения о классах, производных от **CIM \_ биоселемент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="58fc2-334">For more information about classes derived from **CIM\_BIOSElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="58fc2-335">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="58fc2-335">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58fc2-336">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="58fc2-336">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58fc2-337">Требования</span><span class="sxs-lookup"><span data-stu-id="58fc2-337">Requirements</span></span>



| <span data-ttu-id="58fc2-338">Требование</span><span class="sxs-lookup"><span data-stu-id="58fc2-338">Requirement</span></span> | <span data-ttu-id="58fc2-339">Значение</span><span class="sxs-lookup"><span data-stu-id="58fc2-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58fc2-340">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58fc2-340">Minimum supported client</span></span><br/> | <span data-ttu-id="58fc2-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58fc2-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58fc2-342">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58fc2-342">Minimum supported server</span></span><br/> | <span data-ttu-id="58fc2-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58fc2-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58fc2-344">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58fc2-344">Namespace</span></span><br/>                | <span data-ttu-id="58fc2-345">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58fc2-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58fc2-346">MOF</span><span class="sxs-lookup"><span data-stu-id="58fc2-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58fc2-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58fc2-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58fc2-348">DLL</span><span class="sxs-lookup"><span data-stu-id="58fc2-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58fc2-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58fc2-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58fc2-350">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58fc2-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58fc2-351">**\_СОФТВАРИЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="58fc2-351">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

