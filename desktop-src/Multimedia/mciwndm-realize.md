---
title: Сообщение MCIWNDM_REALIZE (VFW. h)
description: Сообщение о \_ реализации мЦивндм понимает палитру, которая в настоящее время используется устройством MCI в окне мЦивнд. Этот макрос определяется с помощью сообщения о \_ реализации мЦивндм. Это сообщение можно отправить явно или с помощью макроса МЦивндреализе.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- сообщение MCIWNDM_REALIZE Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fdbee3757e1fd3aada5292b86cc37577ccb718315c5b81140ceb14278c37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012622"
---
# <a name="mciwndm_realize-message"></a>\_Сообщение о реализации мЦивндм

Сообщение **о \_ реализации мЦивндм** понимает палитру, которая в настоящее время используется устройством MCI в окне мЦивнд. Этот макрос определяется с помощью сообщения **о \_ реализации мЦивндм** . Это сообщение можно отправить явно или с помощью макроса [**мЦивндреализе**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*фбкгнд*
</dt> <dd>

Флаг фона. Укажите **значение true** для этого параметра, если окно является фоновым приложением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

**МЦивндм \_** В процессе реализации используется палитра устройства MCI и вызывается функция [**реализепалетте**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) . Если приложение явным образом обрабатывает сообщения [**WM \_ Палеттечанжед**](/windows/desktop/gdi/wm-palettechanged) и [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) , следует использовать это сообщение в приложении вместо использования **реализепалетте**. Если тело одного из этих обработчиков сообщений содержит только **реализепалетте**, перешлите сообщение в окно мЦивнд, которое будет автоматически реализовывать палитру.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндреализе**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**реализепалетте**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**WM \_ палеттечанжед**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

