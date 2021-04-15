---
description: Класс CIM \_ сторажередунданциграуп представляет сведения о избыточности, связанные с запоминающими устройствами.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: Класс CIM_StorageRedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655681"
---
# <a name="cim_storageredundancygroup-class"></a><span data-ttu-id="dbf50-103">\_Класс CIM сторажередунданциграуп</span><span class="sxs-lookup"><span data-stu-id="dbf50-103">CIM\_StorageRedundancyGroup class</span></span>

<span data-ttu-id="dbf50-104">Класс **CIM \_ сторажередунданциграуп** представляет сведения о избыточности, связанные с запоминающими устройствами.</span><span class="sxs-lookup"><span data-stu-id="dbf50-104">The **CIM\_StorageRedundancyGroup** class represents mass storage-related redundancy information.</span></span> <span data-ttu-id="dbf50-105">Группы избыточности хранилища используются для защиты пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="dbf50-105">Storage redundancy groups are used to protect user data.</span></span> <span data-ttu-id="dbf50-106">Они состоят из одного или нескольких физических экстентов или одного или нескольких Объединенных физических экстентов.</span><span class="sxs-lookup"><span data-stu-id="dbf50-106">They are made up of one or more physical extents, or one or more aggregate physical extents.</span></span> <span data-ttu-id="dbf50-107">Группы избыточности хранилища могут перекрываться; Однако базовые экстенты в перекрытие не должны содержать никаких проверочных данных.</span><span class="sxs-lookup"><span data-stu-id="dbf50-107">Storage redundancy groups may overlap; however, the underlying extents within the overlap should not contain any check data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbf50-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="dbf50-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dbf50-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dbf50-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dbf50-110">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dbf50-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dbf50-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dbf50-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf50-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbf50-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a><span data-ttu-id="dbf50-113">Члены</span><span class="sxs-lookup"><span data-stu-id="dbf50-113">Members</span></span>

<span data-ttu-id="dbf50-114">Класс **CIM \_ сторажередунданциграуп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dbf50-114">The **CIM\_StorageRedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="dbf50-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbf50-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbf50-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbf50-116">Properties</span></span>

<span data-ttu-id="dbf50-117">Класс **CIM \_ сторажередунданциграуп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dbf50-117">The **CIM\_StorageRedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbf50-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dbf50-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbf50-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dbf50-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbf50-122">A short textual description of the object.</span></span>

<span data-ttu-id="dbf50-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbf50-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dbf50-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbf50-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-127">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dbf50-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-128">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dbf50-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dbf50-129">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="dbf50-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dbf50-130">Это свойство наследуется от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbf50-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbf50-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbf50-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-134">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="dbf50-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-135">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbf50-135">A textual description of the object.</span></span>

