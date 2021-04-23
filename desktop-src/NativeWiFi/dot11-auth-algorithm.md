---
description: Определяет алгоритм проверки подлинности беспроводной локальной сети.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: Перечисление DOT11_AUTH_ALGORITHM (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673923"
---
# <a name="dot11_auth_algorithm-enumeration"></a><span data-ttu-id="30ae5-103">\_Перечисление алгоритма проверки подлинности DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="30ae5-103">DOT11\_AUTH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="30ae5-104">Тип **перечисления \_ \_ алгоритма авторизации DOT11** определяет алгоритм проверки подлинности беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="30ae5-104">The **DOT11\_AUTH\_ALGORITHM** enumerated type defines a wireless LAN authentication algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ae5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30ae5-105">Syntax</span></span>


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="30ae5-106">Константы</span><span class="sxs-lookup"><span data-stu-id="30ae5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30ae5-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**\_Открытая проверка подлинности DOT11 \_ Algo \_ 80211 \_**</span><span class="sxs-lookup"><span data-stu-id="30ae5-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11\_AUTH\_ALGO\_80211\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-108">Указывает алгоритм проверки подлинности с открытым системным стандартом IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="30ae5-108">Specifies an IEEE 802.11 Open System authentication algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_Общий ключ проверки подлинности DOT11 \_ Algo \_ 80211 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30ae5-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11\_AUTH\_ALGO\_80211\_SHARED\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-110">Указывает алгоритм проверки подлинности с общим ключом 802,11, который требует использования ключа WEP для проверки подлинности 802,11.</span><span class="sxs-lookup"><span data-stu-id="30ae5-110">Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**\_Проверка подлинности DOT11 \_ Algo \_ WPA**</span><span class="sxs-lookup"><span data-stu-id="30ae5-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11\_AUTH\_ALGO\_WPA**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-112">Указывает алгоритм защиты Wi-Fi защищенного доступа (WPA).</span><span class="sxs-lookup"><span data-stu-id="30ae5-112">Specifies a Wi-Fi Protected Access (WPA) algorithm.</span></span> <span data-ttu-id="30ae5-113">Проверка подлинности по порту IEEE 802.1 X выполняется с помощью запрашивающего устройства, средства проверки подлинности и сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="30ae5-113">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="30ae5-114">Ключи шифра динамически получаются через процесс проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30ae5-114">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="30ae5-115">Этот алгоритм действителен только для типов BSS \_ инфраструктуры типов Dot11 BSS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="30ae5-115">This algorithm is valid only for BSS types of dot11\_BSS\_type\_infrastructure.</span></span>

<span data-ttu-id="30ae5-116">При включении алгоритма WPA станция 802,11 связывается только с точкой доступа, для которой в элементе данных WPA (IE) содержится набор проверки подлинности с типом 1 (802.1 X).</span><span class="sxs-lookup"><span data-stu-id="30ae5-116">When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**\_Проверка подлинности DOT11 \_ Algo \_ WPA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="30ae5-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11\_AUTH\_ALGO\_WPA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-118">Указывает алгоритм WPA, использующий общие ключи (PSK).</span><span class="sxs-lookup"><span data-stu-id="30ae5-118">Specifies a WPA algorithm that uses preshared keys (PSK).</span></span> <span data-ttu-id="30ae5-119">Проверка подлинности по порту IEEE 802.1 X выполняется с помощью запрашивающего устройства и средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30ae5-119">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="30ae5-120">Ключи шифра динамически извлекаются с помощью предварительно общего ключа, который используется как для запрашивающего, так и для средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30ae5-120">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="30ae5-121">Этот алгоритм действителен только для типов BSS **\_ \_ \_ инфраструктуры типов Dot11 BSS**.</span><span class="sxs-lookup"><span data-stu-id="30ae5-121">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="30ae5-122">Когда алгоритм WPA PSK включен, станция 802,11 связывается только с точкой доступа, в которой ответы на маяки или зонды содержат набор проверки подлинности типа 2 (предварительный ключ) в WPA IE.</span><span class="sxs-lookup"><span data-stu-id="30ae5-122">When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**\_ALGOная проверка подлинности DOT11 \_ \_ WPA \_ None**</span><span class="sxs-lookup"><span data-stu-id="30ae5-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11\_AUTH\_ALGO\_WPA\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-124">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="30ae5-124">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**\_ALGOская проверка подлинности DOT11 \_ \_ рсна**</span><span class="sxs-lookup"><span data-stu-id="30ae5-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11\_AUTH\_ALGO\_RSNA**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-126">Указывает алгоритм беспроводного сопоставления сети (РСНА) 802.11 с ненадежным доступом.</span><span class="sxs-lookup"><span data-stu-id="30ae5-126">Specifies an 802.11i Robust Security Network Association (RSNA) algorithm.</span></span> <span data-ttu-id="30ae5-127">WPA2 — это один из таких алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="30ae5-127">WPA2 is one such algorithm.</span></span> <span data-ttu-id="30ae5-128">Проверка подлинности по порту IEEE 802.1 X выполняется с помощью запрашивающего устройства, средства проверки подлинности и сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="30ae5-128">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="30ae5-129">Ключи шифра динамически получаются через процесс проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30ae5-129">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="30ae5-130">Этот алгоритм действителен только для типов BSS **\_ \_ \_ инфраструктуры типов Dot11 BSS**.</span><span class="sxs-lookup"><span data-stu-id="30ae5-130">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="30ae5-131">Если включен алгоритм РСНА, то Станция 802,11 связывается только с точкой доступа, в которой ответы на сигналы маяка или зонды содержат набор проверки подлинности типа 1 (802.1 X) в среде RSN IE.</span><span class="sxs-lookup"><span data-stu-id="30ae5-131">When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ AUTH \_ Algo \_ рсна \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="30ae5-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11\_AUTH\_ALGO\_RSNA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-133">Указывает алгоритм 802.11 i РСНА, использующий PSK.</span><span class="sxs-lookup"><span data-stu-id="30ae5-133">Specifies an 802.11i RSNA algorithm that uses PSK.</span></span> <span data-ttu-id="30ae5-134">Проверка подлинности по порту IEEE 802.1 X выполняется с помощью запрашивающего устройства и средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30ae5-134">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="30ae5-135">Ключи шифра динамически извлекаются с помощью предварительно общего ключа, который используется как для запрашивающего, так и для средства проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="30ae5-135">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="30ae5-136">Этот алгоритм действителен только для типов BSS **\_ \_ \_ инфраструктуры типов Dot11 BSS**.</span><span class="sxs-lookup"><span data-stu-id="30ae5-136">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="30ae5-137">Если включен алгоритм РСНА PSK, то Станция 802,11 связывается только с точкой доступа, в которой ответы на сигналы маяка или зонды содержат набор проверки подлинности типа 2 (предварительный ключ) в обозревателе RSN IE.</span><span class="sxs-lookup"><span data-stu-id="30ae5-137">When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**\_Начало проверки подлинности DOT11 \_ Algo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30ae5-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11\_AUTH\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-139">Указывает начало диапазона, который указывает собственные алгоритмы проверки подлинности, разработанные IHV.</span><span class="sxs-lookup"><span data-stu-id="30ae5-139">Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="30ae5-140">Перечислитель **\_ \_ \_ \_ запуска Algo для проверки** на основе DOT11 действителен, только если драйвер минипорта работает в режиме расширяемой станции (екстста).</span><span class="sxs-lookup"><span data-stu-id="30ae5-140">The **DOT11\_AUTH\_ALGO\_IHV\_START** enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.</span></span>

</dd> <dt>

<span data-ttu-id="30ae5-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**\_Завершение проверки подлинности DOT11 \_ Algo \_ IHV \_**</span><span class="sxs-lookup"><span data-stu-id="30ae5-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11\_AUTH\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="30ae5-142">Указывает конец диапазона, который указывает собственные алгоритмы проверки подлинности, разработанные IHV.</span><span class="sxs-lookup"><span data-stu-id="30ae5-142">Indicates the end of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="30ae5-143">Перечислитель **\_ \_ \_ \_ завершения проверки подлинности DOT11 Algo** действителен только в том случае, если драйвер минипорта работает в режиме екстста.</span><span class="sxs-lookup"><span data-stu-id="30ae5-143">The **DOT11\_AUTH\_ALGO\_IHV\_END** enumerator is valid only when the miniport driver is operating in ExtSTA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30ae5-144">Требования</span><span class="sxs-lookup"><span data-stu-id="30ae5-144">Requirements</span></span>



| <span data-ttu-id="30ae5-145">Требование</span><span class="sxs-lookup"><span data-stu-id="30ae5-145">Requirement</span></span> | <span data-ttu-id="30ae5-146">Значение</span><span class="sxs-lookup"><span data-stu-id="30ae5-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ae5-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30ae5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="30ae5-148">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30ae5-148">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="30ae5-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30ae5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="30ae5-150">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30ae5-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="30ae5-151">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="30ae5-151">Redistributable</span></span><br/>          | <span data-ttu-id="30ae5-152">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="30ae5-152">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="30ae5-153">Header</span><span class="sxs-lookup"><span data-stu-id="30ae5-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="30ae5-154"><dt>Влантипес. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30ae5-154"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ae5-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30ae5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ae5-156">**\_ \_ Пара шифров для проверки подлинности DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="30ae5-156">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="30ae5-157">**\_доступная \_ сеть WLAN**</span><span class="sxs-lookup"><span data-stu-id="30ae5-157">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="30ae5-158">**\_атрибуты безопасности \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="30ae5-158">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




