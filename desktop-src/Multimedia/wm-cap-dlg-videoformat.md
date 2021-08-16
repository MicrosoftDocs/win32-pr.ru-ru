---
title: Сообщение WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: В \_ сообщении о \_ видеоформате WM Cap \_ появляется диалоговое окно, в котором пользователь может выбрать формат видео.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- сообщение WM_CAP_DLG_VIDEOFORMAT Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaa58e99c6a07db9109a0b1a6dae25de8abd46fef2631eb539961de16455ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135403"
---
# <a name="wm_cap_dlg_videoformat-message"></a>\_ \_ Сообщение видеоформат с диалогом WM Cap \_

В сообщении о **\_ \_ \_ видеоформате WM Cap** появляется диалоговое окно, в котором пользователь может выбрать формат видео. Диалоговое окно Формат видео можно использовать для выбора размеров изображения, глубины битов и параметров аппаратного сжатия. Это сообщение можно отправить явно или с помощью макроса [**капдлгвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

После возврата этого сообщения приложениям может потребоваться обновить структуру [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) , так как пользователь мог изменить размеры изображения.

Диалоговое окно Формат видео является уникальным для каждого драйвера записи. Некоторые драйверы записи могут не поддерживать диалоговое окно формата видео. Приложения могут определить, поддерживает ли драйвер записи это сообщение, проверив элемент **фхасдлгвидеоформат** в [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).

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

 

 





