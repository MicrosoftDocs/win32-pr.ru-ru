---
description: CIM \_ манажедсистемелемент является базовым классом для иерархии системных элементов. Любой компонент системы потенциально может быть представлен этим классом или его подклассами.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: Класс CIM_ManagedSystemElement (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265250"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a><span data-ttu-id="88ef5-104">Класс CIM_ManagedSystemElement (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="88ef5-104">CIM_ManagedSystemElement class (Hyper-V management)</span></span>

<span data-ttu-id="88ef5-105">**Модель CIM \_ Манажедсистемелемент** является базовым классом для иерархии системных элементов.</span><span class="sxs-lookup"><span data-stu-id="88ef5-105">**CIM\_ManagedSystemElement** is the base class for the system element hierarchy.</span></span> <span data-ttu-id="88ef5-106">Любой компонент системы потенциально может быть представлен этим классом или его подклассами.</span><span class="sxs-lookup"><span data-stu-id="88ef5-106">Any component of a system can potentially be represented by this class or its subclasses.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ef5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88ef5-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a><span data-ttu-id="88ef5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="88ef5-108">Members</span></span>

<span data-ttu-id="88ef5-109">Класс **CIM \_ манажедсистемелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88ef5-109">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="88ef5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="88ef5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88ef5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="88ef5-111">Properties</span></span>

<span data-ttu-id="88ef5-112">Класс **CIM \_ манажедсистемелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88ef5-112">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88ef5-113">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="88ef5-113">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88ef5-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-116">Указывает способность инструментирования взаимодействовать с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="88ef5-116">Indicates the ability of the instrumentation to communicate with this element.</span></span> <span data-ttu-id="88ef5-117">Значение **null** указывает, что инструментирование не поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="88ef5-117">A **NULL** value indicates that instrumentation does not support this property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ef5-118">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88ef5-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="88ef5-119">**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="88ef5-119">**Not Available** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

<span data-ttu-id="88ef5-120">**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="88ef5-120">**Communication OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="88ef5-121">**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="88ef5-121">**Lost Communication** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="88ef5-122">**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="88ef5-122">**No Contact** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88ef5-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="88ef5-124">**Поставщик зарезервирован** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-124">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ef5-125">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="88ef5-125">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88ef5-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-128">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**Примаристатус**","**CIM \_ манажедсистемелемент**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="88ef5-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-129">Указывает дополнительные сведения о состоянии, дополняющие свойство **примаристатус** .</span><span class="sxs-lookup"><span data-stu-id="88ef5-129">Indicates additional status details that complement the **PrimaryStatus** property.</span></span> <span data-ttu-id="88ef5-130">Значение **null** указывает, что инструментирование не поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="88ef5-130">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="88ef5-131">**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="88ef5-131">**Not Available** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

<span data-ttu-id="88ef5-132">**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="88ef5-132">**No Additional Information** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="88ef5-133">**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="88ef5-133">**Stressed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="88ef5-134">**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="88ef5-134">**Predictive Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="88ef5-135">**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="88ef5-135">**Non-Recoverable Error** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="88ef5-136">**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="88ef5-136">**Supporting Entity in Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88ef5-137">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="88ef5-138">**Поставщик зарезервирован** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-138">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ef5-139">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="88ef5-139">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88ef5-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-142">Указывает текущее состояние работоспособности элемента.</span><span class="sxs-lookup"><span data-stu-id="88ef5-142">Indicates the current health of the element.</span></span> <span data-ttu-id="88ef5-143">Этот атрибут выражает работоспособность этого элемента, но не обязательно является работоспособностью его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="88ef5-143">This attribute expresses the health of this element, but not necessarily the health of its subcomponents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ef5-144">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88ef5-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88ef5-145">**ОК** (5)</span><span class="sxs-lookup"><span data-stu-id="88ef5-145">**OK** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="88ef5-146">**Снижение уровня работоспособности или предупреждение** (10)</span><span class="sxs-lookup"><span data-stu-id="88ef5-146">**Degraded/Warning** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

<span data-ttu-id="88ef5-147">**Незначительная ошибка** (15)</span><span class="sxs-lookup"><span data-stu-id="88ef5-147">**Minor failure** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

<span data-ttu-id="88ef5-148">**Серьезный сбой** (20)</span><span class="sxs-lookup"><span data-stu-id="88ef5-148">**Major failure** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

<span data-ttu-id="88ef5-149">**Критический сбой** (25)</span><span class="sxs-lookup"><span data-stu-id="88ef5-149">**Critical failure** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="88ef5-150">**Неустранимая ошибка** (30)</span><span class="sxs-lookup"><span data-stu-id="88ef5-150">**Non-recoverable error** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88ef5-151">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-151">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ef5-152">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88ef5-152">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-153">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88ef5-153">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-155">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="88ef5-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-156">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="88ef5-156">Indicates when the object was installed.</span></span> <span data-ttu-id="88ef5-157">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="88ef5-157">The lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="88ef5-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88ef5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-161">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="88ef5-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-162">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="88ef5-162">The label by which the object is known.</span></span> <span data-ttu-id="88ef5-163">При создании подкласса свойство **Name** может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="88ef5-163">When subclassed, the **Name** property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="88ef5-164">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="88ef5-164">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88ef5-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-167">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="88ef5-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-168">Указывает текущее рабочее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="88ef5-168">Indicates the current operational condition of the element.</span></span> <span data-ttu-id="88ef5-169">Это свойство можно использовать для предоставления более подробных сведений о значении свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="88ef5-169">This property can be used to provide more detail about the value of the **EnabledState** property.</span></span> <span data-ttu-id="88ef5-170">Значение **null** указывает, что инструментирование не поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="88ef5-170">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<span data-ttu-id="88ef5-171">"Unknown" означает</span><span class="sxs-lookup"><span data-stu-id="88ef5-171">"Unknown" indicates</span></span>

<span data-ttu-id="88ef5-172">"Нет" означает, что</span><span class="sxs-lookup"><span data-stu-id="88ef5-172">"None" indicates that</span></span>

<span data-ttu-id="88ef5-173">Период</span><span class="sxs-lookup"><span data-stu-id="88ef5-173">"Servicing"</span></span>

<span data-ttu-id="88ef5-174">Start</span><span class="sxs-lookup"><span data-stu-id="88ef5-174">"Starting"</span></span>

<span data-ttu-id="88ef5-175">Идет</span><span class="sxs-lookup"><span data-stu-id="88ef5-175">"Stopping"</span></span>

<span data-ttu-id="88ef5-176">"Остановлено" и "прервано" похожи, хотя первый, а второй —</span><span class="sxs-lookup"><span data-stu-id="88ef5-176">"Stopped" and "Aborted" are similar, although the former , while the latter i</span></span>

<span data-ttu-id="88ef5-177">"Неактивный" означает, что</span><span class="sxs-lookup"><span data-stu-id="88ef5-177">"Dormant" indicates that</span></span>

<span data-ttu-id="88ef5-178">"Completed" означает, что t</span><span class="sxs-lookup"><span data-stu-id="88ef5-178">"Completed" indicates that t</span></span>

<span data-ttu-id="88ef5-179">Миграция</span><span class="sxs-lookup"><span data-stu-id="88ef5-179">"Migrating"</span></span>

<span data-ttu-id="88ef5-180">"Преобразование"</span><span class="sxs-lookup"><span data-stu-id="88ef5-180">"Immigrating"</span></span>

<span data-ttu-id="88ef5-181">"Емигратинг"</span><span class="sxs-lookup"><span data-stu-id="88ef5-181">"Emigrating"</span></span>

<span data-ttu-id="88ef5-182">"Завершение работы"</span><span class="sxs-lookup"><span data-stu-id="88ef5-182">"Shutting Down"</span></span>

<span data-ttu-id="88ef5-183">"В тесте"</span><span class="sxs-lookup"><span data-stu-id="88ef5-183">"In Test"</span></span>

<span data-ttu-id="88ef5-184">Переход</span><span class="sxs-lookup"><span data-stu-id="88ef5-184">"Transitioning"</span></span>

<span data-ttu-id="88ef5-185">"В службе"</span><span class="sxs-lookup"><span data-stu-id="88ef5-185">"In Service"</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ef5-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88ef5-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-187">Реализация в целом может возвращать это свойство, но в настоящее время это невозможно.</span><span class="sxs-lookup"><span data-stu-id="88ef5-187">The implementation is in general capable of returning this property, but is unable to do so at this time.</span></span>

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="88ef5-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="88ef5-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-189">Реализация (поставщик) может возвращать значение для этого свойства, но не всегда для данного конкретного фрагмента оборудования или программного обеспечения, либо свойство не используется, так как оно не имеет осмысленной информации (как в случае свойства, которое предназначено для добавления дополнительных сведений в другое свойство).</span><span class="sxs-lookup"><span data-stu-id="88ef5-189">The implementation (provider) is capable of returning a value for this property, but not ever for this particular piece of hardware/software or the property is intentionally not used because it adds no meaningful information (as in the case of a property that is intended to add additional info to another property).</span></span>

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span data-ttu-id="88ef5-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="88ef5-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-191">Описывает настраиваемый, обслуживаемый, очищенный или иным образом настроенный элемент.</span><span class="sxs-lookup"><span data-stu-id="88ef5-191">Describes an element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="88ef5-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="88ef5-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-193">Описывает инициализируемый элемент.</span><span class="sxs-lookup"><span data-stu-id="88ef5-193">Describes an element being initialized.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="88ef5-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="88ef5-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-195">Описывает элемент, который переносится в упорядоченную точку.</span><span class="sxs-lookup"><span data-stu-id="88ef5-195">Describes an element being brought to an orderly stop.</span></span>

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="88ef5-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="88ef5-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-197">Произошла чистая и упорядоченная Отмена.</span><span class="sxs-lookup"><span data-stu-id="88ef5-197">A clean and orderly stop has occurred.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="88ef5-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="88ef5-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-199">Произошла внезапно остановлена, где может потребоваться обновить состояние и конфигурацию элемента.</span><span class="sxs-lookup"><span data-stu-id="88ef5-199">An abrupt stop has occurred, where the state and configuration of the element might need to be updated.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="88ef5-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="88ef5-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-201">Элемент неактивен или заморожен.</span><span class="sxs-lookup"><span data-stu-id="88ef5-201">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="88ef5-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="88ef5-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-203">Элемент завершил операцию.</span><span class="sxs-lookup"><span data-stu-id="88ef5-203">The element has completed its operation.</span></span> <span data-ttu-id="88ef5-204">Это значение должно сочетаться с параметром "ОК", "ошибка" или "деградация" в Примаристатус, чтобы клиент мог определить, завершилась ли завершенная операция с "ОК" (пройдена), завершилась с ошибкой (сбой) или завершилась с пониженной работоспособностью (операция завершена, но она не была завершена или не сообщает об ошибке).</span><span class="sxs-lookup"><span data-stu-id="88ef5-204">This value should be combined with either OK, Error, or Degraded in the PrimaryStatus so that a client can tell if the complete operation Completed with OK (passed), Completed with Error (failed), or Completed with Degraded (the operation finished, but it did not complete OK or did not report an error).</span></span>

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span data-ttu-id="88ef5-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="88ef5-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-206">Элемент перемещается между ведущими элементами.</span><span class="sxs-lookup"><span data-stu-id="88ef5-206">The element is being moved between host elements.</span></span>

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span data-ttu-id="88ef5-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="88ef5-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-208">Элемент находится вне элемента host.</span><span class="sxs-lookup"><span data-stu-id="88ef5-208">The element is being moved away from host element.</span></span>

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span data-ttu-id="88ef5-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="88ef5-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-210">Элемент перемещается в новый ведущий элемент.</span><span class="sxs-lookup"><span data-stu-id="88ef5-210">The element is being moved to new host element.</span></span>

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span data-ttu-id="88ef5-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="88ef5-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="88ef5-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="88ef5-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-213">Описывает элемент, который приводит к внезапной ошибке.</span><span class="sxs-lookup"><span data-stu-id="88ef5-213">Describes an element being brought to an abrupt stop.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="88ef5-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="88ef5-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-215">Элемент выполняет тестовые функции.</span><span class="sxs-lookup"><span data-stu-id="88ef5-215">The element is performing test functions.</span></span>

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span data-ttu-id="88ef5-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="88ef5-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-217">Описывает элемент, который находится между состояниями, то есть он не полностью доступен в своем предыдущем состоянии или в следующем состоянии.</span><span class="sxs-lookup"><span data-stu-id="88ef5-217">Describes an element that is between states, that is, it is not fully available in either its previous state or its next state.</span></span> <span data-ttu-id="88ef5-218">Это значение следует использовать, если другие значения, указывающие на переход к определенному состоянию, неприменимы.</span><span class="sxs-lookup"><span data-stu-id="88ef5-218">This value should be used if other values indicating a transition to a specific state are not applicable.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="88ef5-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="88ef5-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-220">Описывает элемент, который находится в службе и работает.</span><span class="sxs-lookup"><span data-stu-id="88ef5-220">Describes an element that is in service and operational.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88ef5-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="88ef5-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ef5-223">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="88ef5-223">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-224">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="88ef5-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-226">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ манажедсистемелемент**.**Статусдескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="88ef5-226">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**StatusDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-227">Содержит индикаторы текущего состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="88ef5-227">Contains indicators of the current status of the element.</span></span> <span data-ttu-id="88ef5-228">Первое значение свойства **OperationalStatus** должно содержать первичное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="88ef5-228">The first value of the **OperationalStatus** property should contain the primary status for the element.</span></span>

> [!Note]  
> <span data-ttu-id="88ef5-229">Свойство **OperationalStatus** заменяет устаревшее свойство **Status** .</span><span class="sxs-lookup"><span data-stu-id="88ef5-229">The **OperationalStatus** property replaces the deprecated **Status** property.</span></span> <span data-ttu-id="88ef5-230">Из-за широкого использования свойства существующего **состояния** в приложениях управления настоятельно рекомендуется, чтобы поставщики или инструментирование предваряют свойства **Status** и **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="88ef5-230">Due to the widespread use of the existing **Status** property in management applications, we strongly recommend that providers or instrumentation provide both the **Status** and **OperationalStatus** properties.</span></span> <span data-ttu-id="88ef5-231">При инструментированном **состоянии**, так как это свойство с одним значением, должно также предоставлять первичное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="88ef5-231">When instrumented, **Status**, because it is a single-valued property, should also provide the primary status of the element.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ef5-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88ef5-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88ef5-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="88ef5-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88ef5-234"><span id="OK"></span><span id="ok"></span>**ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="88ef5-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88ef5-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (3)</span><span class="sxs-lookup"><span data-stu-id="88ef5-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="88ef5-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Напряженность** (4)</span><span class="sxs-lookup"><span data-stu-id="88ef5-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-237">Элемент работает, но требует внимания.</span><span class="sxs-lookup"><span data-stu-id="88ef5-237">The element is functioning, but needs attention.</span></span> <span data-ttu-id="88ef5-238">Примерами состояний "напряженный" являются перегрузка, перегрев и т. д.</span><span class="sxs-lookup"><span data-stu-id="88ef5-238">Examples of "Stressed" states are overload, overheated, and so on.</span></span>

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="88ef5-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (5)</span><span class="sxs-lookup"><span data-stu-id="88ef5-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (5)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-240">Элемент работает номинально, но прогнозирует сбой в ближайшем будущем.</span><span class="sxs-lookup"><span data-stu-id="88ef5-240">An element is functioning nominally but predicting a failure in the near future.</span></span>

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="88ef5-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="88ef5-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="88ef5-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (7)</span><span class="sxs-lookup"><span data-stu-id="88ef5-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="88ef5-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (8)</span><span class="sxs-lookup"><span data-stu-id="88ef5-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="88ef5-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (9)</span><span class="sxs-lookup"><span data-stu-id="88ef5-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="88ef5-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (10)</span><span class="sxs-lookup"><span data-stu-id="88ef5-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (10)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-246">Произошла упорядоченная Отмена.</span><span class="sxs-lookup"><span data-stu-id="88ef5-246">An orderly stop has occurred.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="88ef5-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (11)</span><span class="sxs-lookup"><span data-stu-id="88ef5-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-248">Элемент, который настраивается, сохраняется, очищается или управляется иным образом.</span><span class="sxs-lookup"><span data-stu-id="88ef5-248">An element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="88ef5-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (12)</span><span class="sxs-lookup"><span data-stu-id="88ef5-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-250">Система мониторинга имеет знания об этом элементе, но никогда не смогла установить связь с ним.</span><span class="sxs-lookup"><span data-stu-id="88ef5-250">The monitoring system has knowledge of this element, but has never been able to establish communications with it.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="88ef5-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (13)</span><span class="sxs-lookup"><span data-stu-id="88ef5-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-252">Известно, что элемент Манажедсистем существует и успешно подключен к прошлому, но сейчас недоступен.</span><span class="sxs-lookup"><span data-stu-id="88ef5-252">The ManagedSystem Element is known to exist and has been contacted successfully in the past, but is currently unreachable.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="88ef5-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (14)</span><span class="sxs-lookup"><span data-stu-id="88ef5-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (14)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-254">Произошла внезапно остановлена, где может потребоваться обновить состояние и конфигурацию элемента.</span><span class="sxs-lookup"><span data-stu-id="88ef5-254">An abrupt stop, where where the state and configuration of the element might need to be updated, has occurred.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="88ef5-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (15)</span><span class="sxs-lookup"><span data-stu-id="88ef5-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-256">Элемент неактивен или заморожен.</span><span class="sxs-lookup"><span data-stu-id="88ef5-256">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="88ef5-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (16)</span><span class="sxs-lookup"><span data-stu-id="88ef5-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-258">Этот элемент может иметь значение "ОК", но другой элемент, от которого он зависит, имеет ошибку.</span><span class="sxs-lookup"><span data-stu-id="88ef5-258">This element might be "OK" but that another element, on which it is dependent, is in error.</span></span> <span data-ttu-id="88ef5-259">Например, это сетевая служба или конечная точка, которая не может функционировать из-за проблем с сетью низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="88ef5-259">An example is a network service or endpoint that cannot function due to lower-layer networking problems.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="88ef5-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (17)</span><span class="sxs-lookup"><span data-stu-id="88ef5-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (17)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-261">Элемент завершил операцию.</span><span class="sxs-lookup"><span data-stu-id="88ef5-261">The element has completed its operation.</span></span>

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span data-ttu-id="88ef5-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Режим питания** (18)</span><span class="sxs-lookup"><span data-stu-id="88ef5-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Power Mode** (18)</span></span>


</dt> <dd>

<span data-ttu-id="88ef5-263">Элемент содержит дополнительные сведения о модели питания, содержащиеся в связанной ассоциации Поверманажементсервице.</span><span class="sxs-lookup"><span data-stu-id="88ef5-263">The element has additional power model information contained in the Associated PowerManagementService association.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88ef5-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="88ef5-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ef5-266">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="88ef5-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88ef5-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-269">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ манажедсистемелемент**.**Детаиледстатус**","**CIM \_ манажедсистемелемент**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="88ef5-269">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**DetailedStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-270">Указывает значение состояния высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="88ef5-270">Indicates a high-level status value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ef5-271">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88ef5-271">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88ef5-272">**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="88ef5-272">**OK** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88ef5-273">С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="88ef5-273">**Degraded** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="88ef5-274">**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="88ef5-274">**Error** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="88ef5-275">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-275">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="88ef5-276">**Поставщик зарезервирован** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="88ef5-276">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ef5-277">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="88ef5-277">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88ef5-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-280">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ манажедсистемелемент**.**OperationalStatus**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="88ef5-280">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-281">Указывает основное состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="88ef5-281">Indicates the primary status of the object.</span></span>

> [!Note]  
> <span data-ttu-id="88ef5-282">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="88ef5-282">This property is deprecated.</span></span> <span data-ttu-id="88ef5-283">Он заменяется свойством **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="88ef5-283">It is replaced by the **OperationalStatus** property.</span></span> <span data-ttu-id="88ef5-284">Если вы решили использовать свойство **Status** для обратной совместимости, оно должно быть вторичным для свойства **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="88ef5-284">If you choose to use the **Status** property for backward compatibility, it should be secondary to the **OperationalStatus** property.</span></span>

 

<dt>



 <span data-ttu-id="88ef5-285">("ОК")</span><span class="sxs-lookup"><span data-stu-id="88ef5-285">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-286">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="88ef5-286">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-287">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="88ef5-287">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-288">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="88ef5-288">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-289">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="88ef5-289">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-290">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="88ef5-290">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-291">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="88ef5-291">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-292">("Служба")</span><span class="sxs-lookup"><span data-stu-id="88ef5-292">("Service")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-293">("Напряженный")</span><span class="sxs-lookup"><span data-stu-id="88ef5-293">("Stressed")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-294">("Невосстановление")</span><span class="sxs-lookup"><span data-stu-id="88ef5-294">("NonRecover")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-295">("Нет контакта")</span><span class="sxs-lookup"><span data-stu-id="88ef5-295">("No Contact")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-296">("Потерянный канал связи")</span><span class="sxs-lookup"><span data-stu-id="88ef5-296">("Lost Comm")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88ef5-297">("Остановлено")</span><span class="sxs-lookup"><span data-stu-id="88ef5-297">("Stopped")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ef5-298">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="88ef5-298">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ef5-299">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="88ef5-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88ef5-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ef5-301">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ манажедсистемелемент**.**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="88ef5-301">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="88ef5-302">Указывает описания соответствующих значений в массиве **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="88ef5-302">Indicates descriptions of the corresponding values in the **OperationalStatus** array.</span></span> <span data-ttu-id="88ef5-303">Например, если элемент в свойстве **OperationalStatus** содержит значение Stopped, то элемент в том же индексе массива в этом свойстве может содержать пояснения **к остановке** объекта.</span><span class="sxs-lookup"><span data-stu-id="88ef5-303">For example, if an element in the **OperationalStatus** property contains the value **Stopping**, then the element at the same array index in this property might contain an explanation as to why an object is being stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88ef5-304">Требования</span><span class="sxs-lookup"><span data-stu-id="88ef5-304">Requirements</span></span>



| <span data-ttu-id="88ef5-305">Требование</span><span class="sxs-lookup"><span data-stu-id="88ef5-305">Requirement</span></span> | <span data-ttu-id="88ef5-306">Значение</span><span class="sxs-lookup"><span data-stu-id="88ef5-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ef5-307">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88ef5-307">Minimum supported client</span></span><br/> | <span data-ttu-id="88ef5-308">Windows 8</span><span class="sxs-lookup"><span data-stu-id="88ef5-308">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="88ef5-309">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88ef5-309">Minimum supported server</span></span><br/> | <span data-ttu-id="88ef5-310">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88ef5-310">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="88ef5-311">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88ef5-311">Namespace</span></span><br/>                | <span data-ttu-id="88ef5-312">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="88ef5-312">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="88ef5-313">MOF</span><span class="sxs-lookup"><span data-stu-id="88ef5-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88ef5-314"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88ef5-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88ef5-315">DLL</span><span class="sxs-lookup"><span data-stu-id="88ef5-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88ef5-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88ef5-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88ef5-317">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88ef5-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ef5-318">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="88ef5-318">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

