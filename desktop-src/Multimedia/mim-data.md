---
title: Сообщение MIM_DATA (Ммсистем. h)
description: сообщение MIM \_ данных отправляется в функцию обратного вызова midi при получении сообщения midi входным устройством midi.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- сообщение MIM_DATA Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebbb9ca6016706605de8fed29e5fa5ebaf6055f4a730fb563323f306606b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137293"
---
# <a name="mim_data-message"></a>MIM \_ Сообщение данных

сообщение **MIM \_ данных** отправляется в функцию обратного вызова midi при получении сообщения midi входным устройством midi.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*двмидимессаже*
</dt> <dd>

Полученное сообщение MIDI. Сообщение упаковывается в значение даублеворд следующим образом:



| Требование | Значение | Описание |
|-----------|-----------------|-----------------------------------------------------|
| Высокое слово | Байт высокого порядка | Не используется.                                           |
|           | Байт низкого порядка  | Содержит второй байт данных MIDI (при необходимости).  |
| Низкое слово  | Байт высокого порядка | Содержит первый байт данных MIDI (при необходимости). |
|           | Байт низкого порядка  | Содержит состояние MIDI.                           |



 

Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*
</dt> <dd>

Время получения сообщения драйвером устройства ввода. Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.

Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.

## <a name="requirements"></a>Requirements (Требования)



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

 

