---
description: '\_Подклассы CIM фисикалелемент определяют любой компонент системы, имеющий уникальное физическое удостоверение. Экземпляры этого класса могут быть определены в терминах меток, которые могут быть физически присоединены к объекту.'
ms.assetid: 7ba6d1a9-f449-4ae2-a37c-517245bea39e
ms.tgt_platform: multiple
title: Класс CIM_PhysicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElement
- CIM_PhysicalElement.Caption
- CIM_PhysicalElement.Description
- CIM_PhysicalElement.InstallDate
- CIM_PhysicalElement.Name
- CIM_PhysicalElement.Status
- CIM_PhysicalElement.CreationClassName
- CIM_PhysicalElement.Manufacturer
- CIM_PhysicalElement.Model
- CIM_PhysicalElement.OtherIdentifyingInfo
- CIM_PhysicalElement.PartNumber
- CIM_PhysicalElement.PoweredOn
- CIM_PhysicalElement.SerialNumber
- CIM_PhysicalElement.SKU
- CIM_PhysicalElement.Tag
- CIM_PhysicalElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5afeda74789bc492aac3d37629b64385b8734f60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538492"
---
# <a name="cim_physicalelement-class"></a><span data-ttu-id="7a525-104">\_Класс CIM фисикалелемент</span><span class="sxs-lookup"><span data-stu-id="7a525-104">CIM\_PhysicalElement class</span></span>

<span data-ttu-id="7a525-105">Подклассы **CIM \_ фисикалелемент** определяют любой компонент системы, имеющий уникальное физическое удостоверение.</span><span class="sxs-lookup"><span data-stu-id="7a525-105">The **CIM\_PhysicalElement** subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="7a525-106">Экземпляры этого класса могут быть определены в терминах меток, которые могут быть физически присоединены к объекту.</span><span class="sxs-lookup"><span data-stu-id="7a525-106">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span> <span data-ttu-id="7a525-107">Все процессы, файлы и логические устройства не считаются физическими элементами.</span><span class="sxs-lookup"><span data-stu-id="7a525-107">All processes, files, and logical devices are not considered to be physical elements.</span></span> <span data-ttu-id="7a525-108">Например, невозможно присоединить метку к модему; можно только подключить метку к карточке, реализующей модем.</span><span class="sxs-lookup"><span data-stu-id="7a525-108">For example, it is not possible to attach a label to a modem; it is only possible to attach a label to the card that implements the modem.</span></span> <span data-ttu-id="7a525-109">На одной карте также может быть реализован адаптер локальной сети.</span><span class="sxs-lookup"><span data-stu-id="7a525-109">The same card could also implement a LAN adapter.</span></span>

<span data-ttu-id="7a525-110">Реальные управляемые системные элементы (обычно аппаратные элементы) имеют физический манифест.</span><span class="sxs-lookup"><span data-stu-id="7a525-110">Tangible managed system elements (usually hardware items) have a physical manifestation.</span></span> <span data-ttu-id="7a525-111">Управляемый системный элемент не обязательно является дискретным компонентом.</span><span class="sxs-lookup"><span data-stu-id="7a525-111">A managed system element is not necessarily a discrete component.</span></span> <span data-ttu-id="7a525-112">Например, одна карта (тип физического элемента) может размещать более одного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7a525-112">For example, it is possible for a single card (a type of physical element) to host more than one logical device.</span></span> <span data-ttu-id="7a525-113">Карточка будет представлена одним физическим элементом, связанным с несколькими логическими устройствами.</span><span class="sxs-lookup"><span data-stu-id="7a525-113">The card would be represented by a single physical element associated with multiple logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a525-114">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7a525-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7a525-115">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7a525-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7a525-116">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7a525-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7a525-117">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7a525-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a525-118">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a525-118">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B61-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="7a525-119">Члены</span><span class="sxs-lookup"><span data-stu-id="7a525-119">Members</span></span>

<span data-ttu-id="7a525-120">Класс **CIM \_ фисикалелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7a525-120">The **CIM\_PhysicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="7a525-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a525-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a525-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a525-122">Properties</span></span>

<span data-ttu-id="7a525-123">Класс **CIM \_ фисикалелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7a525-123">The **CIM\_PhysicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a525-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7a525-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-127">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7a525-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7a525-128">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7a525-128">A short textual description of the object.</span></span>

<span data-ttu-id="7a525-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7a525-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a525-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7a525-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-133">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7a525-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-134">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7a525-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7a525-135">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7a525-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7a525-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-139">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="7a525-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7a525-140">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7a525-140">A textual description of the object.</span></span>

