---
title: Сообщение MIM_CLOSE (Ммсистем. h)
description: Сообщение о \_ закрытии MIM отправляется в функцию обратного вызова MIDI при закрытии входного устройства MIDI.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- MIM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533794"
---
# <a name="mim_close-message"></a>\_Сообщение о закрытии MIM

Сообщение **о \_ закрытии MIM** отправляется в функцию обратного вызова MIDI при закрытии входного устройства MIDI.


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Процессу не используйте.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Процессу не используйте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

После отправки этого сообщения маркер устройства больше не действителен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Цифровой интерфейс музыкальных инструментов (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

 





