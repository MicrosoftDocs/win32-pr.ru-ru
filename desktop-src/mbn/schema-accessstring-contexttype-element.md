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
ms.openlocfilehash: 603c4aa04bb3e86891ec121233474fa96ffd792cbcb6880bad9e76599003d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975283"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Контекст (Мбнпрофиле)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




