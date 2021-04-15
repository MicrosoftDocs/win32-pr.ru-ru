---
description: Определяет имя APN или строку вызова, используемые для установки подключения к данным.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Акцессстринг (contextType), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682744"
---
# <a name="accessstring-contexttype-element"></a>Акцессстринг (contextType), элемент

Элемент **акцессстринг (ContextType)** определяет имя APN или строку вызова для использования при установлении подключения к данным.

Длина этого элемента не может превышать 100 символов.

Этот элемент является необязательным.

``` syntax
<xs:element name="AccessString">
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
```

Элемент **акцессстринг** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .

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

 

 




