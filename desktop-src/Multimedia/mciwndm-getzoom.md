---
title: Сообщение MCIWNDM_GETZOOM (VFW. h)
description: Сообщение МЦИВНДМ \_ Zoom получает текущее значение масштаба, используемое устройством MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетзум.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- сообщение MCIWNDM_GETZOOM Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c247230ffe6269f77b906d874a4cf82a21ed8d3388ffa18193417603e45fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374145"
---
# <a name="mciwndm_getzoom-message"></a>\_Сообщение МЦИВНДМ Zoom

Сообщение **МЦИВНДМ \_ Zoom** получает текущее значение масштаба, используемое устройством MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает последние значения, используемые с [**мЦивндм \_ сетзум**](mciwndm-setzoom.md).

## <a name="remarks"></a>Remarks

Возвращаемое значение 100 означает, что изображение не масштабируется. Значение 200 указывает, что изображение увеличивается вдвое в два раза. Значение 50 указывает, что изображение уменьшается до половины исходного размера.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**МЦИВНДМ \_ сетзум**](mciwndm-setzoom.md)
</dt> </dl>

 

 





