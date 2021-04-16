---
description: Представляет узел виртуальной системы на основе неоднородного доступа к памяти (NUMA).
ms.assetid: a2e9aa74-15e5-4a78-b7f8-ffe2883a31d0
title: Класс Msvm_NumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NumaNode
- Msvm_NumaNode.RequestStateChange
- Msvm_NumaNode.InstanceID
- Msvm_NumaNode.Caption
- Msvm_NumaNode.Description
- Msvm_NumaNode.ElementName
- Msvm_NumaNode.InstallDate
- Msvm_NumaNode.Name
- Msvm_NumaNode.OperationalStatus
- Msvm_NumaNode.StatusDescriptions
- Msvm_NumaNode.Status
- Msvm_NumaNode.HealthState
- Msvm_NumaNode.CommunicationStatus
- Msvm_NumaNode.DetailedStatus
- Msvm_NumaNode.OperatingStatus
- Msvm_NumaNode.PrimaryStatus
- Msvm_NumaNode.EnabledState
- Msvm_NumaNode.OtherEnabledState
- Msvm_NumaNode.RequestedState
- Msvm_NumaNode.EnabledDefault
- Msvm_NumaNode.TimeOfLastStateChange
- Msvm_NumaNode.AvailableRequestedStates
- Msvm_NumaNode.TransitioningToState
- Msvm_NumaNode.SystemCreationClassName
- Msvm_NumaNode.SystemName
- Msvm_NumaNode.CreationClassName
- Msvm_NumaNode.NodeID
- Msvm_NumaNode.NumberOfProcessorCores
- Msvm_NumaNode.NumberOfLogicalProcessors
- Msvm_NumaNode.CurrentlyConsumableMemoryBlocks
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4bdbd600cd4a78f66376f21ee264b2dfe9854147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664506"
---
# <a name="msvm_numanode-class"></a><span data-ttu-id="494ec-103">\_Класс мсвм NumaNode</span><span class="sxs-lookup"><span data-stu-id="494ec-103">Msvm\_NumaNode class</span></span>

<span data-ttu-id="494ec-104">Представляет узел виртуальной системы на основе неоднородного доступа к памяти (NUMA).</span><span class="sxs-lookup"><span data-stu-id="494ec-104">Represents a Non-Uniform Memory Access (NUMA) node of a virtual system.</span></span>

