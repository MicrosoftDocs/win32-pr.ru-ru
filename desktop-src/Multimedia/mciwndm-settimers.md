---
title: Сообщение MCIWNDM_SETTIMERS (VFW. h)
description: Сообщение МЦИВНДМ \_ сеттимерс задает периоды обновления, используемые мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении, отображаемых в строке заголовка окна, и отправки сообщений уведомления родительскому окну.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- сообщение MCIWNDM_SETTIMERS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9c17a131827459555ae51adc5d5bd48d98fabb88fc4c1f0dbbcd1eb3673466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807563"
---
# <a name="mciwndm_settimers-message"></a>\_Сообщение мЦивндм сеттимерс

Сообщение **мЦивндм \_ сеттимерс** задает периоды обновления, используемые мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении, отображаемых в строке заголовка окна, и отправки сообщений уведомления родительскому окну. Это сообщение можно отправить явно или с помощью макроса [**мЦивндсеттимерс**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Active*
</dt> <dd>

Период обновления, используемый МЦивнд, если это активное окно. Значение по умолчанию — 500 миллисекунд. служба хранилища для этого значения ограничено 16 битами.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*Активный*
</dt> <dd>

Период обновления, используемый МЦивнд, если это неактивное окно. Значение по умолчанию — 2000 миллисекунд. служба хранилища для этого значения ограничено 16 битами.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мЦивндсеттимерс**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





