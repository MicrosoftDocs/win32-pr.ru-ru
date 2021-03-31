---
title: Сообщение MCIWNDM_GETEND (VFW. h)
description: Сообщение МЦИВНДМ \_ жетенд извлекает расположение конца содержимого устройства или файла MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетенд.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND сообщения Windows мультимедиа
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
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892577"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетенд**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





