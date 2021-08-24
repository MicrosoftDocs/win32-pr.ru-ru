---
description: Отправляется фильтром модуля записи WM ASF при завершении предварительной обработки многопроходной кодировки.
ms.assetid: 2029afc4-419c-494a-ae52-1f84b08bcb35
title: EC_PREPROCESS_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df07444c501ea89ec0d19f3f727e8325953e3c06f740562f7ec058eafa987fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537004"
---
# <a name="ec_preprocess_complete"></a>\_Предварительная обработка EC \_ завершена

Отправляется фильтром [модуля записи WM ASF](wm-asf-writer-filter.md) при завершении предварительной обработки многопроходной кодировки.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ноль.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Отсутствует.

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

 

 




