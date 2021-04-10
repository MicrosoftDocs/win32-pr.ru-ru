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
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135471"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Кредентиалсблоб (Еафостусеркредентиалс), элемент

Элемент **кредентиалсблоб (еафостусеркредентиалс)** используется, когда конфигурация метода является двоичным BLOB-объектом, а не в ТЕКСТОВОМ формате XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

Элемент **кредентиалсблоб** определяется элементом [**еафостусеркредентиалс**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .

## <a name="remarks"></a>Комментарии

Элементы [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) и **кредентиалсблоб** не могут одновременно использоваться одновременно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



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

 

 





