---
description: Указывает, зашифрован ли общий ключ.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: protected (sharedKey), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673237"
---
# <a name="protected-sharedkey-element"></a>protected (sharedKey), элемент

Защищенный элемент (sharedKey) указывает, зашифрован ли общий ключ.

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

Элемент определяется элементом [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Комментарии

Для Windows Vista и Windows Server 2008 параметр **protected** всегда имеет значение true, если профиль был получен из хранилища профилей (например, путем вызова [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).

Для профилей, предназначенных для использования в Windows XP с пакетом обновления 3 (SP3) или API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2), **Защита** должна иметь значение false.

## <a name="examples"></a>Примеры

Для просмотра образцов профилей, использующих **защищенный** элемент, см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).

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

 

 




