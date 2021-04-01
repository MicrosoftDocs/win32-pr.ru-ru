---
title: Сообщение WM_CAP_PAL_MANUALCREATE (VFW. h)
description: Сообщение WM \_ Cap \_ PAL \_ мануалкреате запрашивает, что драйвер записи выводит образцы видеокадров вручную и создает новую палитру. Это сообщение можно отправить явно или с помощью макроса Каппалеттемануал.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801870"
---
# <a name="wm_cap_pal_manualcreate-message"></a>\_Сообщение о \_ мануалкреатее WM Cap PAL \_

Сообщение **WM \_ Cap \_ PAL \_ мануалкреате** запрашивает, что драйвер записи выводит образцы видеокадров вручную и создает новую палитру. Это сообщение можно отправить явно или с помощью макроса [**каппалеттемануал**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*фграб*
</dt> <dd>

Флаг гистограммы палитры. Задайте для этого параметра **значение true** для каждого кадра, включенного при создании оптимальной палитры. После сбора последнего кадра присвойте этому параметру **значение false** , чтобы вычислить оптимальную палитру и отправить ее драйверу записи.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*иколорс*
</dt> <dd>

Число цветов в палитре. Максимальное значение этого параметра — 256. Это значение используется только во время сбора первого кадра в последовательности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

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

 

 





