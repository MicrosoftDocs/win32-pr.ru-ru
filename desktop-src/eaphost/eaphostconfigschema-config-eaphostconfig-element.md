---
title: Config (Еафостконфиг), элемент
description: Используется, когда конфигурация метода находится в текстовом формате XML вместо двоичного BLOB-объекта.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Элемент конфигурации EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba798afaa418e5de49c48abdc8dac242a300a7228ffe27a76241f4cbabed5833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739084"
---
# <a name="config-eaphostconfig-element"></a>Config (Еафостконфиг), элемент

Элемент **config (еафостконфиг)** используется, когда конфигурация метода находится в текстовой XML-форме вместо двоичного BLOB.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

Элемент **config** определяется элементом [**еафостконфиг**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Remarks

Элементы **config** и [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) не могут одновременно использоваться одновременно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

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

 

 





