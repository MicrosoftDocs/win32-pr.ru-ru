---
title: Сообщение ICM_DRAW_REALIZE (VFW. h)
description: Сообщение ICM \_ Draw дает \_ уведомление драйверу подготовки отчетов о том, что во время рисования он реализует свою палитру рисования. Это сообщение можно отправить явно или с помощью макроса Икдравреализе.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415361"
---
# <a name="icm_draw_realize-message"></a>\_Сообщение о выводе ICM \_

Сообщение **ICM \_ Draw \_** дает уведомление драйверу подготовки отчетов о том, что во время рисования он реализует свою палитру рисования. Это сообщение можно отправить явно или с помощью макроса [**икдравреализе**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*HDC*
</dt> <dd>

Обработчик контроллера домена, используемый для реализации палитры.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*фбаккграунд*
</dt> <dd>

Флаг фона. Укажите **значение true** , чтобы реализовать палитру в качестве фоновой задачи, или **false** , чтобы реализовать палитру на переднем плане.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК, если палитра рисования реализована или ицерр не \_ поддерживается, если реализована палитра, связанная с распакованными данными.

## <a name="remarks"></a>Комментарии

Драйверы должны отвечать на это сообщение, только если палитра рисования отличается от сжатой палитры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 

 





