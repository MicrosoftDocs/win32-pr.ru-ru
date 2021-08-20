---
description: Указывает, следует ли подключаться к скрытой сети.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: нешироковещательный элемент (Ссидконфиг)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 565c0f86bf806c6fed35887116055b31d855be388855f1a7fb59536d915c554b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797962"
---
# <a name="nonbroadcast-ssidconfig-element"></a>нешироковещательный элемент (Ссидконфиг)

Элемент нешироковещательной рассылки (Ссидконфиг) указывает, следует ли подключиться к скрытой сети. Если сеть не выполняет широковещательную рассылку своего идентификатора SSID, она называется скрытой сетью. Если в профиле задано несколько идентификаторов SSID, все они должны иметь одинаковое нешироковещательное значение.

Если параметру [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) присвоено значение **ESS**, это может быть либо "true", либо "false". Если этот элемент отсутствует, по умолчанию используется значение false.

Если параметр [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение **ибсс**, это значение должно быть равно "false". Если этот элемент отсутствует, по умолчанию используется значение false.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

Элемент определяется элементом [**ссидконфиг**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="examples"></a>Примеры

Пример профиля, в котором используется элемент **нешироковещательной рассылки** , см. в разделе [пример профиля без широковещательной рассылки](non-broadcast-profile-sample.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Ссидконфиг (Вланпрофиле)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




