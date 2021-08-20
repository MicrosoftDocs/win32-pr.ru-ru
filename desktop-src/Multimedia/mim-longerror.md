---
title: Сообщение MIM_LONGERROR (Ммсистем. h)
description: сообщение MIM \_ лонжеррор отправляется в функцию обратного вызова midi, если получено недопустимое или неполное сообщение, исключающие midi.
ms.assetid: 7e3b0716-33c4-449c-a200-e5ba72428dc1
keywords:
- сообщение MIM_LONGERROR Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d0be5f2d75ae8ba1eed61f99d1387e1defec556b5e242f713b75eee0a3f70e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985747"
---
# <a name="mim_longerror-message"></a>MIM \_ Сообщение ЛОНЖЕРРОР

сообщение **MIM \_ лонжеррор** отправляется в функцию обратного вызова midi, если получено недопустимое или неполное сообщение, исключающие midi.


```C++
MIM_LONGERROR 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*
</dt> <dd>

Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер, содержащий недопустимое сообщение.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*
</dt> <dd>

Время получения данных драйвером устройства ввода. Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Возвращенный буфер может быть незаполненным. Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , заданную параметром *лпмидихдр*.

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

 

