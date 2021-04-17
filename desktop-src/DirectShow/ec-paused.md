---
description: Запрос на приостановку выполнен.
ms.assetid: 32acad47-65bd-42f0-987e-3690bb824b05
title: EC_PAUSED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa25a2f32f191519e55e286dac52542bcef949a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674822"
---
# <a name="ec_paused"></a>EC \_ приостановлено

Запрос на приостановку выполнен.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Состояние приостановки выполнения операции.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Диспетчер графов фильтров отправляет это событие при завершении команды асинхронной паузы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




