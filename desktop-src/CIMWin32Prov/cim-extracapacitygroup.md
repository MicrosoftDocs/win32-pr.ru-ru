---
description: Класс CIM \_ екстракапаЦитиграуп является производным от группы избыточности, которая указывает, что агрегированные элементы имеют больше емкости или возможностей, чем требуется.
ms.assetid: fbbbd6ed-4a67-4917-8b0e-3cba4cac3b45
ms.tgt_platform: multiple
title: Класс CIM_ExtraCapacityGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExtraCapacityGroup
- CIM_ExtraCapacityGroup.Caption
- CIM_ExtraCapacityGroup.Description
- CIM_ExtraCapacityGroup.InstallDate
- CIM_ExtraCapacityGroup.Name
- CIM_ExtraCapacityGroup.Status
- CIM_ExtraCapacityGroup.CreationClassName
- CIM_ExtraCapacityGroup.RedundancyStatus
- CIM_ExtraCapacityGroup.MinNumberNeeded
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78f9aa79cfcc7b93d176859069d1b71f5adf450e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262671"
---
# <a name="cim_extracapacitygroup-class"></a><span data-ttu-id="d23b7-103">\_Класс CIM екстракапаЦитиграуп</span><span class="sxs-lookup"><span data-stu-id="d23b7-103">CIM\_ExtraCapacityGroup class</span></span>

