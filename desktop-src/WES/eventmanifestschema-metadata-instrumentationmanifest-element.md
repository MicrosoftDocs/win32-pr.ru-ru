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
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135166"
---
# <a name="metadata-instrumentationmanifest-element"></a>Элемент Metadata (Инструментатионманифест)

Содержит глобальные значения, на которые можно ссылаться в других манифестах. Пример см. в файле Winmeta.xml, включенном в \\ папку Include Windows SDK.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

Элемент **метаданных** определяется элементом [**инструментатионманифест**](eventmanifestschema-instrumentationmanifest-element.md) .

## <a name="remarks"></a>Комментарии

Несмотря на то, что можно создать манифест, содержащий раздел метаданных, служба не будет использовать ее. единственными метаданными, распознаваемыми службой, являются метаданные, найденные в файле Winmeta.xml.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**инструментатионманифест**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





