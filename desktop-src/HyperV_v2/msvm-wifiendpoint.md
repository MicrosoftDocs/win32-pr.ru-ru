---
description: Представляет логическую точку подключения для сетевого адаптера. Если конечная точка Wi-Fi подключена к порту коммутатора, сетевой адаптер, подключенный к конечной точке Wi-Fi, имеет подключение к сети.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Класс Msvm_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991076"
---
# <a name="msvm_wifiendpoint-class"></a><span data-ttu-id="2a0a3-104">\_Класс мсвм вифиендпоинт</span><span class="sxs-lookup"><span data-stu-id="2a0a3-104">Msvm\_WiFiEndpoint class</span></span>

<span data-ttu-id="2a0a3-105">Представляет логическую точку подключения для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="2a0a3-106">Если конечная точка Wi-Fi подключена к порту коммутатора, сетевой адаптер, подключенный к конечной точке Wi-Fi, имеет подключение к сети.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-106">When the Wi-Fi endpoint is connected to a switch port, the network adapter connected to the Wi-Fi endpoint has network connectivity.</span></span>

<span data-ttu-id="2a0a3-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a0a3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a0a3-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
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
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a><span data-ttu-id="2a0a3-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2a0a3-109">Members</span></span>

<span data-ttu-id="2a0a3-110">Класс **мсвм \_ вифиендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2a0a3-110">The **Msvm\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="2a0a3-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2a0a3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2a0a3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a0a3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2a0a3-113">Методы</span><span class="sxs-lookup"><span data-stu-id="2a0a3-113">Methods</span></span>

<span data-ttu-id="2a0a3-114">Класс **мсвм \_ вифиендпоинт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-114">The **Msvm\_WiFiEndpoint** class has these methods.</span></span>



| <span data-ttu-id="2a0a3-115">Метод</span><span class="sxs-lookup"><span data-stu-id="2a0a3-115">Method</span></span>                 | <span data-ttu-id="2a0a3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2a0a3-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="2a0a3-117">**Равен**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-117">**RequestStateChange**</span></span> | <span data-ttu-id="2a0a3-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-118">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2a0a3-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a0a3-119">Properties</span></span>

<span data-ttu-id="2a0a3-120">Класс **мсвм \_ вифиендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-120">The **Msvm\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a0a3-121">**акцесспоинтаддресс**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-121">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-124">Содержит MAC-адрес точки доступа, с которой в настоящее время связана конечная точка Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-124">Contains the MAC address of the access point with which the Wi-Fi endpoint is currently associated.</span></span> <span data-ttu-id="2a0a3-125">Если конечная точка Wi-Fi в настоящее время не связана, **акцесспоинтаддресс** должна иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-125">If the Wi-Fi endpoint is not currently associated, then **AccessPointAddress** should be **Null**.</span></span> <span data-ttu-id="2a0a3-126">MAC-адрес должен иметь формат двенадцати шестнадцатеричных цифр (например, "010203040506"), при этом каждая пара представляет один из шести октетов MAC-адреса в каноническом порядке (например, бит адреса группы находится в младших битах первого символа строки).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-126">The MAC address should be formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (for example, the Group address bit is found in the low order bit of the first character of the string).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-127">**алиасаддрессес**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-127">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-128">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-130">Другие адреса одноадресной рассылки, которые могут использоваться для связи с конечной точкой локальной сети.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-130">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="2a0a3-131">Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-131">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-132">**Связь**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-132">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-135">Указывает, связана ли в настоящее время конечная точка Wi-Fi с точкой доступа или клиентской станцией.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-135">Indicates whether the Wi-Fi endpoint is currently associated to an access point or client station.</span></span>

<span data-ttu-id="2a0a3-136">Содержит **значение true** , если конечная точка Wi-Fi связана с точкой доступа или клиентской станцией. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-136">Contains **True** if the Wi-Fi endpoint is associated to an access point or client station; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-137">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-137">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-140">Указывает метод, используемый для проверки подлинности конечной точки Wi-Fi и сети друг с другом.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-140">Specifies the method used to authenticate the Wi-Fi endpoint and the network to one another.</span></span>

<dl> <dt>

