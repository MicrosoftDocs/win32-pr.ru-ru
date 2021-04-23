---
description: Представляет конечную точку VLAN порта коммутатора.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Класс Msvm_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662221"
---
# <a name="msvm_vlanendpoint-class"></a><span data-ttu-id="8eff8-103">\_Класс мсвм вланендпоинт</span><span class="sxs-lookup"><span data-stu-id="8eff8-103">Msvm\_VLANEndpoint class</span></span>

<span data-ttu-id="8eff8-104">Представляет конечную точку VLAN порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="8eff8-104">Represents the VLAN endpoint of a switch port.</span></span> <span data-ttu-id="8eff8-105">Настройка этой конечной точки приведет к изменению способа, которым порт коммутатора отправляет пакеты виртуальной ЛС через коммутатор.</span><span class="sxs-lookup"><span data-stu-id="8eff8-105">The configuration of this endpoint will change the way the switch port sends VLAN packets through the switch.</span></span>

<span data-ttu-id="8eff8-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8eff8-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eff8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8eff8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a><span data-ttu-id="8eff8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8eff8-108">Members</span></span>

<span data-ttu-id="8eff8-109">Класс **мсвм \_ вланендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8eff8-109">The **Msvm\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="8eff8-110">Методы</span><span class="sxs-lookup"><span data-stu-id="8eff8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8eff8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8eff8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8eff8-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8eff8-112">Methods</span></span>

<span data-ttu-id="8eff8-113">Класс **мсвм \_ вланендпоинт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8eff8-113">The **Msvm\_VLANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="8eff8-114">Метод</span><span class="sxs-lookup"><span data-stu-id="8eff8-114">Method</span></span>                                                             | <span data-ttu-id="8eff8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="8eff8-115">Description</span></span>                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="8eff8-116">**Равен**</span><span class="sxs-lookup"><span data-stu-id="8eff8-116">**RequestStateChange**</span></span>](msvm-vlanendpoint-requeststatechange.md) | <span data-ttu-id="8eff8-117">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="8eff8-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8eff8-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="8eff8-118">Properties</span></span>

