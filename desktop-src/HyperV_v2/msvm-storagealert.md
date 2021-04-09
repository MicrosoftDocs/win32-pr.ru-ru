---
description: Представляет событие, которое вызывается каждый раз при изменении свойства OperationalStatus класса Мсвм \_ ResourcePool или мсвм \_ LogicalDisk.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Класс Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081076"
---
# <a name="msvm_storagealert-class"></a><span data-ttu-id="b59f2-103">\_Класс мсвм сторажеалерт</span><span class="sxs-lookup"><span data-stu-id="b59f2-103">Msvm\_StorageAlert class</span></span>

<span data-ttu-id="b59f2-104">Представляет событие, которое вызывается каждый раз при изменении свойства **OperationalStatus** класса [**Мсвм \_ ResourcePool**](msvm-resourcepool.md) или [**мсвм \_ LogicalDisk**](msvm-logicaldisk.md) .</span><span class="sxs-lookup"><span data-stu-id="b59f2-104">Represents an event that is raised each time the **OperationalStatus** property of the [**Msvm\_ResourcePool**](msvm-resourcepool.md) or [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) class changes.</span></span>

<span data-ttu-id="b59f2-105">Следующий синтаксис упрощен из MOF-кода и включает эти свойства.</span><span class="sxs-lookup"><span data-stu-id="b59f2-105">The following syntax is simplified from MOF code and includes these properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b59f2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b59f2-106">Syntax</span></span>

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a><span data-ttu-id="b59f2-107">Члены</span><span class="sxs-lookup"><span data-stu-id="b59f2-107">Members</span></span>

<span data-ttu-id="b59f2-108">Класс **мсвм \_ сторажеалерт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b59f2-108">The **Msvm\_StorageAlert** class has these types of members:</span></span>

