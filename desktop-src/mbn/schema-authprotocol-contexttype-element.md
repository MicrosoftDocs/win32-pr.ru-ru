---
description: Указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Ауспротокол (contextType), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 65b944b2966c9b5cac307f6f8efe6af2f42a1ffa5b4f2f400074caa0efe9f84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975263"
---
# <a name="authprotocol-contexttype-element"></a>Ауспротокол (contextType), элемент

Элемент **ауспротокол (ContextType)** указывает протокол проверки подлинности, используемый для активации контекста протокола данных пакетов (PDP).

Элемент может иметь одно из следующих значений.

| Значение      | Значение                                                                 |
|------------|-------------------------------------------------------------------------|
| None     | Без протокола проверки подлинности.                                             |
| PAP      | Проверка подлинности без шифрования пароля.                                    |
| ПРОТОКОЛА     | Протокол проверки пароля (CHAP).                      |
|  MsCHAPV2 | Используйте протокол проверки пароля (CHAP) версии 2.0 (Microsoft s). |



 

Этот элемент является необязательным и используется только для профилей GSM. Если элемент не указан и профиль предназначен для устройства GSM, то служба мобильной широкополосной связи будет использовать **"нет"**.

``` syntax
<xs:element name="AuthProtocol">
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
```

Элемент **ауспротокол** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .

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

 

 




