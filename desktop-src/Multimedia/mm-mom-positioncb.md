---
title: Сообщение MM_MOM_POSITIONCB (Ммсистем. h)
description: '\_ \_ При \_ \_ достижении события обратного вызова мевт F в потоке вывода MIDI в окно отправляется сообщение поситионкб MOM.'
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- сообщение MM_MOM_POSITIONCB Windows мультимедиа
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
ms.openlocfilehash: 4f68afecddd9b6ca8a0e5f6305b430b059b93db5a2abb966c0a7aed9ab350f7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807164"
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

## <a name="remarks"></a>Remarks

Воспроизведение буфера потока сохраняется даже во время выполнения функции обратного вызова. Все события после \_ \_ события обратного вызова мевт F в буфере будут планироваться и отправляться вовремя независимо от того, сколько времени тратится на функцию обратного вызова.

Если обратные вызовы размещения создаются быстрее, чем приложение может их обработать, элемент **двоффсет** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) может ссылаться на событие, которое еще не обработано приложением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

