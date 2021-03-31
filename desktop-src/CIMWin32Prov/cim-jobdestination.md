---
description: Класс CIM \_ жобдестинатион представляет место отправки задания для обработки.
ms.assetid: ad2a037d-a5d3-4422-972d-8ef10699bb60
ms.tgt_platform: multiple
title: Класс CIM_JobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestination
- CIM_JobDestination.Caption
- CIM_JobDestination.Description
- CIM_JobDestination.InstallDate
- CIM_JobDestination.Name
- CIM_JobDestination.Status
- CIM_JobDestination.CreationClassName
- CIM_JobDestination.SystemCreationClassName
- CIM_JobDestination.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d01fbe3b6025795084bf0af4cca3d644fd3cf4a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896009"
---
# <a name="cim_jobdestination-class"></a><span data-ttu-id="19ca7-103">\_Класс CIM жобдестинатион</span><span class="sxs-lookup"><span data-stu-id="19ca7-103">CIM\_JobDestination class</span></span>

<span data-ttu-id="19ca7-104">Класс **CIM \_ жобдестинатион** представляет место отправки задания для обработки.</span><span class="sxs-lookup"><span data-stu-id="19ca7-104">The **CIM\_JobDestination** class represents where a job is submitted for processing.</span></span> <span data-ttu-id="19ca7-105">Он может ссылаться на очередь, содержащую ноль или более заданий, например очередь печати, содержащую задания печати.</span><span class="sxs-lookup"><span data-stu-id="19ca7-105">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="19ca7-106">Назначения заданий размещаются на системах, аналогично тому, как службы размещаются на системах.</span><span class="sxs-lookup"><span data-stu-id="19ca7-106">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19ca7-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="19ca7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="19ca7-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="19ca7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="19ca7-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="19ca7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="19ca7-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="19ca7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ca7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19ca7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{673E0A2C-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestination : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="19ca7-112">Члены</span><span class="sxs-lookup"><span data-stu-id="19ca7-112">Members</span></span>

<span data-ttu-id="19ca7-113">Класс **CIM \_ жобдестинатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="19ca7-113">The **CIM\_JobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="19ca7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="19ca7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19ca7-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="19ca7-115">Properties</span></span>

<span data-ttu-id="19ca7-116">Класс **CIM \_ жобдестинатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="19ca7-116">The **CIM\_JobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19ca7-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="19ca7-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19ca7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="19ca7-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="19ca7-121">A short textual description of the object.</span></span>

<span data-ttu-id="19ca7-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19ca7-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19ca7-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="19ca7-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19ca7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-126">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="19ca7-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-127">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="19ca7-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="19ca7-128">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="19ca7-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="19ca7-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19ca7-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19ca7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-132">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="19ca7-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-133">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="19ca7-133">A textual description of the object.</span></span>

<span data-ttu-id="19ca7-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19ca7-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19ca7-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="19ca7-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-136">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="19ca7-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="19ca7-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-139">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="19ca7-139">Indicates when the object was installed.</span></span> <span data-ttu-id="19ca7-140">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="19ca7-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="19ca7-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19ca7-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19ca7-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="19ca7-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19ca7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-145">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="19ca7-145">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-146">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="19ca7-146">Label by which the object is known.</span></span> <span data-ttu-id="19ca7-147">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="19ca7-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="19ca7-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19ca7-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19ca7-149">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="19ca7-149">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19ca7-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-152">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="19ca7-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-153">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="19ca7-153">String that indicates the current status of the object.</span></span> <span data-ttu-id="19ca7-154">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="19ca7-154">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="19ca7-155">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="19ca7-155">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="19ca7-156">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="19ca7-156">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="19ca7-157">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="19ca7-157">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="19ca7-158">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="19ca7-158">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="19ca7-159">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="19ca7-159">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="19ca7-160">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19ca7-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="19ca7-161">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="19ca7-161">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="19ca7-162">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="19ca7-162">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="19ca7-163">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="19ca7-163">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="19ca7-164">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="19ca7-164">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19ca7-165">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="19ca7-165">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="19ca7-166">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="19ca7-166">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="19ca7-167">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="19ca7-167">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="19ca7-168">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="19ca7-168">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="19ca7-169">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="19ca7-169">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="19ca7-170">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="19ca7-170">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="19ca7-171">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="19ca7-171">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="19ca7-172">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="19ca7-172">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="19ca7-173">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="19ca7-173">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19ca7-174">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="19ca7-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19ca7-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-177">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="19ca7-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-178">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="19ca7-178">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="19ca7-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="19ca7-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19ca7-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19ca7-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19ca7-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19ca7-182">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="19ca7-182">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="19ca7-183">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="19ca7-183">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19ca7-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19ca7-184">Remarks</span></span>

<span data-ttu-id="19ca7-185">Класс **CIM \_ жобдестинатион** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="19ca7-185">The **CIM\_JobDestination** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="19ca7-186">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="19ca7-186">WMI does not implement this class.</span></span>

<span data-ttu-id="19ca7-187">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="19ca7-187">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="19ca7-188">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="19ca7-188">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ca7-189">Требования</span><span class="sxs-lookup"><span data-stu-id="19ca7-189">Requirements</span></span>



| <span data-ttu-id="19ca7-190">Требование</span><span class="sxs-lookup"><span data-stu-id="19ca7-190">Requirement</span></span> | <span data-ttu-id="19ca7-191">Значение</span><span class="sxs-lookup"><span data-stu-id="19ca7-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19ca7-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19ca7-192">Minimum supported client</span></span><br/> | <span data-ttu-id="19ca7-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19ca7-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19ca7-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19ca7-194">Minimum supported server</span></span><br/> | <span data-ttu-id="19ca7-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19ca7-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19ca7-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="19ca7-196">Namespace</span></span><br/>                | <span data-ttu-id="19ca7-197">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19ca7-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19ca7-198">MOF</span><span class="sxs-lookup"><span data-stu-id="19ca7-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19ca7-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19ca7-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19ca7-200">DLL</span><span class="sxs-lookup"><span data-stu-id="19ca7-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19ca7-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19ca7-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ca7-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19ca7-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ca7-203">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="19ca7-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

