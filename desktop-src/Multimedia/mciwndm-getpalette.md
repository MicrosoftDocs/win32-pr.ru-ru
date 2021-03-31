---
title: Сообщение MCIWNDM_GETPALETTE (VFW. h)
description: Сообщение МЦИВНДМ \_ -Palette получает маркер палитры, используемый устройством MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетпалетте.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071232"
---
# <a name="mciwndm_getpalette-message"></a>\_Сообщение мЦивндм

Сообщение **мЦивндм- \_ Palette** получает маркер палитры, используемый устройством MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер палитры в случае успеха.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