<span data-ttu-id="2a0a3-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Открыть систему** (2)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Общий ключ** (3)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Shared Key** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**КККМ IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (9..</span><span class="sxs-lookup"><span data-stu-id="2a0a3-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (9..</span></span> <span data-ttu-id="2a0a3-151">)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a0a3-152">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-153">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="2a0a3-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-155">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-155">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="2a0a3-156">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-156">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="2a0a3-157">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-157">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="2a0a3-158">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-158">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="2a0a3-159">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2a0a3-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="2a0a3-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="2a0a3-170">)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a0a3-171">**бсстипе**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-171">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-172">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-174">Указывает тип "базовый набор служб (BSS)" сети, соответствующий экземпляру.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-174">Indicates the Basic Service Set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="2a0a3-175">Набор служб "базовый" — это набор станций, управляемых одной функцией координации.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-175">A Basic Service Set is a set of stations controlled by a single coordination function.</span></span>



| <span data-ttu-id="2a0a3-176">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0a3-176">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="2a0a3-177">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0a3-177">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2a0a3-178"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-178"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <span data-ttu-id="2a0a3-179"><dt>**Независимое**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-179"><dt>**Independent**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="2a0a3-180">Конечная точка Wi-Fi связана непосредственно с другой клиентской станцией.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-180">The Wi-Fi endpoint is associated directly to another client station.</span></span><br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <span data-ttu-id="2a0a3-181"><dt>**Инфраструктура**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-181"><dt>**Infrastructure**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="2a0a3-182">Конечная точка Wi-Fi связана с сетью с помощью точки доступа.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-182">The Wi-Fi endpoint is associated to a network by using an access point.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="2a0a3-183"><dt> **Зарезервировано 4 DMTF**</dt> <dt>.</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-183"><dt>**DMTF Reserved** </dt> <dt>4.. </dt></span></span> </dl> |                                                                                    |



 

</dd> <dt>

<span data-ttu-id="2a0a3-184">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-187">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-187">A short description of the object.</span></span> <span data-ttu-id="2a0a3-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-189">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-192">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2a0a3-193">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2a0a3-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-195">**Подключен**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-195">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-198">Это свойство имеет значение **true** , если конечная точка Wi-Fi подключена к порту коммутатора.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-198">This property is set to **True** if the Wi-Fi endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-199">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-199">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-202">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-202">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-203">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-203">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2a0a3-204">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-204">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-205">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-205">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-208">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-208">A description of the object.</span></span> <span data-ttu-id="2a0a3-209">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-210">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-210">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-213">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-213">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2a0a3-214">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-214">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2a0a3-215">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-219">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-219">A display name for the object.</span></span> <span data-ttu-id="2a0a3-220">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-221">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-222">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-224">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2a0a3-225">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2a0a3-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a0a3-229">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-229">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-230">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-232">Указывает включенное состояние запланированной системы.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-232">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="2a0a3-233">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="2a0a3-234">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0a3-234">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2a0a3-235">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0a3-235">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2a0a3-236"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-236"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2a0a3-237">Система отключена.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-237">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="2a0a3-238"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-238"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="2a0a3-239">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-239">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="2a0a3-240"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-240"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2a0a3-241">Система включена, но в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-241">The system is enabled, but offline.</span></span> <span data-ttu-id="2a0a3-242">Все новые запросы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-242">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a0a3-243">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-243">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-244">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-246">Указывает метод шифрования, используемый для защиты конфиденциальности данных, отправляемых и получаемых конечной точкой Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-246">Specifies the encryption method in use to protect the confidentiality of data sent and received by the Wi-Fi endpoint.</span></span>

<dl> <dt>

