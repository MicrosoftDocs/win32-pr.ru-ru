---
description: Предоставляет возможность управлять метриками.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Класс Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684470"
---
# <a name="msvm_metricservice-class"></a><span data-ttu-id="88c78-103">\_Класс мсвм метриксервице</span><span class="sxs-lookup"><span data-stu-id="88c78-103">Msvm\_MetricService class</span></span>

<span data-ttu-id="88c78-104">Предоставляет возможность управлять метриками.</span><span class="sxs-lookup"><span data-stu-id="88c78-104">Provides the ability to manage metrics.</span></span>

<span data-ttu-id="88c78-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="88c78-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c78-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88c78-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="88c78-107">Члены</span><span class="sxs-lookup"><span data-stu-id="88c78-107">Members</span></span>

<span data-ttu-id="88c78-108">Класс **мсвм \_ метриксервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88c78-108">The **Msvm\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="88c78-109">Методы</span><span class="sxs-lookup"><span data-stu-id="88c78-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="88c78-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="88c78-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88c78-111">Методы</span><span class="sxs-lookup"><span data-stu-id="88c78-111">Methods</span></span>

<span data-ttu-id="88c78-112">Класс **мсвм \_ метриксервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="88c78-112">The **Msvm\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="88c78-113">Метод</span><span class="sxs-lookup"><span data-stu-id="88c78-113">Method</span></span>                                                                    | <span data-ttu-id="88c78-114">Описание</span><span class="sxs-lookup"><span data-stu-id="88c78-114">Description</span></span>                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="88c78-115">**контролметрикс**</span><span class="sxs-lookup"><span data-stu-id="88c78-115">**ControlMetrics**</span></span>](controlmetrics-msvm-metricservice.md)               | <span data-ttu-id="88c78-116">Используется для управления сбором метрик для управляемого элемента или элементов.</span><span class="sxs-lookup"><span data-stu-id="88c78-116">Used to control the collection of metrics for a managed element or elements.</span></span><br/> |
| [<span data-ttu-id="88c78-117">**контролметриксбикласс**</span><span class="sxs-lookup"><span data-stu-id="88c78-117">**ControlMetricsByClass**</span></span>](msvm-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="88c78-118">Управляет метриками по классу.</span><span class="sxs-lookup"><span data-stu-id="88c78-118">Controls the metrics by class.</span></span><br/>                                               |
| [<span data-ttu-id="88c78-119">**контролсамплетимес**</span><span class="sxs-lookup"><span data-stu-id="88c78-119">**ControlSampleTimes**</span></span>](msvm-metricservice-controlsampletimes.md)       | <span data-ttu-id="88c78-120">Задает время в образце элемента управления.</span><span class="sxs-lookup"><span data-stu-id="88c78-120">Sets the control sample times.</span></span><br/>                                               |
| [<span data-ttu-id="88c78-121">**жетметриквалуес**</span><span class="sxs-lookup"><span data-stu-id="88c78-121">**GetMetricValues**</span></span>](msvm-metricservice-getmetricvalues.md)             | <span data-ttu-id="88c78-122">Извлекает значения метрик.</span><span class="sxs-lookup"><span data-stu-id="88c78-122">Retrieves the metric values.</span></span><br/>                                                 |
| [<span data-ttu-id="88c78-123">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="88c78-123">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md) | <span data-ttu-id="88c78-124">Изменяет данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="88c78-124">Modifies the setting data for the service.</span></span><br/>                                   |
| [<span data-ttu-id="88c78-125">**Равен**</span><span class="sxs-lookup"><span data-stu-id="88c78-125">**RequestStateChange**</span></span>](msvm-metricservice-requeststatechange.md)       | <span data-ttu-id="88c78-126">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="88c78-126">Requests a state change.</span></span><br/>                                                     |
| [<span data-ttu-id="88c78-127">**шовметрикс**</span><span class="sxs-lookup"><span data-stu-id="88c78-127">**ShowMetrics**</span></span>](msvm-metricservice-showmetrics.md)                     | <span data-ttu-id="88c78-128">Показывает указанные метрики.</span><span class="sxs-lookup"><span data-stu-id="88c78-128">Shows the specified metrics.</span></span><br/>                                                 |
| [<span data-ttu-id="88c78-129">**шовметриксбикласс**</span><span class="sxs-lookup"><span data-stu-id="88c78-129">**ShowMetricsByClass**</span></span>](msvm-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="88c78-130">Показывает метрики по классу.</span><span class="sxs-lookup"><span data-stu-id="88c78-130">Shows the metrics by class.</span></span><br/>                                                  |
| [<span data-ttu-id="88c78-131">**StartService**</span><span class="sxs-lookup"><span data-stu-id="88c78-131">**StartService**</span></span>](msvm-metricservice-startservice.md)                   | <span data-ttu-id="88c78-132">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="88c78-132">Starts the service.</span></span><br/>                                                          |
| [<span data-ttu-id="88c78-133">**StopService**</span><span class="sxs-lookup"><span data-stu-id="88c78-133">**StopService**</span></span>](msvm-metricservice-stopservice.md)                     | <span data-ttu-id="88c78-134">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="88c78-134">Stops the service.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="88c78-135">Свойства</span><span class="sxs-lookup"><span data-stu-id="88c78-135">Properties</span></span>

<span data-ttu-id="88c78-136">Класс **мсвм \_ метриксервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88c78-136">The **Msvm\_MetricService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88c78-137">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="88c78-137">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-138">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="88c78-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88c78-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-140">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="88c78-140">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="88c78-141">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88c78-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-142">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="88c78-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-145">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88c78-145">A short description of the object.</span></span> <span data-ttu-id="88c78-146">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="88c78-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-147">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="88c78-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-148">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-150">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="88c78-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="88c78-151">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="88c78-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88c78-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88c78-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="88c78-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88c78-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="88c78-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="88c78-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="88c78-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="88c78-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88c78-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="88c78-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="88c78-160">)</span><span class="sxs-lookup"><span data-stu-id="88c78-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88c78-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88c78-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-164">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="88c78-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="88c78-165">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ метриксервице".</span><span class="sxs-lookup"><span data-stu-id="88c78-165">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_MetricService".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-166">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88c78-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-169">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88c78-169">A description of the object.</span></span> <span data-ttu-id="88c78-170">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "обеспечивает управление WMI метриками Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="88c78-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Metric WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="88c78-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-172">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-174">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="88c78-174">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="88c78-175">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="88c78-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88c78-176">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88c78-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="88c78-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="88c78-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="88c78-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="88c78-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="88c78-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="88c78-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="88c78-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88c78-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="88c78-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="88c78-185">)</span><span class="sxs-lookup"><span data-stu-id="88c78-185">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88c78-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="88c78-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-189">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="88c78-189">A display name for the object.</span></span> <span data-ttu-id="88c78-190">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="88c78-190">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-191">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="88c78-191">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-192">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-194">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="88c78-194">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="88c78-195">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="88c78-195">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-196">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="88c78-196">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-199">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="88c78-199">The enabled and disabled states of an element.</span></span> <span data-ttu-id="88c78-200">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="88c78-200">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="88c78-201">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="88c78-201">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-202">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="88c78-202">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-203">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-205">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="88c78-205">The current health of the element.</span></span> <span data-ttu-id="88c78-206">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="88c78-206">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="88c78-207">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="88c78-207">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="88c78-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="88c78-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-209">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88c78-209">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-210">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88c78-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-212">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="88c78-212">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="88c78-213">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88c78-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-214">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="88c78-214">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88c78-217">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="88c78-217">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="88c78-218">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="88c78-218">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="88c78-219">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="88c78-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="88c78-220">**Name**</span><span class="sxs-lookup"><span data-stu-id="88c78-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-223">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="88c78-223">The label by which the object is known.</span></span> <span data-ttu-id="88c78-224">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "метриксвк".</span><span class="sxs-lookup"><span data-stu-id="88c78-224">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "metricsvc".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-225">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="88c78-225">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-226">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-228">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="88c78-228">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="88c78-229">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="88c78-229">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88c78-230">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88c78-230">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="88c78-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88c78-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="88c78-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="88c78-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="88c78-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="88c78-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="88c78-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="88c78-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="88c78-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="88c78-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="88c78-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="88c78-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="88c78-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="88c78-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="88c78-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="88c78-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="88c78-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="88c78-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88c78-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="88c78-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="88c78-250">)</span><span class="sxs-lookup"><span data-stu-id="88c78-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88c78-251">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="88c78-251">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-252">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="88c78-252">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88c78-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-254">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="88c78-254">The current statuses of the object.</span></span> <span data-ttu-id="88c78-255">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="88c78-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-256">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="88c78-256">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-259">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="88c78-259">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="88c78-260">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="88c78-260">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="88c78-261">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="88c78-261">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="88c78-262">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="88c78-262">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-265">Значение, которое предоставляет сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="88c78-265">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="88c78-266">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="88c78-266">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="88c78-267">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="88c78-267">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-270">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="88c78-270">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="88c78-271">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="88c78-271">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="88c78-272">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="88c78-272">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="88c78-273">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="88c78-273">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-274">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-276">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="88c78-276">Provides high level status information.</span></span> <span data-ttu-id="88c78-277">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="88c78-277">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="88c78-278">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="88c78-278">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="88c78-279">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="88c78-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="88c78-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88c78-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-281"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="88c78-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="88c78-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="88c78-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="88c78-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="88c78-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="88c78-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="88c78-286">)</span><span class="sxs-lookup"><span data-stu-id="88c78-286">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88c78-287">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="88c78-287">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-288">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-288">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-290">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="88c78-290">The last requested or desired state for the element.</span></span> <span data-ttu-id="88c78-291">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="88c78-291">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="88c78-292">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="88c78-292">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="88c78-293">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="88c78-293">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="88c78-294">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="88c78-294">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="88c78-295">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="88c78-295">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-296">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="88c78-296">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-297">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="88c78-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-299">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="88c78-299">Indicates whether the service is currently running.</span></span> <span data-ttu-id="88c78-300">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="88c78-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-301">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="88c78-301">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-304">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="88c78-304">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="88c78-305">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="88c78-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="88c78-306">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="88c78-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-309">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="88c78-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-310">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="88c78-310">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-311">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="88c78-311">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="88c78-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-313">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="88c78-313">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="88c78-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), а для строк всегда задано значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="88c78-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-315">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="88c78-315">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-318">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="88c78-318">The scoping system's creation class name.</span></span> <span data-ttu-id="88c78-319">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="88c78-319">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="88c78-320">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="88c78-320">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88c78-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-323">Имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="88c78-323">The name of the hosting computer system.</span></span> <span data-ttu-id="88c78-324">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="88c78-324">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-325">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="88c78-325">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-326">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88c78-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-328">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="88c78-328">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="88c78-329">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88c78-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="88c78-330">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="88c78-330">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c78-331">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88c78-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88c78-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88c78-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88c78-333">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="88c78-333">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="88c78-334">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88c78-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88c78-335">Требования</span><span class="sxs-lookup"><span data-stu-id="88c78-335">Requirements</span></span>



| <span data-ttu-id="88c78-336">Требование</span><span class="sxs-lookup"><span data-stu-id="88c78-336">Requirement</span></span> | <span data-ttu-id="88c78-337">Значение</span><span class="sxs-lookup"><span data-stu-id="88c78-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c78-338">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88c78-338">Minimum supported client</span></span><br/> | <span data-ttu-id="88c78-339">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="88c78-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="88c78-340">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88c78-340">Minimum supported server</span></span><br/> | <span data-ttu-id="88c78-341">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="88c78-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88c78-342">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88c78-342">Namespace</span></span><br/>                | <span data-ttu-id="88c78-343">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="88c78-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="88c78-344">MOF</span><span class="sxs-lookup"><span data-stu-id="88c78-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88c78-345"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88c78-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88c78-346">DLL</span><span class="sxs-lookup"><span data-stu-id="88c78-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88c78-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88c78-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

