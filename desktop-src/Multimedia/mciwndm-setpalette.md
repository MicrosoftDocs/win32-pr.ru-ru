---
title: Сообщение MCIWNDM_SETPALETTE (VFW. h)
description: Сообщение МЦИВНДМ \_ сетпалетте отправляет маркер палитры на устройство MCI, связанное с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндсетпалетте.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491721"
---
# <a name="mciwndm_setpalette-message"></a>\_Сообщение мЦивндм сетпалетте

Сообщение **мЦивндм \_ сетпалетте** отправляет маркер палитры на устройство MCI, связанное с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*хпал*
</dt> <dd>

Маркер палитры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндсетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





