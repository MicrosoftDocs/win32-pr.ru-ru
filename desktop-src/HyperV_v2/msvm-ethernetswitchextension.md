---
description: Представляет экземпляр компонента расширения, привязанного к виртуальному коммутатору Ethernet.
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Класс Msvm_EthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664773"
---
# <a name="msvm_ethernetswitchextension-class"></a><span data-ttu-id="c4f9f-103">\_Класс мсвм есернетсвитчекстенсион</span><span class="sxs-lookup"><span data-stu-id="c4f9f-103">Msvm\_EthernetSwitchExtension class</span></span>

<span data-ttu-id="c4f9f-104">Представляет экземпляр компонента расширения, привязанного к виртуальному коммутатору Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-104">Represents an instance of an extension component bound to a virtual Ethernet switch.</span></span>

<span data-ttu-id="c4f9f-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f9f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4f9f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
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
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="c4f9f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c4f9f-107">Members</span></span>

<span data-ttu-id="c4f9f-108">Класс **мсвм \_ есернетсвитчекстенсион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4f9f-108">The **Msvm\_EthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="c4f9f-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c4f9f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4f9f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4f9f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4f9f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c4f9f-111">Methods</span></span>

<span data-ttu-id="c4f9f-112">Класс **мсвм \_ есернетсвитчекстенсион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-112">The **Msvm\_EthernetSwitchExtension** class has these methods.</span></span>



| <span data-ttu-id="c4f9f-113">Метод</span><span class="sxs-lookup"><span data-stu-id="c4f9f-113">Method</span></span>                                                                        | <span data-ttu-id="c4f9f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c4f9f-114">Description</span></span>                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="c4f9f-115">**Равен**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-115">**RequestStateChange**</span></span>](msvm-ethernetswitchextension-requeststatechange.md) | <span data-ttu-id="c4f9f-116">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-116">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c4f9f-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4f9f-117">Properties</span></span>

