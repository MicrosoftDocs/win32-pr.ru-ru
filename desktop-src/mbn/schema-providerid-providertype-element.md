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
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263176"
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
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
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

 

 




