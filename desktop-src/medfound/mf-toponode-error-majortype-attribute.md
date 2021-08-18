---
description: Содержит основной тип носителя для узла топологии. Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Атрибут MF_TOPONODE_ERROR_MAJORTYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e32752f74708272c367e3f15b208ed66fb0d476baab75b8032ed028e1b9e4162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875157"
---
# <a name="mf_toponode_error_majortype-attribute"></a>\_Атрибут MF топоноде \_ Error \_ мажортипе

Содержит основной тип носителя для узла топологии. Этот атрибут задается, когда не удается загрузить топологию, так как не удалось найти правильный декодер.

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="remarks"></a>Remarks

Этот атрибут применяется ко всем типам узлов.

Загрузчик топологии может задать атрибут. Приложения обычно считывают этот атрибут, но не устанавливают его.

Список возможных значений см. в разделе [основные типы носителей](media-type-guids.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



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

 

 