<span data-ttu-id="8eff8-119">Класс **мсвм \_ вланендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8eff8-119">The **Msvm\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8eff8-120">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="8eff8-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-121">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8eff8-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-123">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="8eff8-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="8eff8-124">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8eff8-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="8eff8-125">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8eff8-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="8eff8-126">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8eff8-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="8eff8-127">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8eff8-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8eff8-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff8-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff8-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff8-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="8eff8-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="8eff8-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="8eff8-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="8eff8-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="8eff8-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="8eff8-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="8eff8-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="8eff8-138">)</span><span class="sxs-lookup"><span data-stu-id="8eff8-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8eff8-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8eff8-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-140">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-142">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8eff8-142">A short description of the object.</span></span> <span data-ttu-id="8eff8-143">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "конечная точка VLAN".</span><span class="sxs-lookup"><span data-stu-id="8eff8-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-144">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="8eff8-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-147">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="8eff8-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8eff8-148">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8eff8-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8eff8-149">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-150">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8eff8-150">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-151">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-153">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8eff8-153">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="8eff8-154">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)и всегда имеет значение "мсвм \_ вланендпоинт".</span><span class="sxs-lookup"><span data-stu-id="8eff8-154">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VLANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-155">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8eff8-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-158">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8eff8-158">A description of the object.</span></span> <span data-ttu-id="8eff8-159">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "КОНЕЧНАЯ точка виртуальной ЛС (Майкрософт)".</span><span class="sxs-lookup"><span data-stu-id="8eff8-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-160">**десиредендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="8eff8-160">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-162">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="8eff8-162">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-163">Требуемый режим VLAN, запрашиваемый для использования.</span><span class="sxs-lookup"><span data-stu-id="8eff8-163">The desired VLAN mode that is requested for use.</span></span> <span data-ttu-id="8eff8-164">Текущий режим задается свойством **оператионалендпоинтмоде** .</span><span class="sxs-lookup"><span data-stu-id="8eff8-164">The current mode is given by the **OperationalEndpointMode** property.</span></span> <span data-ttu-id="8eff8-165">Это свойство наследуется от [**CIM \_ вланендпоинт**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-165">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="8eff8-166">Значение</span><span class="sxs-lookup"><span data-stu-id="8eff8-166">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="8eff8-167">Значение</span><span class="sxs-lookup"><span data-stu-id="8eff8-167">Meaning</span></span>                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8eff8-168"><dt>**Зарезервировано**</dt> <dt>0</dt> DMTF</span><span class="sxs-lookup"><span data-stu-id="8eff8-168"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="8eff8-169"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-169"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="8eff8-170"><dt>**Доступ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-170"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="8eff8-171">Помещает Порт конечной точки или коммутатора в постоянный режим без магистрали и согласовывает преобразование ссылки в немагистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-171">Puts the endpoint/switch port into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="8eff8-172">Конечная точка станет немагистральным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="8eff8-172">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="8eff8-173"><dt>**Динамическое автоматическое**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="8eff8-174">Делает конечную точку недоступной для преобразования ссылки на магистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-174">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="8eff8-175">Конечная точка становится магистральным интерфейсом, если для соседнего интерфейса задана магистральная или предпочтительный режим.</span><span class="sxs-lookup"><span data-stu-id="8eff8-175">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="8eff8-176"><dt>**Желательно динамическое**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-176"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="8eff8-177">Делает конечную точку активной попыткой преобразовать ссылку на магистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-177">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="8eff8-178">Конечная точка становится магистральным интерфейсом, если для соседнего интерфейса установлено значение магистрального, желательного или автоматического режима.</span><span class="sxs-lookup"><span data-stu-id="8eff8-178">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="8eff8-179">По умолчанию режим порта коммутатора для всех интерфейсов Ethernet является динамически желательным.</span><span class="sxs-lookup"><span data-stu-id="8eff8-179">The default switch-port mode for all Ethernet interfaces is dynamic desirable.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="8eff8-180"><dt>**Магистраль**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-180"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="8eff8-181">Переводит конечную точку в режим постоянной магистрали и согласовывает, чтобы преобразовать ссылку в магистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-181">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="8eff8-182">Конечная точка становится магистральным интерфейсом, даже если соседний интерфейс не является магистральным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="8eff8-182">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="8eff8-183"><dt>**Туннель Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="8eff8-184">Настраивает интерфейс как туннельную (немагистральную) конечную точку или порт для подключения в асимметричном канале с магистральным портом 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="8eff8-184">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="8eff8-185">туннелирование 802.1 q используется для поддержания целостности VLAN клиента в сети поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8eff8-185">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8eff8-186"><dt>**Зарезервировано**</dt> <dt>7 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="8eff8-186"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="8eff8-187"><dt> **Поставщик зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-187"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="8eff8-188">**десиредвлантрункенкапсулатион**</span><span class="sxs-lookup"><span data-stu-id="8eff8-188">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-189">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-191">Тип инкапсуляции VLAN, запрашиваемый для использования.</span><span class="sxs-lookup"><span data-stu-id="8eff8-191">The type of VLAN encapsulation that is requested for use.</span></span> <span data-ttu-id="8eff8-192">Инкапсуляция, используемая в данный момент, предоставляется свойством **оператионалвлантрункенкапсулатион** .</span><span class="sxs-lookup"><span data-stu-id="8eff8-192">The encapsulation currently in use is given by the **OperationalVLANTrunkEncapsulation** property.</span></span> <span data-ttu-id="8eff8-193">Это свойство применимо только в том случае, если конечная точка работает в режиме магистрали (Дополнительные сведения см. в свойстве **оператионалендпоинтмоде** ).</span><span class="sxs-lookup"><span data-stu-id="8eff8-193">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="8eff8-194">Это свойство имеет значение 2 (неприменимо) (то есть конечная точка никогда не будет помещаться в режим магистрали), определенный тип (802.1 Q или Cisco острова) или 5 (Negotiate) (то есть результат согласования между этим интерфейсом и его соседом).</span><span class="sxs-lookup"><span data-stu-id="8eff8-194">This property is either 2 (Not Applicable) (that is, the endpoint will never be placed in a trunking mode), a particular type (802.1Q or Cisco ISL), or 5 (Negotiate) (that is, the result of the negotiation between this interface and its neighbor).</span></span> <span data-ttu-id="8eff8-195">Значение 5 (Negotiate) не допускается, если конечная точка не поддерживает согласование.</span><span class="sxs-lookup"><span data-stu-id="8eff8-195">The value, 5 (Negotiate) is not allowed if the endpoint does not support negotiation.</span></span> <span data-ttu-id="8eff8-196">Эта возможность зависит от оборудования и поставщика.</span><span class="sxs-lookup"><span data-stu-id="8eff8-196">This capability is hardware and vendor dependent.</span></span> <span data-ttu-id="8eff8-197">Это свойство наследуется от [**CIM \_ вланендпоинт**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-197">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="8eff8-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (0)</span><span class="sxs-lookup"><span data-stu-id="8eff8-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8eff8-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff8-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff8-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco острова** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff8-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Согласование** (5)</span><span class="sxs-lookup"><span data-stu-id="8eff8-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="8eff8-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="8eff8-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8eff8-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8eff8-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-207">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-209">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8eff8-209">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8eff8-210">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8eff8-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8eff8-211">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-212">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8eff8-212">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-213">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-215">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8eff8-215">A display name for the object.</span></span> <span data-ttu-id="8eff8-216">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-216">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-217">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="8eff8-217">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-218">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-220">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8eff8-220">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8eff8-221">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="8eff8-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8eff8-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-223">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-225">Включенные и отключенные состояния этого элемента.</span><span class="sxs-lookup"><span data-stu-id="8eff8-225">The enabled and disabled states of this element.</span></span> <span data-ttu-id="8eff8-226">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="8eff8-226">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-227">**гврпстатус**</span><span class="sxs-lookup"><span data-stu-id="8eff8-227">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-228">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-230">Указывает, включен ли протокол регистрации VLAN Гарп (ГВРП) в конечной точке или порте магистрали.</span><span class="sxs-lookup"><span data-stu-id="8eff8-230">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint/port.</span></span> <span data-ttu-id="8eff8-231">Это свойство имеет значение 2 (неприменимо), если конечная точка не поддерживает ГВРП.</span><span class="sxs-lookup"><span data-stu-id="8eff8-231">This property is 2 (Not Applicable) unless GVRP is supported by the endpoint.</span></span> <span data-ttu-id="8eff8-232">Это свойство применимо только в том случае, если конечная точка работает в режиме магистрали (Дополнительные сведения см. в свойстве **оператионалендпоинтмоде** ).</span><span class="sxs-lookup"><span data-stu-id="8eff8-232">This property is applicable only when the endpoint is operating in trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="8eff8-233">Это свойство наследуется от [**CIM \_ вланендпоинт**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-233">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="8eff8-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8eff8-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff8-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff8-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff8-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabled** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8eff8-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8eff8-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-239">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-241">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="8eff8-241">The current health of the element.</span></span> <span data-ttu-id="8eff8-242">Это свойство выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8eff8-242">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8eff8-243">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="8eff8-243">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8eff8-244">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="8eff8-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-245">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8eff8-245">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-246">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8eff8-246">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-248">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="8eff8-248">The date and time when the object was installed.</span></span> <span data-ttu-id="8eff8-249">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и не используется.</span><span class="sxs-lookup"><span data-stu-id="8eff8-249">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-250">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8eff8-250">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-253">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8eff8-253">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-254">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="8eff8-254">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8eff8-255">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-256">**Name**</span><span class="sxs-lookup"><span data-stu-id="8eff8-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-259">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8eff8-259">The label by which the object is known.</span></span> <span data-ttu-id="8eff8-260">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-261">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="8eff8-261">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-262">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-262">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-264">Эвристический подход именования, который выбран для обеспечения уникальности значения свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="8eff8-264">The naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="8eff8-265">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) и не используется.</span><span class="sxs-lookup"><span data-stu-id="8eff8-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-266">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="8eff8-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-269">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8eff8-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8eff8-270">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8eff8-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8eff8-271">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-272">**оператионалендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="8eff8-272">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-273">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-275">Режим конфигурации для конечной точки VLAN.</span><span class="sxs-lookup"><span data-stu-id="8eff8-275">The configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="8eff8-276">Это свойство наследуется от [**CIM \_ вланендпоинт**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-276">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="8eff8-277">Значение</span><span class="sxs-lookup"><span data-stu-id="8eff8-277">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="8eff8-278">Значение</span><span class="sxs-lookup"><span data-stu-id="8eff8-278">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8eff8-279"><dt>**Зарезервировано**</dt> <dt>0</dt> DMTF</span><span class="sxs-lookup"><span data-stu-id="8eff8-279"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="8eff8-280"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-280"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       | <span data-ttu-id="8eff8-281">Конечная точка не поддерживает виртуальную ЛС.</span><span class="sxs-lookup"><span data-stu-id="8eff8-281">The endpoint is not VLAN aware.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="8eff8-282"><dt>**Доступ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-282"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="8eff8-283">Переводит конечную точку в постоянный немагистральный режим и согласовывает, чтобы преобразовать ссылку в немагистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-283">Puts the endpoint into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="8eff8-284">Конечная точка станет немагистральным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="8eff8-284">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="8eff8-285"><dt>**Динамическое автоматическое**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="8eff8-286">Делает конечную точку недоступной для преобразования ссылки на магистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-286">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="8eff8-287">Конечная точка становится магистральным интерфейсом, если для соседнего интерфейса задана магистральная или предпочтительный режим.</span><span class="sxs-lookup"><span data-stu-id="8eff8-287">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="8eff8-288"><dt>**Желательно динамическое**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-288"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="8eff8-289">Делает конечную точку активной попыткой преобразовать ссылку на магистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-289">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="8eff8-290">Конечная точка становится магистральным интерфейсом, если для соседнего интерфейса установлено значение магистрального, желательного или автоматического режима.</span><span class="sxs-lookup"><span data-stu-id="8eff8-290">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="8eff8-291">Это режим порта коммутатора по умолчанию для всех интерфейсов Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8eff8-291">This is the default switch-port mode for all Ethernet interfaces.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="8eff8-292"><dt>**Магистраль**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-292"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="8eff8-293">Переводит конечную точку в режим постоянной магистрали и согласовывает, чтобы преобразовать ссылку в магистральную ссылку.</span><span class="sxs-lookup"><span data-stu-id="8eff8-293">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="8eff8-294">Конечная точка становится магистральным интерфейсом, даже если соседний интерфейс не является магистральным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="8eff8-294">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="8eff8-295"><dt>**Туннель Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="8eff8-296">Настраивает интерфейс как туннельную (немагистральную) конечную точку или порт для подключения в асимметричном канале с магистральным портом 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="8eff8-296">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="8eff8-297">туннелирование 802.1 q используется для поддержания целостности VLAN клиента в сети поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8eff8-297">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8eff8-298"><dt>**Зарезервировано**</dt> <dt>7 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="8eff8-298"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="8eff8-299"><dt> **Поставщик зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-299"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="8eff8-300">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8eff8-300">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-301">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8eff8-301">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-303">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8eff8-303">The current statuses of the object.</span></span> <span data-ttu-id="8eff8-304">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="8eff8-304">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-305">**оператионалвлантрункенкапсулатион**</span><span class="sxs-lookup"><span data-stu-id="8eff8-305">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-306">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-308">Тип инкапсуляции виртуальной ЛС, используемой в конечной точке или порте магистрали.</span><span class="sxs-lookup"><span data-stu-id="8eff8-308">The type of VLAN encapsulation in use on a trunk endpoint/port.</span></span> <span data-ttu-id="8eff8-309">Это свойство имеет значение 2 (неприменимо) (то есть конечная точка не работает в режиме магистрали), определенный тип (3-802.1 Q или 4-Cisco острова), 5 (Negotiate) (т. е. конечные точки согласовывают тип инкапсуляции).</span><span class="sxs-lookup"><span data-stu-id="8eff8-309">This property is either 2 (Not Applicable) (that is, the endpoint is not operating in trunking mode), a particular type (3 - 802.1Q or 4 - Cisco ISL), 5 (Negotiate) (that is, the endpoints are negotiating the encapsulation type).</span></span> <span data-ttu-id="8eff8-310">Это свойство применимо только в том случае, если конечная точка работает в режиме магистрали (Дополнительные сведения см. в свойстве **оператионалендпоинтмоде** ).</span><span class="sxs-lookup"><span data-stu-id="8eff8-310">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="8eff8-311">Это свойство наследуется от [**CIM \_ вланендпоинт**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-311">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="8eff8-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8eff8-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8eff8-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff8-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff8-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco острова** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff8-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Согласование** (5)</span><span class="sxs-lookup"><span data-stu-id="8eff8-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negotiating** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="8eff8-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="8eff8-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8eff8-320">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="8eff8-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-321">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-323">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="8eff8-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="8eff8-324">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="8eff8-324">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8eff8-325">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8eff8-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-326">**осерендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="8eff8-326">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-327">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-329">Тип модели конечной точки VLAN, поддерживаемой этой конечной точкой VLAN, если значение свойства **оператионалендпоинтмоде** равно 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8eff8-329">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the **OperationalEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="8eff8-330">Это свойство должно иметь значение **null** , если свойство **оператионалендпоинтмоде** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="8eff8-330">This property should be set to **Null** when the **OperationalEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="8eff8-331">Это свойство наследуется от [**CIM \_ вланендпоинт**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-331">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-332">**осертрункенкапсулатион**</span><span class="sxs-lookup"><span data-stu-id="8eff8-332">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-335">Тип инкапсуляции виртуальной ЛС, поддерживаемый этой конечной точкой VLAN, если значение свойства **оператионалвлантрункенкапсулатион** равно 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8eff8-335">The type of VLAN encapsulation that is supported by this VLAN endpoint, when the value of the **OperationalVLANTrunkEncapsulation** property is set to 1 (Other).</span></span> <span data-ttu-id="8eff8-336">Это свойство должно иметь значение **null** , если требуемое свойство инкапсуляции имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="8eff8-336">This property should be set to **Null** when the desired encapsulation property is any value other than 1.</span></span> <span data-ttu-id="8eff8-337">Это свойство наследуется от [**CIM \_ вланендпоинт**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-337">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-338">**осертипедескриптион**</span><span class="sxs-lookup"><span data-stu-id="8eff8-338">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-339">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-339">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-341">Тип конечной точки протокола, если свойство **Type** этого класса (или любого из его подклассов) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8eff8-341">The type of protocol endpoint when the **Type** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="8eff8-342">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)и всегда имеет значение "Virtual Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8eff8-342">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-343">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="8eff8-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-344">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-346">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="8eff8-346">Provides high level status information.</span></span> <span data-ttu-id="8eff8-347">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8eff8-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="8eff8-348">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8eff8-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8eff8-349">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-350">**протоколифтипе**</span><span class="sxs-lookup"><span data-stu-id="8eff8-350">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-351">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-353">[IANA ИФТИПЕ MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="8eff8-353">The [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="8eff8-354">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)и всегда имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8eff8-354">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-355">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="8eff8-355">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-356">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-358">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) и не используется.</span><span class="sxs-lookup"><span data-stu-id="8eff8-358">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-359">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8eff8-359">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-360">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-362">Последнее запрошенное или требуемое состояние для службы управления.</span><span class="sxs-lookup"><span data-stu-id="8eff8-362">The last requested or desired state for the management service.</span></span> <span data-ttu-id="8eff8-363">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="8eff8-363">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="8eff8-364">Значение</span><span class="sxs-lookup"><span data-stu-id="8eff8-364">Value</span></span>                                                                         | <span data-ttu-id="8eff8-365">Значение</span><span class="sxs-lookup"><span data-stu-id="8eff8-365">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="8eff8-366"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-366"><dt>12</dt></span></span> </dl> | <span data-ttu-id="8eff8-367">Не применяется</span><span class="sxs-lookup"><span data-stu-id="8eff8-367">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8eff8-368">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8eff8-368">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-369">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-371">Описывает состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="8eff8-371">Describes the status of the element.</span></span> <span data-ttu-id="8eff8-372">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8eff8-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="8eff8-373">'</span><span class="sxs-lookup"><span data-stu-id="8eff8-373">"OK"</span></span>

<span data-ttu-id="8eff8-374">План</span><span class="sxs-lookup"><span data-stu-id="8eff8-374">"Error"</span></span>

<span data-ttu-id="8eff8-375">Пониженной функциональности</span><span class="sxs-lookup"><span data-stu-id="8eff8-375">"Degraded"</span></span>

<span data-ttu-id="8eff8-376">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="8eff8-376">"Unknown"</span></span>

<span data-ttu-id="8eff8-377">"Пред Fail"</span><span class="sxs-lookup"><span data-stu-id="8eff8-377">"Pred Fail"</span></span>

<span data-ttu-id="8eff8-378">Start</span><span class="sxs-lookup"><span data-stu-id="8eff8-378">"Starting"</span></span>

<span data-ttu-id="8eff8-379">Идет</span><span class="sxs-lookup"><span data-stu-id="8eff8-379">"Stopping"</span></span>

<span data-ttu-id="8eff8-380">Служеб</span><span class="sxs-lookup"><span data-stu-id="8eff8-380">"Service"</span></span>

<span data-ttu-id="8eff8-381">Груз</span><span class="sxs-lookup"><span data-stu-id="8eff8-381">"Stressed"</span></span>

<span data-ttu-id="8eff8-382">"Recover"</span><span class="sxs-lookup"><span data-stu-id="8eff8-382">"NonRecover"</span></span>

<span data-ttu-id="8eff8-383">"Нет контакта"</span><span class="sxs-lookup"><span data-stu-id="8eff8-383">"No Contact"</span></span>

<span data-ttu-id="8eff8-384">"Потеря связи"</span><span class="sxs-lookup"><span data-stu-id="8eff8-384">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-385">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="8eff8-385">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-386">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8eff8-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-388">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8eff8-388">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8eff8-389">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="8eff8-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-390">**суппортедендпоинтмодес**</span><span class="sxs-lookup"><span data-stu-id="8eff8-390">**SupportedEndpointModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-391">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8eff8-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-393">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="8eff8-393">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-394">Режимы конечных точек, поддерживаемые этим портом.</span><span class="sxs-lookup"><span data-stu-id="8eff8-394">The endpoint modes supported by this port.</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-395">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="8eff8-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-396">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-398">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="8eff8-398">The creation class name of the scoping system.</span></span> <span data-ttu-id="8eff8-399">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)и всегда имеет значение "мсвм \_ VirtualSwitch".</span><span class="sxs-lookup"><span data-stu-id="8eff8-399">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VirtualSwitch"</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-400">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8eff8-400">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8eff8-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-403">Системное имя системы области.</span><span class="sxs-lookup"><span data-stu-id="8eff8-403">The system name of the scoping system.</span></span> <span data-ttu-id="8eff8-404">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="8eff8-404">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-405">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="8eff8-405">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-406">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8eff8-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-408">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8eff8-408">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8eff8-409">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8eff8-409">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8eff8-410">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="8eff8-410">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff8-411">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff8-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff8-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8eff8-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff8-413">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8eff8-413">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8eff8-414">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8eff8-414">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8eff8-415">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8eff8-415">Remarks</span></span>

