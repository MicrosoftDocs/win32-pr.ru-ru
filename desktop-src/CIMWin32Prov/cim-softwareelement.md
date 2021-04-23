---
description: Класс CIM \_ софтварилемент разбивает \_ объект CIM софтварефеатуре на набор отдельных управляемых или развертываемых частей для конкретной платформы.
ms.assetid: b2418735-b738-411a-a620-acc31662f824
ms.tgt_platform: multiple
title: Класс CIM_SoftwareElement (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.Caption
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.Description
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.InstallDate
- CIM_SoftwareElement.LanguageEdition
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.Status
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fbe64ddfcf81a7410f5654db89c2924a8eabacc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141674"
---
# <a name="cim_softwareelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="e86a3-103">Класс CIM_SoftwareElement (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e86a3-103">CIM_SoftwareElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e86a3-104">Класс **CIM \_ софтварилемент** разбивает объект [**CIM \_ софтварефеатуре**](cim-softwarefeature.md) на набор отдельных управляемых или развертываемых частей для конкретной платформы.</span><span class="sxs-lookup"><span data-stu-id="e86a3-104">The **CIM\_SoftwareElement** class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="e86a3-105">Платформа программного элемента уникально определяется базовой архитектурой оборудования и операционной системой.</span><span class="sxs-lookup"><span data-stu-id="e86a3-105">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

<span data-ttu-id="e86a3-106">Таким образом, чтобы понять, как работают функции определенной программной функции на конкретной платформе, объекты **CIM \_ софтварилемент** , на которые ссылаются связи [**CIM \_ софтварефеатуресофтварилементс**](cim-softwarefeaturesoftwareelements.md) , упорядочены в наборах, основанных на свойстве **таржетоператингсистем** .</span><span class="sxs-lookup"><span data-stu-id="e86a3-106">As such, to understand the details of how the functionality of a particular software feature is provided on a particular platform, the **CIM\_SoftwareElement** objects referenced by [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) associations are organized in disjoint sets based on the **TargetOperatingSystem** property.</span></span> <span data-ttu-id="e86a3-107">Объект **CIM \_ софтварилемент** фиксирует сведения об управлении частью или компоненте в одном из четырех состояний, характеризующих свойство **софтварилементстате** .</span><span class="sxs-lookup"><span data-stu-id="e86a3-107">A **CIM\_SoftwareElement** object captures the management details of a part or component in one of four states characterized by the **SoftwareElementState** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e86a3-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e86a3-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e86a3-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e86a3-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e86a3-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e86a3-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e86a3-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e86a3-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86a3-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e86a3-112">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C561-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
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

## <a name="members"></a><span data-ttu-id="e86a3-113">Члены</span><span class="sxs-lookup"><span data-stu-id="e86a3-113">Members</span></span>

<span data-ttu-id="e86a3-114">Класс **CIM \_ софтварилемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e86a3-114">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="e86a3-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e86a3-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e86a3-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="e86a3-116">Properties</span></span>

<span data-ttu-id="e86a3-117">Класс **CIM \_ софтварилемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e86a3-117">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e86a3-118">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="e86a3-118">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="e86a3-121">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-122">Внутренний идентификатор компиляции этого программного элемента.</span><span class="sxs-lookup"><span data-stu-id="e86a3-122">Internal identifier for the compilation of this software element.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-123">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e86a3-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-126">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e86a3-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-127">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e86a3-127">Short textual description of the object.</span></span>

<span data-ttu-id="e86a3-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e86a3-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-129">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="e86a3-129">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-132">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e86a3-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-133">Набор кодов, используемый программным элементом.</span><span class="sxs-lookup"><span data-stu-id="e86a3-133">Code set used by the software element.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e86a3-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-137">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="e86a3-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-138">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e86a3-138">Textual description of the object.</span></span>

<span data-ttu-id="e86a3-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e86a3-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-140">**идентификатионкоде**</span><span class="sxs-lookup"><span data-stu-id="e86a3-140">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-143">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="e86a3-143">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-144">Идентификатор производителя программного элемента, который часто является единицей хранения (SKU) или номером части.</span><span class="sxs-lookup"><span data-stu-id="e86a3-144">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e86a3-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-146">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e86a3-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="e86a3-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-149">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="e86a3-149">Date and time the object was installed.</span></span> <span data-ttu-id="e86a3-150">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="e86a3-150">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e86a3-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e86a3-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-152">**лангуажеедитион**</span><span class="sxs-lookup"><span data-stu-id="e86a3-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-155">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о компоненте программного обеспечения DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="e86a3-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-156">Языковой выпуск программного элемента.</span><span class="sxs-lookup"><span data-stu-id="e86a3-156">Language edition of the software element.</span></span> <span data-ttu-id="e86a3-157">Следует использовать коды языков, определенные в стандарте ISO 639.</span><span class="sxs-lookup"><span data-stu-id="e86a3-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="e86a3-158">Если программный элемент представляет многоязычные или международные версии продукта, следует использовать строку "многоязычный".</span><span class="sxs-lookup"><span data-stu-id="e86a3-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-159">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="e86a3-159">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-162">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,1 в DMTF</span><span class="sxs-lookup"><span data-stu-id="e86a3-162">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-163">Производитель программного элемента.</span><span class="sxs-lookup"><span data-stu-id="e86a3-163">Manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-164">**Name**</span><span class="sxs-lookup"><span data-stu-id="e86a3-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-167">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e86a3-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-168">Имя, используемое для распознавания элемента программного обеспечения, унаследованного от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e86a3-168">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-169">**осертаржетос**</span><span class="sxs-lookup"><span data-stu-id="e86a3-169">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-172">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель \_ CIM**](cim-operatingsystem.md).**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="e86a3-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-173">Изготовитель и тип операционной системы для программного элемента, если свойство **таржетоператингсистем** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="e86a3-173">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="e86a3-174">Если свойство **таржетоператингсистем** имеет значение 1, это свойство должно иметь значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="e86a3-174">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="e86a3-175">Для всех остальных значений **таржетоператингсистем** это свойство имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="e86a3-175">For all other **TargetOperatingSystem** values, this property is null.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-176">**Номер**</span><span class="sxs-lookup"><span data-stu-id="e86a3-176">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-179">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,4 в DMTF</span><span class="sxs-lookup"><span data-stu-id="e86a3-179">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-180">Серийный номер программного элемента.</span><span class="sxs-lookup"><span data-stu-id="e86a3-180">Serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-181">**софтварилементид**</span><span class="sxs-lookup"><span data-stu-id="e86a3-181">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-184">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e86a3-184">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-185">Идентификатор программного элемента.</span><span class="sxs-lookup"><span data-stu-id="e86a3-185">Identifier for the software element.</span></span> <span data-ttu-id="e86a3-186">Он предназначен для использования совместно с другими ключами для создания уникального представления этой **\_ софтварилемент CIM**.</span><span class="sxs-lookup"><span data-stu-id="e86a3-186">It is designed to be used in conjunction with other keys to create a unique representation of this **CIM\_SoftwareElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e86a3-187">**софтварилементстате**</span><span class="sxs-lookup"><span data-stu-id="e86a3-187">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-188">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e86a3-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-190">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e86a3-190">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-191">Состояние программного элемента.</span><span class="sxs-lookup"><span data-stu-id="e86a3-191">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="e86a3-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Развертывание** (0)</span><span class="sxs-lookup"><span data-stu-id="e86a3-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-193">Описывает сведения, необходимые для успешного распространения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии, которое можно установить (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="e86a3-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="e86a3-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Устанавливаемый** (1)</span><span class="sxs-lookup"><span data-stu-id="e86a3-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-195">Описывает сведения, необходимые для успешной установки, и сведения (условия и действия), необходимые для создания программного элемента в состоянии исполняемого файла (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="e86a3-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="e86a3-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Исполняемый файл** (2)</span><span class="sxs-lookup"><span data-stu-id="e86a3-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-197">Описывает сведения, необходимые для успешного выполнения, и сведения (условия и действия), необходимые для создания программного элемента в состоянии выполнения (то есть в следующем состоянии).</span><span class="sxs-lookup"><span data-stu-id="e86a3-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="e86a3-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="e86a3-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-199">Описание сведений, необходимых для отслеживания начального элемента и работы с ним.</span><span class="sxs-lookup"><span data-stu-id="e86a3-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e86a3-200">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e86a3-200">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-203">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="e86a3-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-204">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e86a3-204">Current status of the object.</span></span>

