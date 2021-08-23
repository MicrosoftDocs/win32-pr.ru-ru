---
title: Сообщение MCIWNDM_CAN_CONFIG (VFW. h)
description: Сообщение МЦИВНДМ \_ Can \_ config определяет, может ли устройство MCI отобразить диалоговое окно конфигурации. Это сообщение можно отправить явно или с помощью макроса МЦивндканконфиг.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- сообщение MCIWNDM_CAN_CONFIG Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef5b8e4f8e1ab09f128b1294034bbb715c834c3e867f31bbaae0cb6bd620be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525534"
---
# <a name="mciwndm_can_config-message"></a>МЦИВНДМ \_ может \_ сообщение конфигурации

Сообщение **мЦивндм \_ Can \_ config** определяет, может ли устройство MCI отобразить диалоговое окно конфигурации. Это сообщение можно отправить явно или с помощью макроса [**мЦивндканконфиг**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если устройство поддерживает конфигурацию, или **значение false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мЦивндканконфиг**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





