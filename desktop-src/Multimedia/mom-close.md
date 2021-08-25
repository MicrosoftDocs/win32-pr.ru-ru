---
title: Сообщение MOM_CLOSE (Ммсистем. h)
description: '\_Сообщение закрытия MOM отправляется в функцию обратного вызова MIDI OUTPUT при закрытии выходного устройства MIDI.'
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- сообщение MOM_CLOSE Windows мультимедиа
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
ms.openlocfilehash: dbabd0cae61c1b1ea3d88df3cd2e52524b779eb7cdb5ac2c1e1a371546724f44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038874"
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

## <a name="remarks"></a>Remarks

После отправки этого сообщения маркер устройства больше не действителен.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Сообщения MIDI](midi-messages.md)
</dt> </dl>

 

 





