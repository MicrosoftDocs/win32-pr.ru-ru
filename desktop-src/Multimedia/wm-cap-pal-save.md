---
title: Сообщение WM_CAP_PAL_SAVE (VFW. h)
description: Сообщение о \_ СОХРАНЕНИИ WM Cap \_ PAL \_ сохраняет текущую палитру в файле палитры. Файлы палитры обычно используют расширение имени файла. Списком. Это сообщение можно отправить явно или с помощью макроса Каппалеттесаве.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- сообщение WM_CAP_PAL_SAVE Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff8703eafcc3c612fbde5bac7d15433758aa3d6ee44ab47697ffb25f9324dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891884"
---
# <a name="wm_cap_pal_save-message"></a>Сообщение о сохранении в формате WM \_ Cap \_ PAL \_

Сообщение **о \_ \_ \_ сохранении WM Cap PAL** сохраняет текущую палитру в файле палитры. Файлы палитры обычно используют расширение имени файла. Списком. Это сообщение можно отправить явно или с помощью макроса [**каппалеттесаве**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .


```C++
WM_CAP_PAL_SAVE 
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



## <a name="see-also"></a>См. также

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> <dt>

[Сообщения видеозаписи](video-capture-messages.md)
</dt> </dl>

 

 





