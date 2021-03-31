---
title: Сообщение MM_MOM_DONE (Ммсистем. h)
description: Сообщение о \_ завершении программы mm MOM \_ отправляется в окно при воспроизведении указанного системы или буфера потока MIDI и возвращается приложению.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- MM_MOM_DONE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071228"
---
# <a name="mm_mom_done-message"></a>\_Сообщение о \_ завершении диспетчера мм

Сообщение **о \_ \_ завершении программы mm MOM** отправляется в окно при воспроизведении указанного системы или буфера потока MIDI и возвращается приложению.


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*хаутпут*
</dt> <dd>

Обработчик на устройстве вывода MIDI, который воспроизводил буфер.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*
</dt> <dd>

Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

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

 

