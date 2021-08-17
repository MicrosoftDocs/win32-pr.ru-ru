---
description: Указывает идентификатор поставщика сотовой сети.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: Элемент ProviderID (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: b40ac5abab2abf850d927c21f0de66ad419987f594f28dffcd380ead7f982d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959794"
---
# <a name="providerid-providertype-element"></a>Элемент ProviderID (providerType)

Элемент **ProviderID (ProviderType)** указывает идентификатор поставщика сети сотовой связи.

Элемент — это последовательность цифр, длина которой не может превышать 6 цифр.

Этот элемент необходим в элементе [**provider**](schema-provider-dataroamingpartners-element.md) .

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

Элемент **ProviderID** определяется сложным типом [**ProviderType**](schema-providertype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**providerType**](schema-providertype-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Поставщик (Датароамингпартнерс)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




