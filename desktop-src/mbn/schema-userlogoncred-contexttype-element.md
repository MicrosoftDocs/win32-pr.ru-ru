---
description: Содержит учетные данные входа для подключения.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Усерлогонкред (contextType), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145622"
---
# <a name="userlogoncred-contexttype-element"></a>Усерлогонкред (contextType), элемент

Элемент **усерлогонкред (ContextType)** содержит учетные данные входа для подключения.

Этот элемент может иметь следующие дочерние элементы.

-   [**Имен**](schema-username-userlogoncred-element.md)
-   [**Пароль**](schema-password-userlogoncred-element.md)
-   [**игнорепассворд**](schema-ignorepassword-userlogoncred-element.md)

Этот элемент может иметь максимум одно вхождение.

Этот элемент является необязательным.

``` syntax
<xs:element name="UserLogonCred">
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
```

Элемент **усерлогонкред** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Тип                                           | Описание                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [**игнорепассворд**](schema-ignorepassword-userlogoncred-element.md) | Логическое                                        | Как работать с паролями при обновлении профилей.<br/> |
| [**Пароль**](schema-password-userlogoncred-element.md)             | строка                                         | Пароль пользователя.<br/>                                   |
| [**Имен**](schema-username-userlogoncred-element.md)             | [**наметипе**](schema-nametype-simpletype.md) | Имя пользователя.<br/>                                       |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Контекст (Мбнпрофиле)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




