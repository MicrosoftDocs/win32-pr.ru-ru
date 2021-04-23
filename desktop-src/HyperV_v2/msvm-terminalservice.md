---
description: Управляет всеми удаленными подключениями терминала к определенному узлу.
ms.assetid: 7eacb8a6-cb8d-4a2a-951e-f5286cf484e7
title: Класс Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService
- Msvm_TerminalService.InstanceID
- Msvm_TerminalService.Caption
- Msvm_TerminalService.Description
- Msvm_TerminalService.ElementName
- Msvm_TerminalService.InstallDate
- Msvm_TerminalService.OperationalStatus
- Msvm_TerminalService.StatusDescriptions
- Msvm_TerminalService.Status
- Msvm_TerminalService.HealthState
- Msvm_TerminalService.CommunicationStatus
- Msvm_TerminalService.DetailedStatus
- Msvm_TerminalService.OperatingStatus
- Msvm_TerminalService.PrimaryStatus
- Msvm_TerminalService.EnabledState
- Msvm_TerminalService.OtherEnabledState
- Msvm_TerminalService.RequestedState
- Msvm_TerminalService.EnabledDefault
- Msvm_TerminalService.TimeOfLastStateChange
- Msvm_TerminalService.AvailableRequestedStates
- Msvm_TerminalService.TransitioningToState
- Msvm_TerminalService.SystemCreationClassName
- Msvm_TerminalService.SystemName
- Msvm_TerminalService.Name
- Msvm_TerminalService.CreationClassName
- Msvm_TerminalService.PrimaryOwnerName
- Msvm_TerminalService.PrimaryOwnerContact
- Msvm_TerminalService.StartMode
- Msvm_TerminalService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76b12bb49391909638d20df817a3693938c3222c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683022"
---
# <a name="msvm_terminalservice-class"></a><span data-ttu-id="34891-103">\_Класс мсвм терминалсервице</span><span class="sxs-lookup"><span data-stu-id="34891-103">Msvm\_TerminalService class</span></span>

<span data-ttu-id="34891-104">Управляет всеми удаленными подключениями терминала к определенному узлу.</span><span class="sxs-lookup"><span data-stu-id="34891-104">Manages all remote terminal connections to a particular host.</span></span> <span data-ttu-id="34891-105">Служба использует настраиваемый порт для запуска всех подключений терминала.</span><span class="sxs-lookup"><span data-stu-id="34891-105">The service uses a configurable port to initiate all terminal connections.</span></span>

<span data-ttu-id="34891-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="34891-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="34891-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34891-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Terminal Service";
  string   Description = "Microsoft Virtual Terminal Service";
  string   ElementName = "Hyper-V Terminal Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The virtual terminal connection management service is fully operational" };
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
  string   Name = "termsvc";
  string   CreationClassName = "Msvm_TerminalService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="34891-108">Члены</span><span class="sxs-lookup"><span data-stu-id="34891-108">Members</span></span>

<span data-ttu-id="34891-109">Класс **мсвм \_ терминалсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="34891-109">The **Msvm\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="34891-110">Методы</span><span class="sxs-lookup"><span data-stu-id="34891-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="34891-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="34891-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="34891-112">Методы</span><span class="sxs-lookup"><span data-stu-id="34891-112">Methods</span></span>

