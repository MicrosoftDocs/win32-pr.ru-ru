---
title: Сообщение MCIWNDM_SETPALETTE (VFW. h)
description: Сообщение МЦИВНДМ \_ сетпалетте отправляет маркер палитры на устройство MCI, связанное с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндсетпалетте.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- сообщение MCIWNDM_SETPALETTE Windows мультимедиа
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
ms.openlocfilehash: 7b4986224fd23898ef33f8fdda4c12d17880a8bc42441b29cd1865fb7fdfa687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525234"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мЦивндсетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





