---
title: Сообщение WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: '\_ \_ \_ Сообщение VIDEOSTREAM для обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова в приложении.'
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- сообщение WM_CAP_SET_CALLBACK_VIDEOSTREAM Windows мультимедиа
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
ms.openlocfilehash: f2cdb4d7d18997fe437609b43a266242f04bd0bc2bb25429191d944240706244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940722"
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

## <a name="remarks"></a>Remarks

Окно Capture вызывает функцию обратного вызова перед записью захваченного кадра на диск. Это позволяет приложениям изменять фрейм при необходимости.

Если для потоковой передачи используется функция обратного вызова видеопотока, она должна быть установлена перед запуском сеанса записи и должна оставаться включенной в течение сеанса. Его можно отключить после завершения потоковой записи.

## <a name="requirements"></a>Требования



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

 

 





