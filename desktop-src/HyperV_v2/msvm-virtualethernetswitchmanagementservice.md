---
description: Представляет службу виртуализации, имеющуюся в одной системе узла. Мсвм \_ виртуалесернетсвитчманажементсервице используется для управления определением, изменением и удалением виртуальных коммутаторов Ethernet.
ms.assetid: d29935d3-3a88-4186-97e9-b27c0c0d07d0
title: Класс Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService
- Msvm_VirtualEthernetSwitchManagementService.InstanceID
- Msvm_VirtualEthernetSwitchManagementService.Caption
- Msvm_VirtualEthernetSwitchManagementService.Description
- Msvm_VirtualEthernetSwitchManagementService.ElementName
- Msvm_VirtualEthernetSwitchManagementService.InstallDate
- Msvm_VirtualEthernetSwitchManagementService.Name
- Msvm_VirtualEthernetSwitchManagementService.OperationalStatus
- Msvm_VirtualEthernetSwitchManagementService.StatusDescriptions
- Msvm_VirtualEthernetSwitchManagementService.Status
- Msvm_VirtualEthernetSwitchManagementService.HealthState
- Msvm_VirtualEthernetSwitchManagementService.CommunicationStatus
- Msvm_VirtualEthernetSwitchManagementService.DetailedStatus
- Msvm_VirtualEthernetSwitchManagementService.OperatingStatus
- Msvm_VirtualEthernetSwitchManagementService.PrimaryStatus
- Msvm_VirtualEthernetSwitchManagementService.EnabledState
- Msvm_VirtualEthernetSwitchManagementService.OtherEnabledState
- Msvm_VirtualEthernetSwitchManagementService.RequestedState
- Msvm_VirtualEthernetSwitchManagementService.EnabledDefault
- Msvm_VirtualEthernetSwitchManagementService.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitchManagementService.AvailableRequestedStates
- Msvm_VirtualEthernetSwitchManagementService.TransitioningToState
- Msvm_VirtualEthernetSwitchManagementService.SystemCreationClassName
- Msvm_VirtualEthernetSwitchManagementService.SystemName
- Msvm_VirtualEthernetSwitchManagementService.CreationClassName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitchManagementService.StartMode
- Msvm_VirtualEthernetSwitchManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e6c1d4dee775dc6fabbb5fb3c96c987d1f6bda5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684689"
---
# <a name="msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="0c66d-104">\_Класс мсвм виртуалесернетсвитчманажементсервице</span><span class="sxs-lookup"><span data-stu-id="0c66d-104">Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="0c66d-105">Представляет службу виртуализации, имеющуюся в одной системе узла.</span><span class="sxs-lookup"><span data-stu-id="0c66d-105">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="0c66d-106">Мсвм \_ виртуалесернетсвитчманажементсервице используется для управления определением, изменением и удалением виртуальных коммутаторов Ethernet.</span><span class="sxs-lookup"><span data-stu-id="0c66d-106">Msvm\_VirtualEthernetSwitchManagementService is used to control the definition, modification, and deletion of virtual Ethernet switches.</span></span>

<span data-ttu-id="0c66d-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0c66d-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c66d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c66d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual Networking Management Service";
  string   Description = "Provides Hyper-V Networking WMI management";
  string   ElementName = "Hyper-V Networking Management Service";
  datetime InstallDate;
  string   Name = "nvspwmi";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status = { "OK" };
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitchManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="0c66d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="0c66d-109">Members</span></span>

<span data-ttu-id="0c66d-110">Класс **мсвм \_ виртуалесернетсвитчманажементсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0c66d-110">The **Msvm\_VirtualEthernetSwitchManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="0c66d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="0c66d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c66d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c66d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c66d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="0c66d-113">Methods</span></span>

<span data-ttu-id="0c66d-114">Класс **мсвм \_ виртуалесернетсвитчманажементсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0c66d-114">The **Msvm\_VirtualEthernetSwitchManagementService** class has these methods.</span></span>



