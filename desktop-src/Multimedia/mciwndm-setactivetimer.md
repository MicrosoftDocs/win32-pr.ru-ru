---
title: Сообщение MCIWNDM_SETACTIVETIMER (VFW. h)
description: Сообщение МЦИВНДМ \_ сетактиветимер задает период обновления, используемый мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении в строке заголовка окна и отправки сообщений уведомления родительскому окну, когда окно мЦивнд активно. Это сообщение можно отправить явно или с помощью макроса МЦивндсетактиветимер.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136587"
---
# <a name="mciwndm_setactivetimer-message"></a>\_Сообщение мЦивндм сетактиветимер

Сообщение **мЦивндм \_ сетактиветимер** задает период обновления, используемый мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении в строке заголовка окна и отправки сообщений уведомления родительскому окну, когда окно мЦивнд активно. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Active*
</dt> <dd>

Период обновления (в миллисекундах). Значение по умолчанию — 500 миллисекунд.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндсетактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





