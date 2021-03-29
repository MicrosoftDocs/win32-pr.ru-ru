---
title: Сообщение WM_CAP_PAL_AUTOCREATE (VFW. h)
description: Сообщение с \_ \_ \_ автоматическим созданием WM Cap PAL запрашивает в качестве примера видеодрайвера записи образец видеокадра и автоматическое создание новой палитры. Это сообщение можно отправить явно или с помощью макроса Каппалеттеауто.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661863"
---
# <a name="wm_cap_pal_autocreate-message"></a>\_Сообщение с \_ \_ автосозданием WM Cap PAL

Сообщение с автоматическим **\_ \_ \_ созданием WM Cap PAL** запрашивает в качестве примера видеодрайвера записи образец видеокадра и автоматическое создание новой палитры. Это сообщение можно отправить явно или с помощью макроса [**каппалеттеауто**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*IFRAME*
</dt> <dd>

Число кадров для выборки.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*иколорс*
</dt> <dd>

Число цветов в палитре. Максимальное значение этого параметра — 256.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

## <a name="remarks"></a>Комментарии

Последовательность видеороликов с выборкой должна включать все нужные цвета в палитре. Для получения оптимальной палитры может потребоваться выборка всей последовательности, а не ее части.

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

 

 





