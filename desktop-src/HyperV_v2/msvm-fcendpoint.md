---
description: Представляет логическую точку соединения для порта Fibre Channel.
ms.assetid: 54e9cb76-04f2-417b-b250-1b3156772694
title: Класс Msvm_FcEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcEndpoint
- Msvm_FcEndpoint.InstanceID
- Msvm_FcEndpoint.Caption
- Msvm_FcEndpoint.Description
- Msvm_FcEndpoint.ElementName
- Msvm_FcEndpoint.InstallDate
- Msvm_FcEndpoint.Name
- Msvm_FcEndpoint.OperationalStatus
- Msvm_FcEndpoint.StatusDescriptions
- Msvm_FcEndpoint.Status
- Msvm_FcEndpoint.HealthState
- Msvm_FcEndpoint.CommunicationStatus
- Msvm_FcEndpoint.DetailedStatus
- Msvm_FcEndpoint.OperatingStatus
- Msvm_FcEndpoint.PrimaryStatus
- Msvm_FcEndpoint.EnabledState
- Msvm_FcEndpoint.OtherEnabledState
- Msvm_FcEndpoint.RequestedState
- Msvm_FcEndpoint.EnabledDefault
- Msvm_FcEndpoint.TimeOfLastStateChange
- Msvm_FcEndpoint.AvailableRequestedStates
- Msvm_FcEndpoint.TransitioningToState
- Msvm_FcEndpoint.SystemCreationClassName
- Msvm_FcEndpoint.SystemName
- Msvm_FcEndpoint.CreationClassName
- Msvm_FcEndpoint.NameFormat
- Msvm_FcEndpoint.ProtocolType
- Msvm_FcEndpoint.ProtocolIFType
- Msvm_FcEndpoint.OtherTypeDescription
- Msvm_FcEndpoint.Connected
- Msvm_FcEndpoint.WWPN
- Msvm_FcEndpoint.WWNN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b28136cfc4f0afcf84b5f53ade4976760c997e36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542482"
---
# <a name="msvm_fcendpoint-class"></a><span data-ttu-id="1de97-103">\_Класс мсвм фцендпоинт</span><span class="sxs-lookup"><span data-stu-id="1de97-103">Msvm\_FcEndpoint class</span></span>

<span data-ttu-id="1de97-104">Представляет логическую точку соединения для порта Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="1de97-104">Represents the logical connection point for a Fibre Channel port.</span></span> <span data-ttu-id="1de97-105">Если конечная точка Fibre Channel подключена к порту коммутатора, то Fibre Channel подключение к порту Fibre Channel, подключенному к конечной точке Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="1de97-105">When the Fibre Channel endpoint is connected to a switch port, the Fibre Channel port connected to the Fibre Channel endpoint has Fibre Channel connectivity.</span></span>