<span data-ttu-id="7a525-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7a525-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a525-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7a525-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-143">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7a525-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-145">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="7a525-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7a525-146">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="7a525-146">Indicates when the object was installed.</span></span> <span data-ttu-id="7a525-147">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="7a525-147">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7a525-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7a525-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a525-149">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="7a525-149">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-152">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7a525-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-153">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7a525-153">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="7a525-154">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="7a525-154">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a525-155">**Модель**</span><span class="sxs-lookup"><span data-stu-id="7a525-155">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-158">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7a525-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-159">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="7a525-159">Name by which the physical element is generally known.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="7a525-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-163">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="7a525-163">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7a525-164">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7a525-164">Label by which the object is known.</span></span> <span data-ttu-id="7a525-165">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="7a525-165">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7a525-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7a525-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a525-167">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7a525-167">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a525-170">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7a525-170">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="7a525-171">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="7a525-171">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="7a525-172">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="7a525-172">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-173">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="7a525-173">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-176">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7a525-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-177">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7a525-177">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-178">**повередон**</span><span class="sxs-lookup"><span data-stu-id="7a525-178">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-179">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7a525-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a525-181">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="7a525-181">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="7a525-182">В противном случае в данный момент он отключен.</span><span class="sxs-lookup"><span data-stu-id="7a525-182">Otherwise, it is currently off.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-183">**Номер**</span><span class="sxs-lookup"><span data-stu-id="7a525-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-186">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7a525-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-187">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7a525-187">Manufacturer-allocated number used to identify the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-188">**SKU**</span><span class="sxs-lookup"><span data-stu-id="7a525-188">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-191">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7a525-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-192">Номер единицы складского учета для этого физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7a525-192">Stock-keeping unit number for this physical element.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-193">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7a525-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-196">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="7a525-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7a525-197">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7a525-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="7a525-198">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="7a525-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7a525-199">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="7a525-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7a525-200">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="7a525-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7a525-201">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="7a525-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7a525-202">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="7a525-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7a525-203">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="7a525-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7a525-204">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7a525-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7a525-205">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="7a525-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7a525-206">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="7a525-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7a525-207">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="7a525-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7a525-208">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="7a525-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7a525-209">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="7a525-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7a525-210">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="7a525-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7a525-211">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="7a525-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7a525-212">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="7a525-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7a525-213">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="7a525-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7a525-214">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="7a525-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7a525-215">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="7a525-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7a525-216">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="7a525-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7a525-217">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="7a525-217">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7a525-218">**Тег**</span><span class="sxs-lookup"><span data-stu-id="7a525-218">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-221">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7a525-221">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-222">Однозначно идентифицирует физический элемент и служит ключом элемента.</span><span class="sxs-lookup"><span data-stu-id="7a525-222">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="7a525-223">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="7a525-223">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="7a525-224">Ключ для **CIM \_ фисикалелемент** помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="7a525-224">The key for **CIM\_PhysicalElement** is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="7a525-225">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="7a525-225">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="7a525-226">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="7a525-226">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="7a525-227">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="7a525-227">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="7a525-228">**Version**</span><span class="sxs-lookup"><span data-stu-id="7a525-228">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a525-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a525-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a525-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a525-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a525-231">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7a525-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7a525-232">Указывает версию физического элемента.</span><span class="sxs-lookup"><span data-stu-id="7a525-232">Indicates the version of the physical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a525-233">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a525-233">Remarks</span></span>

<span data-ttu-id="7a525-234">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7a525-234">WMI does not implement this class.</span></span> <span data-ttu-id="7a525-235">Классы WMI, производные от **CIM \_ фисикалелемент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7a525-235">For WMI classes derived from **CIM\_PhysicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7a525-236">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7a525-236">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7a525-237">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7a525-237">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a525-238">Требования</span><span class="sxs-lookup"><span data-stu-id="7a525-238">Requirements</span></span>



| <span data-ttu-id="7a525-239">Требование</span><span class="sxs-lookup"><span data-stu-id="7a525-239">Requirement</span></span> | <span data-ttu-id="7a525-240">Значение</span><span class="sxs-lookup"><span data-stu-id="7a525-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a525-241">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a525-241">Minimum supported client</span></span><br/> | <span data-ttu-id="7a525-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a525-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a525-243">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a525-243">Minimum supported server</span></span><br/> | <span data-ttu-id="7a525-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a525-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a525-245">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a525-245">Namespace</span></span><br/>                | <span data-ttu-id="7a525-246">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7a525-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a525-247">MOF</span><span class="sxs-lookup"><span data-stu-id="7a525-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a525-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a525-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a525-249">DLL</span><span class="sxs-lookup"><span data-stu-id="7a525-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a525-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a525-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a525-251">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a525-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a525-252">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="7a525-252">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

