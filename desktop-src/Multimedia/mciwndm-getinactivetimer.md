---
title: Сообщение MCIWNDM_GETINACTIVETIMER (VFW. h)
description: Сообщение МЦИВНДМ \_ жетинактиветимер получает период обновления, используемый, когда окно мЦивнд является неактивным окном. Это сообщение можно отправить явно или с помощью макроса МЦивнджетинактиветимер.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672497"
---
# <a name="mciwndm_getinactivetimer-message"></a>\_Сообщение мЦивндм жетинактиветимер

Сообщение **мЦивндм \_ жетинактиветимер** получает период обновления, используемый, когда окно мЦивнд является неактивным окном. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетинактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает период обновления в миллисекундах. Значение по умолчанию — 2000 миллисекунд.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетинактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