<span data-ttu-id="c4f9f-118">Класс **мсвм \_ есернетсвитчекстенсион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-118">The **Msvm\_EthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4f9f-119">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-120">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c4f9f-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-122">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="c4f9f-123">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-123">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="c4f9f-124">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-124">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="c4f9f-125">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-125">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="c4f9f-126">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-126">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c4f9f-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="c4f9f-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c4f9f-137">)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-137">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4f9f-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-141">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-141">A short description of the object.</span></span> <span data-ttu-id="c4f9f-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Расширение виртуального коммутатора".</span><span class="sxs-lookup"><span data-stu-id="c4f9f-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch Extension".</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-143">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-143">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-146">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-146">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c4f9f-147">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-147">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4f9f-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-148">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-149">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-149">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-152">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-153">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-153">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="c4f9f-154">Для этого свойства всегда задано значение "Мсвм \_ есернетсвитчекстенсион".</span><span class="sxs-lookup"><span data-stu-id="c4f9f-154">This property is always set to "Msvm\_EthernetSwitchExtension".</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-155">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-158">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-158">A description of the object.</span></span> <span data-ttu-id="c4f9f-159">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-160">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-160">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-163">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-163">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c4f9f-164">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4f9f-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-166">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-166">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-169">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-169">A display name for the object.</span></span> <span data-ttu-id="c4f9f-170">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-171">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-171">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-172">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-174">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-174">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c4f9f-175">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c4f9f-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4f9f-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-180">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-182">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-182">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c4f9f-183">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-183">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c4f9f-184">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-184">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c4f9f-185">Значение</span><span class="sxs-lookup"><span data-stu-id="c4f9f-185">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="c4f9f-186">Значение</span><span class="sxs-lookup"><span data-stu-id="c4f9f-186">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="c4f9f-187"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-187"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="c4f9f-188"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="c4f9f-189"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-189"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="c4f9f-190">Элемент или может выполнять команды, обрабатывает все команды в очереди и помещает новые запросы в очередь.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-190">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="c4f9f-191"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="c4f9f-192">Элемент не будет выполнять команды и удалит все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-192">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="c4f9f-193"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-193"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="c4f9f-194">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-194">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="c4f9f-195"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-195"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="c4f9f-196">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-196">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="c4f9f-197"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-197"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="c4f9f-198">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-198">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="c4f9f-199"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-199"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="c4f9f-200">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-200">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="c4f9f-201"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-201"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="c4f9f-202">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-202">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="c4f9f-203"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-203"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="c4f9f-204">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-204">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="c4f9f-205">Поведение элемента аналогично включенному состоянию, но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-205">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="c4f9f-206">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-206">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="c4f9f-207"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-207"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="c4f9f-208">Элемент находится в процессе перехода в состояние Enabled.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-208">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="c4f9f-209">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-209">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="c4f9f-210"><dt>**Зарезервировано**</dt> <dt>11 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="c4f9f-210"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="c4f9f-211">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-211">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="c4f9f-212"><dt>**Поставщик Зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-212"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="c4f9f-213">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-213">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="c4f9f-214">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-214">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-215">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-217">Указывает тип компонента расширения.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-217">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c4f9f-218">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-218">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="c4f9f-219">**Захват** (1)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-219">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="c4f9f-220">**Фильтр** (2)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-220">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="c4f9f-221">**Пересылка** (3)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-221">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="c4f9f-222">**Мониторинг** (4)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-222">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="c4f9f-223">**Машинный код** (5)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-223">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c4f9f-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-225">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-227">Указывает текущую работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-227">Specifies the current health of the element.</span></span> <span data-ttu-id="c4f9f-228">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-228">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="c4f9f-229">При возникновении критической ошибки просмотрите подробные сведения в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-229">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="c4f9f-230">Свойство **EnabledState** также может содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-230">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="c4f9f-231">Например, если место на диске критически низкий, значение **HealthState** равно 25, виртуальная машина будет приостановлена, а параметру **EnabledState** будет присвоено значение 32768 (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-231">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="c4f9f-232">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="c4f9f-233">Значение</span><span class="sxs-lookup"><span data-stu-id="c4f9f-233">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="c4f9f-234">Значение</span><span class="sxs-lookup"><span data-stu-id="c4f9f-234">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="c4f9f-235"><dt>**ОК**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-235"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="c4f9f-236">Элемент является полностью функциональным и работает в нормальных рабочих параметрах и без ошибок.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-236">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="c4f9f-237"><dt>**Серьезный сбой**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-237"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="c4f9f-238">В элементе возникла серьезная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-238">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="c4f9f-239"><dt>**Критический сбой**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-239"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="c4f9f-240">Элемент нефункциональный, и восстановление может быть невозможным.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-240">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="c4f9f-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-242">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-244">Дата и время создания конфигурации виртуальной машины для виртуальной машины или **значение NULL** для операционной системы управления.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-244">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="c4f9f-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-249">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-250">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c4f9f-251">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-252">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-255">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-255">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-256">Уникальное имя компонента расширения.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-256">The unique name of the extension component.</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-257">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-257">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-258">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-260">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c4f9f-260">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c4f9f-261">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-261">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4f9f-262">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-262">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-263">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-263">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-264">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c4f9f-264">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-266">Массив, содержащий текущие состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-266">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="c4f9f-267">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-268">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-268">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-271">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-271">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c4f9f-272">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-272">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c4f9f-273">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-273">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-274">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-274">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-275">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-277">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-277">Provides high level status information.</span></span> <span data-ttu-id="c4f9f-278">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-278">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c4f9f-279">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-279">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4f9f-280">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-281">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-281">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-282">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-284">Последнее запрошенное или требуемое состояние элемента, переданное методу **RequestStateChange** , или 12 (неприменимо), если изменение состояния не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-284">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="c4f9f-285">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-285">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c4f9f-286">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-286">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="c4f9f-287">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-288">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-291">Строка, указывающая состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-291">A string that specifies the status of the element.</span></span> <span data-ttu-id="c4f9f-292">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-293">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-294">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-296">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="c4f9f-296">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-297">Массив, содержащий строки, описывающие соответствующие значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c4f9f-297">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="c4f9f-298">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-298">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-299">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-299">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-302">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-303">Имя класса создания системы.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-303">The system creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-304">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-304">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-307">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c4f9f-307">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-308">Имя виртуального коммутатора, к которому привязан экземпляр расширения.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-308">The name of the virtual switch to which the extension instance is bound to.</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-309">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-309">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-310">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-312">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-312">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c4f9f-313">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4f9f-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-314">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-314">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-315">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-315">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-317">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-317">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c4f9f-318">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-319">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-319">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-322">Указывает поставщика, предоставляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="c4f9f-322">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="c4f9f-323">**Version**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-323">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4f9f-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4f9f-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4f9f-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4f9f-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4f9f-326">Версия расширения в формате "*основной*". *minor*", например" 2,0 ".</span><span class="sxs-lookup"><span data-stu-id="c4f9f-326">The version of the extension in a format of "*major*.*minor*", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4f9f-327">Требования</span><span class="sxs-lookup"><span data-stu-id="c4f9f-327">Requirements</span></span>



| <span data-ttu-id="c4f9f-328">Требование</span><span class="sxs-lookup"><span data-stu-id="c4f9f-328">Requirement</span></span> | <span data-ttu-id="c4f9f-329">Значение</span><span class="sxs-lookup"><span data-stu-id="c4f9f-329">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f9f-330">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4f9f-330">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f9f-331">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c4f9f-331">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4f9f-332">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4f9f-332">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f9f-333">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c4f9f-333">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4f9f-334">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4f9f-334">Namespace</span></span><br/>                | <span data-ttu-id="c4f9f-335">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c4f9f-335">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4f9f-336">MOF</span><span class="sxs-lookup"><span data-stu-id="c4f9f-336">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4f9f-337"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-337"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4f9f-338">DLL</span><span class="sxs-lookup"><span data-stu-id="c4f9f-338">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4f9f-339"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4f9f-339"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

