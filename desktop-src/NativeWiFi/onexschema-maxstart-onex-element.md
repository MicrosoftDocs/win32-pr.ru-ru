---
description: Указывает максимальное число отправленных сообщений EAPOL-Start.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Элемент Максстарт (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7c50945b8de53b6d058556e3b5c995d3ec17bfdc8f8d55ec3dc2e6e56089b2a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800764"
---
# <a name="maxstart-onex-element"></a>Элемент Максстарт (OneX)

Элемент Максстарт (OneX) указывает максимальное число отправленных сообщений EAPOL-Start. После отправки максимального числа EAPOL-Start сообщений клиент предполагает, что в сети отсутствует средство проверки подлинности.

Этот элемент является необязательным. Если Максстарт не указан в профиле, используется значение 3 сообщения.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **максстарт** определяется элементом [**OneX**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> </dl>

 

 




