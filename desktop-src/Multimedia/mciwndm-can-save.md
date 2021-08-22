---
title: Сообщение MCIWNDM_CAN_SAVE (VFW. h)
description: МЦИВНДМ \_ может \_ сохранить сообщение, определяет, может ли устройство MCI сохранять данные. Это сообщение можно отправить явно или с помощью макроса МЦивндкансаве.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- сообщение MCIWNDM_CAN_SAVE Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccab622381208b8213414ed8b156a84e431afffc55acdf2323b0c0a2d31014f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429634"
---
# <a name="mciwndm_can_save-message"></a>МЦИВНДМ \_ может \_ сохранить сообщение

**МЦивндм \_ может \_ сохранить** сообщение, определяет, может ли устройство MCI сохранять данные. Это сообщение можно отправить явно или с помощью макроса [**мЦивндкансаве**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если устройство поддерживает сохранение или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндкансаве**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





