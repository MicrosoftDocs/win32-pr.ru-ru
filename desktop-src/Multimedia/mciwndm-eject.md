---
title: Сообщение MCIWNDM_EJECT (VFW. h)
description: Сообщение о \_ извлечении мЦивндм отправляет команду на устройство MCI для извлечения носителя. Это сообщение можно отправить явно или с помощью макроса МЦивндежект.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- сообщение MCIWNDM_EJECT Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c752f192e8f74f2c6e861e581fd22a561bafd9ff6c0f369ba669bc4bf87fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429434"
---
# <a name="mciwndm_eject-message"></a>\_Сообщение о извлечении мЦивндм

Сообщение **о \_ извлечении мЦивндм** отправляет команду на устройство MCI для извлечения носителя. Это сообщение можно отправить явно или с помощью макроса [**мЦивндежект**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



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

[**мЦивндежект**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





