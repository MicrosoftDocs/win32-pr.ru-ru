---
title: Сообщение MCIWNDM_GETEND (VFW. h)
description: Сообщение МЦИВНДМ \_ жетенд извлекает расположение конца содержимого устройства или файла MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетенд.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- сообщение MCIWNDM_GETEND Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880b1a464d671ca57e1955d4131776a999d1fb6bd8f17ad5d08139abc64a757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137735"
---
# <a name="mciwndm_getend-message"></a>\_Сообщение мЦивндм жетенд

Сообщение **мЦивндм \_ жетенд** извлекает расположение конца содержимого устройства или файла MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетенд**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает расположение в текущем формате времени.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мЦивнджетенд**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





