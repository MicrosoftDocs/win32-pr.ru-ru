---
title: Сообщение WOM_CLOSE (Ммсистем. h)
description: Сообщение о \_ закрытии вом отправляется в функцию выходного обратного вызова звуковой волны при закрытии выходного устройства аудио аудио. После отправки этого сообщения маркер устройства больше не действителен.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- сообщение WOM_CLOSE Windows мультимедиа
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
ms.openlocfilehash: 90ba0187638ec4bc0406066c9a50ee4ce53ca150e4dabc918a829cfaa08733b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803484"
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

 

 