<span data-ttu-id="34891-113">Класс **мсвм \_ терминалсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="34891-113">The **Msvm\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="34891-114">Метод</span><span class="sxs-lookup"><span data-stu-id="34891-114">Method</span></span>                                                                                        | <span data-ttu-id="34891-115">Описание</span><span class="sxs-lookup"><span data-stu-id="34891-115">Description</span></span>                                                                                                      |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34891-116">**жетинтерактивесессионакл**</span><span class="sxs-lookup"><span data-stu-id="34891-116">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)             | <span data-ttu-id="34891-117">Извлекает текущий список DACL, управляющий доступом к интерактивному сеансу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="34891-117">Retrieves the current DACL that controls access to the interactive session of a virtual machine.</span></span><br/>      |
| [<span data-ttu-id="34891-118">**грантинтерактивесессионакцесс**</span><span class="sxs-lookup"><span data-stu-id="34891-118">**GrantInteractiveSessionAccess**</span></span>](grantinteractivesessionaccess-msvm-terminalservice.md)   | <span data-ttu-id="34891-119">Предоставляет доступ к интерактивному сеансу виртуальной машины указанному списку доверенных лиц.</span><span class="sxs-lookup"><span data-stu-id="34891-119">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span><br/>    |
| [<span data-ttu-id="34891-120">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="34891-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-terminalservice.md)                   | <span data-ttu-id="34891-121">Изменяет данные настройки для службы.</span><span class="sxs-lookup"><span data-stu-id="34891-121">Modifies the setting data for the service.</span></span><br/>                                                            |
| [<span data-ttu-id="34891-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="34891-122">**RequestStateChange**</span></span>](msvm-terminalservice-requeststatechange.md)                         | <span data-ttu-id="34891-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="34891-123">Requests a state change.</span></span><br/>                                                                              |
| [<span data-ttu-id="34891-124">**ревокеинтерактивесессионакцесс**</span><span class="sxs-lookup"><span data-stu-id="34891-124">**RevokeInteractiveSessionAccess**</span></span>](revokeinteractivesessionaccess-msvm-terminalservice.md) | <span data-ttu-id="34891-125">Отменяет доступ к интерактивному сеансу виртуальной машины из указанного списка доверенных лиц.</span><span class="sxs-lookup"><span data-stu-id="34891-125">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span><br/> |
| [<span data-ttu-id="34891-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="34891-126">**StartService**</span></span>](msvm-terminalservice-startservice.md)                                     | <span data-ttu-id="34891-127">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="34891-127">Starts the service.</span></span><br/>                                                                                   |
| [<span data-ttu-id="34891-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="34891-128">**StopService**</span></span>](msvm-terminalservice-stopservice.md)                                       | <span data-ttu-id="34891-129">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="34891-129">Stops the service.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="34891-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="34891-130">Properties</span></span>

<span data-ttu-id="34891-131">Класс **мсвм \_ терминалсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="34891-131">The **Msvm\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34891-132">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="34891-132">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-133">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="34891-133">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34891-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-135">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="34891-135">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="34891-136">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34891-136">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34891-137">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="34891-137">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-140">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="34891-140">A short description of the object.</span></span> <span data-ttu-id="34891-141">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="34891-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-142">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="34891-142">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-145">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="34891-145">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="34891-146">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="34891-146">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34891-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34891-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="34891-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34891-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="34891-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34891-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="34891-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34891-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="34891-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34891-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="34891-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34891-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="34891-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34891-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="34891-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34891-155">)</span><span class="sxs-lookup"><span data-stu-id="34891-155">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34891-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="34891-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-159">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="34891-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="34891-160">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-161">**Описание**</span><span class="sxs-lookup"><span data-stu-id="34891-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-164">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="34891-164">A description of the object.</span></span> <span data-ttu-id="34891-165">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="34891-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="34891-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-169">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="34891-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="34891-170">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="34891-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34891-171">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34891-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="34891-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34891-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="34891-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34891-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="34891-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34891-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="34891-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34891-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="34891-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34891-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="34891-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34891-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="34891-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34891-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="34891-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34891-180">)</span><span class="sxs-lookup"><span data-stu-id="34891-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34891-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="34891-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-184">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="34891-184">A display name for the object.</span></span> <span data-ttu-id="34891-185">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="34891-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-186">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="34891-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-189">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="34891-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="34891-190">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34891-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34891-191">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="34891-191">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-194">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="34891-194">The enabled and disabled states of an element.</span></span> <span data-ttu-id="34891-195">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="34891-195">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="34891-196">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34891-196">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34891-197">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="34891-197">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-200">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="34891-200">The current health of the element.</span></span> <span data-ttu-id="34891-201">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="34891-201">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="34891-202">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="34891-202">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="34891-203">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="34891-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-205">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="34891-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34891-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-207">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="34891-207">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="34891-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-209">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="34891-209">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34891-212">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="34891-212">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="34891-213">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="34891-213">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="34891-214">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34891-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34891-215">**Name**</span><span class="sxs-lookup"><span data-stu-id="34891-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-218">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="34891-218">The label by which the object is known.</span></span> <span data-ttu-id="34891-219">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-219">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-220">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="34891-220">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-221">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-223">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="34891-223">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="34891-224">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="34891-224">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34891-225">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34891-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="34891-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34891-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="34891-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34891-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="34891-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34891-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="34891-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34891-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="34891-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34891-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="34891-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34891-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="34891-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="34891-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="34891-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="34891-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="34891-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="34891-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="34891-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="34891-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="34891-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="34891-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="34891-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="34891-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="34891-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="34891-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="34891-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="34891-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="34891-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="34891-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="34891-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="34891-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="34891-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="34891-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="34891-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34891-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="34891-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34891-245">)</span><span class="sxs-lookup"><span data-stu-id="34891-245">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34891-246">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="34891-246">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-247">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="34891-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34891-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-249">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="34891-249">The current statuses of the object.</span></span> <span data-ttu-id="34891-250">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-250">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-251">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="34891-251">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-254">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="34891-254">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="34891-255">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="34891-255">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="34891-256">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34891-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34891-257">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="34891-257">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-260">Значение, которое предоставляет сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="34891-260">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="34891-261">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-261">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-262">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="34891-262">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-265">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="34891-265">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="34891-266">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="34891-266">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="34891-267">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-267">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-268">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="34891-268">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-269">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-271">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="34891-271">Provides high level status information.</span></span> <span data-ttu-id="34891-272">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="34891-272">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="34891-273">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="34891-273">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="34891-274">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-274">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="34891-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="34891-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34891-276"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="34891-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34891-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="34891-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34891-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="34891-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34891-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="34891-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34891-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="34891-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="34891-281">)</span><span class="sxs-lookup"><span data-stu-id="34891-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34891-282">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="34891-282">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-285">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="34891-285">The last requested or desired state for the element.</span></span> <span data-ttu-id="34891-286">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="34891-286">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="34891-287">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="34891-287">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="34891-288">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="34891-288">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="34891-289">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="34891-289">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="34891-290">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="34891-290">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="34891-291">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="34891-291">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-292">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="34891-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34891-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-294">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="34891-294">Indicates whether the service is currently running.</span></span> <span data-ttu-id="34891-295">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-295">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-296">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="34891-296">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-299">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="34891-299">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="34891-300">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-301">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="34891-301">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-304">Состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="34891-304">The status of the element.</span></span> <span data-ttu-id="34891-305">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-306">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="34891-306">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-307">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="34891-307">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="34891-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-309">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="34891-309">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="34891-310">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="34891-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="34891-311">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="34891-311">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-314">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="34891-314">The scoping system's creation class name.</span></span> <span data-ttu-id="34891-315">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-316">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="34891-316">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34891-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34891-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-319">Имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="34891-319">The name of the hosting computer system.</span></span> <span data-ttu-id="34891-320">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="34891-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="34891-321">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="34891-321">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-322">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="34891-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34891-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-324">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="34891-324">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="34891-325">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34891-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="34891-326">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="34891-326">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34891-327">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34891-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34891-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34891-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34891-329">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="34891-329">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="34891-330">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34891-330">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34891-331">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34891-331">Remarks</span></span>

<span data-ttu-id="34891-332">Доступ к классу **\_ терминалсервице мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="34891-332">Access to the **Msvm\_TerminalService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="34891-333">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="34891-333">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="34891-334">Требования</span><span class="sxs-lookup"><span data-stu-id="34891-334">Requirements</span></span>



| <span data-ttu-id="34891-335">Требование</span><span class="sxs-lookup"><span data-stu-id="34891-335">Requirement</span></span> | <span data-ttu-id="34891-336">Значение</span><span class="sxs-lookup"><span data-stu-id="34891-336">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34891-337">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34891-337">Minimum supported client</span></span><br/> | <span data-ttu-id="34891-338">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="34891-338">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34891-339">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34891-339">Minimum supported server</span></span><br/> | <span data-ttu-id="34891-340">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="34891-340">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34891-341">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="34891-341">Namespace</span></span><br/>                | <span data-ttu-id="34891-342">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="34891-342">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34891-343">MOF</span><span class="sxs-lookup"><span data-stu-id="34891-343">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34891-344"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34891-344"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34891-345">DLL</span><span class="sxs-lookup"><span data-stu-id="34891-345">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34891-346"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34891-346"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="34891-347">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34891-347">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34891-348">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="34891-348">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

