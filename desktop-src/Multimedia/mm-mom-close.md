---
title: Сообщение MM_MOM_CLOSE (Ммсистем. h)
description: '\_ \_ При закрытии выходного устройства MIDI в окно отправляется сообщение Close MOM.'
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- сообщение MM_MOM_CLOSE Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8c9af8f6a5fb454a2f7759b5e64804e82c568b15549d01f7478a3d7c6041d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807154"
---
# <a name="mm_mom_close-message"></a>\_Сообщение закрытия MOM (mm) \_

При закрытии выходного устройства MIDI в окно отправляется сообщение **\_ \_ Close MOM** .


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*хаутпут*
</dt> <dd>

Обработчик для устройства вывода MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
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

 

 





