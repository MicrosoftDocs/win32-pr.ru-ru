---
description: Указывает, будет ли подключение к беспроводной локальной сети автоматически или инициировано пользователем.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: connectionMode (Вланпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811465"
---
# <a name="connectionmode-wlanprofile-element"></a>connectionMode (Вланпрофиле), элемент

Элемент connectionMode (Вланпрофиле) указывает, будет ли подключение к беспроводной локальной сети автоматически или инициировано пользователем.

Если для параметра [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) задано значение ESS, то оно может быть либо автоматически, либо вручную. Значение по умолчанию — Auto, если этот элемент отсутствует.

Если параметр [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение ибсс, это значение должно быть задано вручную.

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **connectionMode** определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Комментарии

В следующей таблице описаны значения перечисления.



| Значение  | Описание                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | Подключение к беспроводной сети должно инициироваться автоматически, когда сеть находится в диапазоне. |
| manual | Подключение к беспроводной сети инитатед только после явного запроса пользователя.               |



 

## <a name="examples"></a>Примеры

Чтобы просмотреть образцы профилей, использующих элемент **connectionMode** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