-   [<span data-ttu-id="b59f2-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="b59f2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b59f2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b59f2-110">Properties</span></span>

<span data-ttu-id="b59f2-111">Класс **мсвм \_ сторажеалерт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b59f2-111">The **Msvm\_StorageAlert** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b59f2-112">**алертинжелементформат**</span><span class="sxs-lookup"><span data-stu-id="b59f2-112">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b59f2-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-115">Квалификаторы: **моделкорреспонденце** ("CIM \_ алертиндикатион. алертингманажеделемент", "CIM \_ алертиндикатион. осералертинжелементформат")</span><span class="sxs-lookup"><span data-stu-id="b59f2-115">Qualifiers: **ModelCorrespondence** ("CIM\_AlertIndication.AlertingManagedElement", "CIM\_AlertIndication.OtherAlertingElementFormat")</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-116">Задает формат свойства **алертингманажеделемент** .</span><span class="sxs-lookup"><span data-stu-id="b59f2-116">Specifies the format of the **AlertingManagedElement** property.</span></span> <span data-ttu-id="b59f2-117">Формат — Цимобжектпас с форматом *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, который указывает экземпляр в схеме CIM.</span><span class="sxs-lookup"><span data-stu-id="b59f2-117">The format is a CIMObjectPath, with the format *<NamespacePath>:<ClassName>.<Prop1>=\\"<Value1>\\", "<Prop2>=\\"<Value2>\\"*, which specifies an instance in the CIM Schema.</span></span>

<span data-ttu-id="b59f2-118">Это свойство наследуется от класса **CIM \_ алертиндикатион** .</span><span class="sxs-lookup"><span data-stu-id="b59f2-118">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

<span data-ttu-id="b59f2-119">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b59f2-119">The possible values are:</span></span>

<dl> <dt>

<span data-ttu-id="b59f2-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b59f2-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b59f2-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Цимобжектпас** (2)</span><span class="sxs-lookup"><span data-stu-id="b59f2-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b59f2-123">**алертингманажеделемент**</span><span class="sxs-lookup"><span data-stu-id="b59f2-123">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-124">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="b59f2-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-126">Пути WMI экземпляра, для которого создается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="b59f2-126">The WMI paths of the instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="b59f2-127">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="b59f2-127">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b59f2-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-130">Указывает основную классификацию предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b59f2-130">Specifies the primary classification of the alert.</span></span> <span data-ttu-id="b59f2-131">Возможные значения этого свойства:</span><span class="sxs-lookup"><span data-stu-id="b59f2-131">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="b59f2-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Предупреждение качества обслуживания** (3)</span><span class="sxs-lookup"><span data-stu-id="b59f2-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b59f2-133">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="b59f2-133">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-134">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b59f2-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-136">Дата и время обнаружения базового события.</span><span class="sxs-lookup"><span data-stu-id="b59f2-136">The date and time at which the underlying event was detected.</span></span>

</dd> <dt>

<span data-ttu-id="b59f2-137">**Message**</span><span class="sxs-lookup"><span data-stu-id="b59f2-137">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b59f2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-140">Форматированное сообщение, созданное путем объединения некоторых или всех динамических элементов, указанных в свойстве **мессажеаргументс** , со статическими элементами, однозначно идентифицируемыми свойством **MessageId** в реестре сообщений или в другом каталоге, связанном со свойством **овнинжентити** .</span><span class="sxs-lookup"><span data-stu-id="b59f2-140">A formatted message that is constructed by combining some or all of the dynamic elements that are specified in the **MessageArguments** property with the static elements uniquely identified by the **MessageID** property in a message registry or other catalog associated with the **OwningEntity** property.</span></span>

</dd> <dt>

<span data-ttu-id="b59f2-141">**мессажеаргументс**</span><span class="sxs-lookup"><span data-stu-id="b59f2-141">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-142">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="b59f2-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-144">Массив, содержащий динамическое содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="b59f2-144">An array that contains the dynamic content of the message.</span></span> <span data-ttu-id="b59f2-145">Если значение **MessageId** равно 32930, аргумент в позиции 0 является **Пулидом** экземпляра [**мсвм \_ ResourcePool**](msvm-resourcepoolcomponent.md) , для которого создается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="b59f2-145">If the value of **MessageID** is 32930, the argument at position 0 is the **PoolID** of the [**Msvm\_ResourcePool**](msvm-resourcepoolcomponent.md) instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="b59f2-146">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="b59f2-146">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b59f2-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-149">Однозначно определяет в области свойства **овнинжентити** формат свойства **Message** .</span><span class="sxs-lookup"><span data-stu-id="b59f2-149">Uniquely identifies, within the scope of the **OwningEntity** property, the format of the **Message** property.</span></span> <span data-ttu-id="b59f2-150">Возможные значения этого свойства:</span><span class="sxs-lookup"><span data-stu-id="b59f2-150">The possible values for this property are:</span></span>

<span data-ttu-id="b59f2-151">32930 ("недостаточное сообщение о пропускной способности для пула носителей")</span><span class="sxs-lookup"><span data-stu-id="b59f2-151">32930 ("Storage Pool QoS Insufficient Throughput Message")</span></span>

</dd> <dt>

<span data-ttu-id="b59f2-152">**осералертинжелементформат**</span><span class="sxs-lookup"><span data-stu-id="b59f2-152">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b59f2-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-155">Строка, которая определяет значения "Other" для **алертингманажеделемент**.</span><span class="sxs-lookup"><span data-stu-id="b59f2-155">A string that defines "Other" values for **AlertingManagedElement**.</span></span> <span data-ttu-id="b59f2-156">Это значение должно быть задано как значение, отличное от NULL, если для **алертингманажеделемент** задано значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="b59f2-156">This value MUST be set to a non NULL value when **AlertingManagedElement** is set to a value of 1 ("Other").</span></span> <span data-ttu-id="b59f2-157">Для всех остальных значений **алертингманажеделемент** значение этой строки должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="b59f2-157">For all other values of **AlertingManagedElement**, the value of this string must be set to NULL.</span></span>

<span data-ttu-id="b59f2-158">Это свойство наследуется от класса **CIM \_ алертиндикатион** .</span><span class="sxs-lookup"><span data-stu-id="b59f2-158">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

</dd> <dt>

<span data-ttu-id="b59f2-159">**овнинжентити**</span><span class="sxs-lookup"><span data-stu-id="b59f2-159">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b59f2-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-162">Однозначно определяет сущность, которая владеет определением формата **сообщения** , описанного в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="b59f2-162">Uniquely identifies the entity that owns the definition of the format of the **Message** described in this instance.</span></span> <span data-ttu-id="b59f2-163">Значение этого свойства всегда равно "Microsoft-Windows-Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="b59f2-163">The value of this property is always "Microsoft-Windows- Hyper-V."</span></span>

<span data-ttu-id="b59f2-164">"Microsoft-Windows-Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="b59f2-164">"Microsoft-Windows- Hyper-V"</span></span>

</dd> <dt>

<span data-ttu-id="b59f2-165">**перцеиведсеверити**</span><span class="sxs-lookup"><span data-stu-id="b59f2-165">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b59f2-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-168">Описывает серьезность индикации предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b59f2-168">Describes the severity of the alert indication.</span></span> <span data-ttu-id="b59f2-169">Возможные значения этого свойства:</span><span class="sxs-lookup"><span data-stu-id="b59f2-169">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="b59f2-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Информация** (2)</span><span class="sxs-lookup"><span data-stu-id="b59f2-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Снижение уровня работоспособности/предупреждение** (3)</span><span class="sxs-lookup"><span data-stu-id="b59f2-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b59f2-172">**пробаблекаусе**</span><span class="sxs-lookup"><span data-stu-id="b59f2-172">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-173">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b59f2-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-175">Описывает возможную причину ситуации, которая привела к появлению предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b59f2-175">Describes the probable cause of the situation that resulted in the alert indication.</span></span>

<dl> <dt>

<span data-ttu-id="b59f2-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Проблема с емкостью хранилища** (50)</span><span class="sxs-lookup"><span data-stu-id="b59f2-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Предыдущее оповещение сброшено** (59)</span><span class="sxs-lookup"><span data-stu-id="b59f2-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b59f2-178">**пробаблекауседескриптион**</span><span class="sxs-lookup"><span data-stu-id="b59f2-178">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b59f2-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b59f2-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b59f2-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b59f2-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b59f2-181">Текстовое описание, соответствующее значению свойства **пробаблекаусе** .</span><span class="sxs-lookup"><span data-stu-id="b59f2-181">A textual description that corresponds to the value of the **ProbableCause** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b59f2-182">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b59f2-182">Remarks</span></span>

<span data-ttu-id="b59f2-183">Поставщик WMI Hyper-V не будет создавать события для отдельных виртуальных дисков, чтобы избежать перегрузки клиентов с событиями в случае крупномасштабных неисправностей базовых систем хранения.</span><span class="sxs-lookup"><span data-stu-id="b59f2-183">The Hyper-V WMI provider won't raise events for individual virtual disks to avoid flooding clients with events in case of large scale malfunctions of the underlying storage systems.</span></span>

<span data-ttu-id="b59f2-184">Когда клиент получает событие **мсвм \_ сторажеалерт** , если значение свойства **Пробаблекаусе** равно 50 (проблема с емкостью хранилища), клиент может обнаружить, какие виртуальные диски работают за пределами политики качества обслуживания с помощью одной из следующих процедур:</span><span class="sxs-lookup"><span data-stu-id="b59f2-184">When a client receives an **Msvm\_StorageAlert** event, if the value of the **ProbableCause** property is 50 ( Storage Capacity Problem ), the client can discover which virtual disks are operating outside their QoS policy by using one of these procedures:</span></span>

-   <span data-ttu-id="b59f2-185">Запросите все экземпляры [**мсвм \_ LogicalDisk**](msvm-logicaldisk.md) , которые были выделены из пула ресурсов, для которого было создано событие.</span><span class="sxs-lookup"><span data-stu-id="b59f2-185">Query all the [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) instances that were allocated from the resource pool for which the event was generated.</span></span> <span data-ttu-id="b59f2-186">Эти экземпляры **мсвм \_ LogicalDisk** связаны с пулом ресурсов через ассоциацию [**мсвм \_ елементаллокатедфромпул**](msvm-elementallocatedfrompool.md) .</span><span class="sxs-lookup"><span data-stu-id="b59f2-186">These **Msvm\_LogicalDisk** instances are associated to the resource pool via the [**Msvm\_ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) association.</span></span>
-   <span data-ttu-id="b59f2-187">Отфильтруйте список результатов, выбрав экземпляры, для которых параметр OperationalStatus содержит недостаточную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="b59f2-187">Filter the result list by selecting instances whose OperationalStatus contains  Insufficient Throughput .</span></span>

## <a name="requirements"></a><span data-ttu-id="b59f2-188">Требования</span><span class="sxs-lookup"><span data-stu-id="b59f2-188">Requirements</span></span>



| <span data-ttu-id="b59f2-189">Требование</span><span class="sxs-lookup"><span data-stu-id="b59f2-189">Requirement</span></span> | <span data-ttu-id="b59f2-190">Значение</span><span class="sxs-lookup"><span data-stu-id="b59f2-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b59f2-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b59f2-191">Minimum supported client</span></span><br/> | <span data-ttu-id="b59f2-192">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b59f2-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b59f2-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b59f2-193">Minimum supported server</span></span><br/> | <span data-ttu-id="b59f2-194">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b59f2-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b59f2-195">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b59f2-195">Namespace</span></span><br/>                | <span data-ttu-id="b59f2-196">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b59f2-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b59f2-197">MOF</span><span class="sxs-lookup"><span data-stu-id="b59f2-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b59f2-198"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b59f2-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b59f2-199">DLL</span><span class="sxs-lookup"><span data-stu-id="b59f2-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b59f2-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b59f2-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b59f2-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b59f2-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59f2-202">**\_АЛЕРТИНДИКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="b59f2-202">**CIM\_AlertIndication**</span></span>](cim-alertindication.md)
</dt> <dt>

[<span data-ttu-id="b59f2-203">**Мсвм \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="b59f2-203">**Msvm\_LogicalDisk**</span></span>](msvm-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="b59f2-204">**Мсвм \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="b59f2-204">**Msvm\_ResourcePool**</span></span>](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




