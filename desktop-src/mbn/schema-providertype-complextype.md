---
description: Указывает сведения о сети сотовой связи.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Сложный тип providerType (мобильное широкополосное подключение)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: eb62fbb55f83d004f70093fbde974f8ab08e6367742f34dbf166d1c25a63b28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975063"
---
# <a name="providertype-complex-type"></a>Сложный тип providerType

Сложный тип **ProviderType** указывает сведения о сети сотовой связи.

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                          | Тип                                                           | Описание               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [**ProviderID**](schema-providerid-providertype-element.md)     | [**провидеридтипе**](schema-provideridtype-simpletype.md)     | Идентификатор поставщика.<br/>   |
| [**ProviderName**](schema-providername-providertype-element.md) | [**провидернаметипе**](schema-providernametype-simpletype.md) | Имя поставщика.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



 

 




