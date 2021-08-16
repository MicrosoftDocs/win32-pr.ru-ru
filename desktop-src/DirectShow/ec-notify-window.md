---
description: Уведомляет фильтр окна модуля подготовки видео.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355d4ec8b5b6bea55a2f32f01cc2f83aabeab84443b28e431e5b0d6155acc6d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820116"
---
# <a name="ec_notify_window"></a>\_окно уведомления \_ EC

Уведомляет фильтр окна модуля подготовки видео.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HWND**) Обработчик для окна.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Это событие используется внутренне DirectShow. Диспетчер графов фильтров не передает это событие в приложение. Приложения не могут переопределять действие по умолчанию для этого события.

## <a name="remarks"></a>Remarks

При подключении модуля обработки видео он проверяет, поддерживает ли выходной ПИН-код вышестоящего выхода интерфейс [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Если это так, модуль подготовки отчетов отправляет это событие в вышестоящий фильтр.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




