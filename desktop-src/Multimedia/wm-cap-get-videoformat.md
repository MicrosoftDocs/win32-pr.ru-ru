---
title: Сообщение WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: Сообщение о \_ получении крепления WM \_ \_ видеоформат извлекает копию используемого видеоформата или размер, необходимый для формата видео. Это сообщение можно отправить явно или с помощью макросов Капжетвидеоформат и Капжетвидеоформатсизе.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- сообщение WM_CAP_GET_VIDEOFORMAT Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afae3ea79b29cad6a758272f8f3952fdfb830a2b3d6d60f9fc5b4ca5042179fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622623"
---
# <a name="wm_cap_get_videoformat-message"></a>\_Сообщение о \_ получении крепления WM \_ видеоформат

Сообщение **о \_ получении крепления WM \_ \_ видеоформат** извлекает копию используемого видеоформата или размер, необходимый для формата видео. Это сообщение можно отправить явно или с помощью макросов [**капжетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) и [**капжетвидеоформатсизе**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .


```C++
WM_CAP_GET_VIDEOFORMAT 
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

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Можно также указать **значение NULL** , чтобы получить необходимое количество байтов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает размер (в байтах) формата видео или нуль, если окно записи не подключено к драйверу записи. Для форматов видео, для которых требуется палитра, также возвращается текущая палитра.

## <a name="remarks"></a>Remarks

Поскольку формат сжатого видео зависит от требований к размеру, приложения должны сначала получить размер, затем выделить память и, наконец, запросить данные в формате видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

