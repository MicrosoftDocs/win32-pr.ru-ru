---
description: Служит заполнителем для службы внутри коммутатора, который изучает MAC-адреса и служит мостом между \_ классами мсвм виртуалесернетсвитч и мсвм \_ динамикфорвардинжентри.
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Класс Msvm_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991372"
---
# <a name="msvm_transparentbridgingservice-class"></a><span data-ttu-id="15b97-103">\_Класс мсвм транспарентбридгингсервице</span><span class="sxs-lookup"><span data-stu-id="15b97-103">Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="15b97-104">Служит заполнителем для службы внутри коммутатора, который изучает MAC-адреса и служит мостом между классами [**мсвм \_ Виртуалесернетсвитч**](msvm-virtualethernetswitch.md) и [**мсвм \_ динамикфорвардинжентри**](msvm-dynamicforwardingentry.md) .</span><span class="sxs-lookup"><span data-stu-id="15b97-104">Serves as a placeholder for the service inside the switch that learns MAC addresses and serves as a bridge between the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) and [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) classes.</span></span>

<span data-ttu-id="15b97-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="15b97-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b97-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15b97-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a><span data-ttu-id="15b97-107">Члены</span><span class="sxs-lookup"><span data-stu-id="15b97-107">Members</span></span>

<span data-ttu-id="15b97-108">Класс **мсвм \_ транспарентбридгингсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="15b97-108">The **Msvm\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="15b97-109">Методы</span><span class="sxs-lookup"><span data-stu-id="15b97-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="15b97-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="15b97-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="15b97-111">Методы</span><span class="sxs-lookup"><span data-stu-id="15b97-111">Methods</span></span>

<span data-ttu-id="15b97-112">Класс **мсвм \_ транспарентбридгингсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="15b97-112">The **Msvm\_TransparentBridgingService** class has these methods.</span></span>



| <span data-ttu-id="15b97-113">Метод</span><span class="sxs-lookup"><span data-stu-id="15b97-113">Method</span></span>                                                                           | <span data-ttu-id="15b97-114">Описание</span><span class="sxs-lookup"><span data-stu-id="15b97-114">Description</span></span>                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="15b97-115">**Равен**</span><span class="sxs-lookup"><span data-stu-id="15b97-115">**RequestStateChange**</span></span>](msvm-transparentbridgingservice-requeststatechange.md) | <span data-ttu-id="15b97-116">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="15b97-116">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="15b97-117">**StartService**</span><span class="sxs-lookup"><span data-stu-id="15b97-117">**StartService**</span></span>](msvm-transparentbridgingservice-startservice.md)             | <span data-ttu-id="15b97-118">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="15b97-118">Starts the service.</span></span><br/>      |
| [<span data-ttu-id="15b97-119">**StopService**</span><span class="sxs-lookup"><span data-stu-id="15b97-119">**StopService**</span></span>](msvm-transparentbridgingservice-stopservice.md)               | <span data-ttu-id="15b97-120">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="15b97-120">Stops the service.</span></span><br/>       |



 

### <a name="properties"></a><span data-ttu-id="15b97-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="15b97-121">Properties</span></span>

