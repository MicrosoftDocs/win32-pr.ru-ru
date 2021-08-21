---
title: Сообщение MM_MOM_OPEN (Ммсистем. h)
description: Сообщение о \_ открытом формате mm MOM \_ отправляется в окно при открытии выходного устройства MIDI.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- сообщение MM_MOM_OPEN Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842eaeeb6e18e6623f8c88d8f5c65527db36ee8370c48a4cb26edca55f6d5f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065494"
---
# <a name="mm_mom_open-message"></a>\_Открытое сообщение для MOM (mm) \_

Сообщение **о \_ \_ открытом формате mm MOM** отправляется в окно при открытии выходного устройства MIDI.


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*хаутпут*
</dt> <dd>

Обработчик для устройства вывода MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Процессу не используйте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

 





