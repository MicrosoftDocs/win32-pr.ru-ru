---
description: Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Элемент Compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897530"
---
# <a name="compression-contexttype-element"></a>Элемент Compression (contextType)

Элемент **Compression (ContextType)** указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.

Этот элемент может иметь одно из следующих значений.

| Значение     | Значение                       |
|-----------|-------------------------------|
| ПАРАМЕТР  | Будет использоваться сжатие.     |
| ВКЛЮЧЕН | Сжатие не будет использоваться. |



 

Этот элемент является необязательным. Если этот элемент не указан, то система мобильной широкополосной связи не будет использовать сжатие.

``` syntax
<xs:element name="Compression">
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
```

Элемент **Compression** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .

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

 

 




