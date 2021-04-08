---
description: Представляет виртуальный коммутатор Ethernet. Каждый коммутатор имеет много портов, к которым могут быть подключены сетевые адаптеры. Сам переключатель не настраивается с высокой назначением и действует в основном как заполнитель.
ms.assetid: 9415477a-9423-40fa-a887-3a93da1374af
title: Класс Msvm_VirtualEthernetSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitch
- Msvm_VirtualEthernetSwitch.SetPowerState
- Msvm_VirtualEthernetSwitch.InstanceID
- Msvm_VirtualEthernetSwitch.Caption
- Msvm_VirtualEthernetSwitch.Description
- Msvm_VirtualEthernetSwitch.ElementName
- Msvm_VirtualEthernetSwitch.InstallDate
- Msvm_VirtualEthernetSwitch.OperationalStatus
- Msvm_VirtualEthernetSwitch.StatusDescriptions
- Msvm_VirtualEthernetSwitch.Status
- Msvm_VirtualEthernetSwitch.HealthState
- Msvm_VirtualEthernetSwitch.CommunicationStatus
- Msvm_VirtualEthernetSwitch.DetailedStatus
- Msvm_VirtualEthernetSwitch.OperatingStatus
- Msvm_VirtualEthernetSwitch.PrimaryStatus
- Msvm_VirtualEthernetSwitch.EnabledState
- Msvm_VirtualEthernetSwitch.OtherEnabledState
- Msvm_VirtualEthernetSwitch.RequestedState
- Msvm_VirtualEthernetSwitch.EnabledDefault
- Msvm_VirtualEthernetSwitch.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitch.AvailableRequestedStates
- Msvm_VirtualEthernetSwitch.TransitioningToState
- Msvm_VirtualEthernetSwitch.CreationClassName
- Msvm_VirtualEthernetSwitch.Name
- Msvm_VirtualEthernetSwitch.PrimaryOwnerName
- Msvm_VirtualEthernetSwitch.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitch.Roles
- Msvm_VirtualEthernetSwitch.NameFormat
- Msvm_VirtualEthernetSwitch.OtherIdentifyingInfo
- Msvm_VirtualEthernetSwitch.IdentifyingDescriptions
- Msvm_VirtualEthernetSwitch.Dedicated
- Msvm_VirtualEthernetSwitch.OtherDedicatedDescriptions
- Msvm_VirtualEthernetSwitch.ResetCapability
- Msvm_VirtualEthernetSwitch.PowerManagementCapabilities
- Msvm_VirtualEthernetSwitch.MaxVMQOffloads
- Msvm_VirtualEthernetSwitch.MaxIOVOffloads
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cd916e24a6e34ed6a70002c4988f55810050c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911011"
---
# <a name="msvm_virtualethernetswitch-class"></a><span data-ttu-id="8bf55-105">\_Класс мсвм виртуалесернетсвитч</span><span class="sxs-lookup"><span data-stu-id="8bf55-105">Msvm\_VirtualEthernetSwitch class</span></span>

