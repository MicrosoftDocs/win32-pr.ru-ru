---
description: Предоставляет интерфейс обратного вызова, который приложение получает объект средства включения содержимого из сеанса защищенного пути к носителю (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Атрибут MF_SESSION_CONTENT_PROTECTION_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712397"
---
# <a name="mf_session_content_protection_manager-attribute"></a>\_ \_ \_ Атрибут диспетчера защиты содержимого сеанса MF \_

Предоставляет интерфейс обратного вызова, который приложение получает объект средства включения содержимого из сеанса защищенного пути к носителю (PMP).

## <a name="data-type"></a>Тип данных

**IUnknown \** _

## <a name="remarks"></a>Комментарии

Значение этого атрибута является указателем на интерфейс [_ *имфконтентпротектионманажер* *](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) приложения.

Установите этот атрибут в сеансе PMP с помощью параметра *пконфигуратион* функции [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

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
</dt> <dt>

[Воспроизведение защищенных файлов мультимедиа](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




