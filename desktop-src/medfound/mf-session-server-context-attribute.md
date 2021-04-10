---
description: Позволяет двум экземплярам сеанса мультимедиа совместно использовать один и тот же процесс защищенного пути к файлам мультимедиа (PMP).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Атрибут MF_SESSION_SERVER_CONTEXT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156803"
---
# <a name="mf_session_server_context-attribute"></a>\_ \_ Атрибут контекста сервера сеанса MF \_

Позволяет двум экземплярам сеанса мультимедиа совместно использовать один и тот же процесс защищенного пути к файлам мультимедиа (PMP).

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Используйте этот атрибут, если вы хотите создать сеанс мультимедиа PMP в существующем процессе PMP. Значение атрибута является указателем на интерфейс [_ *имфпмпсервер* *](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .

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

[**Имфаттрибутес:: неизвестный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**Имфаттрибутес:: Сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Атрибуты сеанса мультимедиа](media-session-attributes.md)
</dt> </dl>

 

 