<span data-ttu-id="8bf55-106">Представляет виртуальный коммутатор Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8bf55-106">Represents a virtual Ethernet switch.</span></span> <span data-ttu-id="8bf55-107">Каждый коммутатор имеет много портов, к которым могут быть подключены сетевые адаптеры.</span><span class="sxs-lookup"><span data-stu-id="8bf55-107">Each switch has many different ports to which network adapters can be attached.</span></span> <span data-ttu-id="8bf55-108">Сам переключатель не настраивается с высокой назначением и действует в основном как заполнитель.</span><span class="sxs-lookup"><span data-stu-id="8bf55-108">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="8bf55-109">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8bf55-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf55-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf55-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Virtual Switch";
  string   Description = "Microsoft Virtual Switch";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName = "Msvm_VirtualEthernetSwitch";
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 5;
  uint16   PowerManagementCapabilities[];
  uint32   MaxVMQOffloads;
  uint32   MaxIOVOffloads;
};
```

## <a name="members"></a><span data-ttu-id="8bf55-111">Члены</span><span class="sxs-lookup"><span data-stu-id="8bf55-111">Members</span></span>

<span data-ttu-id="8bf55-112">Класс **мсвм \_ виртуалесернетсвитч** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8bf55-112">The **Msvm\_VirtualEthernetSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="8bf55-113">Методы</span><span class="sxs-lookup"><span data-stu-id="8bf55-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="8bf55-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="8bf55-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8bf55-115">Методы</span><span class="sxs-lookup"><span data-stu-id="8bf55-115">Methods</span></span>

<span data-ttu-id="8bf55-116">Класс **мсвм \_ виртуалесернетсвитч** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8bf55-116">The **Msvm\_VirtualEthernetSwitch** class has these methods.</span></span>



| <span data-ttu-id="8bf55-117">Метод</span><span class="sxs-lookup"><span data-stu-id="8bf55-117">Method</span></span>                                                                      | <span data-ttu-id="8bf55-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8bf55-118">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="8bf55-119">**Равен**</span><span class="sxs-lookup"><span data-stu-id="8bf55-119">**RequestStateChange**</span></span>](msvm-virtualethernetswitch-requeststatechange.md) | <span data-ttu-id="8bf55-120">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf55-120">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="8bf55-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8bf55-121">**SetPowerState**</span></span>                                                           | <span data-ttu-id="8bf55-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8bf55-122">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8bf55-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="8bf55-123">Properties</span></span>

<span data-ttu-id="8bf55-124">Класс **мсвм \_ виртуалесернетсвитч** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8bf55-124">The **Msvm\_VirtualEthernetSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bf55-125">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="8bf55-125">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-126">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf55-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-128">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf55-128">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="8bf55-129">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8bf55-129">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="8bf55-130">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf55-130">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="8bf55-131">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf55-131">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="8bf55-132">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf55-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8bf55-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="8bf55-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="8bf55-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="8bf55-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="8bf55-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="8bf55-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="8bf55-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="8bf55-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="8bf55-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="8bf55-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="8bf55-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="8bf55-143">)</span><span class="sxs-lookup"><span data-stu-id="8bf55-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bf55-144">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8bf55-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-147">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf55-147">A short description of the object.</span></span> <span data-ttu-id="8bf55-148">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "виртуальный коммутатор".</span><span class="sxs-lookup"><span data-stu-id="8bf55-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-149">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="8bf55-149">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-152">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="8bf55-152">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8bf55-153">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf55-153">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf55-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8bf55-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8bf55-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="8bf55-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="8bf55-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="8bf55-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="8bf55-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8bf55-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8bf55-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8bf55-162">)</span><span class="sxs-lookup"><span data-stu-id="8bf55-162">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bf55-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8bf55-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-166">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8bf55-166">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="8bf55-167">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение "мсвм \_ виртуалесернетсвитч".</span><span class="sxs-lookup"><span data-stu-id="8bf55-167">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-168">**Выделенные**</span><span class="sxs-lookup"><span data-stu-id="8bf55-168">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-169">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf55-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-171">Указывает, является ли компьютерная система специальной (выделенной для конкретного использования), а не универсальной системой.</span><span class="sxs-lookup"><span data-stu-id="8bf55-171">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="8bf55-172">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение 0 (не выделено).</span><span class="sxs-lookup"><span data-stu-id="8bf55-172">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-173">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8bf55-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-176">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf55-176">A description of the object.</span></span> <span data-ttu-id="8bf55-177">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "виртуальный коммутатор Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="8bf55-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8bf55-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-181">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8bf55-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8bf55-182">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf55-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf55-183">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8bf55-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="8bf55-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="8bf55-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="8bf55-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="8bf55-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="8bf55-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="8bf55-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8bf55-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8bf55-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8bf55-192">)</span><span class="sxs-lookup"><span data-stu-id="8bf55-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bf55-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8bf55-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-196">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf55-196">A display name for the object.</span></span> <span data-ttu-id="8bf55-197">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-198">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="8bf55-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-199">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-201">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf55-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8bf55-202">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8bf55-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8bf55-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="8bf55-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="8bf55-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="8bf55-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bf55-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8bf55-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-207">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-209">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf55-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8bf55-210">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="8bf55-210">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8bf55-211">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="8bf55-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-212">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8bf55-212">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-215">Указывает текущую работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf55-215">Specifies the current health of the element.</span></span> <span data-ttu-id="8bf55-216">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8bf55-216">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="8bf55-217">При возникновении критической ошибки просмотрите подробные сведения в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="8bf55-217">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="8bf55-218">Свойство **EnabledState** также может содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8bf55-218">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="8bf55-219">Например, если место на диске критически низкий, значение **HealthState** равно 25, виртуальная машина будет приостановлена, а параметру **EnabledState** будет присвоено значение 32768 (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="8bf55-219">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="8bf55-220">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="8bf55-221">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf55-221">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="8bf55-222">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf55-222">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="8bf55-223"><dt>**ОК**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8bf55-223"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="8bf55-224">Элемент является полностью функциональным и работает в нормальных рабочих параметрах и без ошибок.</span><span class="sxs-lookup"><span data-stu-id="8bf55-224">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="8bf55-225"><dt>**Серьезный сбой**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="8bf55-225"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="8bf55-226">В элементе возникла серьезная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8bf55-226">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="8bf55-227"><dt>**Критический сбой**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="8bf55-227"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="8bf55-228">Элемент нефункциональный, и восстановление может быть невозможным.</span><span class="sxs-lookup"><span data-stu-id="8bf55-228">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="8bf55-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8bf55-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-230">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf55-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-232">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-232">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-233">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8bf55-233">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-234">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8bf55-234">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-236">Дата и время создания конфигурации виртуальной машины для виртуальной машины или **значение NULL** для операционной системы управления.</span><span class="sxs-lookup"><span data-stu-id="8bf55-236">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="8bf55-237">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-238">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8bf55-238">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-239">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-241">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8bf55-241">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-242">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="8bf55-242">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8bf55-243">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-243">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-244">**максиовоффлоадс**</span><span class="sxs-lookup"><span data-stu-id="8bf55-244">**MaxIOVOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-245">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8bf55-245">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-247">Максимальное число разгрузок однокорневых виртуальных функций виртуализации (SR-IOV), доступных на этом коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="8bf55-247">The maximum number of single root IO virtualization (SR-IOV) virtual function offloads available on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-248">**максвмкоффлоадс**</span><span class="sxs-lookup"><span data-stu-id="8bf55-248">**MaxVMQOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-249">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8bf55-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8bf55-250">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-251">Максимальное число разгрузок очереди виртуальных машин (VMQ), разрешенное для порта данного коммутатора.</span><span class="sxs-lookup"><span data-stu-id="8bf55-251">The maximum number of virtual machine queue (VMQ) offloads allowed for a port on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-252">**Name**</span><span class="sxs-lookup"><span data-stu-id="8bf55-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-255">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8bf55-255">The label by which the object is known.</span></span> <span data-ttu-id="8bf55-256">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="8bf55-256">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-257">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="8bf55-257">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-260">Строка, которая определяет, как было создано системное имя с использованием эвристики подкласса.</span><span class="sxs-lookup"><span data-stu-id="8bf55-260">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="8bf55-261">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-261">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-262">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="8bf55-262">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-263">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-265">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8bf55-265">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8bf55-266">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf55-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf55-267">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8bf55-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8bf55-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="8bf55-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="8bf55-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="8bf55-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="8bf55-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="8bf55-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="8bf55-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="8bf55-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="8bf55-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="8bf55-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="8bf55-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="8bf55-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="8bf55-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="8bf55-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="8bf55-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="8bf55-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="8bf55-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8bf55-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8bf55-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8bf55-287">)</span><span class="sxs-lookup"><span data-stu-id="8bf55-287">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bf55-288">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8bf55-288">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-289">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf55-289">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-291">Массив, содержащий текущие состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf55-291">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="8bf55-292">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-293">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8bf55-293">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-294">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf55-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-296">Строка, описывающая, как или почему система выделяется, когда **выделенный** массив включает значение 2 (другое).</span><span class="sxs-lookup"><span data-stu-id="8bf55-296">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="8bf55-297">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-298">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="8bf55-298">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-301">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8bf55-301">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8bf55-302">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="8bf55-302">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8bf55-303">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-304">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8bf55-304">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-305">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf55-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-307">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-307">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-308">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8bf55-308">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-309">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf55-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-311">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf55-311">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-312">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="8bf55-312">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-315">Строка, которая указывает, как можно достичь основного владельца системы (например, номер телефона или адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="8bf55-315">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="8bf55-316">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-316">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-317">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="8bf55-317">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-320">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="8bf55-320">The name of the primary system owner.</span></span> <span data-ttu-id="8bf55-321">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-321">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-322">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="8bf55-322">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-323">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-325">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="8bf55-325">Provides high level status information.</span></span> <span data-ttu-id="8bf55-326">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8bf55-326">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8bf55-327">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf55-327">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf55-328">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8bf55-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8bf55-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-330"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="8bf55-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="8bf55-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="8bf55-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8bf55-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8bf55-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8bf55-335">)</span><span class="sxs-lookup"><span data-stu-id="8bf55-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bf55-336">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8bf55-336">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-337">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-339">Последнее запрошенное или требуемое состояние элемента, переданное методу **RequestStateChange** , или 12 (неприменимо), если изменение состояния не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bf55-339">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="8bf55-340">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-340">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8bf55-341">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf55-341">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8bf55-342">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf55-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-343">**ресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="8bf55-343">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-344">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-346">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение 5 (не реализовано).</span><span class="sxs-lookup"><span data-stu-id="8bf55-346">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 5 (Not implemented).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-347">**Роли**</span><span class="sxs-lookup"><span data-stu-id="8bf55-347">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-348">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf55-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-350">Массив строк, описывающих роли, которые система играет в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="8bf55-350">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="8bf55-351">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf55-351">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-352">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8bf55-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf55-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-355">Строка, указывающая состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf55-355">A string that specifies the status of the element.</span></span> <span data-ttu-id="8bf55-356">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-357">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="8bf55-357">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-358">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf55-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-360">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="8bf55-360">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-361">Массив, содержащий строки, описывающие соответствующие значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8bf55-361">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="8bf55-362">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf55-362">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-363">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="8bf55-363">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-364">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8bf55-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-366">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf55-366">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8bf55-367">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf55-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf55-368">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="8bf55-368">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf55-369">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf55-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf55-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf55-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf55-371">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8bf55-371">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8bf55-372">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf55-372">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bf55-373">Требования</span><span class="sxs-lookup"><span data-stu-id="8bf55-373">Requirements</span></span>



| <span data-ttu-id="8bf55-374">Требование</span><span class="sxs-lookup"><span data-stu-id="8bf55-374">Requirement</span></span> | <span data-ttu-id="8bf55-375">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf55-375">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf55-376">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bf55-376">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf55-377">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8bf55-377">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8bf55-378">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bf55-378">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf55-379">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8bf55-379">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bf55-380">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8bf55-380">Namespace</span></span><br/>                | <span data-ttu-id="8bf55-381">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8bf55-381">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8bf55-382">MOF</span><span class="sxs-lookup"><span data-stu-id="8bf55-382">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bf55-383"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bf55-383"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bf55-384">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf55-384">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf55-385"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8bf55-385"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

