---
description: Фильтр не получает достаточно данных.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651628"
---
# <a name="ec_starvation"></a>нехватка ресурсов EC \_

Фильтр не получает достаточно данных.

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

Событие не отправляется в приложение. Если граф фильтра выполняется, диспетчер графа фильтров приостанавливает граф и ждет завершения паузы. Затем он снова запускает граф. Фильтр, отправляющий событие, не должен завершать его работу до тех пор, пока не пойдет достаточно данных для возобновления. Если граф фильтра не работает, диспетчер графа фильтров игнорирует это событие.

## <a name="remarks"></a>Комментарии

Средство синтаксического анализа или фильтр источников может отправить это событие, если поступают слишком мало данных.

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

 

 




