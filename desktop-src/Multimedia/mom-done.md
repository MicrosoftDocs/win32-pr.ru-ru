---
title: Сообщение MOM_DONE (МЦиапи. h)
description: Сообщение «MOM \_ done» отправляется в функцию обратного вызова MIDI Output, когда заданный системный или потоковый буфер воспроизводится и возвращается приложению.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- MOM_DONE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415269"
---
# <a name="mom_done-message"></a>\_Сообщение о завершении MOM

Сообщение « **MOM \_ done** » отправляется в функцию обратного вызова MIDI Output, когда заданный системный или потоковый буфер воспроизводится и возвращается приложению.


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*
</dt> <dd>

Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Процессу не используйте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

