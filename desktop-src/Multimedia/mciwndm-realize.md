---
title: Сообщение MCIWNDM_REALIZE (VFW. h)
description: Сообщение о \_ реализации мЦивндм понимает палитру, которая в настоящее время используется устройством MCI в окне мЦивнд. Этот макрос определяется с помощью сообщения о \_ реализации мЦивндм. Это сообщение можно отправить явно или с помощью макроса МЦивндреализе.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE сообщения Windows мультимедиа
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
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988260"
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

## <a name="remarks"></a>Комментарии

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

 