<span data-ttu-id="494ec-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="494ec-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="494ec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="494ec-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_NumaNode : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NodeID;
  uint32   NumberOfProcessorCores;
  uint32   NumberOfLogicalProcessors;
  uint64   CurrentlyConsumableMemoryBlocks;
};
```

## <a name="members"></a><span data-ttu-id="494ec-107">Члены</span><span class="sxs-lookup"><span data-stu-id="494ec-107">Members</span></span>

<span data-ttu-id="494ec-108">Класс **мсвм \_ NumaNode** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="494ec-108">The **Msvm\_NumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="494ec-109">Методы</span><span class="sxs-lookup"><span data-stu-id="494ec-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="494ec-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="494ec-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="494ec-111">Методы</span><span class="sxs-lookup"><span data-stu-id="494ec-111">Methods</span></span>

<span data-ttu-id="494ec-112">Класс **мсвм \_ NumaNode** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="494ec-112">The **Msvm\_NumaNode** class has these methods.</span></span>



| <span data-ttu-id="494ec-113">Метод</span><span class="sxs-lookup"><span data-stu-id="494ec-113">Method</span></span>                 | <span data-ttu-id="494ec-114">Описание</span><span class="sxs-lookup"><span data-stu-id="494ec-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="494ec-115">**Равен**</span><span class="sxs-lookup"><span data-stu-id="494ec-115">**RequestStateChange**</span></span> | <span data-ttu-id="494ec-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="494ec-116">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="494ec-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="494ec-117">Properties</span></span>

<span data-ttu-id="494ec-118">Класс **мсвм \_ NumaNode** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="494ec-118">The **Msvm\_NumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="494ec-119">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="494ec-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-120">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="494ec-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="494ec-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-122">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="494ec-122">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="494ec-123">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="494ec-123">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="494ec-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-127">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="494ec-127">A short description of the object.</span></span> <span data-ttu-id="494ec-128">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-129">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="494ec-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-132">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="494ec-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="494ec-133">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="494ec-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="494ec-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="494ec-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="494ec-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="494ec-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="494ec-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="494ec-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="494ec-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="494ec-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="494ec-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="494ec-142">)</span><span class="sxs-lookup"><span data-stu-id="494ec-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="494ec-143">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="494ec-143">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="494ec-146">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="494ec-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="494ec-147">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="494ec-147">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-148">**куррентликонсумаблемемориблоккс**</span><span class="sxs-lookup"><span data-stu-id="494ec-148">**CurrentlyConsumableMemoryBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-149">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="494ec-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-151">Количество блоков памяти, доступных для использования виртуальными машинами в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="494ec-151">The number of memory blocks currently available for consumption by virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-152">**Описание**</span><span class="sxs-lookup"><span data-stu-id="494ec-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-155">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="494ec-155">A description of the object.</span></span> <span data-ttu-id="494ec-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="494ec-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-158">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-160">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="494ec-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="494ec-161">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="494ec-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="494ec-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="494ec-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="494ec-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="494ec-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="494ec-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="494ec-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="494ec-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="494ec-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="494ec-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="494ec-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="494ec-171">)</span><span class="sxs-lookup"><span data-stu-id="494ec-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="494ec-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="494ec-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-175">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="494ec-175">A display name for the object.</span></span> <span data-ttu-id="494ec-176">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-177">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="494ec-177">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-178">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-180">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="494ec-180">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="494ec-181">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="494ec-181">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-182">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="494ec-182">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-183">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-185">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="494ec-185">The enabled and disabled states of an element.</span></span> <span data-ttu-id="494ec-186">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="494ec-186">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="494ec-187">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="494ec-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="494ec-188">Значение</span><span class="sxs-lookup"><span data-stu-id="494ec-188">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="494ec-189">Значение</span><span class="sxs-lookup"><span data-stu-id="494ec-189">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="494ec-190"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-190"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="494ec-191">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="494ec-191">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="494ec-192"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-192"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="494ec-193"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-193"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="494ec-194">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="494ec-194">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="494ec-195"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-195"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="494ec-196">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="494ec-196">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="494ec-197"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-197"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="494ec-198">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="494ec-198">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="494ec-199"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="494ec-200">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="494ec-200">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="494ec-201"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="494ec-202">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="494ec-202">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="494ec-203"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-203"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="494ec-204">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="494ec-204">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="494ec-205"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-205"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="494ec-206">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="494ec-206">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="494ec-207"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-207"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="494ec-208">Элемент включен, но находится в ограниченном режиме.</span><span class="sxs-lookup"><span data-stu-id="494ec-208">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="494ec-209">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="494ec-209">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="494ec-210">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="494ec-210">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="494ec-211"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-211"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="494ec-212">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="494ec-212">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="494ec-213">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="494ec-213">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="494ec-214">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="494ec-214">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-215">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-217">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="494ec-217">The current health of the element.</span></span> <span data-ttu-id="494ec-218">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="494ec-218">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="494ec-219">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="494ec-219">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="494ec-220">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="494ec-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-221">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="494ec-221">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-222">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="494ec-222">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-224">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="494ec-224">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="494ec-225">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-226">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="494ec-226">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="494ec-229">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="494ec-229">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="494ec-230">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="494ec-230">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="494ec-231">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-232">**Name**</span><span class="sxs-lookup"><span data-stu-id="494ec-232">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-235">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="494ec-235">The label by which the object is known.</span></span> <span data-ttu-id="494ec-236">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-237">**NodeID**</span><span class="sxs-lookup"><span data-stu-id="494ec-237">**NodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-238">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="494ec-240">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="494ec-240">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="494ec-241">Идентификатор узла NUMA.</span><span class="sxs-lookup"><span data-stu-id="494ec-241">The NUMA node identifier.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-242">**нумберофлогикалпроцессорс**</span><span class="sxs-lookup"><span data-stu-id="494ec-242">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-243">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="494ec-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-245">Общее число ядер логических процессоров в этом узле.</span><span class="sxs-lookup"><span data-stu-id="494ec-245">The total number of logical processor cores in this node.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-246">**NumberOfProcessorCores**</span><span class="sxs-lookup"><span data-stu-id="494ec-246">**NumberOfProcessorCores**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-247">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="494ec-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-249">Общее число ядер процессора в этом узле NUMA.</span><span class="sxs-lookup"><span data-stu-id="494ec-249">The total number of processor cores in this NUMA node.</span></span> <span data-ttu-id="494ec-250">Это может отличаться от количества объектов [**\_ процессора мсвм**](msvm-processor.md) , связанных с этим узлом, если каждый процессорный ядро поддерживает несколько потоков вычислений.</span><span class="sxs-lookup"><span data-stu-id="494ec-250">This may differ from the number of [**Msvm\_Processor**](msvm-processor.md) objects associated to this node if each processor core supports multiple compute threads.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-251">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="494ec-251">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-252">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-254">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="494ec-254">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="494ec-255">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="494ec-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="494ec-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="494ec-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="494ec-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="494ec-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="494ec-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="494ec-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="494ec-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="494ec-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="494ec-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="494ec-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="494ec-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="494ec-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="494ec-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="494ec-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="494ec-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="494ec-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="494ec-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="494ec-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="494ec-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="494ec-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="494ec-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="494ec-276">)</span><span class="sxs-lookup"><span data-stu-id="494ec-276">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="494ec-277">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="494ec-277">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-278">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="494ec-278">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="494ec-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-280">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="494ec-280">The current statuses of the object.</span></span> <span data-ttu-id="494ec-281">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-282">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="494ec-282">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-283">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-285">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="494ec-285">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="494ec-286">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="494ec-286">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="494ec-287">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="494ec-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-288">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="494ec-288">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-289">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-291">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="494ec-291">Provides high level status information.</span></span> <span data-ttu-id="494ec-292">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="494ec-292">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="494ec-293">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="494ec-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="494ec-294">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="494ec-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="494ec-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-296"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="494ec-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="494ec-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="494ec-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="494ec-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="494ec-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="494ec-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="494ec-301">)</span><span class="sxs-lookup"><span data-stu-id="494ec-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="494ec-302">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="494ec-302">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-303">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-305">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="494ec-305">The last requested or desired state for the element.</span></span> <span data-ttu-id="494ec-306">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="494ec-306">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="494ec-307">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="494ec-307">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="494ec-308">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="494ec-308">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="494ec-309">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="494ec-309">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="494ec-310">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="494ec-310">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-311">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="494ec-311">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="494ec-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-315">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="494ec-315">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-316">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="494ec-316">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="494ec-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-318">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="494ec-318">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="494ec-319">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="494ec-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="494ec-320">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="494ec-320">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="494ec-323">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="494ec-323">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="494ec-324">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="494ec-324">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-325">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="494ec-325">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="494ec-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="494ec-328">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="494ec-328">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="494ec-329">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="494ec-329">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="494ec-330">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="494ec-330">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-331">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="494ec-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-333">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="494ec-333">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="494ec-334">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение "null".</span><span class="sxs-lookup"><span data-stu-id="494ec-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="494ec-335">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="494ec-335">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="494ec-336">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="494ec-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="494ec-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="494ec-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="494ec-338">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="494ec-338">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="494ec-339">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="494ec-339">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="494ec-340">Требования</span><span class="sxs-lookup"><span data-stu-id="494ec-340">Requirements</span></span>



| <span data-ttu-id="494ec-341">Требование</span><span class="sxs-lookup"><span data-stu-id="494ec-341">Requirement</span></span> | <span data-ttu-id="494ec-342">Значение</span><span class="sxs-lookup"><span data-stu-id="494ec-342">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="494ec-343">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="494ec-343">Minimum supported client</span></span><br/> | <span data-ttu-id="494ec-344">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="494ec-344">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="494ec-345">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="494ec-345">Minimum supported server</span></span><br/> | <span data-ttu-id="494ec-346">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="494ec-346">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="494ec-347">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="494ec-347">Namespace</span></span><br/>                | <span data-ttu-id="494ec-348">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="494ec-348">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="494ec-349">MOF</span><span class="sxs-lookup"><span data-stu-id="494ec-349">MOF</span></span><br/>                      | <dl> <span data-ttu-id="494ec-350"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-350"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="494ec-351">DLL</span><span class="sxs-lookup"><span data-stu-id="494ec-351">DLL</span></span><br/>                      | <dl> <span data-ttu-id="494ec-352"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="494ec-352"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

