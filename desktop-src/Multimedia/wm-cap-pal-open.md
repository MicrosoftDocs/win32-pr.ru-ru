---
title: Сообщение WM_CAP_PAL_OPEN (VFW. h)
description: Сообщение WM \_ Cap \_ PAL \_ Open загружает новую палитру из файла палитры и передает его драйверу записи.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- сообщение WM_CAP_PAL_OPEN Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29cb831ca0128b0562d6ee53b8e66309d2e1dbd91803dab13202dc4a6723bfa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800583"
---
# <a name="wm_cap_pal_open-message"></a>\_ \_ Открытое сообщение с ограничением WM PAL \_

Сообщение **WM \_ Cap \_ PAL \_ Open** загружает новую палитру из файла палитры и передает его драйверу записи. Файлы палитры обычно используют расширение имени файла. Списком. Драйвер записи использует палитру, если это требуется для указанного формата изображения в цифровом формате. Это сообщение можно отправить явно или с помощью макроса [**каппалеттеопен**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Указатель на строку с завершающим нулем, содержащую имя файла палитры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

## <a name="requirements"></a>Requirements (Требования)



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

 

 





