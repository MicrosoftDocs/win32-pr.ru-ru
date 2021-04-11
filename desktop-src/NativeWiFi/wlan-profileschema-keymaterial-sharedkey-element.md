---
description: Содержит ключ сети или парольную фразу.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Кэйматериал (sharedKey), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264700"
---
# <a name="keymaterial-sharedkey-element"></a><span data-ttu-id="13d2b-103">Кэйматериал (sharedKey), элемент</span><span class="sxs-lookup"><span data-stu-id="13d2b-103">keyMaterial (sharedKey) Element</span></span>

<span data-ttu-id="13d2b-104">Элемент Кэйматериал (sharedKey) содержит ключ сети или парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="13d2b-104">The keyMaterial (sharedKey) element contains a network key or passphrase.</span></span> <span data-ttu-id="13d2b-105">Если [**защищенный**](wlan-profileschema-protected-sharedkey-element.md) элемент имеет значение true, этот материал ключа шифруется; в противном случае материал ключа не шифруется.</span><span class="sxs-lookup"><span data-stu-id="13d2b-105">If the [**protected**](wlan-profileschema-protected-sharedkey-element.md) element has a value of TRUE, then this key material is encrypted; otherwise, the key material is unencrypted.</span></span> <span data-ttu-id="13d2b-106">Зашифрованный материал ключа выражается в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="13d2b-106">Encrypted key material is expressed in hexadecimal form.</span></span>

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

