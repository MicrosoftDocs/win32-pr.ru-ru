---
description: Посылается, когда VMR выбрал механизм рендеринга.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2c8bef78156c4438e1e4e7aea45326562002ed8f4a3786377d7ee43a00a57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015862"
---
# <a name="ec_vmr_renderdevice_set"></a>\_ \_ набор рендердевицеов EC VMR \_

Посылается, когда VMR выбрал механизм рендеринга.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Может иметь одно из следующих значений:



| Значение                        | Значение                                                  |
|------------------------------|----------------------------------------------------------|
| \_ \_ наложение устройства VMR \_ | VMR будет отображаться на поверхности наложения (только VMR-7). |
| VMR \_ отрисовывает \_ устройство \_ видмем  | Фильтр VMR будет отображаться в видеопамяти.                     |
| VMR \_ отрисовывает \_ устройство \_ сисмем  | Фильтр VMR будет отображаться в системной памяти (только VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это событие отправляется с помощью VMR-7 и VMR-9 и перенаправляется в приложения. Обратите внимание, что VMR-9 поддерживает только целевые объекты отрисовки видео в памяти.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




