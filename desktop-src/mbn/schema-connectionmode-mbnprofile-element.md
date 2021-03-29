---
description: Задает параметр автоматического подключения, используемый для устройства мобильной широкополосной связи.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: ConnectionMode (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991096"
---
# <a name="connectionmode-mbnprofile-element"></a>ConnectionMode (Мбнпрофиле), элемент

Элемент **ConnectionMode (мбнпрофиле)** задает параметр автоматического подключения, который будет использоваться для устройства мобильной широкополосной связи.

Этот элемент может иметь одно из следующих значений.



| Значение       | Значение                                                                |
|-------------|------------------------------------------------------------------------|
| документации    | Никогда не подключайтесь к сети автоматически.                            |
| Выбор      | Всегда автоматически подключаться к сети.                           |
| "Авто-Домашняя" | Автоматически подключаться к сети, кроме случаев, когда в роуминге сеть. |



 

Этот элемент может иметь максимум одно вхождение.

Этот обязательный элемент.

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **ConnectionMode** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




