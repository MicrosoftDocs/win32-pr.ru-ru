---
description: Указывает контекст конненктион мобильного широкополосного устройства.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: Сложный тип contextType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 58189cf27f667b3d7e5e6c387a52143b8c757724106e8d9941d31d2582002b0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744451"
---
# <a name="contexttype-complex-type"></a>Сложный тип contextType

Сложный тип **ContextType** указывает контекст Конненктион мобильного широкополосного устройства.

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Тип                                           | Описание                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**AccessString**](schema-accessstring-contexttype-element.md)       |                                                | Имя точки доступа или строка вызова, используемые для установки подключения к данным<br/>                        |
| [**AuthProtocol**](schema-authprotocol-contexttype-element.md)       |                                                | Протокол проверки подлинности, используемый для активации контекста PDP.<br/>                    |
| [**Компакт**](schema-compression-contexttype-element.md)         |                                                | Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных<br/> |
| [**игнорепассворд**](schema-ignorepassword-userlogoncred-element.md) | Логическое                                        | Как работать с паролями при обновлении профилей.<br/>                                    |
| [**Пароль**](schema-password-userlogoncred-element.md)             | строка                                         | Пароль, используемый для проверки подлинности пользователя<br/>                                                |
| [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)     |                                                | Учетные данные входа для подключения.<br/>                                                |
| [**Имен**](schema-username-userlogoncred-element.md)             | [**наметипе**](schema-nametype-simpletype.md) | Имя пользователя для входа<br/>                                                                 |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




