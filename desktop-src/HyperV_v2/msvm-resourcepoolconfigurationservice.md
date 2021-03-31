---
description: Обеспечивает активное управление пулами ресурсов.
ms.assetid: 34ee3189-cb89-4d36-b12f-333449103968
title: Класс Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService
- Msvm_ResourcePoolConfigurationService.RequestStateChange
- Msvm_ResourcePoolConfigurationService.StartService
- Msvm_ResourcePoolConfigurationService.StopService
- Msvm_ResourcePoolConfigurationService.InstanceID
- Msvm_ResourcePoolConfigurationService.Caption
- Msvm_ResourcePoolConfigurationService.Description
- Msvm_ResourcePoolConfigurationService.ElementName
- Msvm_ResourcePoolConfigurationService.InstallDate
- Msvm_ResourcePoolConfigurationService.Name
- Msvm_ResourcePoolConfigurationService.OperationalStatus
- Msvm_ResourcePoolConfigurationService.StatusDescriptions
- Msvm_ResourcePoolConfigurationService.Status
- Msvm_ResourcePoolConfigurationService.HealthState
- Msvm_ResourcePoolConfigurationService.CommunicationStatus
- Msvm_ResourcePoolConfigurationService.DetailedStatus
- Msvm_ResourcePoolConfigurationService.OperatingStatus
- Msvm_ResourcePoolConfigurationService.PrimaryStatus
- Msvm_ResourcePoolConfigurationService.EnabledState
- Msvm_ResourcePoolConfigurationService.OtherEnabledState
- Msvm_ResourcePoolConfigurationService.RequestedState
- Msvm_ResourcePoolConfigurationService.EnabledDefault
- Msvm_ResourcePoolConfigurationService.TimeOfLastStateChange
- Msvm_ResourcePoolConfigurationService.AvailableRequestedStates
- Msvm_ResourcePoolConfigurationService.TransitioningToState
- Msvm_ResourcePoolConfigurationService.SystemCreationClassName
- Msvm_ResourcePoolConfigurationService.SystemName
- Msvm_ResourcePoolConfigurationService.CreationClassName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerContact
- Msvm_ResourcePoolConfigurationService.StartMode
- Msvm_ResourcePoolConfigurationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3160e8ac9ba011db70a5d7118e4d1f72733ff23f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913108"
---
# <a name="msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="885d9-103">\_Класс мсвм ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="885d9-103">Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="885d9-104">Обеспечивает активное управление пулами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="885d9-104">Provides for active management of resource pools.</span></span>

<span data-ttu-id="885d9-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="885d9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="885d9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="885d9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationService : CIM_Service
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
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="885d9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="885d9-107">Members</span></span>

<span data-ttu-id="885d9-108">Класс **мсвм \_ ресаурцепулконфигуратионсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="885d9-108">The **Msvm\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="885d9-109">Методы</span><span class="sxs-lookup"><span data-stu-id="885d9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="885d9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="885d9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="885d9-111">Методы</span><span class="sxs-lookup"><span data-stu-id="885d9-111">Methods</span></span>

