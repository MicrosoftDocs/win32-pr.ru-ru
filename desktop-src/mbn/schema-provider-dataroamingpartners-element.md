---
description: Определяет имя и идентификатор поставщика для сети сотовой связи.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Элемент Provider (Датароамингпартнерс)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: d5ce12ddf15ad57071f2717e5801fbd05f8e2925ea474345f7c376bc2445cd02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347164"
---
# <a name="provider-dataroamingpartners-element"></a>Элемент Provider (Датароамингпартнерс)

Элемент **provider (датароамингпартнерс)** определяет имя и идентификатор поставщика для сети сотовой связи.

Этот элемент содержит следующие дочерние элементы.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Этот элемент может быть определен несколько раз в элементе [**датароамингпартнерс**](schema-dataroamingpartners-mbnprofile-element.md) . Его необходимо определить по крайней мере один раз.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

Элемент **provider** определяется элементом [**датароамингпартнерс**](schema-dataroamingpartners-mbnprofile-element.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Датароамингпартнерс (Мбнпрофиле)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




