---
title: Кредентиалсблоб (Еафостусеркредентиалс), элемент
description: Используется, когда конфигурация метода является двоичным BLOB-объектом, а не в текстовом формате XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Элемент Кредентиалсблоб EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e56fe90677d0988420a97510da75ea24bf9d50610f9b0b06555a127ef5f731c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274478"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Кредентиалсблоб (Еафостусеркредентиалс), элемент

Элемент **кредентиалсблоб (еафостусеркредентиалс)** используется, когда конфигурация метода является двоичным BLOB-объектом, а не в ТЕКСТОВОМ формате XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

Элемент **кредентиалсблоб** определяется элементом [**еафостусеркредентиалс**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .

## <a name="remarks"></a>Remarks

Элементы [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) и **кредентиалсблоб** не могут одновременно использоваться одновременно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еафостусеркредентиалс**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еафостусеркредентиалс**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема еафостусеркредентиалс](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





