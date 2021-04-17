---
title: Сообщение WOM_CLOSE (Ммсистем. h)
description: Сообщение о \_ закрытии вом отправляется в функцию выходного обратного вызова звуковой волны при закрытии выходного устройства аудио аудио. После отправки этого сообщения маркер устройства больше не действителен.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- WOM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672605"
---
# <a name="wom_close-message"></a>\_Сообщение о закрытии ВОМ

Сообщение **о \_ закрытии вом** отправляется в функцию выходного обратного вызова звуковой волны при закрытии выходного устройства аудио аудио. После отправки этого сообщения маркер устройства больше не действителен.


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Процессу должно быть равно нулю.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Процессу должно быть равно нулю.

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

[Звуковая волна](waveform-audio.md)
</dt> <dt>

[Сообщения волны](waveform-messages.md)
</dt> </dl>

 

 





