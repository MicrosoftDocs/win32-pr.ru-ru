---
title: Сообщение ICM_DRAW_CHANGEPALETTE (VFW. h)
description: Сообщение ICM \_ Draw \_ чанжепалетте уведомляет драйвер подготовки к просмотру, что изменяется палитра роликов. Это сообщение можно отправить явно или с помощью макроса Икдравчанжепалетте.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- сообщение ICM_DRAW_CHANGEPALETTE Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e936c7dce397910ef70a80e2efa7f3e031ab8a61b8f59fece158d5c28e9e1270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987600"
---
# <a name="icm_draw_changepalette-message"></a>\_Сообщение ICM Draw \_ чанжепалетте

Сообщение **ICM \_ Draw \_ чанжепалетте** уведомляет драйвер подготовки к просмотру, что изменяется палитра роликов. Это сообщение можно отправить явно или с помощью макроса [**икдравчанжепалетте**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*лпбиинпут*
</dt> <dd>

Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , содержащую новый формат и необязательную таблицу цветов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Это сообщение должно поддерживаться с помощью устанавливаемых обработчиков отрисовки, которые рисуют DIB с внутренней структурой, содержащей палитру.

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

 

