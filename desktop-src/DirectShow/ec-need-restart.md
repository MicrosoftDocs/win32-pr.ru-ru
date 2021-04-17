---
description: Фильтр запрашивает перезапуск графа.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674824"
---
# <a name="ec_need_restart"></a>EC \_ требуется \_ Перезагрузка

Фильтр запрашивает перезапуск графа.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ноль.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Диспетчер графов фильтров приостанавливает и перезапускает граф. Он не передает событие в приложение.

## <a name="remarks"></a>Комментарии

Если фильтр отклоняет выборку в середине потока, восходящий ПИН-код перестанет предоставлять образцы. Фильтр может перезапустить поток, отправив это событие. Например, модуль подготовки звука может потерять доступ к звуковому устройству, так как в окне видео теряется фокус. На этом этапе модуль подготовки звука начинает отклонять образцы. Когда он восстанавливает доступ к звуковому устройству, он отправляет это событие для перезапуска аудиопотока.

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

 

 




