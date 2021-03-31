---
title: Сообщение MOM_POSITIONCB (Ммсистем. h)
description: Сообщение о \_ должности MOM отправляется при \_ \_ достижении события обратного вызова мевт F в потоке вывода MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803665"
---
# <a name="mom_positioncb-message"></a>\_Сообщение MOM поситионкб

Сообщение **о \_ должности MOM** отправляется при достижении события **\_ \_ обратного вызова МЕВТ F** в потоке вывода MIDI.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую входной буфер.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Воспроизведение буфера потока сохраняется даже во время выполнения функции обратного вызова. Все события после события **\_ \_ обратного вызова мевт F** в буфере будут планироваться и отправляться вовремя независимо от того, сколько времени тратится на функцию обратного вызова.

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

 