<span data-ttu-id="e86a3-205">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e86a3-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e86a3-206">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="e86a3-206">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e86a3-207">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="e86a3-207">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e86a3-208">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="e86a3-208">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e86a3-209">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="e86a3-209">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e86a3-210">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="e86a3-210">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e86a3-211">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="e86a3-211">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e86a3-212">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="e86a3-212">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e86a3-213">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="e86a3-213">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e86a3-214">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="e86a3-214">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e86a3-215">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="e86a3-215">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e86a3-216">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="e86a3-216">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e86a3-217">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="e86a3-217">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e86a3-218">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="e86a3-218">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e86a3-219">**таржетоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="e86a3-219">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-220">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e86a3-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-222">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сведения о программном компоненте DMTF \| 002,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**модель CIM \_**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="e86a3-222">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-223">Среда операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e86a3-223">Operating system environment.</span></span> <span data-ttu-id="e86a3-224">Значение этого свойства не гарантирует двоичного ексекутабилити, требуется дополнительная информация.</span><span class="sxs-lookup"><span data-stu-id="e86a3-224">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="e86a3-225">Версию операционной системы необходимо указать с помощью проверки версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e86a3-225">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="e86a3-226">Также требуется архитектура, на которой выполняется операционная система.</span><span class="sxs-lookup"><span data-stu-id="e86a3-226">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="e86a3-227">Сочетание этих конструкций позволяет поставщику четко определить уровень операционной системы, необходимый для конкретного программного элемента.</span><span class="sxs-lookup"><span data-stu-id="e86a3-227">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e86a3-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e86a3-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e86a3-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e86a3-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="e86a3-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="e86a3-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-231">MacOS</span><span class="sxs-lookup"><span data-stu-id="e86a3-231">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="e86a3-232"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="e86a3-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-233">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="e86a3-233">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="e86a3-234"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="e86a3-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="e86a3-235"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="e86a3-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="e86a3-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="e86a3-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="e86a3-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="e86a3-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-238">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="e86a3-238">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="e86a3-239"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="e86a3-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-240">HP-UX</span><span class="sxs-lookup"><span data-stu-id="e86a3-240">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="e86a3-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="e86a3-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="e86a3-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="e86a3-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="e86a3-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="e86a3-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="e86a3-244"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="e86a3-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="e86a3-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="e86a3-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-246">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="e86a3-246">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="e86a3-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="e86a3-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="e86a3-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="e86a3-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-249">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="e86a3-249">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="e86a3-250"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="e86a3-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-251">Windows 95</span><span class="sxs-lookup"><span data-stu-id="e86a3-251">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="e86a3-252"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="e86a3-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-253">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e86a3-253">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="e86a3-254"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="e86a3-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-255">Windows NT</span><span class="sxs-lookup"><span data-stu-id="e86a3-255">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="e86a3-256"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="e86a3-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-257">Windows CE</span><span class="sxs-lookup"><span data-stu-id="e86a3-257">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="e86a3-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="e86a3-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-259">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="e86a3-259">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="e86a3-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="e86a3-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="e86a3-261"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="e86a3-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="e86a3-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="e86a3-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="e86a3-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="e86a3-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="e86a3-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="e86a3-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="e86a3-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="e86a3-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="e86a3-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="e86a3-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="e86a3-267"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="e86a3-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="e86a3-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="e86a3-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="e86a3-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="e86a3-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="e86a3-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="e86a3-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="e86a3-271"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="e86a3-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-272">Серия</span><span class="sxs-lookup"><span data-stu-id="e86a3-272">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="e86a3-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="e86a3-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-274">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="e86a3-274">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="e86a3-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="e86a3-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-276">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="e86a3-276">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="e86a3-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="e86a3-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-278">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="e86a3-278">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="e86a3-279"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="e86a3-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="e86a3-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="e86a3-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="e86a3-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="e86a3-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="e86a3-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="e86a3-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="e86a3-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="e86a3-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="e86a3-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="e86a3-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-285">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="e86a3-285">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="e86a3-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="e86a3-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="e86a3-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="e86a3-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="e86a3-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="e86a3-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="e86a3-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="e86a3-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-290">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="e86a3-290">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="e86a3-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="e86a3-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="e86a3-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="e86a3-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="e86a3-293"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="e86a3-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="e86a3-294"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="e86a3-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="e86a3-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="e86a3-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="e86a3-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="e86a3-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="e86a3-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="e86a3-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="e86a3-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="e86a3-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="e86a3-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="e86a3-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="e86a3-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="e86a3-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="e86a3-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="e86a3-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="e86a3-302">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="e86a3-302">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="e86a3-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="e86a3-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="e86a3-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="e86a3-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="e86a3-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="e86a3-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="e86a3-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="e86a3-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="e86a3-307"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (61)</span><span class="sxs-lookup"><span data-stu-id="e86a3-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e86a3-308">**Version**</span><span class="sxs-lookup"><span data-stu-id="e86a3-308">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86a3-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e86a3-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e86a3-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86a3-311">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,3 в DMTF</span><span class="sxs-lookup"><span data-stu-id="e86a3-311">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="e86a3-312">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="e86a3-312">Version of the operation.</span></span>

