---
description: Указывает, включен ли режим федеральной информационной обработки (FIPS).
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Фипсмоде (Аусенкриптион), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810378"
---
# <a name="fipsmode-authencryption-element"></a>Фипсмоде (Аусенкриптион), элемент

Элемент **фипсмоде** (аусенкриптион) указывает, включен ли режим федеральной информационной обработки (FIPS). Если беспроводное подключение работает в режиме FIPS, уровень безопасности подключения соответствует стандарту FIPS 140-2. Дополнительные сведения о FIPS см. на [домашней странице FIPS](https://www.itl.nist.gov/fipspubs/).

Этот элемент является необязательным. Если этот элемент не указан в профиле, то режим FIPS не включен.

**Фипсмоде** может иметь значение true только при соблюдении следующих условий.

-   Элемент [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение `ESS` (то есть соединение является подключением инфраструктуры).
-   Элемент [**authentication**](wlan-profileschema-authentication-authencryption-element.md) имеет значение `WPA2` или `WPA2PSK` .
-   Элемент [**ENCRYPTION**](wlan-profileschema-encryption-authencryption-element.md) имеет значение `AES` .

В отличие от большинства элементов в \_ схеме профиля WLAN этот элемент находится в `https://www.microsoft.com/networking/WLAN/profile/v2` пространстве имен.

Значение элемента **фипсмоде** игнорируется, если драйвер минипорта для беспроводного интерфейса не поддерживает режим FIPS.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается. Если **фипсмоде** есть в профиле, элемент игнорируется.

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Комментарии

Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** . Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="examples"></a>Примеры

Пример профиля, в котором используется элемент **фипсмоде** , см. в разделе [пример профиля FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Аусенкриптион (безопасность)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
