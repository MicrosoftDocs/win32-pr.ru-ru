---
description: Указывает, насколько далеко позади расписания компонент предназначен для обработки образцов.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685068"
---
# <a name="ec_sample_latency"></a>\_пример \_ задержки для EC

Указывает, насколько далеко позади расписания компонент предназначен для обработки образцов.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**\_ время ссылки на константу** \* ) расстояние от компонента до, в 100-наносекундных единицах. Если это значение положительное, компонент отстает от расписания. Если это значение отрицательное, компонент опережает расписание.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Пользовательский выступающий для фильтра [**расширенного обработчика видео**](enhanced-video-renderer-filter.md) (Евр) может отправить это сообщение в евр, чтобы уведомить Евр о том, что средство находится за расписанием или с опережением расписания.

Самый простой способ вычислить *lParam1* : *QPC Now*   *QPC Target*, где *QPC Now* — это время, а *QPC целевой объект* — время презентации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Написание выступающего Евр](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