<span data-ttu-id="e86a3-313">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="e86a3-313">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="e86a3-314"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="e86a3-314"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="e86a3-315"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="e86a3-315"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e86a3-316">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e86a3-316">Remarks</span></span>

<span data-ttu-id="e86a3-317">Класс **CIM \_ софтварилемент** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e86a3-317">The **CIM\_SoftwareElement** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e86a3-318">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e86a3-318">WMI does not implement this class.</span></span> <span data-ttu-id="e86a3-319">Классы WMI, производные от **CIM \_ софтварилемент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e86a3-319">For WMI classes derived from **CIM\_SoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e86a3-320">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e86a3-320">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e86a3-321">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e86a3-321">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86a3-322">Требования</span><span class="sxs-lookup"><span data-stu-id="e86a3-322">Requirements</span></span>



| <span data-ttu-id="e86a3-323">Требование</span><span class="sxs-lookup"><span data-stu-id="e86a3-323">Requirement</span></span> | <span data-ttu-id="e86a3-324">Значение</span><span class="sxs-lookup"><span data-stu-id="e86a3-324">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e86a3-325">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e86a3-325">Minimum supported client</span></span><br/> | <span data-ttu-id="e86a3-326">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e86a3-326">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e86a3-327">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e86a3-327">Minimum supported server</span></span><br/> | <span data-ttu-id="e86a3-328">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e86a3-328">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e86a3-329">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e86a3-329">Namespace</span></span><br/>                | <span data-ttu-id="e86a3-330">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e86a3-330">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e86a3-331">MOF</span><span class="sxs-lookup"><span data-stu-id="e86a3-331">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e86a3-332"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e86a3-332"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e86a3-333">DLL</span><span class="sxs-lookup"><span data-stu-id="e86a3-333">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e86a3-334"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e86a3-334"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86a3-335">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e86a3-335">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86a3-336">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e86a3-336">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

