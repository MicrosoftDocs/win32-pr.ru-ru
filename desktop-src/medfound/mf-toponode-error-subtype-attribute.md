---
description: Содержит подтип носителя для узла топологии. Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: Атрибут MF_TOPONODE_ERROR_SUBTYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711293"
---
# <a name="mf_toponode_error_subtype-attribute"></a>\_ \_ \_ Атрибут подтипа MF топоноде Error

Содержит подтип носителя для узла топологии. Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется ко всем типам узлов.

Загрузчик топологии может задать атрибут. Приложения обычно считывают этот атрибут, но не устанавливают его.

Список возможных значений см. в разделе [идентификаторы GUID типа носителя](media-type-guids.md).

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

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