<span data-ttu-id="15b97-122">Класс **мсвм \_ транспарентбридгингсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15b97-122">The **Msvm\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15b97-123">**агингтиме**</span><span class="sxs-lookup"><span data-stu-id="15b97-123">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15b97-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-126">Время ожидания в секундах для динамически изученных MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="15b97-126">The time-out period, in seconds, for aging out dynamically learned MAC addresses.</span></span> <span data-ttu-id="15b97-127">Это свойство наследуется от [**CIM \_ транспарентбридгингсервице**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="15b97-127">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-128">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="15b97-128">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-129">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="15b97-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="15b97-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-131">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="15b97-131">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="15b97-132">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-133">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="15b97-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-136">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="15b97-136">A short description of the object.</span></span> <span data-ttu-id="15b97-137">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда является "виртуальным коммутатором со прозрачным мостом".</span><span class="sxs-lookup"><span data-stu-id="15b97-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always "Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="15b97-138">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="15b97-138">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-141">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="15b97-141">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="15b97-142">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="15b97-142">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="15b97-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-143">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="15b97-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="15b97-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="15b97-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="15b97-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="15b97-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="15b97-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="15b97-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="15b97-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="15b97-151">)</span><span class="sxs-lookup"><span data-stu-id="15b97-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15b97-152">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="15b97-152">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-155">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="15b97-155">A short description of the object.</span></span> <span data-ttu-id="15b97-156">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-156">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="15b97-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-160">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="15b97-160">A description of the object.</span></span> <span data-ttu-id="15b97-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба виртуального коммутатора со прозрачным мостом (Майкрософт)".</span><span class="sxs-lookup"><span data-stu-id="15b97-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="15b97-162">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="15b97-162">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-165">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="15b97-165">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="15b97-166">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="15b97-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="15b97-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="15b97-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="15b97-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="15b97-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="15b97-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="15b97-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="15b97-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="15b97-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="15b97-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="15b97-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="15b97-176">)</span><span class="sxs-lookup"><span data-stu-id="15b97-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15b97-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="15b97-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-180">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="15b97-180">A display name for the object.</span></span> <span data-ttu-id="15b97-181">Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="15b97-181">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="15b97-182">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-183">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="15b97-183">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-184">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-186">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="15b97-186">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="15b97-187">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-188">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="15b97-188">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-189">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-191">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="15b97-191">The enabled and disabled states of an element.</span></span> <span data-ttu-id="15b97-192">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-193">**FID**</span><span class="sxs-lookup"><span data-stu-id="15b97-193">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-194">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15b97-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-196">Идентификатор базы данных фильтрации, используемый коммутаторами, которые поддерживают виртуальную ЛС и имеют более одной фильтрации базы данных.</span><span class="sxs-lookup"><span data-stu-id="15b97-196">The filtering database identifier used by switches that support VLAN and that have more than one filtering database.</span></span> <span data-ttu-id="15b97-197">Это свойство наследуется от [**CIM \_ транспарентбридгингсервице**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="15b97-197">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="15b97-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-199">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-201">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="15b97-201">The current health of the element.</span></span> <span data-ttu-id="15b97-202">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="15b97-202">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="15b97-203">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="15b97-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-205">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15b97-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-207">Указывает время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="15b97-207">Specifies the time when the object was installed.</span></span> <span data-ttu-id="15b97-208">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="15b97-208">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="15b97-209">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и не используется.</span><span class="sxs-lookup"><span data-stu-id="15b97-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="15b97-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15b97-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15b97-213">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="15b97-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="15b97-214">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="15b97-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="15b97-215">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-216">**Ключевые слова**</span><span class="sxs-lookup"><span data-stu-id="15b97-216">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-217">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="15b97-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15b97-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-219">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="15b97-219">Do not use.</span></span> <span data-ttu-id="15b97-220">Массив строк произвольной формы, который предоставляет описательные слова и фразы, которые можно использовать в запросах.</span><span class="sxs-lookup"><span data-stu-id="15b97-220">A free-form array of strings that provide descriptive words and phrases that can be used in queries.</span></span> <span data-ttu-id="15b97-221">Это свойство не реализовано, так как оно не стандартизовано.</span><span class="sxs-lookup"><span data-stu-id="15b97-221">This property is not implemented because it is not standardized.</span></span> <span data-ttu-id="15b97-222">Если это свойство является необходимой конструкцией запроса, то в иерархии наследования потребуется больше.</span><span class="sxs-lookup"><span data-stu-id="15b97-222">If this property were a necessary query construct, then it would be required higher in the inheritance hierarchy.</span></span> <span data-ttu-id="15b97-223">Это свойство наследуется [**от \_ сетевой NetworkService CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-223">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-224">**Name**</span><span class="sxs-lookup"><span data-stu-id="15b97-224">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-227">Имя, однозначно идентифицирующее службу и предоставляющее сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="15b97-227">A name that uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="15b97-228">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-228">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-229">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="15b97-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-230">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-232">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="15b97-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="15b97-233">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="15b97-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="15b97-234">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="15b97-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="15b97-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="15b97-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="15b97-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="15b97-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="15b97-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="15b97-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="15b97-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="15b97-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="15b97-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="15b97-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="15b97-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="15b97-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="15b97-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="15b97-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="15b97-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="15b97-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="15b97-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="15b97-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="15b97-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="15b97-254">)</span><span class="sxs-lookup"><span data-stu-id="15b97-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15b97-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="15b97-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-256">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="15b97-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="15b97-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-258">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="15b97-258">The current status of the element.</span></span> <span data-ttu-id="15b97-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-260">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="15b97-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-263">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="15b97-263">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="15b97-264">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="15b97-264">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="15b97-265">**осерпротоколтипе**</span><span class="sxs-lookup"><span data-stu-id="15b97-265">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-266">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-268">Тип перенаправляемого протокола, если значение **ProtocolType** равно 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="15b97-268">The type of protocol that is being forwarded when the value of **ProtocolType** is 1 (Other).</span></span> <span data-ttu-id="15b97-269">Это свойство наследуется от [**CIM \_ форвардингсервице**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="15b97-269">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-270">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="15b97-270">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-273">Строка, которая предоставляет сведения о том, как можно достичь основного владельца службы.</span><span class="sxs-lookup"><span data-stu-id="15b97-273">A string that provides information about how the primary owner of the Service can be reached.</span></span> <span data-ttu-id="15b97-274">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-274">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-275">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="15b97-275">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-278">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="15b97-278">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="15b97-279">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-280">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="15b97-280">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-281">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-283">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="15b97-283">Provides high level status information.</span></span> <span data-ttu-id="15b97-284">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="15b97-284">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="15b97-285">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="15b97-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="15b97-286">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="15b97-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="15b97-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-288"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="15b97-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="15b97-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="15b97-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="15b97-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="15b97-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="15b97-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="15b97-293">)</span><span class="sxs-lookup"><span data-stu-id="15b97-293">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15b97-294">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="15b97-294">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-295">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-295">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-297">Тип перенаправляемого протокола.</span><span class="sxs-lookup"><span data-stu-id="15b97-297">The type of protocol that is being forwarded.</span></span> <span data-ttu-id="15b97-298">Это свойство наследуется от [**CIM \_ форвардингсервице**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="15b97-298">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-299">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="15b97-299">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-300">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-302">Последнее запрошенное или требуемое состояние для службы управления.</span><span class="sxs-lookup"><span data-stu-id="15b97-302">The last requested or desired state for the management service.</span></span> <span data-ttu-id="15b97-303">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-304">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="15b97-304">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-307">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="15b97-307">Do not use.</span></span> <span data-ttu-id="15b97-308">URL-адрес, предоставляющий протокол, сетевое расположение и другие сведения, относящиеся к службе, необходимые для доступа к службе.</span><span class="sxs-lookup"><span data-stu-id="15b97-308">A URL that provides the protocol, network location, and other service-specific information required to access the service.</span></span> <span data-ttu-id="15b97-309">Вместо этого используйте класс **сервицеакцессури** , который правильно позиционирует семантику доступа к службе и уточняет формат информации.</span><span class="sxs-lookup"><span data-stu-id="15b97-309">Instead, use the **ServiceAccessURI** class, which correctly positions the semantics of the service access, and clarifies the format of the information.</span></span> <span data-ttu-id="15b97-310">Это свойство наследуется [**от \_ сетевой NetworkService CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-310">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-311">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="15b97-311">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-312">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="15b97-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-314">Указывает, была ли служба запущена (**true**) или остановлена (**false**).</span><span class="sxs-lookup"><span data-stu-id="15b97-314">Indicates whether the service has been started (**True**), or stopped (**False**).</span></span> <span data-ttu-id="15b97-315">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-316">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="15b97-316">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-319">Указывает, запускается ли служба автоматически системой, операционной системой и т. д. или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="15b97-319">Indicates whether the service is automatically started by a system, an operating system, and so on, or is started only upon request.</span></span> <span data-ttu-id="15b97-320">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-321">**стартупкондитионс**</span><span class="sxs-lookup"><span data-stu-id="15b97-321">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-322">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="15b97-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15b97-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-324">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="15b97-324">Do not use.</span></span> <span data-ttu-id="15b97-325">Массив строк произвольной формы, указывающий все конкретные предусловия, которые должны быть выполнены для правильной работы этой службы.</span><span class="sxs-lookup"><span data-stu-id="15b97-325">A free-form array of strings that specify any specific preconditions that must be met for this service to start correctly.</span></span> <span data-ttu-id="15b97-326">Это свойство нецелесообразно, так как оно не является стандартизированным.</span><span class="sxs-lookup"><span data-stu-id="15b97-326">This property is not useful because it is not standardized.</span></span> <span data-ttu-id="15b97-327">Если это свойство является необходимой конструкцией, оно должно быть выше в иерархии наследования (для службы).</span><span class="sxs-lookup"><span data-stu-id="15b97-327">If this property were a necessary construct, then it would be required higher in the inheritance hierarchy (on Service).</span></span> <span data-ttu-id="15b97-328">Это свойство наследуется [**от \_ сетевой NetworkService CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-328">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-329">**стартуппараметерс**</span><span class="sxs-lookup"><span data-stu-id="15b97-329">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-330">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="15b97-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15b97-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-332">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="15b97-332">Do not use.</span></span> <span data-ttu-id="15b97-333">Массив строк произвольной формы, указывающий все конкретные параметры, которые должны быть передаваться методу **StartService** для запуска службы.</span><span class="sxs-lookup"><span data-stu-id="15b97-333">A free-form array of strings that specify any specific parameters that must be supplied to the **StartService** method for this service to start correctly.</span></span> <span data-ttu-id="15b97-334">Если этот метод был уточнен, его параметры более формально сообщают эту информацию.</span><span class="sxs-lookup"><span data-stu-id="15b97-334">If this method were refined, then its parameters would more formally convey this information.</span></span> <span data-ttu-id="15b97-335">Это свойство наследуется [**от \_ сетевой NetworkService CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-335">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-336">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="15b97-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-339">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="15b97-339">The current status of the object.</span></span> <span data-ttu-id="15b97-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-341">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="15b97-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-342">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="15b97-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15b97-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-344">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="15b97-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="15b97-345">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="15b97-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-346">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="15b97-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-349">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="15b97-349">The creation class name of the scoping system.</span></span> <span data-ttu-id="15b97-350">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="15b97-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15b97-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-354">NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="15b97-354">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="15b97-355">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="15b97-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="15b97-356">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="15b97-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-357">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15b97-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-359">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="15b97-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="15b97-360">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и не используется.</span><span class="sxs-lookup"><span data-stu-id="15b97-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="15b97-361">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="15b97-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15b97-362">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15b97-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15b97-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15b97-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15b97-364">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="15b97-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="15b97-365">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15b97-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15b97-366">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15b97-366">Remarks</span></span>

<span data-ttu-id="15b97-367">Доступ к классу **\_ транспарентбридгингсервице мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="15b97-367">Access to the **Msvm\_TransparentBridgingService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="15b97-368">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="15b97-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="15b97-369">Требования</span><span class="sxs-lookup"><span data-stu-id="15b97-369">Requirements</span></span>



| <span data-ttu-id="15b97-370">Требование</span><span class="sxs-lookup"><span data-stu-id="15b97-370">Requirement</span></span> | <span data-ttu-id="15b97-371">Значение</span><span class="sxs-lookup"><span data-stu-id="15b97-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b97-372">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15b97-372">Minimum supported client</span></span><br/> | <span data-ttu-id="15b97-373">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="15b97-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="15b97-374">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15b97-374">Minimum supported server</span></span><br/> | <span data-ttu-id="15b97-375">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="15b97-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15b97-376">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="15b97-376">Namespace</span></span><br/>                | <span data-ttu-id="15b97-377">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="15b97-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15b97-378">MOF</span><span class="sxs-lookup"><span data-stu-id="15b97-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15b97-379"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15b97-380">DLL</span><span class="sxs-lookup"><span data-stu-id="15b97-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15b97-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15b97-382">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15b97-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b97-383">**\_ТРАНСПАРЕНТБРИДГИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="15b97-383">**CIM\_TransparentBridgingService**</span></span>](cim-transparentbridgingservice.md)
</dt> <dt>

[<span data-ttu-id="15b97-384">**\_ТРАНСПАРЕНТБРИДГИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="15b97-384">**CIM\_TransparentBridgingService**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

