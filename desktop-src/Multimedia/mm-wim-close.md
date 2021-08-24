---
title: Сообщение MM_WIM_CLOSE (Ммсистем. h)
description: Сообщение о закрытии \_ WIM-файла mm \_ отправляется в окно при закрытии входного устройства звуковой волны. После отправки этого сообщения маркер устройства больше не действителен.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- сообщение MM_WIM_CLOSE Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506311f9938198e2ceb99646670c954eaa433825855e31c036241df6be1b2491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807114"
---
# <a name="mm_wim_close-message"></a>MM \_ . \_ сообщение о закрытии WIM

Сообщение о закрытии **\_ WIM \_** -файла mm отправляется в окно при закрытии входного устройства звуковой волны. После отправки этого сообщения маркер устройства больше не действителен.


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*хинпутдев*
</dt> <dd>

Обработано выходное устройство ввода аудио-сигнала, которое было закрыто.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Процессу должно быть равно нулю.

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

[Звуковая волна](waveform-audio.md)
</dt> <dt>

[Сообщения волны](waveform-messages.md)
</dt> </dl>

 

 





