---
title: Сообщение MCIWNDM_GETSTART (VFW. h)
description: Сообщение МЦИВНДМ \_ OnStart получает расположение начала содержимого устройства или файла MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетстарт.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- сообщение MCIWNDM_GETSTART Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0efb5689009fdd6928afd1d2f232bcb1bbeb2160aecf3d79ddb263ed6f315de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429234"
---
# <a name="mciwndm_getstart-message"></a>Сообщение МЦИВНДМ о \_ запуске

Сообщение **мЦивндм \_ OnStart** получает расположение начала содержимого устройства или файла MCI. Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетстарт**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Возвращаемое значение

Возвращает расположение в текущем формате времени.

## <a name="remarks"></a>Remarks

Как правило, возвращаемое значение равно нулю; но некоторые устройства используют ненулевое начальное расположение. При поиске в этом расположении устройство настраивается на начало носителя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивнджетстарт**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





