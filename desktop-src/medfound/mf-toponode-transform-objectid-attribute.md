---
description: Идентификатор класса (CLSID) преобразования Media Foundation (MFT), связанного с этим узлом топологии.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Атрибут MF_TOPONODE_TRANSFORM_OBJECTID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543250"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>\_ \_ Атрибут ObjectID преобразования топоноде MF \_

Идентификатор класса (CLSID) преобразования Media Foundation (MFT), связанного с этим узлом топологии.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к узлам преобразования (**\_ \_ \_ узел преобразования топологии MF**).

Приложения могут использовать этот атрибут для инициализации узла, производного от. Если задать этот атрибут, не нужно вызывать [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) с указателем на таблицу MFT или объект активации. И наоборот, при вызове **setObject** не нужно задавать этот атрибут. Дополнительные сведения см. в разделе [Создание топологий](creating-topologies.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

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

 

 




