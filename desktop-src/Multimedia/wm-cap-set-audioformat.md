---
title: Сообщение WM_CAP_SET_AUDIOFORMAT (VFW. h)
description: '\_ \_ Сообщение аудиоформат, установленное с помощью WM Cap, \_ задает формат аудио, используемый при выполнении потоковой передачи или записи шага. Это сообщение можно отправить явно или с помощью макроса Капсетаудиоформат.'
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- WM_CAP_SET_AUDIOFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136214"
---
# <a name="wm_cap_set_audioformat-message"></a>\_ \_ Сообщение аудиоформат установки крепления WM \_

Сообщение **\_ \_ \_ аудиоформат, установленное с помощью WM Cap** , задает формат аудио, используемый при выполнении потоковой передачи или записи шага. Это сообщение можно отправить явно или с помощью макроса [**капсетаудиоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) .


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*
</dt> <dd>

Размер (в байтах) структуры, на которую ссылается **s**.

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*псаудиоформат*
</dt> <dd>

Указатель на структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) или [**пкмвавеформат**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) , определяющую аудио формат.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

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

 

