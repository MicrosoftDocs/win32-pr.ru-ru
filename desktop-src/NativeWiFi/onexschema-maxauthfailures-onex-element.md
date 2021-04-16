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
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545399"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Таймаут**](onexschema-onex-element.md)
</dt> </dl>

 

 




