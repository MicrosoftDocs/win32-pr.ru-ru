---
description: Представляет конечную точку беспроводной связи, которая может отправлять и получать кадры данных, когда связанное устройство интерфейса подключено к беспроводной локальной сети IEEE 802,11.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: Класс CIM_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e09d040f9d4530bee4347528d704cfe2e9403b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684027"
---
# <a name="cim_wifiendpoint-class"></a><span data-ttu-id="5c24c-103">\_Класс CIM вифиендпоинт</span><span class="sxs-lookup"><span data-stu-id="5c24c-103">CIM\_WiFiEndpoint class</span></span>

<span data-ttu-id="5c24c-104">Представляет конечную точку беспроводной связи, которая может отправлять и получать кадры данных, когда связанное устройство интерфейса подключено к беспроводной локальной сети IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="5c24c-104">Represents a wireless communication endpoint, which can send and receive data frames when its associated interface device is connected with an IEEE 802.11 wireless LAN.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c24c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c24c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a><span data-ttu-id="5c24c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5c24c-106">Members</span></span>

<span data-ttu-id="5c24c-107">Класс **CIM \_ вифиендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5c24c-107">The **CIM\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="5c24c-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c24c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c24c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c24c-109">Properties</span></span>

<span data-ttu-id="5c24c-110">Класс **CIM \_ вифиендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5c24c-110">The **CIM\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c24c-111">**акцесспоинтаддресс**</span><span class="sxs-lookup"><span data-stu-id="5c24c-111">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5c24c-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-114">MAC-адрес точки доступа, связанной с конечной точкой Wi-Fi; в противном случае **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c24c-114">The MAC address of the access point that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c24c-115">**Связь**</span><span class="sxs-lookup"><span data-stu-id="5c24c-115">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5c24c-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-118">**значение true** , если конечная точка Wi-Fi в настоящее время связана с точкой доступа или клиентской станцией; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5c24c-118">**true** if the WiFi endpoint is currently associated with an access point or client station; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="5c24c-119">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="5c24c-119">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-120">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c24c-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-122">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вифиендпоинт**.**Енкриптионмесод**","**CIM \_ вифиендпоинт**.**IEEE8021xAuthenticationProtocol**","**CIM \_ вифиендпоинт**.**Осераусентикатионмесод**")</span><span class="sxs-lookup"><span data-stu-id="5c24c-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**", "**CIM\_WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM\_WiFiEndpoint**.**OtherAuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-123">Тип проверки подлинности, используемый между конечной точкой Wi-Fi и сетью.</span><span class="sxs-lookup"><span data-stu-id="5c24c-123">The authentication type used between the Wi-Fi endpoint and the network.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c24c-124">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5c24c-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c24c-125">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5c24c-125">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

<span data-ttu-id="5c24c-126">**Открыть систему** (2)</span><span class="sxs-lookup"><span data-stu-id="5c24c-126">**Open System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

<span data-ttu-id="5c24c-127">**Общий ключ** (3)</span><span class="sxs-lookup"><span data-stu-id="5c24c-127">**Shared Key** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

<span data-ttu-id="5c24c-128">**WPA PSK** (4)</span><span class="sxs-lookup"><span data-stu-id="5c24c-128">**WPA PSK** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

<span data-ttu-id="5c24c-129">**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="5c24c-129">**WPA IEEE 802.1x** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

<span data-ttu-id="5c24c-130">**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="5c24c-130">**WPA2 PSK** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

<span data-ttu-id="5c24c-131">**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="5c24c-131">**WPA2 IEEE 802.1x** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

<span data-ttu-id="5c24c-132">**КККМ IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="5c24c-132">**CCKM IEEE 802.1x** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5c24c-133">**Зарезервировано DMTF** (9..)</span><span class="sxs-lookup"><span data-stu-id="5c24c-133">**DMTF Reserved** (9..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c24c-134">**бсстипе**</span><span class="sxs-lookup"><span data-stu-id="5c24c-134">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c24c-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-137">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3,16")</span><span class="sxs-lookup"><span data-stu-id="5c24c-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-138">Тип "базовый набор служб (BSS)" сети, соответствующий экземпляру.</span><span class="sxs-lookup"><span data-stu-id="5c24c-138">The basic service set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="5c24c-139">BSS — это набор станций, управляемых одной функцией координации.</span><span class="sxs-lookup"><span data-stu-id="5c24c-139">A BSS is a set of stations controlled by a single coordination function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c24c-140">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5c24c-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="5c24c-141">**Независимое** (2)</span><span class="sxs-lookup"><span data-stu-id="5c24c-141">**Independent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

