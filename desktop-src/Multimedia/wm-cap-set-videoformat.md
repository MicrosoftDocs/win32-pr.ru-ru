---
title: Сообщение WM_CAP_SET_VIDEOFORMAT (VFW. h)
description: Сообщение WM \_ Cap \_ Set \_ видеоформат устанавливает формат записываемых видеоданных. Это сообщение можно отправить явно или с помощью макроса Капсетвидеоформат.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- сообщение WM_CAP_SET_VIDEOFORMAT Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c543f613fedf54518579829d6825bd20dc4738ae03cb77f0996f8a58a123cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135025"
---
# <a name="wm_cap_set_videoformat-message"></a>\_ \_ Сообщение видеоформат установки крепления WM \_

Сообщение **WM \_ Cap \_ Set \_ видеоформат** устанавливает формат записываемых видеоданных. Это сообщение можно отправить явно или с помощью макроса [**капсетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) .


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) структуры, на которую ссылается **s**.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*псвидеоформат*
</dt> <dd>

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Так как форматы видео специфичны для конкретного устройства, приложения должны проверить возвращаемое значение этой функции, чтобы определить, принимается ли формат драйвером.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

