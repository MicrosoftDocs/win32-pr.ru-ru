---
title: Сообщение MOM_CLOSE (Ммсистем. h)
description: '\_Сообщение закрытия MOM отправляется в функцию обратного вызова MIDI OUTPUT при закрытии выходного устройства MIDI.'
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989273"
---
# <a name="mom_close-message"></a>\_Сообщение закрытия MOM

Сообщение **\_ закрытия MOM** отправляется в функцию обратного вызова MIDI OUTPUT при закрытии выходного устройства MIDI.


```C++
MOM_CLOSE 
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

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

 





