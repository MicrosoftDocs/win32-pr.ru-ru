---
description: Класс CIM \_ редунданциграуп представляет коллекцию управляемых системных элементов, которая указывает, что агрегированные компоненты вместе обеспечивают избыточность.
ms.assetid: b47899cc-eafc-431f-96d4-edb01bf4bcd1
ms.tgt_platform: multiple
title: Класс CIM_RedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyGroup
- CIM_RedundancyGroup.Caption
- CIM_RedundancyGroup.Description
- CIM_RedundancyGroup.InstallDate
- CIM_RedundancyGroup.Name
- CIM_RedundancyGroup.Status
- CIM_RedundancyGroup.CreationClassName
- CIM_RedundancyGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1394e052b4741dee5b2646c903d83477bfa1ccf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895413"
---
# <a name="cim_redundancygroup-class"></a><span data-ttu-id="be07f-103">\_Класс CIM редунданциграуп</span><span class="sxs-lookup"><span data-stu-id="be07f-103">CIM\_RedundancyGroup class</span></span>

<span data-ttu-id="be07f-104">Класс **CIM \_ редунданциграуп** представляет коллекцию управляемых системных элементов, которая указывает, что агрегированные компоненты вместе обеспечивают избыточность.</span><span class="sxs-lookup"><span data-stu-id="be07f-104">The **CIM\_RedundancyGroup** class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="be07f-105">Все элементы, Объединенные в группу избыточности, должны быть экземплярами одного и того же класса объектов.</span><span class="sxs-lookup"><span data-stu-id="be07f-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be07f-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="be07f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be07f-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="be07f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be07f-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="be07f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="be07f-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="be07f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be07f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be07f-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C3A040A-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
};
```

## <a name="members"></a><span data-ttu-id="be07f-111">Члены</span><span class="sxs-lookup"><span data-stu-id="be07f-111">Members</span></span>

<span data-ttu-id="be07f-112">Класс **CIM \_ редунданциграуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be07f-112">The **CIM\_RedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="be07f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="be07f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be07f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="be07f-114">Properties</span></span>

<span data-ttu-id="be07f-115">Класс **CIM \_ редунданциграуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be07f-115">The **CIM\_RedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be07f-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="be07f-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be07f-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be07f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be07f-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be07f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be07f-119">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="be07f-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="be07f-120">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="be07f-120">A short textual description of the object.</span></span>

<span data-ttu-id="be07f-121">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be07f-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be07f-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be07f-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be07f-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be07f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be07f-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be07f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be07f-125">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="be07f-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="be07f-126">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="be07f-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="be07f-127">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="be07f-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="be07f-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be07f-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be07f-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be07f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be07f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be07f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be07f-131">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="be07f-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="be07f-132">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="be07f-132">A textual description of the object.</span></span>

<span data-ttu-id="be07f-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be07f-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be07f-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="be07f-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be07f-135">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be07f-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be07f-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be07f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be07f-137">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="be07f-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="be07f-138">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="be07f-138">Indicates when the object was installed.</span></span> <span data-ttu-id="be07f-139">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="be07f-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="be07f-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be07f-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be07f-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="be07f-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be07f-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be07f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be07f-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be07f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be07f-144">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="be07f-144">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="be07f-145">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="be07f-145">Label by which the object is known.</span></span> <span data-ttu-id="be07f-146">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="be07f-146">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="be07f-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be07f-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be07f-148">**редунданцистатус**</span><span class="sxs-lookup"><span data-stu-id="be07f-148">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be07f-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be07f-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be07f-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be07f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be07f-151">Сведения о состоянии группы избыточности.</span><span class="sxs-lookup"><span data-stu-id="be07f-151">Information about the state of the redundancy group.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="be07f-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="be07f-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="be07f-153">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="be07f-153">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="be07f-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="be07f-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="be07f-155">Другое</span><span class="sxs-lookup"><span data-stu-id="be07f-155">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="be07f-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Полностью избыточное** (2)</span><span class="sxs-lookup"><span data-stu-id="be07f-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="be07f-157">Доступна вся настроенная избыточность.</span><span class="sxs-lookup"><span data-stu-id="be07f-157">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="be07f-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Пониженная избыточность** (3)</span><span class="sxs-lookup"><span data-stu-id="be07f-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="be07f-159">Уменьшение объема избыточности доступно из-за некоторых сбоев.</span><span class="sxs-lookup"><span data-stu-id="be07f-159">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="be07f-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Потеря избыточности** (4)</span><span class="sxs-lookup"><span data-stu-id="be07f-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="be07f-161">Избыточность недоступна из-за достаточного количества сбоев.</span><span class="sxs-lookup"><span data-stu-id="be07f-161">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="be07f-162">Следующий сбой приведет к общему сбою.</span><span class="sxs-lookup"><span data-stu-id="be07f-162">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="be07f-163">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="be07f-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be07f-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be07f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be07f-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be07f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be07f-166">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="be07f-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="be07f-167">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="be07f-167">String that indicates the current status of the object.</span></span> <span data-ttu-id="be07f-168">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="be07f-168">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="be07f-169">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="be07f-169">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="be07f-170">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="be07f-170">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="be07f-171">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="be07f-171">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="be07f-172">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="be07f-172">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="be07f-173">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="be07f-173">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="be07f-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be07f-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="be07f-175">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="be07f-175">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="be07f-176">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="be07f-176">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="be07f-177">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="be07f-177">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="be07f-178">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="be07f-178">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="be07f-179">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="be07f-179">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="be07f-180">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="be07f-180">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="be07f-181">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="be07f-181">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="be07f-182">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="be07f-182">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="be07f-183">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="be07f-183">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="be07f-184">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="be07f-184">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="be07f-185">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="be07f-185">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="be07f-186">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="be07f-186">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="be07f-187">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="be07f-187">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="be07f-188"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="be07f-188"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="be07f-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be07f-189">Remarks</span></span>

<span data-ttu-id="be07f-190">Класс **CIM \_ редунданциграуп** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="be07f-190">The **CIM\_RedundancyGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="be07f-191">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="be07f-191">WMI does not implement this class.</span></span>

<span data-ttu-id="be07f-192">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="be07f-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be07f-193">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="be07f-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be07f-194">Требования</span><span class="sxs-lookup"><span data-stu-id="be07f-194">Requirements</span></span>



| <span data-ttu-id="be07f-195">Требование</span><span class="sxs-lookup"><span data-stu-id="be07f-195">Requirement</span></span> | <span data-ttu-id="be07f-196">Значение</span><span class="sxs-lookup"><span data-stu-id="be07f-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be07f-197">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be07f-197">Minimum supported client</span></span><br/> | <span data-ttu-id="be07f-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be07f-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be07f-199">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be07f-199">Minimum supported server</span></span><br/> | <span data-ttu-id="be07f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be07f-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be07f-201">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be07f-201">Namespace</span></span><br/>                | <span data-ttu-id="be07f-202">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="be07f-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be07f-203">MOF</span><span class="sxs-lookup"><span data-stu-id="be07f-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be07f-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be07f-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be07f-205">DLL</span><span class="sxs-lookup"><span data-stu-id="be07f-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be07f-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be07f-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be07f-207">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be07f-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be07f-208">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="be07f-208">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