<span data-ttu-id="885d9-112">Класс **мсвм \_ ресаурцепулконфигуратионсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="885d9-112">The **Msvm\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="885d9-113">Метод</span><span class="sxs-lookup"><span data-stu-id="885d9-113">Method</span></span>                                                                                   | <span data-ttu-id="885d9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="885d9-114">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="885d9-115">**CreatePool**</span><span class="sxs-lookup"><span data-stu-id="885d9-115">**CreatePool**</span></span>](createpool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="885d9-116">Создает дочерний пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="885d9-116">Creates a child resource pool.</span></span><br/>                                                    |
| [<span data-ttu-id="885d9-117">**DeletePool**</span><span class="sxs-lookup"><span data-stu-id="885d9-117">**DeletePool**</span></span>](deletepool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="885d9-118">Удаляет пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="885d9-118">Deletes a resource pool.</span></span><br/>                                                          |
| [<span data-ttu-id="885d9-119">**модифипулресаурцес**</span><span class="sxs-lookup"><span data-stu-id="885d9-119">**ModifyPoolResources**</span></span>](modifypoolresources-msvm-resourcepoolconfigurationservice.md) | <span data-ttu-id="885d9-120">Изменяет параметры ресурсов родительского пула для ресурсов, назначенных дочернему пулу.</span><span class="sxs-lookup"><span data-stu-id="885d9-120">Changes the parent pool resource settings for resources assigned to a child pool.</span></span><br/> |
| [<span data-ttu-id="885d9-121">**модифипулсеттингс**</span><span class="sxs-lookup"><span data-stu-id="885d9-121">**ModifyPoolSettings**</span></span>](modifypoolsettings-msvm-resourcepoolconfigurationservice.md)   | <span data-ttu-id="885d9-122">Изменяет параметры дочернего пула, не связанные с распределением.</span><span class="sxs-lookup"><span data-stu-id="885d9-122">Changes the settings of a child pool that are not allocation related.</span></span><br/>             |
| <span data-ttu-id="885d9-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="885d9-123">**RequestStateChange**</span></span>                                                                   | <span data-ttu-id="885d9-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="885d9-124">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="885d9-125">**StartService**</span><span class="sxs-lookup"><span data-stu-id="885d9-125">**StartService**</span></span>                                                                         | <span data-ttu-id="885d9-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="885d9-126">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="885d9-127">**StopService**</span><span class="sxs-lookup"><span data-stu-id="885d9-127">**StopService**</span></span>                                                                          | <span data-ttu-id="885d9-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="885d9-128">This method is not supported.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="885d9-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="885d9-129">Properties</span></span>

<span data-ttu-id="885d9-130">Класс **мсвм \_ ресаурцепулконфигуратионсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="885d9-130">The **Msvm\_ResourcePoolConfigurationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="885d9-131">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="885d9-131">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-132">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="885d9-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="885d9-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-134">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="885d9-134">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="885d9-135">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="885d9-135">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="885d9-136">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="885d9-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-139">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="885d9-139">A short description of the object.</span></span> <span data-ttu-id="885d9-140">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-141">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="885d9-141">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-144">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="885d9-144">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="885d9-145">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="885d9-145">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="885d9-146">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-146">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="885d9-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="885d9-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="885d9-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="885d9-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="885d9-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="885d9-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="885d9-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="885d9-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="885d9-154">)</span><span class="sxs-lookup"><span data-stu-id="885d9-154">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="885d9-155">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="885d9-155">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-158">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="885d9-158">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="885d9-159">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="885d9-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="885d9-160">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="885d9-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-161">**Описание**</span><span class="sxs-lookup"><span data-stu-id="885d9-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-164">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="885d9-164">A description of the object.</span></span> <span data-ttu-id="885d9-165">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="885d9-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-169">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="885d9-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="885d9-170">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="885d9-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="885d9-171">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="885d9-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="885d9-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="885d9-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="885d9-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="885d9-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="885d9-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="885d9-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="885d9-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="885d9-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="885d9-180">)</span><span class="sxs-lookup"><span data-stu-id="885d9-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="885d9-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="885d9-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-184">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="885d9-184">A display name for the object.</span></span> <span data-ttu-id="885d9-185">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-186">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="885d9-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-189">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="885d9-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="885d9-190">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="885d9-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="885d9-191">Значение</span><span class="sxs-lookup"><span data-stu-id="885d9-191">Value</span></span>                                                                        | <span data-ttu-id="885d9-192">Значение</span><span class="sxs-lookup"><span data-stu-id="885d9-192">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="885d9-193"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="885d9-193"><dt>2</dt></span></span> </dl> | <span data-ttu-id="885d9-194">Активировано</span><span class="sxs-lookup"><span data-stu-id="885d9-194">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="885d9-195">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="885d9-195">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-198">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="885d9-198">The enabled and disabled states of an element.</span></span> <span data-ttu-id="885d9-199">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="885d9-199">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="885d9-200">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="885d9-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="885d9-201">Значение</span><span class="sxs-lookup"><span data-stu-id="885d9-201">Value</span></span>                                                                        | <span data-ttu-id="885d9-202">Значение</span><span class="sxs-lookup"><span data-stu-id="885d9-202">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="885d9-203"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="885d9-203"><dt>2</dt></span></span> </dl> | <span data-ttu-id="885d9-204">Активировано</span><span class="sxs-lookup"><span data-stu-id="885d9-204">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="885d9-205">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="885d9-205">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-206">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-208">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="885d9-208">The current health of the element.</span></span> <span data-ttu-id="885d9-209">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="885d9-209">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="885d9-210">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="885d9-210">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="885d9-211">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="885d9-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-213">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="885d9-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-215">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="885d9-215">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="885d9-216">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-217">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="885d9-217">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-220">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="885d9-220">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="885d9-221">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="885d9-221">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="885d9-222">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-223">**Name**</span><span class="sxs-lookup"><span data-stu-id="885d9-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-226">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="885d9-226">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="885d9-227">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="885d9-227">The label by which the object is known.</span></span> <span data-ttu-id="885d9-228">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-229">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="885d9-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-230">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-232">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="885d9-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="885d9-233">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="885d9-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="885d9-234">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="885d9-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="885d9-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="885d9-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="885d9-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="885d9-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="885d9-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="885d9-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="885d9-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="885d9-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="885d9-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="885d9-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="885d9-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="885d9-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="885d9-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="885d9-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="885d9-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="885d9-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="885d9-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="885d9-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="885d9-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="885d9-254">)</span><span class="sxs-lookup"><span data-stu-id="885d9-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="885d9-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="885d9-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-256">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="885d9-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="885d9-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-258">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="885d9-258">The current statuses of the object.</span></span> <span data-ttu-id="885d9-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-260">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="885d9-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-263">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="885d9-263">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="885d9-264">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="885d9-264">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="885d9-265">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="885d9-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="885d9-266">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="885d9-266">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-269">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="885d9-269">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="885d9-270">Любые сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="885d9-270">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="885d9-271">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="885d9-271">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="885d9-272">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="885d9-272">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-275">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="885d9-275">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="885d9-276">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="885d9-276">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="885d9-277">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="885d9-277">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="885d9-278">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="885d9-278">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="885d9-279">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="885d9-279">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-280">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-282">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="885d9-282">Provides high level status information.</span></span> <span data-ttu-id="885d9-283">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="885d9-283">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="885d9-284">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="885d9-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="885d9-285">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="885d9-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="885d9-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-287"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="885d9-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="885d9-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="885d9-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="885d9-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="885d9-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="885d9-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="885d9-292">)</span><span class="sxs-lookup"><span data-stu-id="885d9-292">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="885d9-293">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="885d9-293">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-294">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-296">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="885d9-296">The last requested or desired state for the element.</span></span> <span data-ttu-id="885d9-297">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="885d9-297">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="885d9-298">Это свойство предназначено для сравнения последнего запрошенного и текущего состояний элемента.</span><span class="sxs-lookup"><span data-stu-id="885d9-298">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="885d9-299">Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать свойство **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="885d9-299">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="885d9-300">В этом случае используется значение 12 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="885d9-300">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="885d9-301">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="885d9-301">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="885d9-302">Значение</span><span class="sxs-lookup"><span data-stu-id="885d9-302">Value</span></span>                                                                         | <span data-ttu-id="885d9-303">Значение</span><span class="sxs-lookup"><span data-stu-id="885d9-303">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="885d9-304"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="885d9-304"><dt>12</dt></span></span> </dl> | <span data-ttu-id="885d9-305">Не применяется</span><span class="sxs-lookup"><span data-stu-id="885d9-305">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="885d9-306">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="885d9-306">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-307">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="885d9-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-309">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="885d9-309">Indicates whether the service is currently running.</span></span> <span data-ttu-id="885d9-310">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="885d9-310">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-311">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="885d9-311">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-314">Квалификаторы: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="885d9-314">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="885d9-315">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="885d9-315">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="885d9-316">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="885d9-316">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="885d9-317">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="885d9-317">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-320">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="885d9-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="885d9-321">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="885d9-321">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-322">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="885d9-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="885d9-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-324">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="885d9-324">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="885d9-325">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="885d9-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-326">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="885d9-326">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-327">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-329">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="885d9-329">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="885d9-330">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="885d9-330">The scoping system's creation class name.</span></span> <span data-ttu-id="885d9-331">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="885d9-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-332">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="885d9-332">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="885d9-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="885d9-335">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="885d9-335">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="885d9-336">NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="885d9-336">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="885d9-337">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="885d9-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-338">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="885d9-338">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-339">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="885d9-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-341">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="885d9-341">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="885d9-342">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="885d9-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="885d9-343">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="885d9-343">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="885d9-344">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="885d9-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="885d9-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="885d9-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="885d9-346">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="885d9-346">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="885d9-347">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="885d9-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="885d9-348">Требования</span><span class="sxs-lookup"><span data-stu-id="885d9-348">Requirements</span></span>



| <span data-ttu-id="885d9-349">Требование</span><span class="sxs-lookup"><span data-stu-id="885d9-349">Requirement</span></span> | <span data-ttu-id="885d9-350">Значение</span><span class="sxs-lookup"><span data-stu-id="885d9-350">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="885d9-351">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="885d9-351">Minimum supported client</span></span><br/> | <span data-ttu-id="885d9-352">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="885d9-352">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="885d9-353">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="885d9-353">Minimum supported server</span></span><br/> | <span data-ttu-id="885d9-354">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="885d9-354">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="885d9-355">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="885d9-355">Namespace</span></span><br/>                | <span data-ttu-id="885d9-356">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="885d9-356">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="885d9-357">MOF</span><span class="sxs-lookup"><span data-stu-id="885d9-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="885d9-358"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="885d9-358"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="885d9-359">DLL</span><span class="sxs-lookup"><span data-stu-id="885d9-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="885d9-360"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="885d9-360"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

