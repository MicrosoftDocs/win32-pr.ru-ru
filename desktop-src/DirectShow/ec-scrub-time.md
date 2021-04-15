---
description: Задает отметку времени для последнего шага кадра.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675755"
---
# <a name="ec_scrub_time"></a>\_время очистки \_ EC

Задает отметку времени для последнего шага кадра.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Нижний 32 бит метки времени.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Верхний 32 бит метки времени.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Выступающий для фильтра " [**Улучшенный обработчик видео**](enhanced-video-renderer-filter.md) " (Евр) отправляет это сообщение в Евр при завершении шага кадра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> </dl>

 

 




