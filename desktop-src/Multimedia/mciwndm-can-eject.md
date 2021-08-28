---
title: Сообщение MCIWNDM_CAN_EJECT (VFW. h)
description: МЦИВНДМ \_ может \_ извлечь сообщение, определяет, может ли устройство MCI извлечь свой носитель. Это сообщение можно отправить явно или с помощью макроса МЦивндканежект.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- сообщение MCIWNDM_CAN_EJECT Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde4c9fec3972fe0e22b0a562454e1ef680e9ccae3851c272d28468fc2c91f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429674"
---
# <a name="mciwndm_can_eject-message"></a>МЦИВНДМ \_ может \_ извлечь сообщение

**МЦивндм \_ может \_ извлечь** сообщение, определяет, может ли устройство MCI извлечь свой носитель. Это сообщение можно отправить явно или с помощью макроса [**мЦивндканежект**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если устройство может извлечь носитель или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндканежект**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





