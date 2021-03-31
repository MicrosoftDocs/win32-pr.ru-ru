---
description: Представляет виртуальный Fibre Channel коммутатор.
ms.assetid: 4300747b-3ffc-4caf-8f0b-76cab6d2294e
title: Класс Msvm_VirtualFcSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitch
- Msvm_VirtualFcSwitch.SetPowerState
- Msvm_VirtualFcSwitch.InstanceID
- Msvm_VirtualFcSwitch.Caption
- Msvm_VirtualFcSwitch.Description
- Msvm_VirtualFcSwitch.ElementName
- Msvm_VirtualFcSwitch.InstallDate
- Msvm_VirtualFcSwitch.OperationalStatus
- Msvm_VirtualFcSwitch.StatusDescriptions
- Msvm_VirtualFcSwitch.Status
- Msvm_VirtualFcSwitch.HealthState
- Msvm_VirtualFcSwitch.CommunicationStatus
- Msvm_VirtualFcSwitch.DetailedStatus
- Msvm_VirtualFcSwitch.OperatingStatus
- Msvm_VirtualFcSwitch.PrimaryStatus
- Msvm_VirtualFcSwitch.EnabledState
- Msvm_VirtualFcSwitch.OtherEnabledState
- Msvm_VirtualFcSwitch.RequestedState
- Msvm_VirtualFcSwitch.EnabledDefault
- Msvm_VirtualFcSwitch.TimeOfLastStateChange
- Msvm_VirtualFcSwitch.AvailableRequestedStates
- Msvm_VirtualFcSwitch.TransitioningToState
- Msvm_VirtualFcSwitch.CreationClassName
- Msvm_VirtualFcSwitch.Name
- Msvm_VirtualFcSwitch.PrimaryOwnerName
- Msvm_VirtualFcSwitch.PrimaryOwnerContact
- Msvm_VirtualFcSwitch.Roles
- Msvm_VirtualFcSwitch.NameFormat
- Msvm_VirtualFcSwitch.OtherIdentifyingInfo
- Msvm_VirtualFcSwitch.IdentifyingDescriptions
- Msvm_VirtualFcSwitch.Dedicated
- Msvm_VirtualFcSwitch.OtherDedicatedDescriptions
- Msvm_VirtualFcSwitch.ResetCapability
- Msvm_VirtualFcSwitch.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66c6b7a284a2751b1c9b664428a9c90db9f468a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143888"
---
# <a name="msvm_virtualfcswitch-class"></a><span data-ttu-id="ddd19-103">\_Класс мсвм виртуалфксвитч</span><span class="sxs-lookup"><span data-stu-id="ddd19-103">Msvm\_VirtualFcSwitch class</span></span>

<span data-ttu-id="ddd19-104">Представляет виртуальный Fibre Channel коммутатор.</span><span class="sxs-lookup"><span data-stu-id="ddd19-104">Represents a virtual Fibre Channel switch.</span></span> <span data-ttu-id="ddd19-105">Каждый коммутатор связан с одним физическим Fibre Channel портом, к которому можно подключить множество портов искусственного Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="ddd19-105">Each switch is associated with one physical Fibre Channel port to which many synthetic Fibre Channel ports can be connected.</span></span> <span data-ttu-id="ddd19-106">Сам переключатель не настраивается с высокой назначением и действует в основном как заполнитель.</span><span class="sxs-lookup"><span data-stu-id="ddd19-106">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="ddd19-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ddd19-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddd19-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddd19-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
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
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="ddd19-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ddd19-109">Members</span></span>

<span data-ttu-id="ddd19-110">Класс **мсвм \_ виртуалфксвитч** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ddd19-110">The **Msvm\_VirtualFcSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="ddd19-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ddd19-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ddd19-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ddd19-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ddd19-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ddd19-113">Methods</span></span>

<span data-ttu-id="ddd19-114">Класс **мсвм \_ виртуалфксвитч** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ddd19-114">The **Msvm\_VirtualFcSwitch** class has these methods.</span></span>



| <span data-ttu-id="ddd19-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ddd19-115">Method</span></span>                                                                | <span data-ttu-id="ddd19-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ddd19-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="ddd19-117">**Равен**</span><span class="sxs-lookup"><span data-stu-id="ddd19-117">**RequestStateChange**</span></span>](msvm-virtualfcswitch-requeststatechange.md) | <span data-ttu-id="ddd19-118">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="ddd19-118">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="ddd19-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ddd19-119">**SetPowerState**</span></span>                                                     | <span data-ttu-id="ddd19-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ddd19-120">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ddd19-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="ddd19-121">Properties</span></span>