<span data-ttu-id="1de97-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1de97-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de97-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1de97-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcEndpoint : CIM_ProtocolEndpoint
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  boolean  Connected;
  string   WWPN;
  string   WWNN;
};
```

## <a name="members"></a><span data-ttu-id="1de97-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1de97-108">Members</span></span>

<span data-ttu-id="1de97-109">Класс **мсвм \_ фцендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1de97-109">The **Msvm\_FcEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="1de97-110">Методы</span><span class="sxs-lookup"><span data-stu-id="1de97-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1de97-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1de97-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1de97-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1de97-112">Methods</span></span>

<span data-ttu-id="1de97-113">Класс **мсвм \_ фцендпоинт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1de97-113">The **Msvm\_FcEndpoint** class has these methods.</span></span>



| <span data-ttu-id="1de97-114">Метод</span><span class="sxs-lookup"><span data-stu-id="1de97-114">Method</span></span>                                                           | <span data-ttu-id="1de97-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1de97-115">Description</span></span>                         |
|:-----------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="1de97-116">**Равен**</span><span class="sxs-lookup"><span data-stu-id="1de97-116">**RequestStateChange**</span></span>](msvm-fcendpoint-requeststatechange.md) | <span data-ttu-id="1de97-117">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="1de97-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1de97-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="1de97-118">Properties</span></span>

<span data-ttu-id="1de97-119">Класс **мсвм \_ фцендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1de97-119">The **Msvm\_FcEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1de97-120">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="1de97-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-121">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1de97-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1de97-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-123">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="1de97-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="1de97-124">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1de97-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class.</span></span> <span data-ttu-id="1de97-125">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="1de97-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="1de97-126">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="1de97-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="1de97-127">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1de97-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1de97-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="1de97-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="1de97-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="1de97-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="1de97-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="1de97-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="1de97-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="1de97-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="1de97-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="1de97-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="1de97-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="1de97-138">)</span><span class="sxs-lookup"><span data-stu-id="1de97-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1de97-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1de97-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-142">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1de97-142">A short description of the object.</span></span> <span data-ttu-id="1de97-143">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-144">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="1de97-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-147">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="1de97-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1de97-148">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1de97-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1de97-149">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-150">**Подключен**</span><span class="sxs-lookup"><span data-stu-id="1de97-150">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-151">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1de97-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-153">Это свойство имеет значение **true** , если эта Fibre Channelная конечная точка активно подключена к другой конечной точке Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="1de97-153">This property is set to **True** if this Fibre Channel endpoint is actively connected to another Fibre Channel endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="1de97-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1de97-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1de97-157">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1de97-157">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1de97-158">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1de97-158">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1de97-159">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="1de97-159">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-160">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1de97-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-163">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1de97-163">A description of the object.</span></span> <span data-ttu-id="1de97-164">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-165">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1de97-165">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-168">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="1de97-168">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1de97-169">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1de97-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1de97-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1de97-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-174">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1de97-174">A display name for the object.</span></span> <span data-ttu-id="1de97-175">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-176">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="1de97-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-177">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-179">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="1de97-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="1de97-180">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1de97-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1de97-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="1de97-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="1de97-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="1de97-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1de97-184">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1de97-184">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-185">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-187">Указывает включенное состояние запланированной системы.</span><span class="sxs-lookup"><span data-stu-id="1de97-187">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="1de97-188">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1de97-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="1de97-189">Значение</span><span class="sxs-lookup"><span data-stu-id="1de97-189">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1de97-190">Значение</span><span class="sxs-lookup"><span data-stu-id="1de97-190">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1de97-191"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1de97-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="1de97-192">Система отключена.</span><span class="sxs-lookup"><span data-stu-id="1de97-192">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="1de97-193"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1de97-193"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="1de97-194">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="1de97-194">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="1de97-195"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1de97-195"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="1de97-196">Система включена, но в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="1de97-196">The system is enabled, but offline.</span></span> <span data-ttu-id="1de97-197">Все новые запросы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="1de97-197">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1de97-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1de97-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-199">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-201">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="1de97-201">The current health of the element.</span></span> <span data-ttu-id="1de97-202">Это свойство выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="1de97-202">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1de97-203">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="1de97-203">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1de97-204">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-205">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1de97-205">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-206">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1de97-206">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-208">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1de97-208">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1de97-209">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1de97-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1de97-213">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="1de97-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1de97-214">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="1de97-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1de97-215">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-216">**Name**</span><span class="sxs-lookup"><span data-stu-id="1de97-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-219">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="1de97-219">The label by which the object is known.</span></span> <span data-ttu-id="1de97-220">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-221">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="1de97-221">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1de97-224">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1de97-224">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1de97-225">Содержит эвристику именования, выбранную для обеспечения уникальности значения свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="1de97-225">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="1de97-226">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="1de97-226">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-227">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="1de97-227">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-228">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-230">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="1de97-230">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1de97-231">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1de97-231">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1de97-232">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-233">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1de97-233">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-234">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1de97-234">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1de97-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-236">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1de97-236">The current statuses of the object.</span></span> <span data-ttu-id="1de97-237">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-238">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="1de97-238">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-239">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-241">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="1de97-241">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="1de97-242">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="1de97-242">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1de97-243">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1de97-243">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1de97-244">**осертипедескриптион**</span><span class="sxs-lookup"><span data-stu-id="1de97-244">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1de97-247">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1de97-247">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1de97-248">Строка, описывающая тип конечной точки протокола, если свойство **протоколифтипе** этого класса (или любого из его подклассов) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="1de97-248">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="1de97-249">Это свойство должно иметь значение **null** , если свойство **протоколифтипе** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="1de97-249">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="1de97-250">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="1de97-250">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-251">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="1de97-251">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-252">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-254">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="1de97-254">Provides high level status information.</span></span> <span data-ttu-id="1de97-255">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="1de97-255">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="1de97-256">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1de97-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1de97-257">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-258">**протоколифтипе**</span><span class="sxs-lookup"><span data-stu-id="1de97-258">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-259">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-261">Свойство используется для категоризации и классификации экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="1de97-261">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="1de97-262">Если для **протоколифтипе** задано значение 1 (другое), то сведения о типе должны быть предоставлены в свойстве **осертипедескриптион** .</span><span class="sxs-lookup"><span data-stu-id="1de97-262">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="1de97-263">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="1de97-263">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="1de97-264">**Протоколифтипе** — это перечисление, которое синхронизируется с [IANA ифтипе MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="1de97-264">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="1de97-265">Также включаются дополнительные значения, определенные в DMTF.</span><span class="sxs-lookup"><span data-stu-id="1de97-265">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="1de97-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1de97-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1de97-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Регулярное 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="1de97-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**Хдх 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="1de97-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**ДДН X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="1de97-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="1de97-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet КСМа/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="1de97-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 КСМа/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="1de97-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Шина маркеров ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="1de97-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802,5 Token Ring** (9)</span><span class="sxs-lookup"><span data-stu-id="1de97-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**Человек ISO 802,6 Man** (10)</span><span class="sxs-lookup"><span data-stu-id="1de97-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**Старлан** (11)</span><span class="sxs-lookup"><span data-stu-id="1de97-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Протеон 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="1de97-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Протеон 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="1de97-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Канал** связи (14)</span><span class="sxs-lookup"><span data-stu-id="1de97-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-281"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="1de97-281"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-282"><span id="LAP-B"></span><span id="lap-b"></span>**Подлинный-B** (16)</span><span class="sxs-lookup"><span data-stu-id="1de97-282"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="1de97-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-284"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="1de97-284"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-285"><span id="E1"></span><span id="e1"></span>**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="1de97-285"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Базовый ISDN** (20)</span><span class="sxs-lookup"><span data-stu-id="1de97-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Основной ISDN** (21)</span><span class="sxs-lookup"><span data-stu-id="1de97-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Собственная последовательное подключение "точка — точка** " (22)</span><span class="sxs-lookup"><span data-stu-id="1de97-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="1de97-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Замыкание программного обеспечения** (24)</span><span class="sxs-lookup"><span data-stu-id="1de97-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-291"><span id="EON"></span><span id="eon"></span>**ЕОН** (25)</span><span class="sxs-lookup"><span data-stu-id="1de97-291"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span><span class="sxs-lookup"><span data-stu-id="1de97-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-293"><span id="NSIP"></span><span id="nsip"></span>**НСИП** (27)</span><span class="sxs-lookup"><span data-stu-id="1de97-293"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-294"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span><span class="sxs-lookup"><span data-stu-id="1de97-294"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="1de97-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="1de97-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="1de97-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span><span class="sxs-lookup"><span data-stu-id="1de97-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="1de97-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Параллельно** (34)</span><span class="sxs-lookup"><span data-stu-id="1de97-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**АркНет** (35)</span><span class="sxs-lookup"><span data-stu-id="1de97-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**АркНет Plus** (36)</span><span class="sxs-lookup"><span data-stu-id="1de97-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="1de97-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**МиО X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="1de97-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-305"><span id="SONET"></span><span id="sonet"></span>**Сонет** (39)</span><span class="sxs-lookup"><span data-stu-id="1de97-305"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 Борки** (40)</span><span class="sxs-lookup"><span data-stu-id="1de97-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41)</span><span class="sxs-lookup"><span data-stu-id="1de97-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="1de97-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**СМДС дкси** (43)</span><span class="sxs-lookup"><span data-stu-id="1de97-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Служба Frame Relay** (44)</span><span class="sxs-lookup"><span data-stu-id="1de97-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-311"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="1de97-311"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-312"><span id="HSSI"></span><span id="hssi"></span>**Хсси** (46)</span><span class="sxs-lookup"><span data-stu-id="1de97-312"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-313"><span id="HIPPI"></span><span id="hippi"></span>**Хиппи** (47)</span><span class="sxs-lookup"><span data-stu-id="1de97-313"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Модем** (48)</span><span class="sxs-lookup"><span data-stu-id="1de97-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="1de97-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Путь Сонет** (50)</span><span class="sxs-lookup"><span data-stu-id="1de97-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**Сонет VT** (51)</span><span class="sxs-lookup"><span data-stu-id="1de97-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**СМДС иЦип** (52)</span><span class="sxs-lookup"><span data-stu-id="1de97-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Собственная виртуальная/внутренняя** (53)</span><span class="sxs-lookup"><span data-stu-id="1de97-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Собственный мультиплексор** (54)</span><span class="sxs-lookup"><span data-stu-id="1de97-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="1de97-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="1de97-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Интерфейс хиппи** (57)</span><span class="sxs-lookup"><span data-stu-id="1de97-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Соединение Frame Relay** (58)</span><span class="sxs-lookup"><span data-stu-id="1de97-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM-Эмуляция LAN для 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="1de97-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM-Эмуляция LAN для 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="1de97-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM-Эмуляция** (61)</span><span class="sxs-lookup"><span data-stu-id="1de97-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BASE)** (62)</span><span class="sxs-lookup"><span data-stu-id="1de97-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span><span class="sxs-lookup"><span data-stu-id="1de97-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-330"><span id="V.11"></span><span id="v.11"></span>**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="1de97-330"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-331"><span id="V.36"></span><span id="v.36"></span>**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="1de97-331"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 в 64 КБ** (66)</span><span class="sxs-lookup"><span data-stu-id="1de97-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 в 2 МБ** (67)</span><span class="sxs-lookup"><span data-stu-id="1de97-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-334"><span id="QLLC"></span><span id="qllc"></span>**Кллк** (68)</span><span class="sxs-lookup"><span data-stu-id="1de97-334"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="1de97-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Канал** (70)</span><span class="sxs-lookup"><span data-stu-id="1de97-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="1de97-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Канал IBM 260/370 оеми** (72)</span><span class="sxs-lookup"><span data-stu-id="1de97-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-339"><span id="ESCON"></span><span id="escon"></span>**Ескон** (73)</span><span class="sxs-lookup"><span data-stu-id="1de97-339"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Переключение каналов передачи данных** (74)</span><span class="sxs-lookup"><span data-stu-id="1de97-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Интерфейс ISDN S/T** (75)</span><span class="sxs-lookup"><span data-stu-id="1de97-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Интерфейс ISDN U** (76)</span><span class="sxs-lookup"><span data-stu-id="1de97-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-343"><span id="LAP-D"></span><span id="lap-d"></span>**Длинный** (77)</span><span class="sxs-lookup"><span data-stu-id="1de97-343"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP-параметр** (78)</span><span class="sxs-lookup"><span data-stu-id="1de97-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Мост удаленных маршрутов удаленного источника** (79)</span><span class="sxs-lookup"><span data-stu-id="1de97-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**Логический ATM** (80)</span><span class="sxs-lookup"><span data-stu-id="1de97-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="1de97-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Пакет DS0** (82)</span><span class="sxs-lookup"><span data-stu-id="1de97-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-349"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="1de97-349"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="1de97-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Борьбы с сетевым радио** (85)</span><span class="sxs-lookup"><span data-stu-id="1de97-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5 r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="1de97-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Система отчетов ext POS Loc** (87)</span><span class="sxs-lookup"><span data-stu-id="1de97-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Протокол удаленного доступа AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="1de97-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Собственная без подключения** (89)</span><span class="sxs-lookup"><span data-stu-id="1de97-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Хост-приложение ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="1de97-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**Клавиатура терминала ITU X. 3** (91)</span><span class="sxs-lookup"><span data-stu-id="1de97-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI Frame Relay** (92)</span><span class="sxs-lookup"><span data-stu-id="1de97-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="1de97-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="1de97-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-361"><span id="RADSL"></span><span id="radsl"></span>**Радсл** (95)</span><span class="sxs-lookup"><span data-stu-id="1de97-361"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-362"><span id="SDSL"></span><span id="sdsl"></span>**Сдсл** (96)</span><span class="sxs-lookup"><span data-stu-id="1de97-362"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-363"><span id="VDSL"></span><span id="vdsl"></span>**Вдсл** (97)</span><span class="sxs-lookup"><span data-stu-id="1de97-363"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 крфп** (98)</span><span class="sxs-lookup"><span data-stu-id="1de97-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Миринет** (99)</span><span class="sxs-lookup"><span data-stu-id="1de97-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Получение и передача голоса** (100)</span><span class="sxs-lookup"><span data-stu-id="1de97-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Голосовое внешнее приложение Exchange** (101)</span><span class="sxs-lookup"><span data-stu-id="1de97-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Служба Voice иностранных валют** (102)</span><span class="sxs-lookup"><span data-stu-id="1de97-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Инкапсуляция голоса** (103)</span><span class="sxs-lookup"><span data-stu-id="1de97-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>Передача **голоса по IP** (104)</span><span class="sxs-lookup"><span data-stu-id="1de97-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM дкси** (105)</span><span class="sxs-lookup"><span data-stu-id="1de97-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM Фуни** (106)</span><span class="sxs-lookup"><span data-stu-id="1de97-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM Има** (107)</span><span class="sxs-lookup"><span data-stu-id="1de97-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Многоканальный пакет PPP** (108)</span><span class="sxs-lookup"><span data-stu-id="1de97-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP через кдлк** (109)</span><span class="sxs-lookup"><span data-stu-id="1de97-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP через клав** (110)</span><span class="sxs-lookup"><span data-stu-id="1de97-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Стек в стек** (111)</span><span class="sxs-lookup"><span data-stu-id="1de97-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Виртуальный IP-адрес** (112)</span><span class="sxs-lookup"><span data-stu-id="1de97-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="1de97-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP через ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="1de97-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5 j Fibre Token Ring** (115)</span><span class="sxs-lookup"><span data-stu-id="1de97-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-382"><span id="TDLC"></span><span id="tdlc"></span>**Тдлк** (116)</span><span class="sxs-lookup"><span data-stu-id="1de97-382"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Гигабитный Ethernet** (117)</span><span class="sxs-lookup"><span data-stu-id="1de97-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-384"><span id="HDLC"></span><span id="hdlc"></span>**Хдлк** (118)</span><span class="sxs-lookup"><span data-stu-id="1de97-384"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-385"><span id="LAP-F"></span><span id="lap-f"></span>**Подлинный-F** (119)</span><span class="sxs-lookup"><span data-stu-id="1de97-385"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-386"><span id="V.37"></span><span id="v.37"></span>**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="1de97-386"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X. 25 MLP** (121)</span><span class="sxs-lookup"><span data-stu-id="1de97-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**Группа слежения X. 25** (122)</span><span class="sxs-lookup"><span data-stu-id="1de97-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Трансп хдлк** (123)</span><span class="sxs-lookup"><span data-stu-id="1de97-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Канал чередования** (124)</span><span class="sxs-lookup"><span data-stu-id="1de97-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**Быстрый канал** (125)</span><span class="sxs-lookup"><span data-stu-id="1de97-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP-адрес (для АППН ХПР в IP-сетях)** (126)</span><span class="sxs-lookup"><span data-stu-id="1de97-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**КАТВ Mac Layer** (127)</span><span class="sxs-lookup"><span data-stu-id="1de97-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**Нисходящий КАТВ** (128)</span><span class="sxs-lookup"><span data-stu-id="1de97-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**Вышестоящий КАТВ** (129)</span><span class="sxs-lookup"><span data-stu-id="1de97-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Параметр Avalon 12MPP** (130)</span><span class="sxs-lookup"><span data-stu-id="1de97-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Туннель** (131)</span><span class="sxs-lookup"><span data-stu-id="1de97-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Кофе** (132)</span><span class="sxs-lookup"><span data-stu-id="1de97-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Служба эмуляции канала** (133)</span><span class="sxs-lookup"><span data-stu-id="1de97-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**Подинтерфейс ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="1de97-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Виртуальная ЛС уровня 2 с помощью 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="1de97-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Виртуальная ЛС уровня 3 с использованием IP-адреса** (136)</span><span class="sxs-lookup"><span data-stu-id="1de97-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Виртуальная ЛС уровня 3 с использованием IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="1de97-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Цифровая линия электропитания** (138)</span><span class="sxs-lookup"><span data-stu-id="1de97-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Мультимедийная почта через IP-адрес** (139)</span><span class="sxs-lookup"><span data-stu-id="1de97-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="1de97-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-407"><span id="DCN"></span><span id="dcn"></span>**ДКН** (141)</span><span class="sxs-lookup"><span data-stu-id="1de97-407"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP-пересылка** (142)</span><span class="sxs-lookup"><span data-stu-id="1de97-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-409"><span id="MSDSL"></span><span id="msdsl"></span>**MsDS** (143)</span><span class="sxs-lookup"><span data-stu-id="1de97-409"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="1de97-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-ГСН/хиппи-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="1de97-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Уровень DVB-RCC Mac** (146)</span><span class="sxs-lookup"><span data-stu-id="1de97-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**Подчиненный DVB-RCC** (147)</span><span class="sxs-lookup"><span data-stu-id="1de97-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**Вышестоящее телевидение DVB-RCC** (148)</span><span class="sxs-lookup"><span data-stu-id="1de97-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**Виртуальная Банкомат** (149)</span><span class="sxs-lookup"><span data-stu-id="1de97-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Туннель MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="1de97-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="1de97-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>Передача **голоса по сети ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="1de97-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>Передача **голоса через Frame Relay** (153)</span><span class="sxs-lookup"><span data-stu-id="1de97-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-420"><span id="ISDL"></span><span id="isdl"></span>**Исдл** (154)</span><span class="sxs-lookup"><span data-stu-id="1de97-420"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Составная ссылка** (155)</span><span class="sxs-lookup"><span data-stu-id="1de97-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Канал сигнализации SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="1de97-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Частная сеть P2P** (157)</span><span class="sxs-lookup"><span data-stu-id="1de97-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Кадр вперед** (158)</span><span class="sxs-lookup"><span data-stu-id="1de97-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 по протоколу ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="1de97-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-426"><span id="USB"></span><span id="usb"></span>**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="1de97-426"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Агрегирование ссылок AD IEEE 802.3** (161)</span><span class="sxs-lookup"><span data-stu-id="1de97-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Учет политики BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="1de97-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**ФРФ .16 многоканальная связь fr** (163)</span><span class="sxs-lookup"><span data-stu-id="1de97-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**Привратник H. 323** (164)</span><span class="sxs-lookup"><span data-stu-id="1de97-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H. 323-прокси** (165)</span><span class="sxs-lookup"><span data-stu-id="1de97-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="1de97-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Многочастотная ссылка на сигнал** (167)</span><span class="sxs-lookup"><span data-stu-id="1de97-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**Хдсл-2** (168)</span><span class="sxs-lookup"><span data-stu-id="1de97-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-хдсл** (169)</span><span class="sxs-lookup"><span data-stu-id="1de97-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Ссылка на данные DS1-устройства** (170)</span><span class="sxs-lookup"><span data-stu-id="1de97-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Пакет через Сонет/СДХ** (171)</span><span class="sxs-lookup"><span data-stu-id="1de97-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Вход DVB-АСИ** (172)</span><span class="sxs-lookup"><span data-stu-id="1de97-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Выходные данные DVB-АСИ** (173)</span><span class="sxs-lookup"><span data-stu-id="1de97-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Линия электропитания** (174)</span><span class="sxs-lookup"><span data-stu-id="1de97-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Связанные сигналы без устройства** (175)</span><span class="sxs-lookup"><span data-stu-id="1de97-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="1de97-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 РДТ** (177)</span><span class="sxs-lookup"><span data-stu-id="1de97-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="1de97-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-445"><span id="ISUP"></span><span id="isup"></span>**ИСУП** (179)</span><span class="sxs-lookup"><span data-stu-id="1de97-445"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Частный уровень беспроводной сети Mac** (180)</span><span class="sxs-lookup"><span data-stu-id="1de97-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Собственная беспроводная сеть** (181)</span><span class="sxs-lookup"><span data-stu-id="1de97-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Частные Беспроводные потоки** (182)</span><span class="sxs-lookup"><span data-stu-id="1de97-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**Тип хиперлан 2** (183)</span><span class="sxs-lookup"><span data-stu-id="1de97-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Собственная широкополосная беспроводная точка доступа к MultiPoint** (184)</span><span class="sxs-lookup"><span data-stu-id="1de97-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Канал накладных расходов Сонет** (185)</span><span class="sxs-lookup"><span data-stu-id="1de97-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Канал накладных расходов цифровых оболочек** (186)</span><span class="sxs-lookup"><span data-stu-id="1de97-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Уровень адаптации ATM 2** (187)</span><span class="sxs-lookup"><span data-stu-id="1de97-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Радио Mac** (188)</span><span class="sxs-lookup"><span data-stu-id="1de97-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM-радио** (189)</span><span class="sxs-lookup"><span data-stu-id="1de97-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Межмашинная магистраль между компьютерами** (190)</span><span class="sxs-lookup"><span data-stu-id="1de97-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**МВЛ DSL** (191)</span><span class="sxs-lookup"><span data-stu-id="1de97-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Общедоступный для чтения DSL** (192)</span><span class="sxs-lookup"><span data-stu-id="1de97-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Конечная точка DLCI Frame Relay** (193)</span><span class="sxs-lookup"><span data-stu-id="1de97-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Конечная точка ATM VCI** (194)</span><span class="sxs-lookup"><span data-stu-id="1de97-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Оптический канал** (195)</span><span class="sxs-lookup"><span data-stu-id="1de97-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Оптический транспорт** (196)</span><span class="sxs-lookup"><span data-stu-id="1de97-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Собственная ATM** (197)</span><span class="sxs-lookup"><span data-stu-id="1de97-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Речь по кабелю** (198)</span><span class="sxs-lookup"><span data-stu-id="1de97-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="1de97-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Ссылка TE** (200)</span><span class="sxs-lookup"><span data-stu-id="1de97-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-467"><span id="Q.2931"></span><span id="q.2931"></span>**Q. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="1de97-467"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Виртуальная магистральная группа** (202)</span><span class="sxs-lookup"><span data-stu-id="1de97-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Магистральная группа SIP** (203)</span><span class="sxs-lookup"><span data-stu-id="1de97-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Сигнал SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="1de97-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Вышестоящий канал КАТВ** (205)</span><span class="sxs-lookup"><span data-stu-id="1de97-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Еконет** (206)</span><span class="sxs-lookup"><span data-stu-id="1de97-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**ФСАН 155MB Пон** (207)</span><span class="sxs-lookup"><span data-stu-id="1de97-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**ФСАН 622MB Пон** (208)</span><span class="sxs-lookup"><span data-stu-id="1de97-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Прозрачный мост** (209)</span><span class="sxs-lookup"><span data-stu-id="1de97-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Группа линий** (210)</span><span class="sxs-lookup"><span data-stu-id="1de97-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Группа функций Voice &** (211)</span><span class="sxs-lookup"><span data-stu-id="1de97-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice ФГД еана** (212)</span><span class="sxs-lookup"><span data-stu-id="1de97-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice** (213)</span><span class="sxs-lookup"><span data-stu-id="1de97-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Транспорт MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="1de97-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="1de97-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-482"><span id="GTP"></span><span id="gtp"></span>**Гтп** (216)</span><span class="sxs-lookup"><span data-stu-id="1de97-482"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Парадине есерлуп 1** (217)</span><span class="sxs-lookup"><span data-stu-id="1de97-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Парадине есерлуп 2** (218)</span><span class="sxs-lookup"><span data-stu-id="1de97-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Группа оптических каналов** (219)</span><span class="sxs-lookup"><span data-stu-id="1de97-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**Хомепна** (220)</span><span class="sxs-lookup"><span data-stu-id="1de97-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-487"><span id="GFP"></span><span id="gfp"></span>**ГФП** (221)</span><span class="sxs-lookup"><span data-stu-id="1de97-487"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**Цискоислвлан** (222)</span><span class="sxs-lookup"><span data-stu-id="1de97-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**актелисметалуп** (223)</span><span class="sxs-lookup"><span data-stu-id="1de97-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**ФЦип** (224)</span><span class="sxs-lookup"><span data-stu-id="1de97-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**Зарезервирован IANA** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="1de97-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="1de97-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="1de97-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="1de97-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="1de97-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>Протокол **DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="1de97-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="1de97-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-498"><span id="CONP"></span><span id="conp"></span>**КОНП** (4102)</span><span class="sxs-lookup"><span data-stu-id="1de97-498"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-499"><span id="CLNP"></span><span id="clnp"></span>**Клнп** (4103)</span><span class="sxs-lookup"><span data-stu-id="1de97-499"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-500"><span id="VINES"></span><span id="vines"></span>**Vines** (4104)</span><span class="sxs-lookup"><span data-stu-id="1de97-500"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-501"><span id="XNS"></span><span id="xns"></span>**КСНС** (4105)</span><span class="sxs-lookup"><span data-stu-id="1de97-501"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Конечная точка канала ISDN B** (4106)</span><span class="sxs-lookup"><span data-stu-id="1de97-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Конечная точка D канала ISDN** (4107)</span><span class="sxs-lookup"><span data-stu-id="1de97-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="1de97-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="1de97-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="1de97-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="1de97-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="1de97-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="1de97-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="1de97-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="1de97-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="1de97-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="1de97-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-514"><span id="DAFS"></span><span id="dafs"></span>**ДАФС** (4202)</span><span class="sxs-lookup"><span data-stu-id="1de97-514"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>Протокол **WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="1de97-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-516"><span id="HTTP"></span><span id="http"></span>**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="1de97-516"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="1de97-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-518"><span id="NDMP"></span><span id="ndmp"></span>**Ндмп** (4300)</span><span class="sxs-lookup"><span data-stu-id="1de97-518"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="1de97-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="1de97-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span><span class="sxs-lookup"><span data-stu-id="1de97-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="1de97-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="1de97-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="1de97-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-525"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span><span class="sxs-lookup"><span data-stu-id="1de97-525"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1de97-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1de97-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (32768..</span><span class="sxs-lookup"><span data-stu-id="1de97-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="1de97-528">)</span><span class="sxs-lookup"><span data-stu-id="1de97-528">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1de97-529">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="1de97-529">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-530">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-531">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-532">Это свойство не рекомендуется использовать вместо свойства **протоколифтипе** .</span><span class="sxs-lookup"><span data-stu-id="1de97-532">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="1de97-533">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="1de97-533">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-534">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1de97-534">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-535">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-535">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-536">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-537">Последнее запрошенное или требуемое состояние для службы управления.</span><span class="sxs-lookup"><span data-stu-id="1de97-537">The last requested or desired state for the management service.</span></span> <span data-ttu-id="1de97-538">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1de97-538">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="1de97-539">Значение</span><span class="sxs-lookup"><span data-stu-id="1de97-539">Value</span></span>                                                                         | <span data-ttu-id="1de97-540">Значение</span><span class="sxs-lookup"><span data-stu-id="1de97-540">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="1de97-541"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1de97-541"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1de97-542">Не применяется</span><span class="sxs-lookup"><span data-stu-id="1de97-542">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1de97-543">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1de97-543">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-544">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-545">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-545">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-546">Описывает состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="1de97-546">Describes the status of the element.</span></span> <span data-ttu-id="1de97-547">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-547">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="1de97-548">'</span><span class="sxs-lookup"><span data-stu-id="1de97-548">"OK"</span></span>

<span data-ttu-id="1de97-549">План</span><span class="sxs-lookup"><span data-stu-id="1de97-549">"Error"</span></span>

<span data-ttu-id="1de97-550">Пониженной функциональности</span><span class="sxs-lookup"><span data-stu-id="1de97-550">"Degraded"</span></span>

<span data-ttu-id="1de97-551">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="1de97-551">"Unknown"</span></span>

<span data-ttu-id="1de97-552">"Пред Fail"</span><span class="sxs-lookup"><span data-stu-id="1de97-552">"Pred Fail"</span></span>

<span data-ttu-id="1de97-553">Start</span><span class="sxs-lookup"><span data-stu-id="1de97-553">"Starting"</span></span>

<span data-ttu-id="1de97-554">Идет</span><span class="sxs-lookup"><span data-stu-id="1de97-554">"Stopping"</span></span>

<span data-ttu-id="1de97-555">Служеб</span><span class="sxs-lookup"><span data-stu-id="1de97-555">"Service"</span></span>

<span data-ttu-id="1de97-556">Груз</span><span class="sxs-lookup"><span data-stu-id="1de97-556">"Stressed"</span></span>

<span data-ttu-id="1de97-557">"Recover"</span><span class="sxs-lookup"><span data-stu-id="1de97-557">"NonRecover"</span></span>

<span data-ttu-id="1de97-558">"Нет контакта"</span><span class="sxs-lookup"><span data-stu-id="1de97-558">"No Contact"</span></span>

<span data-ttu-id="1de97-559">"Потеря связи"</span><span class="sxs-lookup"><span data-stu-id="1de97-559">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="1de97-560">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="1de97-560">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-561">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1de97-561">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1de97-562">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-562">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-563">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="1de97-563">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1de97-564">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1de97-564">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-565">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1de97-565">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-566">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-567">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-568">Имя класса создания системы размещения.</span><span class="sxs-lookup"><span data-stu-id="1de97-568">The hosting system's creation class name.</span></span> <span data-ttu-id="1de97-569">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="1de97-569">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-570">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1de97-570">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-571">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-572">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1de97-573">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1de97-573">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1de97-574">Имя системы размещения.</span><span class="sxs-lookup"><span data-stu-id="1de97-574">The name of the hosting system.</span></span> <span data-ttu-id="1de97-575">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="1de97-575">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="1de97-576">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="1de97-576">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-577">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1de97-577">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-578">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-578">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-579">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="1de97-579">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1de97-580">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1de97-580">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1de97-581">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="1de97-581">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-582">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1de97-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-583">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-583">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-584">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1de97-584">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1de97-585">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="1de97-585">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1de97-586">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="1de97-586">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-587">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-588">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-588">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-589">WWN-имя узла Fibre Channel порта, к которому подключена эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="1de97-589">The world wide node name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="1de97-590">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="1de97-590">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1de97-591">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1de97-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1de97-592">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de97-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1de97-593">WWN-имя порта Fibre Channel порта, к которому подключена эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="1de97-593">The world wide port name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1de97-594">Требования</span><span class="sxs-lookup"><span data-stu-id="1de97-594">Requirements</span></span>



| <span data-ttu-id="1de97-595">Требование</span><span class="sxs-lookup"><span data-stu-id="1de97-595">Requirement</span></span> | <span data-ttu-id="1de97-596">Значение</span><span class="sxs-lookup"><span data-stu-id="1de97-596">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de97-597">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1de97-597">Minimum supported client</span></span><br/> | <span data-ttu-id="1de97-598">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1de97-598">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1de97-599">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1de97-599">Minimum supported server</span></span><br/> | <span data-ttu-id="1de97-600">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1de97-600">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1de97-601">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1de97-601">Namespace</span></span><br/>                | <span data-ttu-id="1de97-602">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1de97-602">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1de97-603">MOF</span><span class="sxs-lookup"><span data-stu-id="1de97-603">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1de97-604"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1de97-604"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1de97-605">DLL</span><span class="sxs-lookup"><span data-stu-id="1de97-605">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1de97-606"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1de97-606"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

