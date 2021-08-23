---
description: Указывает период времени в секундах, в течение которого клиент не будет повторно пытаться пройти проверку подлинности после неудачной попытки проверки подлинности.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Элемент Хелдпериод (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5a2009ac8518d114353e3323b97c4ea57c54fc801447c375641b8f6bbd1b2bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684855"
---
# <a name="heldperiod-onex-element"></a>Элемент Хелдпериод (OneX)

Элемент Хелдпериод (OneX) указывает продолжительность времени в секундах, в течение которого клиент не будет повторно пытаться пройти проверку подлинности после неудачной попытки проверки подлинности.

Этот элемент является необязательным. Если Хелдпериод не указан в профиле, используется значение, равное 1 секунде.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Элемент **хелдпериод** определяется элементом [**OneX**](onexschema-onex-element.md) .

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

 

 




