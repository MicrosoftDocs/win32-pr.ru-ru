---
title: Сообщение MCIWNDM_CAN_PLAY (VFW. h)
description: МЦИВНДМ \_ может \_ воспроизвести сообщение определяет, может ли устройство MCI воспроизвести файл данных или содержимое какого-либо другого типа. Это сообщение можно отправить явно или с помощью макроса МЦивндканплай.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672887"
---
# <a name="mciwndm_can_play-message"></a>МЦИВНДМ \_ может \_ воспроизвести сообщение

**МЦивндм \_ может \_ воспроизвести** сообщение определяет, может ли устройство MCI воспроизвести файл данных или содержимое какого-либо другого типа. Это сообщение можно отправить явно или с помощью макроса [**мЦивндканплай**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если устройство поддерживает воспроизведение данных, или **значение false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндканплай**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