<span data-ttu-id="5c24c-142">**Инфраструктура** (3)</span><span class="sxs-lookup"><span data-stu-id="5c24c-142">**Infrastructure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5c24c-143">**Зарезервировано DMTF** (4..)</span><span class="sxs-lookup"><span data-stu-id="5c24c-143">**DMTF Reserved** (4..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c24c-144">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="5c24c-144">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c24c-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-147">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вифиендпоинт**.**AuthenticationMethod**","**CIM \_ вифиендпоинт**.**Осеренкриптионмесод**")</span><span class="sxs-lookup"><span data-stu-id="5c24c-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**", "**CIM\_WiFiEndpoint**.**OtherEncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-148">Тип шифрования, используемый при отправке и получении данных через конечную точку Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="5c24c-148">The encryption type used when sending and receiving data through the Wi-Fi endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c24c-149">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5c24c-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c24c-150">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5c24c-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

<span data-ttu-id="5c24c-151">**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="5c24c-151">**WEP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

<span data-ttu-id="5c24c-152">**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="5c24c-152">**TKIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

<span data-ttu-id="5c24c-153">**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="5c24c-153">**CCMP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5c24c-154">**Нет** (5)</span><span class="sxs-lookup"><span data-stu-id="5c24c-154">**None** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5c24c-155">**Зарезервировано DMTF** (6..)</span><span class="sxs-lookup"><span data-stu-id="5c24c-155">**DMTF Reserved** (6..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c24c-156">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="5c24c-156">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c24c-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-159">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF "," RFC2716. IETF "," черновик-IETF-пппекст-EAP-TTLS. IETF "," черновик-Камас-пппекст-PEAPv0. IETF "," черновик-(josefsson-пппекст-EAP-TLS-EAP "," RFC4851. IETF "," RFC3748. IETF "," RFC4764. IETF "," RFC4186. IETF "," RFC4187. IETF "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вифиендпоинт**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="5c24c-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017.IETF", "RFC2716.IETF", "draft-ietf-pppext-eap-ttls.IETF", "draft-kamath-pppext-peapv0.IETF", "draft-josefsson-pppext-eap-tls-eap", "RFC4851.IETF", "RFC3748.IETF", "RFC4764.IETF", "RFC4186.IETF", "RFC4187.IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-160">Тип EAP (расширяемого протокола проверки подлинности) для конечной точки Wi-Fi, если параметр **AuthenticationMethod** содержит "7" (WPA IEEE 802.1 x) или "8" (КККМ IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="5c24c-160">The EAP (Extensible Authentication Protocol) type for the Wi-Fi endpoint when **AuthenticationMethod** contains "7" (WPA IEEE 802.1x) or "8" (CCKM IEEE 802.1x).</span></span>

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

<span data-ttu-id="5c24c-161">**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="5c24c-161">**EAP-TLS** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

<span data-ttu-id="5c24c-162">**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="5c24c-162">**EAP-TTLS/MSCHAPv2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

<span data-ttu-id="5c24c-163">**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="5c24c-163">**PEAPv0/EAP-MSCHAPv2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

<span data-ttu-id="5c24c-164">**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="5c24c-164">**PEAPv1/EAP-GTC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

<span data-ttu-id="5c24c-165">**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="5c24c-165">**EAP-FAST/MSCHAPv2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

<span data-ttu-id="5c24c-166">**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="5c24c-166">**EAP-FAST/GTC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

<span data-ttu-id="5c24c-167">**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="5c24c-167">**EAP-MD5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

<span data-ttu-id="5c24c-168">**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="5c24c-168">**EAP-PSK** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

<span data-ttu-id="5c24c-169">**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="5c24c-169">**EAP-SIM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

<span data-ttu-id="5c24c-170">**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="5c24c-170">**EAP-AKA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

<span data-ttu-id="5c24c-171">**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="5c24c-171">**EAP-FAST/TLS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5c24c-172">**Зарезервировано DMTF** (11..)</span><span class="sxs-lookup"><span data-stu-id="5c24c-172">**DMTF Reserved** (11..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c24c-173">**ланид**</span><span class="sxs-lookup"><span data-stu-id="5c24c-173">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5c24c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-176">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ланид"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span><span class="sxs-lookup"><span data-stu-id="5c24c-176">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-177">Идентификатор набора служб (SSID) беспроводной локальной сети, связанной с конечной точкой Wi-Fi; в противном случае **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c24c-177">The service set identifier (SSID) of the wireless LAN that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c24c-178">**осераусентикатионмесод**</span><span class="sxs-lookup"><span data-stu-id="5c24c-178">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5c24c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-181">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вифиендпоинт**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="5c24c-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-182">Тип проверки подлинности, используемый между конечной точкой Wi-Fi и сетью, если параметр **AuthenticationMethod** содержит "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="5c24c-182">The authentication type used between the Wi-Fi endpoint and the network when **AuthenticationMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="5c24c-183">**осеренкриптионмесод**</span><span class="sxs-lookup"><span data-stu-id="5c24c-183">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5c24c-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-186">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ вифиендпоинт**.**Енкриптионмесод**")</span><span class="sxs-lookup"><span data-stu-id="5c24c-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-187">Описывает тип шифрования для конечной точки Wi-Fi, если **енкриптионмесод** содержит "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="5c24c-187">Describes the encryption type for the Wi-Fi endpoint when **EncryptionMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="5c24c-188">**протоколифтипе**</span><span class="sxs-lookup"><span data-stu-id="5c24c-188">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24c-189">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c24c-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c24c-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24c-191">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("протоколифтипе")</span><span class="sxs-lookup"><span data-stu-id="5c24c-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span></span>
</dt> </dl>

<span data-ttu-id="5c24c-192">Категория или классификация данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5c24c-192">The category or classification of this instance.</span></span> <span data-ttu-id="5c24c-193">Возможные значения ограничены Wi-Fi и зарезервированными значениями из [ИФТИПЕ MIB и IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="5c24c-193">The possible values are limited to the Wi-Fi and reserved values from the DMTF and [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span>

<span data-ttu-id="5c24c-194">Если для **протоколифтипе** задано значение "1" (другое), то сведения о типе должны быть предоставлены в свойстве **осертипедескриптион** .</span><span class="sxs-lookup"><span data-stu-id="5c24c-194">If the **ProtocolIFType** is set to "1" (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c24c-195">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5c24c-195">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="5c24c-196">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="5c24c-196">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="5c24c-197">**Зарезервирован IANA** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="5c24c-197">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5c24c-198">**Зарезервировано DMTF** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5c24c-198">**DMTF Reserved** (4301..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5c24c-199">**Поставщик зарезервирован** (32768...)</span><span class="sxs-lookup"><span data-stu-id="5c24c-199">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="5c24c-200"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5c24c-200"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5c24c-201">Требования</span><span class="sxs-lookup"><span data-stu-id="5c24c-201">Requirements</span></span>



| <span data-ttu-id="5c24c-202">Требование</span><span class="sxs-lookup"><span data-stu-id="5c24c-202">Requirement</span></span> | <span data-ttu-id="5c24c-203">Значение</span><span class="sxs-lookup"><span data-stu-id="5c24c-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c24c-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c24c-204">Minimum supported client</span></span><br/> | <span data-ttu-id="5c24c-205">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5c24c-205">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5c24c-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c24c-206">Minimum supported server</span></span><br/> | <span data-ttu-id="5c24c-207">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c24c-207">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5c24c-208">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5c24c-208">Namespace</span></span><br/>                | <span data-ttu-id="5c24c-209">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5c24c-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5c24c-210">MOF</span><span class="sxs-lookup"><span data-stu-id="5c24c-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c24c-211"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c24c-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c24c-212">DLL</span><span class="sxs-lookup"><span data-stu-id="5c24c-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c24c-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c24c-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c24c-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c24c-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c24c-215">**\_ЛАНЕНДПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="5c24c-215">**CIM\_LANEndpoint**</span></span>](cim-lanendpoint.md)
</dt> </dl>

 