<span data-ttu-id="13d2b-107">Элемент определяется элементом [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="13d2b-107">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="13d2b-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13d2b-108">Remarks</span></span>

<span data-ttu-id="13d2b-109">Диапазон допустимых значений для элемента Кэйматериал зависит от типа проверки подлинности и используемого шифрования, как указано в элементах [**проверки подлинности**](wlan-profileschema-authentication-authencryption-element.md) и [**шифрования**](wlan-profileschema-encryption-authencryption-element.md) .</span><span class="sxs-lookup"><span data-stu-id="13d2b-109">The range of valid values for the keyMaterial element varies by the type of authentication and encryption used, as specified by the [**authentication**](wlan-profileschema-authentication-authencryption-element.md) and [**encryption**](wlan-profileschema-encryption-authencryption-element.md) elements.</span></span> <span data-ttu-id="13d2b-110">Он также зависит от [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md).</span><span class="sxs-lookup"><span data-stu-id="13d2b-110">It also varies by [**keyType**](wlan-profileschema-keytype-sharedkey-element.md).</span></span>

<span data-ttu-id="13d2b-111">В следующей таблице показаны допустимые значения **кэйматериал** для некоторых пар шифрования и проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="13d2b-111">The following table shows valid **keyMaterial** values for some authentication and encryption pairs.</span></span>



| <span data-ttu-id="13d2b-112">значение [**проверки подлинности**](wlan-profileschema-authentication-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="13d2b-112">[**authentication**](wlan-profileschema-authentication-authencryption-element.md) value</span></span> | <span data-ttu-id="13d2b-113">значение [**шифрования**](wlan-profileschema-encryption-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="13d2b-113">[**encryption**](wlan-profileschema-encryption-authencryption-element.md) value</span></span> | <span data-ttu-id="13d2b-114">значение [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md)</span><span class="sxs-lookup"><span data-stu-id="13d2b-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) value</span></span> | <span data-ttu-id="13d2b-115">Допустимые значения **кэйматериал**</span><span class="sxs-lookup"><span data-stu-id="13d2b-115">Valid **keyMaterial** values</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d2b-116">Открытый или общий</span><span class="sxs-lookup"><span data-stu-id="13d2b-116">open or shared</span></span>                                                                           | <span data-ttu-id="13d2b-117">WEP</span><span class="sxs-lookup"><span data-stu-id="13d2b-117">WEP</span></span>                                                                              | <span data-ttu-id="13d2b-118">нетворккэй</span><span class="sxs-lookup"><span data-stu-id="13d2b-118">networkKey</span></span>                                                            | <span data-ttu-id="13d2b-119">Этот элемент содержит WEP-ключ длиной 5 или 13 символов ANSI либо 10 или 26 шестнадцатеричных символов.</span><span class="sxs-lookup"><span data-stu-id="13d2b-119">This element contains a WEP key of 5 or 13 ANSI characters, or of 10 or 26 hexadecimal characters.</span></span>                                                                                             |
| <span data-ttu-id="13d2b-120">ВПАПСК или WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="13d2b-120">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="13d2b-121">TKIP или AES</span><span class="sxs-lookup"><span data-stu-id="13d2b-121">TKIP or AES</span></span>                                                                      | <span data-ttu-id="13d2b-122">passPhrase</span><span class="sxs-lookup"><span data-stu-id="13d2b-122">passPhrase</span></span>                                                            | <span data-ttu-id="13d2b-123">Этот элемент содержит парольную фразу от 8 до 63 символов ASCII, то есть от 8 до 63 символов ANSI в диапазоне от 32 до 126.</span><span class="sxs-lookup"><span data-stu-id="13d2b-123">This element contains a passphrase of 8 to 63 ASCII characters, that is, 8 to 63 ANSI characters in the range of 32 to 126.</span></span> <span data-ttu-id="13d2b-124">Значения ключей должны соответствовать требованиям, заданным в 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="13d2b-124">Key values must comply with the requirements specified by 802.11i.</span></span> |
| <span data-ttu-id="13d2b-125">ВПАПСК или WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="13d2b-125">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="13d2b-126">TKIP или AES</span><span class="sxs-lookup"><span data-stu-id="13d2b-126">TKIP or AES</span></span>                                                                      | <span data-ttu-id="13d2b-127">нетворккэй</span><span class="sxs-lookup"><span data-stu-id="13d2b-127">networkKey</span></span>                                                            | <span data-ttu-id="13d2b-128">Этот элемент содержит ключ 64 шестнадцатеричных символов.</span><span class="sxs-lookup"><span data-stu-id="13d2b-128">This element contains a key of 64 hexadecimal characters.</span></span>                                                                                                                                      |



 

<span data-ttu-id="13d2b-129">Символы Юникода могут быть введены, где указаны символы ANSI или ASCII, указанные выше.</span><span class="sxs-lookup"><span data-stu-id="13d2b-129">Unicode characters may be entered where ANSI or ASCII characters are specified above.</span></span> <span data-ttu-id="13d2b-130">Однако если указанные символы Юникода не могут быть сопоставлены с символами ANSI или ASCII, указанный материал ключа отклоняется.</span><span class="sxs-lookup"><span data-stu-id="13d2b-130">However, if the supplied Unicode characters cannot be mapped to ANSI or ASCII characters, then the supplied key material is rejected.</span></span>

<span data-ttu-id="13d2b-131">Материал ключа, возвращенный [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) , всегда шифруется.</span><span class="sxs-lookup"><span data-stu-id="13d2b-131">Key material returned by [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) is always encrypted.</span></span> <span data-ttu-id="13d2b-132">Кроме того, если незашифрованный материал ключа передается в [**влансетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), материал ключа автоматически шифруется перед сохранением в хранилище профилей.</span><span class="sxs-lookup"><span data-stu-id="13d2b-132">Also, if unencrypted key material is passed to [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), the key material is automatically encrypted before it is stored in the profile store.</span></span>

<span data-ttu-id="13d2b-133">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Материал ключа никогда не шифруется.</span><span class="sxs-lookup"><span data-stu-id="13d2b-133">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The key material is never encrypted.</span></span>

<span data-ttu-id="13d2b-134">Если процесс выполняется в контексте учетной записи LocalSystem, то можно отшифровать материал ключа, вызвав [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="13d2b-134">If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span>

## <a name="examples"></a><span data-ttu-id="13d2b-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="13d2b-135">Examples</span></span>

<span data-ttu-id="13d2b-136">Для просмотра образцов профилей, использующих элемент **кэйматериал** , см. пример [профиля без широковещательной рассылки](non-broadcast-profile-sample.md), [пример профиля WPA-личное](wpa-personal-profile-sample.md)и [профиль WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="13d2b-136">To view sample profiles that use the **keyMaterial** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13d2b-137">Требования</span><span class="sxs-lookup"><span data-stu-id="13d2b-137">Requirements</span></span>



| <span data-ttu-id="13d2b-138">Требование</span><span class="sxs-lookup"><span data-stu-id="13d2b-138">Requirement</span></span> | <span data-ttu-id="13d2b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="13d2b-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="13d2b-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13d2b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="13d2b-141">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13d2b-141">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="13d2b-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13d2b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="13d2b-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13d2b-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="13d2b-144">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="13d2b-144">Redistributable</span></span><br/>          | <span data-ttu-id="13d2b-145">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="13d2b-145">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="13d2b-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13d2b-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="13d2b-147">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="13d2b-147">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="13d2b-148">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="13d2b-148">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="13d2b-149">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="13d2b-149">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="13d2b-150">**sharedKey (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="13d2b-150">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
