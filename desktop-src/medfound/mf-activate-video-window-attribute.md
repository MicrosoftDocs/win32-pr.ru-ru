---
description: Обработчик для окна обрезки видео.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Атрибут MF_ACTIVATE_VIDEO_WINDOW (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674014"
---
# <a name="mf_activate_video_window-attribute"></a>\_Порт MF \_ активировать \_ атрибут окна видео

Обработчик для окна обрезки видео.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как **DWORD \_ ptr** (**HWND**).

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к объекту активации расширенного обработчика видео (Евр). Значение задается автоматически при вызове [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) для создания объекта активации Евр.

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

[Расширенные атрибуты модуля подготовки видео](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[Объекты активации](activation-objects.md)
</dt> </dl>

 

 




