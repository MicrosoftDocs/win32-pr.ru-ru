---
title: Конфигблоб (Еафостконфиг), элемент
description: Используется, когда конфигурация метода находится в двоичном виде двоичного объекта, а не в виде текстовой строки.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Элемент Конфигблоб EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f0d3b928ebc6cd24a6d7102ea37a8d0ae980c54499f568d25ca224b1121a20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021644"
---
# <a name="configblob-eaphostconfig-element"></a>Конфигблоб (Еафостконфиг), элемент

Элемент **конфигблоб (еафостконфиг)** используется, когда конфигурация метода находится в двоичном виде ДВОИЧного объекта, а не в виде текстовой строки.

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

Элемент **конфигблоб** определяется элементом [**еафостконфиг**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Remarks

Элементы [**config**](eaphostconfigschema-config-eaphostconfig-element.md) и **конфигблоб** не могут одновременно использоваться одновременно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**еафостконфиг**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**еафостконфиг**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема еафостконфиг](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





