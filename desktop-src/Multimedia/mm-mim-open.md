---
title: Сообщение MM_MIM_OPEN (Ммсистем. h)
description: сообщение MM \_ MIM \_ OPEN отправляется в окно при открытии входного устройства MIDI.
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- сообщение MM_MIM_OPEN Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d6b090968c4823ab14159772f5e8ba8531166a299bf1d9e90061739831d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985524"
---
# <a name="mm_mim_open-message"></a>MM \_ MIM \_ открыть сообщение

сообщение **MM \_ MIM \_ OPEN** отправляется в окно при открытии входного устройства MIDI.


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*
</dt> <dd>

Обработано открытое устройство ввода MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Процессу не используйте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Цифровой интерфейс музыкальных инструментов (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

 





