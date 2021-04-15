---
description: Класс CIM \_ софтварефеатуре представляет определенную функцию или возможность продукта или системы приложений.
ms.assetid: 7beeb32c-d285-44f7-adeb-3b661d8ab037
ms.tgt_platform: multiple
title: Класс CIM_SoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeature
- CIM_SoftwareFeature.Caption
- CIM_SoftwareFeature.Description
- CIM_SoftwareFeature.IdentifyingNumber
- CIM_SoftwareFeature.InstallDate
- CIM_SoftwareFeature.Name
- CIM_SoftwareFeature.ProductName
- CIM_SoftwareFeature.Status
- CIM_SoftwareFeature.Vendor
- CIM_SoftwareFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3959f7b99170cf1470d3688a101e4858f70e9a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655684"
---
# <a name="cim_softwarefeature-class"></a><span data-ttu-id="b7347-103">\_Класс CIM софтварефеатуре</span><span class="sxs-lookup"><span data-stu-id="b7347-103">CIM\_SoftwareFeature class</span></span>

<span data-ttu-id="b7347-104">Класс **CIM \_ софтварефеатуре** представляет определенную функцию или возможность продукта или системы приложений.</span><span class="sxs-lookup"><span data-stu-id="b7347-104">The **CIM\_SoftwareFeature** class represents a particular function or capability of a product or application system.</span></span> <span data-ttu-id="b7347-105">Этот класс отражает уровень гранулярности, значимый для пользователя продукта, а не единицы, отражающие процесс сборки или упаковки продукта (захваченного с помощью класса [**CIM \_ софтварилемент**](cim-softwareelement.md) ).</span><span class="sxs-lookup"><span data-stu-id="b7347-105">This class reflects a level of granularity that is meaningful to a user of a product rather than the units that reflect how the product is built or packaged (captured using a [**CIM\_SoftwareElement**](cim-softwareelement.md) class).</span></span> <span data-ttu-id="b7347-106">Если программное обеспечение может существовать на нескольких платформах или операционных системах, то Программная функция представляет собой коллекцию программных элементов для различных платформ.</span><span class="sxs-lookup"><span data-stu-id="b7347-106">When a software feature can exist on multiple platforms or operating systems, the software feature is a collection of the software elements for the different platforms.</span></span> <span data-ttu-id="b7347-107">В этом случае пользователи модели обычно заинтересованы во вложенной коллекции программных элементов, необходимых для конкретной платформы.</span><span class="sxs-lookup"><span data-stu-id="b7347-107">In which case, the users of the model will be typically interested in a sub-collection of the software elements required for a particular platform.</span></span> <span data-ttu-id="b7347-108">Поскольку функции доставляются по продуктам, функции программного обеспечения всегда определяются в контексте класса [**\_ продуктов CIM**](cim-product.md) с помощью ассоциации [**CIM \_ продуктсофтварефеатурес**](cim-productsoftwarefeatures.md) .</span><span class="sxs-lookup"><span data-stu-id="b7347-108">Because features are delivered through products, software features are always defined in the context of a [**CIM\_Product**](cim-product.md) class using the [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association.</span></span> <span data-ttu-id="b7347-109">При необходимости функции программного обеспечения из одного или нескольких продуктов могут быть организованы в системы приложений с помощью ассоциации [**CIM \_ аппликатионсистемсофтварефеатуре**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="b7347-109">Optionally, software features from one or more products can be organized into application systems using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7347-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b7347-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b7347-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b7347-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b7347-112">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b7347-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b7347-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b7347-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7347-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7347-114">Syntax</span></span>

``` syntax
[UUID("{E527D7F2-E3D4-11d2-8601-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_SoftwareFeature : CIM_LogicalElement
{
  string   Caption;
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

## <a name="members"></a><span data-ttu-id="b7347-115">Члены</span><span class="sxs-lookup"><span data-stu-id="b7347-115">Members</span></span>

<span data-ttu-id="b7347-116">Класс **CIM \_ софтварефеатуре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b7347-116">The **CIM\_SoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="b7347-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7347-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7347-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7347-118">Properties</span></span>

<span data-ttu-id="b7347-119">Класс **CIM \_ софтварефеатуре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b7347-119">The **CIM\_SoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7347-120">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b7347-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-123">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b7347-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-124">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b7347-124">Short textual description of the object.</span></span>

<span data-ttu-id="b7347-125">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7347-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7347-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7347-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-129">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b7347-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-130">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b7347-130">Textual description of the object.</span></span>

<span data-ttu-id="b7347-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7347-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7347-132">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="b7347-132">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-135">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="b7347-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-136">Идентификация продукта, например серийный номер программного обеспечения или номер кристалла в микросхеме оборудования.</span><span class="sxs-lookup"><span data-stu-id="b7347-136">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="b7347-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b7347-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-138">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7347-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b7347-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-141">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b7347-141">Date and time the object was installed.</span></span> <span data-ttu-id="b7347-142">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b7347-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b7347-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7347-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7347-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="b7347-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-147">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b7347-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b7347-148">Метка, по которой объект известен за пределами системы обработки данных.</span><span class="sxs-lookup"><span data-stu-id="b7347-148">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="b7347-149">Метка является понятным для человека именем, которое однозначно определяет элемент в контексте пространства имен элемента.</span><span class="sxs-lookup"><span data-stu-id="b7347-149">The label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="b7347-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7347-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7347-151">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="b7347-151">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-154">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="b7347-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-155">Часто используемое название продукта.</span><span class="sxs-lookup"><span data-stu-id="b7347-155">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="b7347-156">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b7347-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-159">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b7347-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-160">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b7347-160">Current status of the object.</span></span>

<span data-ttu-id="b7347-161">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7347-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b7347-162">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b7347-162">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b7347-163">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b7347-163">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b7347-164">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b7347-164">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b7347-165">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b7347-165">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7347-166">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b7347-166">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b7347-167">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b7347-167">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b7347-168">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b7347-168">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b7347-169">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b7347-169">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b7347-170">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b7347-170">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b7347-171">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b7347-171">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b7347-172">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b7347-172">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b7347-173">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b7347-173">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b7347-174">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b7347-174">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b7347-175">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="b7347-175">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-178">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Поставщик**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="b7347-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-179">Название поставщика продукта, соответствующее свойству **Vendor** объекта Product стандарта Exchange решения DMTF Standard.</span><span class="sxs-lookup"><span data-stu-id="b7347-179">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> <dt>

<span data-ttu-id="b7347-180">**Version**</span><span class="sxs-lookup"><span data-stu-id="b7347-180">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7347-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7347-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7347-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7347-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7347-183">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ продукт CIM**](cim-product.md)".**Версия**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="b7347-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b7347-184">Сведения о версии продукта, которые соответствуют свойству **Version** объекта Product стандарта Exchange решения DMTF Standard.</span><span class="sxs-lookup"><span data-stu-id="b7347-184">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7347-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7347-185">Remarks</span></span>

<span data-ttu-id="b7347-186">Класс **CIM \_ софтварефеатуре** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7347-186">The **CIM\_SoftwareFeature** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="b7347-187">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b7347-187">WMI does not implement this class.</span></span> <span data-ttu-id="b7347-188">Классы WMI, производные от **CIM \_ софтварефеатуре**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b7347-188">For WMI classes derived from **CIM\_SoftwareFeature**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b7347-189">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b7347-189">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b7347-190">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b7347-190">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7347-191">Требования</span><span class="sxs-lookup"><span data-stu-id="b7347-191">Requirements</span></span>



| <span data-ttu-id="b7347-192">Требование</span><span class="sxs-lookup"><span data-stu-id="b7347-192">Requirement</span></span> | <span data-ttu-id="b7347-193">Значение</span><span class="sxs-lookup"><span data-stu-id="b7347-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7347-194">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7347-194">Minimum supported client</span></span><br/> | <span data-ttu-id="b7347-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7347-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7347-196">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7347-196">Minimum supported server</span></span><br/> | <span data-ttu-id="b7347-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7347-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7347-198">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b7347-198">Namespace</span></span><br/>                | <span data-ttu-id="b7347-199">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b7347-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7347-200">MOF</span><span class="sxs-lookup"><span data-stu-id="b7347-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7347-201"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7347-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7347-202">DLL</span><span class="sxs-lookup"><span data-stu-id="b7347-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7347-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7347-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7347-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7347-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7347-205">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="b7347-205">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

