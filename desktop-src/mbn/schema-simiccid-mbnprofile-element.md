---
description: Определяет идентификационный номер SIM-карты для устройств GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: СимикЦид (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: 8a6e4a20d93396337e2af0f0533486618dc707760f1ccd5c4f20f399cbdbf203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777864"
---
# <a name="simiccid-mbnprofile-element"></a>СимикЦид (Мбнпрофиле), элемент

Элемент **симикЦид (мбнпрофиле)** определяет идентификационный номер SIM-карты для устройств GSM.

Этот элемент является необязательным и задается службой мобильного широкополосного подключения для внутреннего использования. Приложение не должно задавать это поле при создании или обновлении профиля.

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

Элемент **симикЦид** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
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

 

 




