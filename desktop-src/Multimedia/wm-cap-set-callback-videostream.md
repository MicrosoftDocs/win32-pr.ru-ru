---
title: Сообщение WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: '\_ \_ \_ Сообщение VIDEOSTREAM для обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова в приложении.'
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414797"
---
# <a name="wm_cap_set_callback_videostream-message"></a>\_Сообщение о \_ \_ VIDEOSTREAM обратного вызова Set крепления WM \_

Сообщение **\_ VIDEOSTREAM для \_ \_ обратного \_ вызова Set крепления WM** устанавливает функцию обратного вызова в приложении. Авикап вызывает эту процедуру при захвате потоковой передачи при заполнении буфера видео. Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконвидеостреам**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*
</dt> <dd>

Указатель на функцию обратного вызова видео-Stream типа [**капвидеостреамкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова видео-потока.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.

## <a name="remarks"></a>Комментарии

Окно Capture вызывает функцию обратного вызова перед записью захваченного кадра на диск. Это позволяет приложениям изменять фрейм при необходимости.

Если для потоковой передачи используется функция обратного вызова видеопотока, она должна быть установлена перед запуском сеанса записи и должна оставаться включенной в течение сеанса. Его можно отключить после завершения потоковой записи.

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

 

 





