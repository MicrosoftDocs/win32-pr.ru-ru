---
description: Идентификатор класса (CLSID) преобразования Media Foundation (MFT), связанного с этим узлом топологии.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Атрибут MF_TOPONODE_TRANSFORM_OBJECTID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b5013bc43f07e08e1a2c26530e9325595e62666986516029ef9d76e2c72ffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244318"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>\_ \_ Атрибут ObjectID преобразования топоноде MF \_

Идентификатор класса (CLSID) преобразования Media Foundation (MFT), связанного с этим узлом топологии.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к узлам преобразования (**\_ \_ \_ узел преобразования топологии MF**).

Приложения могут использовать этот атрибут для инициализации узла, производного от. Если задать этот атрибут, не нужно вызывать [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) с указателем на таблицу MFT или объект активации. И наоборот, при вызове **setObject** не нужно задавать этот атрибут. Дополнительные сведения см. в разделе [Создание топологий](creating-topologies.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: a GUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Имфаттрибутес:: Сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Создание топологий](creating-topologies.md)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




