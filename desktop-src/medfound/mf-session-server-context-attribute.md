---
description: Позволяет двум экземплярам сеанса мультимедиа совместно использовать один и тот же процесс защищенного пути к файлам мультимедиа (PMP).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Атрибут MF_SESSION_SERVER_CONTEXT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9674a2e25a7cdfd0a88ebcc43c18d6fd636bf22116f76a24255b55f857a677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102340"
---
# <a name="mf_session_server_context-attribute"></a>\_ \_ Атрибут контекста сервера сеанса MF \_

Позволяет двум экземплярам сеанса мультимедиа совместно использовать один и тот же процесс защищенного пути к файлам мультимедиа (PMP).

## <a name="data-type"></a>Тип данных

**IUnknown\***

## <a name="remarks"></a>Remarks

Используйте этот атрибут, если вы хотите создать сеанс мультимедиа PMP в существующем процессе PMP. Значение атрибута является указателем на интерфейс [**имфпмпсервер**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: неизвестный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**Имфаттрибутес:: Сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Атрибуты сеанса мультимедиа](media-session-attributes.md)
</dt> </dl>

 

 




