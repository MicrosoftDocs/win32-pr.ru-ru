---
description: Класс CIM \_ спареграуп является производным от класса CIM \_ редунданциграуп и указывает, что один или несколько агрегированных элементов могут быть запасными.
ms.assetid: e60f8cab-a9e8-4f5a-b8d7-833c7832ef7e
ms.tgt_platform: multiple
title: Класс CIM_SpareGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SpareGroup
- CIM_SpareGroup.Caption
- CIM_SpareGroup.Description
- CIM_SpareGroup.InstallDate
- CIM_SpareGroup.Name
- CIM_SpareGroup.Status
- CIM_SpareGroup.CreationClassName
- CIM_SpareGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 17907c62ace9f75c8d807e56d35b91f4c28e5f42
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807024"
---
# <a name="cim_sparegroup-class"></a><span data-ttu-id="34c66-103">\_Класс CIM спареграуп</span><span class="sxs-lookup"><span data-stu-id="34c66-103">CIM\_SpareGroup class</span></span>

<span data-ttu-id="34c66-104">Класс **CIM \_ спареграуп** является производным от класса [**CIM \_ редунданциграуп**](cim-redundancygroup.md) и указывает, что один или несколько агрегированных элементов могут быть запасными.</span><span class="sxs-lookup"><span data-stu-id="34c66-104">The **CIM\_SpareGroup** class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span> <span data-ttu-id="34c66-105">Запасы определяются с помощью ассоциации [**CIM \_ актсасспаре**](cim-actsasspare.md) .</span><span class="sxs-lookup"><span data-stu-id="34c66-105">Spares are defined using the [**CIM\_ActsAsSpare**](cim-actsasspare.md) association.</span></span> <span data-ttu-id="34c66-106">Примером запасного диска является использование избыточных сетевых интерфейсов в компьютерной системе, где одна сетевая карта является основной, а другая — запасной.</span><span class="sxs-lookup"><span data-stu-id="34c66-106">An example of a spare is the use of redundant NICs in a computer system, where one NIC is primary and the other is spare.</span></span> <span data-ttu-id="34c66-107">Основная сетевая карта будет членом группы запчастей, связанной с использованием класса [**CIM \_ редунданцикомпонент**](cim-redundancycomponent.md) , а другая сетевая карта будет связана с использованием отношения **CIM \_ актсасспаре** .</span><span class="sxs-lookup"><span data-stu-id="34c66-107">The primary NIC would be a member of the spare group, associated using the [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class, and the other NIC would be associated using the **CIM\_ActsAsSpare** relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34c66-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="34c66-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="34c66-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="34c66-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="34c66-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="34c66-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="34c66-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="34c66-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="34c66-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34c66-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{64B86CA6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SpareGroup : CIM_RedundancyGroup
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

## <a name="members"></a><span data-ttu-id="34c66-113">Члены</span><span class="sxs-lookup"><span data-stu-id="34c66-113">Members</span></span>

<span data-ttu-id="34c66-114">Класс **CIM \_ спареграуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="34c66-114">The **CIM\_SpareGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="34c66-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="34c66-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34c66-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="34c66-116">Properties</span></span>

<span data-ttu-id="34c66-117">Класс **CIM \_ спареграуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="34c66-117">The **CIM\_SpareGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34c66-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="34c66-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c66-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34c66-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34c66-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34c66-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34c66-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="34c66-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="34c66-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="34c66-122">A short textual description of the object.</span></span>

<span data-ttu-id="34c66-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34c66-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="34c66-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c66-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34c66-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34c66-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34c66-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34c66-127">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="34c66-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="34c66-128">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="34c66-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="34c66-129">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="34c66-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="34c66-130">Это свойство наследуется от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="34c66-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="34c66-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c66-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34c66-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34c66-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34c66-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34c66-134">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="34c66-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="34c66-135">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="34c66-135">A textual description of the object.</span></span>

<span data-ttu-id="34c66-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34c66-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="34c66-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c66-138">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="34c66-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34c66-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34c66-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34c66-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="34c66-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="34c66-141">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="34c66-141">Indicates when the object was installed.</span></span> <span data-ttu-id="34c66-142">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="34c66-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="34c66-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34c66-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="34c66-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c66-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34c66-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34c66-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34c66-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34c66-147">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="34c66-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="34c66-148">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="34c66-148">Label by which the object is known.</span></span> <span data-ttu-id="34c66-149">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="34c66-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="34c66-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34c66-151">**редунданцистатус**</span><span class="sxs-lookup"><span data-stu-id="34c66-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c66-152">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34c66-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34c66-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34c66-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34c66-154">Сведения о состоянии группы избыточности.</span><span class="sxs-lookup"><span data-stu-id="34c66-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="34c66-155">Это свойство наследуется от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34c66-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="34c66-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="34c66-157">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="34c66-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34c66-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="34c66-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="34c66-159">Другое</span><span class="sxs-lookup"><span data-stu-id="34c66-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="34c66-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Полностью избыточное** (2)</span><span class="sxs-lookup"><span data-stu-id="34c66-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="34c66-161">Доступна вся настроенная избыточность.</span><span class="sxs-lookup"><span data-stu-id="34c66-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="34c66-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Пониженная избыточность** (3)</span><span class="sxs-lookup"><span data-stu-id="34c66-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="34c66-163">Уменьшение объема избыточности доступно из-за некоторых сбоев.</span><span class="sxs-lookup"><span data-stu-id="34c66-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="34c66-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Потеря избыточности** (4)</span><span class="sxs-lookup"><span data-stu-id="34c66-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="34c66-165">Избыточность недоступна из-за достаточного количества сбоев.</span><span class="sxs-lookup"><span data-stu-id="34c66-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="34c66-166">Следующий сбой приведет к общему сбою.</span><span class="sxs-lookup"><span data-stu-id="34c66-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34c66-167">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="34c66-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34c66-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34c66-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34c66-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34c66-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34c66-170">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="34c66-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="34c66-171">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="34c66-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="34c66-172">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="34c66-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="34c66-173">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="34c66-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="34c66-174">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="34c66-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="34c66-175">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="34c66-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="34c66-176">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="34c66-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="34c66-177">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="34c66-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="34c66-178">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="34c66-179">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="34c66-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="34c66-180">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="34c66-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="34c66-181">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="34c66-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="34c66-182">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="34c66-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34c66-183">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="34c66-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="34c66-184">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="34c66-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="34c66-185">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="34c66-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="34c66-186">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="34c66-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="34c66-187">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="34c66-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="34c66-188">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="34c66-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="34c66-189">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="34c66-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="34c66-190">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="34c66-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="34c66-191">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="34c66-191">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="34c66-192"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="34c66-192"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="34c66-193">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34c66-193">Remarks</span></span>

<span data-ttu-id="34c66-194">Класс **CIM \_ спареграуп** является производным от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="34c66-194">The **CIM\_SpareGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="34c66-195">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="34c66-195">WMI does not implement this class.</span></span>

<span data-ttu-id="34c66-196">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="34c66-196">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="34c66-197">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="34c66-197">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="34c66-198">Требования</span><span class="sxs-lookup"><span data-stu-id="34c66-198">Requirements</span></span>



| <span data-ttu-id="34c66-199">Требование</span><span class="sxs-lookup"><span data-stu-id="34c66-199">Requirement</span></span> | <span data-ttu-id="34c66-200">Значение</span><span class="sxs-lookup"><span data-stu-id="34c66-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34c66-201">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34c66-201">Minimum supported client</span></span><br/> | <span data-ttu-id="34c66-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34c66-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34c66-203">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34c66-203">Minimum supported server</span></span><br/> | <span data-ttu-id="34c66-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34c66-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34c66-205">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="34c66-205">Namespace</span></span><br/>                | <span data-ttu-id="34c66-206">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="34c66-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34c66-207">MOF</span><span class="sxs-lookup"><span data-stu-id="34c66-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34c66-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34c66-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34c66-209">DLL</span><span class="sxs-lookup"><span data-stu-id="34c66-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34c66-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34c66-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c66-211">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34c66-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c66-212">**\_РЕДУНДАНЦИГРАУП CIM**</span><span class="sxs-lookup"><span data-stu-id="34c66-212">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