<span data-ttu-id="dbf50-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbf50-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dbf50-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-138">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbf50-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="dbf50-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-141">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="dbf50-141">Indicates when the object was installed.</span></span> <span data-ttu-id="dbf50-142">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="dbf50-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="dbf50-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbf50-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="dbf50-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbf50-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-147">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="dbf50-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-148">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="dbf50-148">Label by which the object is known.</span></span> <span data-ttu-id="dbf50-149">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="dbf50-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dbf50-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbf50-151">**редунданцистатус**</span><span class="sxs-lookup"><span data-stu-id="dbf50-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-152">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbf50-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-154">Сведения о состоянии группы избыточности.</span><span class="sxs-lookup"><span data-stu-id="dbf50-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="dbf50-155">Это свойство наследуется от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbf50-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dbf50-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dbf50-157">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="dbf50-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbf50-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dbf50-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dbf50-159">Другое</span><span class="sxs-lookup"><span data-stu-id="dbf50-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="dbf50-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Полностью избыточное** (2)</span><span class="sxs-lookup"><span data-stu-id="dbf50-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dbf50-161">Доступна вся настроенная избыточность.</span><span class="sxs-lookup"><span data-stu-id="dbf50-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="dbf50-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Пониженная избыточность** (3)</span><span class="sxs-lookup"><span data-stu-id="dbf50-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dbf50-163">Уменьшение объема избыточности доступно из-за некоторых сбоев.</span><span class="sxs-lookup"><span data-stu-id="dbf50-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="dbf50-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Потеря избыточности** (4)</span><span class="sxs-lookup"><span data-stu-id="dbf50-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dbf50-165">Избыточность недоступна из-за достаточного количества сбоев.</span><span class="sxs-lookup"><span data-stu-id="dbf50-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="dbf50-166">Следующий сбой приведет к общему сбою.</span><span class="sxs-lookup"><span data-stu-id="dbf50-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf50-167">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="dbf50-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbf50-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-170">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="dbf50-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-171">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="dbf50-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="dbf50-172">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="dbf50-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="dbf50-173">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="dbf50-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="dbf50-174">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="dbf50-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="dbf50-175">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="dbf50-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dbf50-176">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="dbf50-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dbf50-177">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="dbf50-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dbf50-178">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dbf50-179">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="dbf50-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dbf50-180">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="dbf50-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dbf50-181">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="dbf50-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dbf50-182">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="dbf50-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbf50-183">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="dbf50-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dbf50-184">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="dbf50-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dbf50-185">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="dbf50-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dbf50-186">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="dbf50-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dbf50-187">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="dbf50-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dbf50-188">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="dbf50-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dbf50-189">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="dbf50-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dbf50-190">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="dbf50-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dbf50-191">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="dbf50-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbf50-192">**типеофалгорисм**</span><span class="sxs-lookup"><span data-stu-id="dbf50-192">**TypeOfAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf50-193">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbf50-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbf50-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf50-195">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Группа избыточности DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="dbf50-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Redundancy Group\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="dbf50-196">Алгоритм, используемый для избыточности и реконструкции данных.</span><span class="sxs-lookup"><span data-stu-id="dbf50-196">Algorithm used for data redundancy and reconstruction.</span></span> <span data-ttu-id="dbf50-197">Значение 0 недопустимо в схеме CIM, так как оно представляет, что в DMI не существует избыточности.</span><span class="sxs-lookup"><span data-stu-id="dbf50-197">The value 0 is not valid in the CIM schema since it represents that no redundancy exists in DMI.</span></span> <span data-ttu-id="dbf50-198">В этом случае объект не должен создаваться.</span><span class="sxs-lookup"><span data-stu-id="dbf50-198">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="dbf50-199">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="dbf50-199">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbf50-200">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dbf50-200">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbf50-201">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dbf50-201">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="dbf50-202">**Копировать** (3)</span><span class="sxs-lookup"><span data-stu-id="dbf50-202">**Copy** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

<span data-ttu-id="dbf50-203">**XOR** (4)</span><span class="sxs-lookup"><span data-stu-id="dbf50-203">**XOR** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

<span data-ttu-id="dbf50-204">**P + Q** (5)</span><span class="sxs-lookup"><span data-stu-id="dbf50-204">**P+Q** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

<span data-ttu-id="dbf50-205">**S** (6)</span><span class="sxs-lookup"><span data-stu-id="dbf50-205">**S** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

<span data-ttu-id="dbf50-206">**P + S** (7)</span><span class="sxs-lookup"><span data-stu-id="dbf50-206">**P+S** (7)</span></span>


<span data-ttu-id="dbf50-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dbf50-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dbf50-208">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbf50-208">Remarks</span></span>

<span data-ttu-id="dbf50-209">Класс **CIM \_ сторажередунданциграуп** является производным от [**CIM \_ редунданциграуп**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="dbf50-209">The **CIM\_StorageRedundancyGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="dbf50-210">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="dbf50-210">WMI does not implement this class.</span></span>

<span data-ttu-id="dbf50-211">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="dbf50-211">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dbf50-212">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dbf50-212">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf50-213">Требования</span><span class="sxs-lookup"><span data-stu-id="dbf50-213">Requirements</span></span>



| <span data-ttu-id="dbf50-214">Требование</span><span class="sxs-lookup"><span data-stu-id="dbf50-214">Requirement</span></span> | <span data-ttu-id="dbf50-215">Значение</span><span class="sxs-lookup"><span data-stu-id="dbf50-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf50-216">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbf50-216">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf50-217">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbf50-217">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbf50-218">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbf50-218">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf50-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbf50-219">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbf50-220">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbf50-220">Namespace</span></span><br/>                | <span data-ttu-id="dbf50-221">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbf50-221">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbf50-222">MOF</span><span class="sxs-lookup"><span data-stu-id="dbf50-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbf50-223"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbf50-223"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbf50-224">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf50-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf50-225"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf50-225"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf50-226">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbf50-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf50-227">**\_РЕДУНДАНЦИГРАУП CIM**</span><span class="sxs-lookup"><span data-stu-id="dbf50-227">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

