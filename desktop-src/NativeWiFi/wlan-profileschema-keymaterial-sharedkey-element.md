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
# <a name="keymaterial-sharedkey-element"></a>Кэйматериал (sharedKey), элемент

Элемент Кэйматериал (sharedKey) содержит ключ сети или парольную фразу. Если [**защищенный**](wlan-profileschema-protected-sharedkey-element.md) элемент имеет значение true, этот материал ключа шифруется; в противном случае материал ключа не шифруется. Зашифрованный материал ключа выражается в шестнадцатеричном формате.

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

Элемент определяется элементом [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Комментарии

Диапазон допустимых значений для элемента Кэйматериал зависит от типа проверки подлинности и используемого шифрования, как указано в элементах [**проверки подлинности**](wlan-profileschema-authentication-authencryption-element.md) и [**шифрования**](wlan-profileschema-encryption-authencryption-element.md) . Он также зависит от [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md).

В следующей таблице показаны допустимые значения **кэйматериал** для некоторых пар шифрования и проверки подлинности.



| значение [**проверки подлинности**](wlan-profileschema-authentication-authencryption-element.md) | значение [**шифрования**](wlan-profileschema-encryption-authencryption-element.md) | значение [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) | Допустимые значения **кэйматериал**                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Открытый или общий                                                                           | WEP                                                                              | нетворккэй                                                            | Этот элемент содержит WEP-ключ длиной 5 или 13 символов ANSI либо 10 или 26 шестнадцатеричных символов.                                                                                             |
| ВПАПСК или WPA2PSK                                                                        | TKIP или AES                                                                      | passPhrase                                                            | Этот элемент содержит парольную фразу от 8 до 63 символов ASCII, то есть от 8 до 63 символов ANSI в диапазоне от 32 до 126. Значения ключей должны соответствовать требованиям, заданным в 802.11 i. |
| ВПАПСК или WPA2PSK                                                                        | TKIP или AES                                                                      | нетворккэй                                                            | Этот элемент содержит ключ 64 шестнадцатеричных символов.                                                                                                                                      |



 

Символы Юникода могут быть введены, где указаны символы ANSI или ASCII, указанные выше. Однако если указанные символы Юникода не могут быть сопоставлены с символами ANSI или ASCII, указанный материал ключа отклоняется.

Материал ключа, возвращенный [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) , всегда шифруется. Кроме того, если незашифрованный материал ключа передается в [**влансетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), материал ключа автоматически шифруется перед сохранением в хранилище профилей.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Материал ключа никогда не шифруется.

Если процесс выполняется в контексте учетной записи LocalSystem, то можно отшифровать материал ключа, вызвав [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).

## <a name="examples"></a>Примеры

Для просмотра образцов профилей, использующих элемент **кэйматериал** , см. пример [профиля без широковещательной рассылки](non-broadcast-profile-sample.md), [пример профиля WPA-личное](wpa-personal-profile-sample.md)и [профиль WPA2-Personal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                |
| Распространяемые компоненты<br/>          | Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**sharedKey (безопасность)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
