---
title: Элемент Metadata (Инструментатионманифест)
description: Содержит глобальные значения, на которые можно ссылаться в других манифестах.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- Журнал событий элемента метаданных
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eaa22cc13c611b90ace42a2a71517fe0771d6e9ed03d6d964f11a4e4c93cda43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136327"
---
# <a name="metadata-instrumentationmanifest-element"></a>Элемент Metadata (Инструментатионманифест)

Содержит глобальные значения, на которые можно ссылаться в других манифестах. пример см. в файле Winmeta.xml, включенном в \\ папку Include Windows SDK.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

Элемент **метаданных** определяется элементом [**инструментатионманифест**](eventmanifestschema-instrumentationmanifest-element.md) .

## <a name="remarks"></a>Remarks

Несмотря на то, что можно создать манифест, содержащий раздел метаданных, служба не будет использовать ее. единственными метаданными, распознаваемыми службой, являются метаданные, найденные в файле Winmeta.xml.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**инструментатионманифест**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





