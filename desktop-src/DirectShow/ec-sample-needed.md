---
description: Запрашивает новый входной пример из расширенного фильтра модуля подготовки видео (Евр).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0058f8d0b7f8404a59f8c7e4fc5a4029c5ebaf4bc4f5c1b2678b1ed8c0f4f90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686124"
---
# <a name="ec_sample_needed"></a>\_требуется образец \_ EC

Запрашивает новый входной пример из [**расширенного фильтра модуля подготовки видео**](enhanced-video-renderer-filter.md) (Евр).

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Идентификатор входного потока, которому требуются новые входные данные.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Микшер для фильтра Евр отправляет это сообщение, когда ему нужен новый входной пример.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> </dl>

 

 




