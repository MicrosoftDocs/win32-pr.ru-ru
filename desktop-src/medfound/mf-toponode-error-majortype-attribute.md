---
description: Содержит основной тип носителя для узла топологии. Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Атрибут MF_TOPONODE_ERROR_MAJORTYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711294"
---
# <a name="mf_toponode_error_majortype-attribute"></a>\_Атрибут MF топоноде \_ Error \_ мажортипе

Содержит основной тип носителя для узла топологии. Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Комментарии

Этот атрибут применяется ко всем типам узлов.

Загрузчик топологии может задать атрибут. Приложения обычно считывают этот атрибут, но не устанавливают его.

Список возможных значений см. в разделе [основные типы носителей](media-type-guids.md).

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

 

 