<span data-ttu-id="d23b7-104">Класс **CIM \_ екстракапаЦитиграуп** является производным от группы избыточности, которая указывает, что агрегированные элементы имеют больше емкости или возможностей, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="d23b7-104">The **CIM\_ExtraCapacityGroup** class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="d23b7-105">Примером такого типа избыточности является установка N + 1 источников питания или вентиляторов в системе.</span><span class="sxs-lookup"><span data-stu-id="d23b7-105">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d23b7-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d23b7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d23b7-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d23b7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d23b7-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d23b7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d23b7-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d23b7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d23b7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d23b7-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{570ED2E8-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ExtraCapacityGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint32   MinNumberNeeded;
};
```

## <a name="members"></a><span data-ttu-id="d23b7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="d23b7-111">Members</span></span>

<span data-ttu-id="d23b7-112">Класс **CIM \_ екстракапаЦитиграуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d23b7-112">The **CIM\_ExtraCapacityGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="d23b7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d23b7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d23b7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="d23b7-114">Properties</span></span>

<span data-ttu-id="d23b7-115">Класс **CIM \_ екстракапаЦитиграуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d23b7-115">The **CIM\_ExtraCapacityGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d23b7-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d23b7-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d23b7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-119">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d23b7-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-120">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d23b7-120">A short textual description of the object.</span></span>

<span data-ttu-id="d23b7-121">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d23b7-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d23b7-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d23b7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-125">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d23b7-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-126">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d23b7-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d23b7-127">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="d23b7-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d23b7-128">Это свойство наследуется от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-128">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="d23b7-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d23b7-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d23b7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-132">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d23b7-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-133">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d23b7-133">A textual description of the object.</span></span>

<span data-ttu-id="d23b7-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d23b7-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d23b7-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-136">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d23b7-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d23b7-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-139">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="d23b7-139">Indicates when the object was installed.</span></span> <span data-ttu-id="d23b7-140">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="d23b7-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d23b7-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d23b7-142">**миннумбернидед**</span><span class="sxs-lookup"><span data-stu-id="d23b7-142">**MinNumberNeeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d23b7-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-145">Наименьшее число элементов, которые должны быть работоспособны для обеспечения избыточности.</span><span class="sxs-lookup"><span data-stu-id="d23b7-145">Smallest number of elements that must be operational to have redundancy.</span></span> <span data-ttu-id="d23b7-146">Например, для отношения избыточности N + 1 это свойство должно быть установлено равным N.</span><span class="sxs-lookup"><span data-stu-id="d23b7-146">For example, in an N+1 redundancy relationship, this property should be set equal to N.</span></span>

</dd> <dt>

<span data-ttu-id="d23b7-147">**Name**</span><span class="sxs-lookup"><span data-stu-id="d23b7-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d23b7-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-150">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="d23b7-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-151">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="d23b7-151">Label by which the object is known.</span></span> <span data-ttu-id="d23b7-152">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="d23b7-152">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d23b7-153">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d23b7-154">**редунданцистатус**</span><span class="sxs-lookup"><span data-stu-id="d23b7-154">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-155">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d23b7-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-157">Сведения о состоянии группы избыточности.</span><span class="sxs-lookup"><span data-stu-id="d23b7-157">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="d23b7-158">Это свойство наследуется от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-158">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d23b7-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d23b7-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d23b7-160">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="d23b7-160">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d23b7-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d23b7-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d23b7-162">Другое</span><span class="sxs-lookup"><span data-stu-id="d23b7-162">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="d23b7-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Полностью избыточное** (2)</span><span class="sxs-lookup"><span data-stu-id="d23b7-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d23b7-164">Доступна вся настроенная избыточность.</span><span class="sxs-lookup"><span data-stu-id="d23b7-164">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="d23b7-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Пониженная избыточность** (3)</span><span class="sxs-lookup"><span data-stu-id="d23b7-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d23b7-166">Уменьшение объема избыточности доступно из-за некоторых сбоев.</span><span class="sxs-lookup"><span data-stu-id="d23b7-166">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="d23b7-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Потеря избыточности** (4)</span><span class="sxs-lookup"><span data-stu-id="d23b7-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d23b7-168">Избыточность недоступна из-за достаточного количества сбоев.</span><span class="sxs-lookup"><span data-stu-id="d23b7-168">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="d23b7-169">Следующий сбой приведет к общему сбою.</span><span class="sxs-lookup"><span data-stu-id="d23b7-169">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d23b7-170">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d23b7-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d23b7-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d23b7-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d23b7-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d23b7-173">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d23b7-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d23b7-174">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d23b7-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="d23b7-175">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="d23b7-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d23b7-176">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="d23b7-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d23b7-177">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="d23b7-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d23b7-178">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="d23b7-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d23b7-179">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="d23b7-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d23b7-180">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="d23b7-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d23b7-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d23b7-182">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="d23b7-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d23b7-183">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="d23b7-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d23b7-184">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="d23b7-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d23b7-185">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="d23b7-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d23b7-186">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d23b7-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d23b7-187">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="d23b7-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d23b7-188">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="d23b7-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d23b7-189">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="d23b7-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d23b7-190">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="d23b7-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d23b7-191">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="d23b7-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d23b7-192">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="d23b7-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d23b7-193">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="d23b7-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d23b7-194">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="d23b7-194">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="d23b7-195"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d23b7-195"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d23b7-196">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d23b7-196">Remarks</span></span>

<span data-ttu-id="d23b7-197">Класс **CIM \_ екстракапаЦитиграуп** является производным от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="d23b7-197">The **CIM\_ExtraCapacityGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="d23b7-198">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="d23b7-198">WMI does not implement this class.</span></span>

<span data-ttu-id="d23b7-199">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d23b7-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d23b7-200">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d23b7-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d23b7-201">Требования</span><span class="sxs-lookup"><span data-stu-id="d23b7-201">Requirements</span></span>



| <span data-ttu-id="d23b7-202">Требование</span><span class="sxs-lookup"><span data-stu-id="d23b7-202">Requirement</span></span> | <span data-ttu-id="d23b7-203">Значение</span><span class="sxs-lookup"><span data-stu-id="d23b7-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d23b7-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d23b7-204">Minimum supported client</span></span><br/> | <span data-ttu-id="d23b7-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d23b7-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d23b7-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d23b7-206">Minimum supported server</span></span><br/> | <span data-ttu-id="d23b7-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d23b7-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d23b7-208">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d23b7-208">Namespace</span></span><br/>                | <span data-ttu-id="d23b7-209">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d23b7-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d23b7-210">MOF</span><span class="sxs-lookup"><span data-stu-id="d23b7-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d23b7-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d23b7-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d23b7-212">DLL</span><span class="sxs-lookup"><span data-stu-id="d23b7-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d23b7-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d23b7-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d23b7-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d23b7-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d23b7-215">**\_РЕДУНДАНЦИГРАУП CIM**</span><span class="sxs-lookup"><span data-stu-id="d23b7-215">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

