---
title: Сообщение WM_CAP_SET_SCROLL (VFW. h)
description: '\_Сообщение SCROLL Set с закреплением WM \_ \_ определяет часть видеокадра, отображаемую в окне Capture (захват).'
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- сообщение WM_CAP_SET_SCROLL Windows мультимедиа
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
ms.openlocfilehash: 352d65c2ad8e80622f7ff50cca0a8f7d6e523d53ae002a2325327a634b97c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134988"
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

## <a name="remarks"></a>Remarks

Расположение прокрутки влияет на изображение в режимах предварительного просмотра и наложения.

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

 

 