| <span data-ttu-id="0c66d-115">Метод</span><span class="sxs-lookup"><span data-stu-id="0c66d-115">Method</span></span>                                                                                               | <span data-ttu-id="0c66d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0c66d-116">Description</span></span>                                                                       |
|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="0c66d-117">**аддфеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-117">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)         | <span data-ttu-id="0c66d-118">Добавляет параметры компонентов в конфигурацию порта коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="0c66d-118">Adds feature settings to the configuration of an Ethernet switch port.</span></span><br/> |
| [<span data-ttu-id="0c66d-119">**аддресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-119">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)       | <span data-ttu-id="0c66d-120">Добавляет ресурсы в конфигурацию виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="0c66d-120">Adds resources to a virtual switch configuration.</span></span><br/>                      |
| [<span data-ttu-id="0c66d-121">**дефинесистем**</span><span class="sxs-lookup"><span data-stu-id="0c66d-121">**DefineSystem**</span></span>](definesystem-msvm-virtualethernetswitchmanagementservice.md)                     | <span data-ttu-id="0c66d-122">Создает новый виртуальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="0c66d-122">Creates a new virtual switch.</span></span><br/>                                          |
| [<span data-ttu-id="0c66d-123">**дестройсистем**</span><span class="sxs-lookup"><span data-stu-id="0c66d-123">**DestroySystem**</span></span>](destroysystem-msvm-virtualethernetswitchmanagementservice.md)                   | <span data-ttu-id="0c66d-124">Уничтожает виртуальный коммутатор.</span><span class="sxs-lookup"><span data-stu-id="0c66d-124">Destroys a virtual switch.</span></span><br/>                                             |
| [<span data-ttu-id="0c66d-125">**модифифеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-125">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="0c66d-126">Изменяет настройки компонентов порта коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="0c66d-126">Modifies the feature settings of an Ethernet switch port.</span></span><br/>              |
| [<span data-ttu-id="0c66d-127">**модифиресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-127">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="0c66d-128">Изменяет параметры ресурсов для виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="0c66d-128">Modifies resource settings for a virtual switch.</span></span><br/>                       |
| [<span data-ttu-id="0c66d-129">**модифисистемсеттингс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-129">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualethernetswitchmanagementservice.md)     | <span data-ttu-id="0c66d-130">Изменяет параметры виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="0c66d-130">Modifies virtual switch settings.</span></span><br/>                                      |
| [<span data-ttu-id="0c66d-131">**ремовефеатуресеттингс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-131">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="0c66d-132">Удаляет параметры компонента с порта коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="0c66d-132">Removes feature settings from an Ethernet switch port.</span></span><br/>                 |
| [<span data-ttu-id="0c66d-133">**ремовересаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-133">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="0c66d-134">Удаляет параметры виртуального ресурса из конфигурации виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="0c66d-134">Removes virtual resource settings from a virtual switch configuration.</span></span><br/> |
| [<span data-ttu-id="0c66d-135">**Равен**</span><span class="sxs-lookup"><span data-stu-id="0c66d-135">**RequestStateChange**</span></span>](msvm-virtualethernetswitchmanagementservice-requeststatechange.md)         | <span data-ttu-id="0c66d-136">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="0c66d-136">Requests a state change.</span></span><br/>                                               |
| [<span data-ttu-id="0c66d-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="0c66d-137">**StartService**</span></span>](msvm-virtualethernetswitchmanagementservice-startservice.md)                     | <span data-ttu-id="0c66d-138">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="0c66d-138">Starts the service.</span></span><br/>                                                    |
| [<span data-ttu-id="0c66d-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="0c66d-139">**StopService**</span></span>](msvm-virtualethernetswitchmanagementservice-stopservice.md)                       | <span data-ttu-id="0c66d-140">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="0c66d-140">Stops the service.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="0c66d-141">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c66d-141">Properties</span></span>

<span data-ttu-id="0c66d-142">Класс **мсвм \_ виртуалесернетсвитчманажементсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0c66d-142">The **Msvm\_VirtualEthernetSwitchManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c66d-143">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="0c66d-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-144">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0c66d-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-146">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="0c66d-146">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0c66d-147">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-148">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0c66d-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-151">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0c66d-151">A short description of the object.</span></span> <span data-ttu-id="0c66d-152">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными сетями Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="0c66d-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-153">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="0c66d-153">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-156">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="0c66d-156">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0c66d-157">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="0c66d-157">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c66d-158">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0c66d-158">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c66d-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0c66d-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="0c66d-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="0c66d-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="0c66d-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="0c66d-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0c66d-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0c66d-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c66d-166">)</span><span class="sxs-lookup"><span data-stu-id="0c66d-166">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c66d-167">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c66d-167">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-170">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0c66d-170">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-171">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0c66d-171">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0c66d-172">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ виртуалесернетсвитчманажементсервице".</span><span class="sxs-lookup"><span data-stu-id="0c66d-172">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualEthernetSwitchManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-173">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0c66d-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-176">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0c66d-176">A description of the object.</span></span> <span data-ttu-id="0c66d-177">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "обеспечивает управление WMI сетевыми подключениями Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="0c66d-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Networking WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0c66d-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-181">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="0c66d-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0c66d-182">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="0c66d-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c66d-183">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0c66d-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c66d-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="0c66d-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="0c66d-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="0c66d-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="0c66d-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="0c66d-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="0c66d-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0c66d-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0c66d-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c66d-192">)</span><span class="sxs-lookup"><span data-stu-id="0c66d-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c66d-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0c66d-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-196">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0c66d-196">A display name for the object.</span></span> <span data-ttu-id="0c66d-197">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления сетью Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="0c66d-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-198">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="0c66d-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-199">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-201">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="0c66d-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0c66d-202">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="0c66d-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="0c66d-203">Значение</span><span class="sxs-lookup"><span data-stu-id="0c66d-203">Value</span></span>                                                                        | <span data-ttu-id="0c66d-204">Значение</span><span class="sxs-lookup"><span data-stu-id="0c66d-204">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="0c66d-205"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0c66d-205"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0c66d-206">Активировано</span><span class="sxs-lookup"><span data-stu-id="0c66d-206">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0c66d-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0c66d-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-210">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="0c66d-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0c66d-211">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="0c66d-211">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0c66d-212">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="0c66d-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-213">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0c66d-213">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-214">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-216">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="0c66d-216">The current health of the element.</span></span> <span data-ttu-id="0c66d-217">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="0c66d-217">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0c66d-218">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="0c66d-218">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0c66d-219">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="0c66d-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="0c66d-220">Значение</span><span class="sxs-lookup"><span data-stu-id="0c66d-220">Value</span></span>                                                                        | <span data-ttu-id="0c66d-221">Значение</span><span class="sxs-lookup"><span data-stu-id="0c66d-221">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="0c66d-222"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0c66d-222"><dt>5</dt></span></span> </dl> | <span data-ttu-id="0c66d-223">Состояние работоспособности — нормальное.</span><span class="sxs-lookup"><span data-stu-id="0c66d-223">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0c66d-224">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0c66d-224">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-225">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c66d-225">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-227">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c66d-227">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0c66d-228">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0c66d-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-229">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0c66d-229">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-232">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="0c66d-232">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-233">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="0c66d-233">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0c66d-234">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c66d-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-235">**Name**</span><span class="sxs-lookup"><span data-stu-id="0c66d-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-238">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0c66d-238">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-239">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="0c66d-239">The label by which the object is known.</span></span> <span data-ttu-id="0c66d-240">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "VMMS".</span><span class="sxs-lookup"><span data-stu-id="0c66d-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-241">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="0c66d-241">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-242">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-244">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0c66d-244">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0c66d-245">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="0c66d-245">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c66d-246">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0c66d-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c66d-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0c66d-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="0c66d-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="0c66d-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="0c66d-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="0c66d-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="0c66d-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="0c66d-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="0c66d-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="0c66d-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="0c66d-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="0c66d-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="0c66d-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="0c66d-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="0c66d-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="0c66d-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="0c66d-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="0c66d-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0c66d-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0c66d-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c66d-266">)</span><span class="sxs-lookup"><span data-stu-id="0c66d-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c66d-267">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0c66d-267">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-268">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0c66d-268">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-270">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0c66d-270">The current statuses of the object.</span></span> <span data-ttu-id="0c66d-271">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="0c66d-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-272">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="0c66d-272">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-275">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="0c66d-275">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="0c66d-276">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="0c66d-276">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0c66d-277">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-277">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-278">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="0c66d-278">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-281">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0c66d-281">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-282">Любые сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0c66d-282">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="0c66d-283">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-283">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-284">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="0c66d-284">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-287">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="0c66d-287">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-288">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="0c66d-288">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="0c66d-289">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="0c66d-289">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="0c66d-290">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-290">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-291">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="0c66d-291">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-292">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-292">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-294">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="0c66d-294">Provides high level status information.</span></span> <span data-ttu-id="0c66d-295">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="0c66d-295">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0c66d-296">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="0c66d-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c66d-297">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0c66d-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c66d-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0c66d-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-299"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="0c66d-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="0c66d-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="0c66d-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0c66d-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0c66d-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c66d-304">)</span><span class="sxs-lookup"><span data-stu-id="0c66d-304">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c66d-305">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0c66d-305">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-306">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-308">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="0c66d-308">The last requested or desired state for the element.</span></span> <span data-ttu-id="0c66d-309">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-309">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0c66d-310">Это свойство предназначено для сравнения последнего запрошенного и текущего состояний элемента.</span><span class="sxs-lookup"><span data-stu-id="0c66d-310">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="0c66d-311">Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать свойство **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="0c66d-311">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="0c66d-312">В этом случае используется значение 12 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="0c66d-312">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="0c66d-313">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="0c66d-313">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="0c66d-314">Значение</span><span class="sxs-lookup"><span data-stu-id="0c66d-314">Value</span></span>                                                                         | <span data-ttu-id="0c66d-315">Значение</span><span class="sxs-lookup"><span data-stu-id="0c66d-315">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="0c66d-316"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0c66d-316"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0c66d-317">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0c66d-317">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0c66d-318">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="0c66d-318">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-319">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0c66d-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-321">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="0c66d-321">Indicates whether the service is currently running.</span></span> <span data-ttu-id="0c66d-322">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-322">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-323">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="0c66d-323">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-326">Квалификаторы: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="0c66d-326">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-327">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="0c66d-327">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="0c66d-328">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-328">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-329">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0c66d-329">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-332">Описывает текущее состояние службы.</span><span class="sxs-lookup"><span data-stu-id="0c66d-332">Describes the current status of the service.</span></span> <span data-ttu-id="0c66d-333">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="0c66d-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-334">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="0c66d-334">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-335">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0c66d-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-337">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0c66d-337">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0c66d-338">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="0c66d-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-339">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="0c66d-339">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-342">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0c66d-342">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-343">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="0c66d-343">The scoping system's creation class name.</span></span> <span data-ttu-id="0c66d-344">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="0c66d-344">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-345">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0c66d-345">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c66d-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-348">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="0c66d-348">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-349">NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="0c66d-349">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="0c66d-350">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="0c66d-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-351">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="0c66d-351">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-352">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c66d-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-354">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="0c66d-354">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0c66d-355">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c66d-355">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c66d-356">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="0c66d-356">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c66d-357">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c66d-357">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c66d-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c66d-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c66d-359">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0c66d-359">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0c66d-360">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0c66d-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c66d-361">Требования</span><span class="sxs-lookup"><span data-stu-id="0c66d-361">Requirements</span></span>



| <span data-ttu-id="0c66d-362">Требование</span><span class="sxs-lookup"><span data-stu-id="0c66d-362">Requirement</span></span> | <span data-ttu-id="0c66d-363">Значение</span><span class="sxs-lookup"><span data-stu-id="0c66d-363">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c66d-364">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c66d-364">Minimum supported client</span></span><br/> | <span data-ttu-id="0c66d-365">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0c66d-365">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c66d-366">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c66d-366">Minimum supported server</span></span><br/> | <span data-ttu-id="0c66d-367">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0c66d-367">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c66d-368">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0c66d-368">Namespace</span></span><br/>                | <span data-ttu-id="0c66d-369">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0c66d-369">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c66d-370">MOF</span><span class="sxs-lookup"><span data-stu-id="0c66d-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c66d-371"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c66d-371"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c66d-372">DLL</span><span class="sxs-lookup"><span data-stu-id="0c66d-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c66d-373"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c66d-373"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

