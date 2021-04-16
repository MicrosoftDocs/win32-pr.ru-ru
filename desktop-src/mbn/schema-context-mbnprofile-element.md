---
description: Задает параметры, необходимые для настройки подключения к данным.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Элемент context (Мбнпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692464"
---
# <a name="context-mbnprofile-element"></a>Элемент context (Мбнпрофиле)

Элемент **context (мбнпрофиле)** задает параметры, необходимые для настройки подключения к данным.

Элемент может иметь следующие дочерние элементы.

-   [**AccessString**](schema-accessstring-contexttype-element.md)
-   [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
-   [**Сжатие**](schema-compression-contexttype-element.md)
-   [**AuthProtocol**](schema-authprotocol-contexttype-element.md)

Этот элемент может иметь максимум одно вхождение.

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

Элемент **context** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

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

 

 




