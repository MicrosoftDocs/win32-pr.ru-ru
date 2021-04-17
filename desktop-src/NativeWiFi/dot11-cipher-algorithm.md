---
description: Определяет алгоритм шифра для шифрования и расшифровки данных.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Перечисление DOT11_CIPHER_ALGORITHM (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673921"
---
# <a name="dot11_cipher_algorithm-enumeration"></a><span data-ttu-id="317a8-103">\_ \_ Перечисление алгоритма шифрования DOT11</span><span class="sxs-lookup"><span data-stu-id="317a8-103">DOT11\_CIPHER\_ALGORITHM enumeration</span></span>

<span data-ttu-id="317a8-104">Перечисляемый тип **\_ \_ алгоритма шифра DOT11** определяет алгоритм шифра для шифрования и расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="317a8-104">The **DOT11\_CIPHER\_ALGORITHM** enumerated type defines a cipher algorithm for data encryption and decryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="317a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="317a8-105">Syntax</span></span>


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="317a8-106">Константы</span><span class="sxs-lookup"><span data-stu-id="317a8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="317a8-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Algo шифра DOT11 \_ \_ нет**</span><span class="sxs-lookup"><span data-stu-id="317a8-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11\_CIPHER\_ALGO\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-108">Указывает, что алгоритм шифра не включен или не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="317a8-108">Specifies that no cipher algorithm is enabled or supported.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**\_Algo шифра DOT11 \_ \_ WEP40**</span><span class="sxs-lookup"><span data-stu-id="317a8-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11\_CIPHER\_ALGO\_WEP40**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-110">Задает алгоритм, основанный на протоколе WEP, который является алгоритмом на основе RC4, указанным в стандарте 802.11-1999.</span><span class="sxs-lookup"><span data-stu-id="317a8-110">Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.</span></span> <span data-ttu-id="317a8-111">Этот перечислитель задает алгоритм шифра WEP с 40-битным ключом шифрования.</span><span class="sxs-lookup"><span data-stu-id="317a8-111">This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Шифрование DOT11 \_ Algo \_ TKIP**</span><span class="sxs-lookup"><span data-stu-id="317a8-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11\_CIPHER\_ALGO\_TKIP**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-113">Указывает алгоритм TKIP, который является комплектом шифров на основе RC4, основанным на алгоритмах, определенных в спецификации WPA и стандарте IEEE 802.11 i-2004 Standard.</span><span class="sxs-lookup"><span data-stu-id="317a8-113">Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard.</span></span> <span data-ttu-id="317a8-114">Этот шифр также использует алгоритм MIC (код целостности сообщений) для защиты от подделки.</span><span class="sxs-lookup"><span data-stu-id="317a8-114">This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Шифрование DOT11 \_ Algo \_ CCMP**</span><span class="sxs-lookup"><span data-stu-id="317a8-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11\_CIPHER\_ALGO\_CCMP**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-116">Указывает алгоритм AES-CCMP, как указано в стандарте IEEE 802.11 i-2004 Standard и RFC 3610.</span><span class="sxs-lookup"><span data-stu-id="317a8-116">Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610.</span></span> <span data-ttu-id="317a8-117">AES (AES) — алгоритм шифрования, определенный в FIPS PUB 197.</span><span class="sxs-lookup"><span data-stu-id="317a8-117">Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**\_Algo шифра DOT11 \_ \_ WEP104**</span><span class="sxs-lookup"><span data-stu-id="317a8-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11\_CIPHER\_ALGO\_WEP104**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-119">Задает алгоритм шифра WEP с 104-битным ключом шифрования.</span><span class="sxs-lookup"><span data-stu-id="317a8-119">Specifies a WEP cipher algorithm with a 104-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Группа шифрования DOT11 \_ Algo \_ WPA \_ USE \_**</span><span class="sxs-lookup"><span data-stu-id="317a8-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11\_CIPHER\_ALGO\_WPA\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-121">Указывает Wi-Fi защищенный доступ (WPA) использование набора шифров группового ключа.</span><span class="sxs-lookup"><span data-stu-id="317a8-121">Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite.</span></span> <span data-ttu-id="317a8-122">Дополнительные сведения об использовании набора шифров групповых ключей см. в предложении 7.3.2.25.1 стандарта IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="317a8-122">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Группа шифрования DOT11 \_ Algo \_ RSN \_ USE \_**</span><span class="sxs-lookup"><span data-stu-id="317a8-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11\_CIPHER\_ALGO\_RSN\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-124">Указывает надежную сеть безопасности (RSN) использовать набор шифров группового ключа.</span><span class="sxs-lookup"><span data-stu-id="317a8-124">Specifies a Robust Security Network (RSN) Use Group Key cipher suite.</span></span> <span data-ttu-id="317a8-125">Дополнительные сведения об использовании набора шифров групповых ключей см. в предложении 7.3.2.25.1 стандарта IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="317a8-125">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_Шифрование DOT11 \_ Algo \_ WEP**</span><span class="sxs-lookup"><span data-stu-id="317a8-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11\_CIPHER\_ALGO\_WEP**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-127">Задает алгоритм шифра WEP с ключом шифра любой длины.</span><span class="sxs-lookup"><span data-stu-id="317a8-127">Specifies a WEP cipher algorithm with a cipher key of any length.</span></span>

</dd> <dt>

<span data-ttu-id="317a8-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_ \_ \_ Запуск Algo IHV \_ для шифра DOT11**</span><span class="sxs-lookup"><span data-stu-id="317a8-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11\_CIPHER\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-129">Указывает начало диапазона, используемого для определения собственных алгоритмов шифра, разработанных независимым поставщиком оборудования (IHV).</span><span class="sxs-lookup"><span data-stu-id="317a8-129">Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="317a8-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_ \_ \_ Окончание IHV Algo для шифра DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="317a8-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11\_CIPHER\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="317a8-131">Задает конец диапазона, который используется для определения собственных алгоритмов шифра, разработанных независимо от поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="317a8-131">Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="317a8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="317a8-132">Requirements</span></span>



| <span data-ttu-id="317a8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="317a8-133">Requirement</span></span> | <span data-ttu-id="317a8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="317a8-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="317a8-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="317a8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="317a8-136">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="317a8-136">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="317a8-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="317a8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="317a8-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="317a8-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="317a8-139">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="317a8-139">Redistributable</span></span><br/>          | <span data-ttu-id="317a8-140">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="317a8-140">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="317a8-141">Header</span><span class="sxs-lookup"><span data-stu-id="317a8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="317a8-142"><dt>Влантипес. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="317a8-142"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="317a8-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="317a8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317a8-144">**\_ \_ Пара шифров для проверки подлинности DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="317a8-144">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="317a8-145">**\_доступная \_ сеть WLAN**</span><span class="sxs-lookup"><span data-stu-id="317a8-145">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="317a8-146">**\_атрибуты безопасности \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="317a8-146">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




