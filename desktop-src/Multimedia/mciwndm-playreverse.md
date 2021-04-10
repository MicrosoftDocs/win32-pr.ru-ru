---
title: Сообщение MCIWNDM_PLAYREVERSE (VFW. h)
description: Сообщение МЦИВНДМ \_ плайреверсе воспроизводит текущее содержимое в обратном направлении, начиная с текущей позиции и заканчивая в начале содержимого, или пока другая команда не останавливает воспроизведение.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135074"
---
# <a name="mciwndm_playreverse-message"></a>\_Сообщение мЦивндм плайреверсе

Сообщение **мЦивндм \_ плайреверсе** воспроизводит текущее содержимое в обратном направлении, начиная с текущей позиции и заканчивая в начале содержимого, или пока другая команда не останавливает воспроизведение. Это сообщение можно отправить явно или с помощью макроса [**мЦивндплайреверсе**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .


```C++
MCIWNDM_PLAYREVERSE 
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

[**мЦивндплайреверсе**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