<span data-ttu-id="ddd19-122">Класс **мсвм \_ виртуалфксвитч** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ddd19-122">The **Msvm\_VirtualFcSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddd19-123">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="ddd19-123">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-124">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ddd19-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-126">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="ddd19-126">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="ddd19-127">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ddd19-127">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="ddd19-128">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="ddd19-128">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="ddd19-129">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="ddd19-129">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="ddd19-130">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddd19-130">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ddd19-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="ddd19-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="ddd19-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="ddd19-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="ddd19-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="ddd19-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="ddd19-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="ddd19-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="ddd19-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="ddd19-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="ddd19-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="ddd19-141">)</span><span class="sxs-lookup"><span data-stu-id="ddd19-141">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddd19-142">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ddd19-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-145">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ddd19-145">A short description of the object.</span></span> <span data-ttu-id="ddd19-146">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-147">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="ddd19-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-148">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-150">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="ddd19-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ddd19-151">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ddd19-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddd19-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ddd19-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ddd19-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="ddd19-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="ddd19-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="ddd19-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="ddd19-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ddd19-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ddd19-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ddd19-160">)</span><span class="sxs-lookup"><span data-stu-id="ddd19-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddd19-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddd19-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-164">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ddd19-164">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="ddd19-165">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="ddd19-165">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-166">**Выделенные**</span><span class="sxs-lookup"><span data-stu-id="ddd19-166">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-167">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ddd19-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-169">Указывает, является ли компьютерная система специальной (выделенной для конкретного использования), а не универсальной системой.</span><span class="sxs-lookup"><span data-stu-id="ddd19-169">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="ddd19-170">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение 0 (не выделено).</span><span class="sxs-lookup"><span data-stu-id="ddd19-170">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ddd19-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-174">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ddd19-174">A description of the object.</span></span> <span data-ttu-id="ddd19-175">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ddd19-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-177">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-179">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="ddd19-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ddd19-180">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ddd19-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddd19-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ddd19-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="ddd19-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="ddd19-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="ddd19-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="ddd19-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="ddd19-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="ddd19-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ddd19-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ddd19-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ddd19-190">)</span><span class="sxs-lookup"><span data-stu-id="ddd19-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddd19-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ddd19-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-194">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ddd19-194">A display name for the object.</span></span> <span data-ttu-id="ddd19-195">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-196">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="ddd19-196">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-197">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-199">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ddd19-199">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ddd19-200">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ddd19-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ddd19-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="ddd19-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="ddd19-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="ddd19-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddd19-204">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ddd19-204">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-205">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-207">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ddd19-207">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ddd19-208">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="ddd19-208">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="ddd19-209">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="ddd19-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-210">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ddd19-210">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-213">Указывает текущую работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="ddd19-213">Specifies the current health of the element.</span></span> <span data-ttu-id="ddd19-214">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="ddd19-214">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="ddd19-215">При возникновении критической ошибки просмотрите подробные сведения в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="ddd19-215">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="ddd19-216">Свойство **EnabledState** также может содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ddd19-216">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="ddd19-217">Например, если место на диске критически низкий, значение **HealthState** равно 25, виртуальная машина будет приостановлена, а параметру **EnabledState** будет присвоено значение 32768 (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="ddd19-217">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="ddd19-218">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="ddd19-219">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd19-219">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="ddd19-220">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd19-220">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="ddd19-221"><dt>**ОК**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ddd19-221"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="ddd19-222">Элемент является полностью функциональным и работает в нормальных рабочих параметрах и без ошибок.</span><span class="sxs-lookup"><span data-stu-id="ddd19-222">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="ddd19-223"><dt>**Серьезный сбой**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="ddd19-223"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="ddd19-224">В элементе возникла серьезная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ddd19-224">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="ddd19-225"><dt>**Критический сбой**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="ddd19-225"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="ddd19-226">Элемент нефункциональный, и восстановление может быть невозможным.</span><span class="sxs-lookup"><span data-stu-id="ddd19-226">The element is nonfunctional and recovery might not be possible.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="ddd19-227">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ddd19-227">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-228">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ddd19-228">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-230">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-230">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ddd19-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-232">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddd19-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-234">Дата и время создания конфигурации виртуальной машины для виртуальной машины или **значение NULL** для операционной системы управления.</span><span class="sxs-lookup"><span data-stu-id="ddd19-234">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="ddd19-235">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-236">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ddd19-236">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-239">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ddd19-239">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-240">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ddd19-240">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ddd19-241">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-241">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-242">**Name**</span><span class="sxs-lookup"><span data-stu-id="ddd19-242">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-245">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="ddd19-245">The label by which the object is known.</span></span> <span data-ttu-id="ddd19-246">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="ddd19-246">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-247">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="ddd19-247">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-250">Строка, которая определяет, как было создано системное имя с использованием эвристики подкласса.</span><span class="sxs-lookup"><span data-stu-id="ddd19-250">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="ddd19-251">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-251">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-252">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="ddd19-252">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-253">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-255">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ddd19-255">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ddd19-256">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ddd19-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddd19-257">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ddd19-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ddd19-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="ddd19-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="ddd19-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="ddd19-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="ddd19-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="ddd19-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="ddd19-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="ddd19-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="ddd19-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="ddd19-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="ddd19-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="ddd19-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="ddd19-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="ddd19-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="ddd19-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="ddd19-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="ddd19-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ddd19-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ddd19-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ddd19-277">)</span><span class="sxs-lookup"><span data-stu-id="ddd19-277">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddd19-278">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ddd19-278">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-279">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ddd19-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-281">Массив, содержащий текущие состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="ddd19-281">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="ddd19-282">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-283">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ddd19-283">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-284">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ddd19-284">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-286">Строка, описывающая, как или почему система выделяется, когда **выделенный** массив включает значение 2 (другое).</span><span class="sxs-lookup"><span data-stu-id="ddd19-286">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="ddd19-287">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-287">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-288">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="ddd19-288">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-291">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ddd19-291">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ddd19-292">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="ddd19-292">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ddd19-293">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-293">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-294">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ddd19-294">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-295">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ddd19-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-297">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-298">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ddd19-298">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-299">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ddd19-299">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-301">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ddd19-301">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-302">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="ddd19-302">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-305">Строка, которая указывает, как можно достичь основного владельца системы (например, номер телефона или адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="ddd19-305">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="ddd19-306">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-306">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-307">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="ddd19-307">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-310">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="ddd19-310">The name of the primary system owner.</span></span> <span data-ttu-id="ddd19-311">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-311">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-312">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="ddd19-312">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-313">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-315">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="ddd19-315">Provides high level status information.</span></span> <span data-ttu-id="ddd19-316">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="ddd19-316">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ddd19-317">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ddd19-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddd19-318">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ddd19-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ddd19-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-320"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="ddd19-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="ddd19-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="ddd19-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ddd19-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ddd19-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ddd19-325">)</span><span class="sxs-lookup"><span data-stu-id="ddd19-325">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddd19-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ddd19-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-327">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-329">Последнее запрошенное или требуемое состояние элемента, переданное методу **RequestStateChange** , или 12 (неприменимо), если изменение состояния не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddd19-329">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="ddd19-330">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="ddd19-331">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="ddd19-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="ddd19-332">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddd19-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-333">**ресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="ddd19-333">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-334">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-336">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span><span class="sxs-lookup"><span data-stu-id="ddd19-336">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-337">**Роли**</span><span class="sxs-lookup"><span data-stu-id="ddd19-337">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-338">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ddd19-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-340">Массив строк, описывающих роли, которые система играет в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="ddd19-340">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="ddd19-341">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddd19-341">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-342">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ddd19-342">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ddd19-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-345">Строка, указывающая состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="ddd19-345">A string that specifies the status of the element.</span></span> <span data-ttu-id="ddd19-346">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-346">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-347">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ddd19-347">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-348">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ddd19-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-350">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ddd19-350">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-351">Массив, содержащий строки, описывающие соответствующие значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ddd19-351">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="ddd19-352">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddd19-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-353">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="ddd19-353">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-354">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddd19-354">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-356">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ddd19-356">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ddd19-357">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddd19-357">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddd19-358">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="ddd19-358">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddd19-359">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddd19-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddd19-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ddd19-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddd19-361">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ddd19-361">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ddd19-362">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddd19-362">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddd19-363">Требования</span><span class="sxs-lookup"><span data-stu-id="ddd19-363">Requirements</span></span>



| <span data-ttu-id="ddd19-364">Требование</span><span class="sxs-lookup"><span data-stu-id="ddd19-364">Requirement</span></span> | <span data-ttu-id="ddd19-365">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd19-365">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd19-366">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddd19-366">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd19-367">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ddd19-367">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ddd19-368">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddd19-368">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd19-369">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ddd19-369">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ddd19-370">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ddd19-370">Namespace</span></span><br/>                | <span data-ttu-id="ddd19-371">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ddd19-371">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ddd19-372">MOF</span><span class="sxs-lookup"><span data-stu-id="ddd19-372">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddd19-373"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddd19-373"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddd19-374">DLL</span><span class="sxs-lookup"><span data-stu-id="ddd19-374">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddd19-375"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ddd19-375"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