<span data-ttu-id="2a0a3-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (5)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (6..</span><span class="sxs-lookup"><span data-stu-id="2a0a3-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (6..</span></span> <span data-ttu-id="2a0a3-254">)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a0a3-255">**граупаддрессес**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-255">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-256">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-258">Адреса многоадресной рассылки, на которые прослушивается конечная точка локальной сети.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-258">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="2a0a3-259">Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-259">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-260">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-260">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-261">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-263">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-263">The current health of the element.</span></span> <span data-ttu-id="2a0a3-264">Это свойство выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-264">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="2a0a3-265">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-265">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2a0a3-266">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-267">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-267">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-268">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-270">Содержит тип EAP, если параметр **AuthenticationMethod** содержит 5 (WPA IEEE 802.1 x), 7 (WPA2 IEEE 802.1 x) или 8 (КККМ IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-270">Contains the Extensible Authentication Protocol (EAP) type if and only if **AuthenticationMethod** contains 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x), or 8 (CCKM IEEE 802.1x).</span></span>

<dl> <dt>

<span data-ttu-id="2a0a3-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (11..</span><span class="sxs-lookup"><span data-stu-id="2a0a3-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (11..</span></span> <span data-ttu-id="2a0a3-283">)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-283">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a0a3-284">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-284">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-285">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-287">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-287">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="2a0a3-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-289">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-289">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-292">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-292">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-293">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-293">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2a0a3-294">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-294">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-295">**ланид**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-295">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-298">Метка или идентификатор сегмента локальной сети, к которой подключена конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-298">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="2a0a3-299">Если конечная точка в данный момент не активна или подключена, или эта информация неизвестна, это свойство будет иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-299">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="2a0a3-300">Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-300">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-301">**лантипе**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-301">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-302">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-304">Это свойство не рекомендуется использовать вместо свойства **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="2a0a3-304">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="2a0a3-305">Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-305">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-306">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-306">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-309">Квалификаторы: **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-309">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-310">MAC-адрес, используемый для связи с конечной точкой локальной сети.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-310">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="2a0a3-311">MAC-адрес имеет формат двенадцати шестнадцатеричных цифр (например, "010203040506"), при этом каждая пара представляет один из шести октетов MAC-адреса в каноническом порядке в соответствии с RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-311">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="2a0a3-312">Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-312">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-313">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-313">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-314">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-316">Квалификаторы: **единицы** ("биты")</span><span class="sxs-lookup"><span data-stu-id="2a0a3-316">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-317">Самый крупный размер (в битах) информационного поля, который может быть отправлен или получен конечной точкой локальной сети.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-317">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="2a0a3-318">Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-318">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-322">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-322">The label by which the object is known.</span></span> <span data-ttu-id="2a0a3-323">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-324">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-324">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-327">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-327">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-328">Содержит эвристику именования, выбранную для обеспечения уникальности значения свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="2a0a3-328">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="2a0a3-329">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-329">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-330">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-330">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-331">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-333">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2a0a3-333">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2a0a3-334">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-334">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2a0a3-335">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-335">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-337">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="2a0a3-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-339">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-339">The current statuses of the object.</span></span> <span data-ttu-id="2a0a3-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-341">**осераусентикатионмесод**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-341">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-344">Указывает метод проверки подлинности 802,11, только если параметр **AuthenticationMethod** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-344">Specifies the 802.11 authentication method if and only if **AuthenticationMethod** contains 1 (Other).</span></span> <span data-ttu-id="2a0a3-345">Формат этой строки зависит от вендора.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-345">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-346">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-346">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-349">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="2a0a3-349">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="2a0a3-350">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-350">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2a0a3-351">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-351">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-352">**осеренкриптионмесод**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-352">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-355">Указывает метод шифрования 802,11, только если **енкриптионмесод** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-355">Specifies the 802.11 encryption method if and only if **EncryptionMethod** contains 1 (Other).</span></span> <span data-ttu-id="2a0a3-356">Формат этой строки зависит от вендора.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-356">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-357">**осерлантипе**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-357">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-360">Это свойство не рекомендуется использовать вместо свойства **осертипедескриптион** .</span><span class="sxs-lookup"><span data-stu-id="2a0a3-360">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="2a0a3-361">Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-361">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-362">**осертипедескриптион**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-362">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-363">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-365">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-365">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-366">Строка, описывающая тип конечной точки протокола, если свойство **протоколифтипе** этого класса (или любого из его подклассов) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-366">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="2a0a3-367">Это свойство должно иметь значение **null** , если свойство **протоколифтипе** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-367">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="2a0a3-368">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-368">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-369">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-369">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-370">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-372">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-372">Provides high level status information.</span></span> <span data-ttu-id="2a0a3-373">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-373">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="2a0a3-374">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-374">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2a0a3-375">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-376">**протоколифтипе**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-376">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-377">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-379">Свойство используется для категоризации и классификации экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-379">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="2a0a3-380">Если для **протоколифтипе** задано значение 1 (другое), то сведения о типе должны быть предоставлены в свойстве **осертипедескриптион** .</span><span class="sxs-lookup"><span data-stu-id="2a0a3-380">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="2a0a3-381">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-381">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="2a0a3-382">**Протоколифтипе** — это перечисление, которое синхронизируется с [IANA ифтипе MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-382">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="2a0a3-383">Также включаются дополнительные значения, определенные в DMTF.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-383">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="2a0a3-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**Зарезервирован IANA** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (4301..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (32768..</span><span class="sxs-lookup"><span data-stu-id="2a0a3-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="2a0a3-389">)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-389">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a0a3-390">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-390">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-391">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-393">Это свойство не рекомендуется использовать вместо свойства **протоколифтипе** .</span><span class="sxs-lookup"><span data-stu-id="2a0a3-393">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="2a0a3-394">Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-394">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-396">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-398">Последнее запрошенное или требуемое состояние для службы управления.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="2a0a3-399">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-400">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-400">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-403">Описывает состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-403">Describes the status of the element.</span></span> <span data-ttu-id="2a0a3-404">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-404">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="2a0a3-405">'</span><span class="sxs-lookup"><span data-stu-id="2a0a3-405">"OK"</span></span>

<span data-ttu-id="2a0a3-406">План</span><span class="sxs-lookup"><span data-stu-id="2a0a3-406">"Error"</span></span>

<span data-ttu-id="2a0a3-407">Пониженной функциональности</span><span class="sxs-lookup"><span data-stu-id="2a0a3-407">"Degraded"</span></span>

<span data-ttu-id="2a0a3-408">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="2a0a3-408">"Unknown"</span></span>

<span data-ttu-id="2a0a3-409">"Пред Fail"</span><span class="sxs-lookup"><span data-stu-id="2a0a3-409">"Pred Fail"</span></span>

<span data-ttu-id="2a0a3-410">Start</span><span class="sxs-lookup"><span data-stu-id="2a0a3-410">"Starting"</span></span>

<span data-ttu-id="2a0a3-411">Идет</span><span class="sxs-lookup"><span data-stu-id="2a0a3-411">"Stopping"</span></span>

<span data-ttu-id="2a0a3-412">Служеб</span><span class="sxs-lookup"><span data-stu-id="2a0a3-412">"Service"</span></span>

<span data-ttu-id="2a0a3-413">Груз</span><span class="sxs-lookup"><span data-stu-id="2a0a3-413">"Stressed"</span></span>

<span data-ttu-id="2a0a3-414">"Recover"</span><span class="sxs-lookup"><span data-stu-id="2a0a3-414">"NonRecover"</span></span>

<span data-ttu-id="2a0a3-415">"Нет контакта"</span><span class="sxs-lookup"><span data-stu-id="2a0a3-415">"No Contact"</span></span>

<span data-ttu-id="2a0a3-416">"Потеря связи"</span><span class="sxs-lookup"><span data-stu-id="2a0a3-416">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-417">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-417">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-418">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-418">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-420">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2a0a3-420">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2a0a3-421">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-421">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-422">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-423">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-425">Имя класса создания системы размещения.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-425">The hosting system's creation class name.</span></span> <span data-ttu-id="2a0a3-426">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-426">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-427">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-427">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-430">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2a0a3-430">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-431">Имя системы размещения.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-431">The name of the hosting system.</span></span> <span data-ttu-id="2a0a3-432">Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-432">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-433">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-433">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-434">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-436">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-436">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2a0a3-437">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-437">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2a0a3-438">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-438">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a0a3-439">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a0a3-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a0a3-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a0a3-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a0a3-441">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="2a0a3-441">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2a0a3-442">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a0a3-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a0a3-443">Требования</span><span class="sxs-lookup"><span data-stu-id="2a0a3-443">Requirements</span></span>



| <span data-ttu-id="2a0a3-444">Требование</span><span class="sxs-lookup"><span data-stu-id="2a0a3-444">Requirement</span></span> | <span data-ttu-id="2a0a3-445">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0a3-445">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0a3-446">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a0a3-446">Minimum supported client</span></span><br/> | <span data-ttu-id="2a0a3-447">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2a0a3-447">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a0a3-448">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a0a3-448">Minimum supported server</span></span><br/> | <span data-ttu-id="2a0a3-449">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2a0a3-449">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a0a3-450">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2a0a3-450">Namespace</span></span><br/>                | <span data-ttu-id="2a0a3-451">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2a0a3-451">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a0a3-452">MOF</span><span class="sxs-lookup"><span data-stu-id="2a0a3-452">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a0a3-453"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-453"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a0a3-454">DLL</span><span class="sxs-lookup"><span data-stu-id="2a0a3-454">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a0a3-455"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a0a3-455"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

