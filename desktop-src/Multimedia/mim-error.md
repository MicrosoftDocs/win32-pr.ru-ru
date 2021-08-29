---
title: Сообщение MIM_ERROR (Ммсистем. h)
description: MIM \_ сообщение об ошибке отправляется в функцию обратного вызова midi, когда получено недопустимое сообщение midi.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- сообщение MIM_ERROR Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44793587b35c5d3e614c6a52f0cc9299e899b5feb4154f21b1ff278b96afde9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525064"
---
# <a name="mim_error-message"></a>MIM \_ Сообщение об ОШИБКе

**MIM сообщение \_ об ошибке** отправляется в функцию обратного вызова midi, когда получено недопустимое сообщение midi.


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*двмидимессаже*
</dt> <dd>

Получено недопустимое сообщение MIDI. Сообщение упаковывается в значение даублеворд с первым байтом сообщения в байте нижнего порядка.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*
</dt> <dd>

Время получения сообщения драйвером устройства ввода. Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

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

[Цифровой интерфейс музыкальных инструментов (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

