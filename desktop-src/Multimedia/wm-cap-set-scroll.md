---
title: Сообщение WM_CAP_SET_SCROLL (VFW. h)
description: '\_Сообщение SCROLL Set с закреплением WM \_ \_ определяет часть видеокадра, отображаемую в окне Capture (захват).'
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492945"
---
# <a name="wm_cap_set_scroll-message"></a>\_ \_ \_ Сообщение прокрутки установки крепления WM

Сообщение **\_ \_ \_ SCROLL Set с закреплением WM** определяет часть видеокадра, отображаемую в окне Capture (захват). Это сообщение задает для левого верхнего угла клиентской области окна захвата координаты указанного пикселя в кадре видео. Это сообщение можно отправить явно или с помощью макроса [**капсетскроллпос**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*лпп*
</dt> <dd>

Адрес, содержащий нужную точку прокрутки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Расположение прокрутки влияет на изображение в режимах предварительного просмотра и наложения.

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

 

 





