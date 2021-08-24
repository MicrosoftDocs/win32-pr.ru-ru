---
description: Указывает максимальное количество ошибок проверки подлинности, разрешенных для набора учетных данных.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Элемент Максаусфаилурес (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9cb48479b2fe26ecb2667812cc6ee2048226c0665c25b12e25e8c7edbc35dac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800784"
---
# <a name="maxauthfailures-onex-element"></a>Элемент Максаусфаилурес (OneX)

Элемент Максаусфаилурес (OneX) указывает максимальное количество ошибок проверки подлинности, разрешенных для набора учетных данных.

Этот элемент является необязательным. Если Максаусфаилурес не указан в профиле, используется значение, равное единице.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.

``` syntax
<xs:element name="maxAuthFailures">
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

Элемент **максаусфаилурес** определяется элементом [**OneX**](onexschema-onex-element.md) .

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

 

 




