---
title: Сообщение MM_MIM_ERROR (Ммсистем. h)
description: '\_ \_ При получении недопустимого сообщения MIDI в окно отправляется сообщение об ошибке в MIM.'
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- MM_MIM_ERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135267"
---
# <a name="mm_mim_error-message"></a>ММ \_ — \_ сообщение об ошибке MIM

При получении недопустимого сообщения MIDI в окно отправляется сообщение **\_ \_ об ошибке в MIM** .


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*
</dt> <dd>

Обрабатывает входное устройство MIDI, которое получило недопустимое сообщение.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*лмидимессаже*
</dt> <dd>

Недопустимое сообщение MIDI. Сообщение упаковывается в значение **DWORD** с первым байтом сообщения в байте нижнего порядка.

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

[Цифровой интерфейс музыкальных инструментов (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

 





