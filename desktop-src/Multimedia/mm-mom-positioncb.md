---
title: Сообщение MM_MOM_POSITIONCB (Ммсистем. h)
description: '\_ \_ При \_ \_ достижении события обратного вызова мевт F в потоке вывода MIDI в окно отправляется сообщение поситионкб MOM.'
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988258"
---
# <a name="mm_mom_positioncb-message"></a>\_ \_ Сообщение поситионкб MOM

При **\_ \_** \_ \_ достижении события обратного вызова МЕВТ F в потоке вывода MIDI в окно отправляется сообщение поситионкб MOM.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*
</dt> <dd>

Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , которая идентифицирует событие, вызвавшее обратный вызов. Элемент **двоффсет** дает смещение события.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Процессу не используйте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Воспроизведение буфера потока сохраняется даже во время выполнения функции обратного вызова. Все события после \_ \_ события обратного вызова мевт F в буфере будут планироваться и отправляться вовремя независимо от того, сколько времени тратится на функцию обратного вызова.

Если обратные вызовы размещения создаются быстрее, чем приложение может их обработать, элемент **двоффсет** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) может ссылаться на событие, которое еще не обработано приложением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