<span data-ttu-id="8eff8-416">Доступ к классу **\_ вланендпоинт мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="8eff8-416">Access to the **Msvm\_VLANEndpoint** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8eff8-417">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8eff8-417">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="8eff8-418">Примеры</span><span class="sxs-lookup"><span data-stu-id="8eff8-418">Examples</span></span>

<span data-ttu-id="8eff8-419">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8eff8-419">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eff8-420">Требования</span><span class="sxs-lookup"><span data-stu-id="8eff8-420">Requirements</span></span>



| <span data-ttu-id="8eff8-421">Требование</span><span class="sxs-lookup"><span data-stu-id="8eff8-421">Requirement</span></span> | <span data-ttu-id="8eff8-422">Значение</span><span class="sxs-lookup"><span data-stu-id="8eff8-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eff8-423">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8eff8-423">Minimum supported client</span></span><br/> | <span data-ttu-id="8eff8-424">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8eff8-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8eff8-425">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8eff8-425">Minimum supported server</span></span><br/> | <span data-ttu-id="8eff8-426">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8eff8-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8eff8-427">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8eff8-427">Namespace</span></span><br/>                | <span data-ttu-id="8eff8-428">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8eff8-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8eff8-429">MOF</span><span class="sxs-lookup"><span data-stu-id="8eff8-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8eff8-430"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8eff8-431">DLL</span><span class="sxs-lookup"><span data-stu-id="8eff8-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eff8-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8eff8-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8eff8-433">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8eff8-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eff8-434">**\_ВЛАНЕНДПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="8eff8-434">**CIM\_VLANEndpoint**</span></span>](cim-vlanendpoint.md)
</dt> <dt>

[<span data-ttu-id="8eff8-435">**\_ВЛАНЕНДПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="8eff8-435">**CIM\_VLANEndpoint**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

