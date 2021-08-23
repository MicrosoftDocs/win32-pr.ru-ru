---
title: Сообщение WM_CAP_PAL_PASTE (VFW. h)
description: Сообщение о \_ \_ вставке WM Cap PAL \_ копирует палитру из буфера обмена и передает ее драйверу записи. Это сообщение можно отправить явно или с помощью макроса Каппалеттепасте.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- сообщение WM_CAP_PAL_PASTE Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bedb760a444abe9b0667592855d701dc24a02b8ee57ea15ab30912a5e216d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686834"
---
# <a name="wm_cap_pal_paste-message"></a>\_Вставка сообщения с ограничением WM \_ PAL \_

Сообщение **о \_ \_ \_ вставке WM Cap PAL** копирует палитру из буфера обмена и передает ее драйверу записи. Это сообщение можно отправить явно или с помощью макроса [**каппалеттепасте**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.

## <a name="remarks"></a>Remarks

Драйвер записи использует палитру при необходимости в указанном цифровом формате видео.

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

 

 





