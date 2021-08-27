---
description: Для модуля подготовки видео требуется перерисовка.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edd498d84aaace460a10c88d5579c2f5a87bba42e1a5f393786134bbe727af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102794"
---
# <a name="ec_repaint"></a>\_ПЕРЕрисовка EC

Для модуля подготовки видео требуется перерисовка.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного ПИН-кода модуля подготовки видео или **значение NULL**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Параметр *lParam1* может указывать входной ПИН-код модуля подготовки видео. Если да, диспетчер графов фильтров находит ПИН-код вывода, подключенный к этому ПИН-коду, и запрашивает его для интерфейса [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Если выходной ПИН-код поддерживает **имедиаевентсинк**, диспетчер графа фильтров вызывает [**Имедиаевентсинк:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) с \_ кодом события repain EC. Это дает вышестоящему фильтру возможность повторной отправки последней выборки.

Если *lParam1* имеет **значение NULL** или если ПИН-код не поддерживает [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)или если метод [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) завершается неудачей, диспетчер графа фильтра обрабатывает \_ событие перерисовки EC по отдельности. Его поведение зависит от состояния графа:

-   Работает: пропускает событие. (Модуль подготовки отчетов получит следующий пример в потоке.)
-   Приостановлено: выполняет поиск диаграммы в ее текущем расположении, тем самым заменяя фильтр и повторно поставит в очередь данные.
-   Остановлено: Приостановка и остановка графа, таким образом, повторная постановка данных в очередь.

По умолчанию диспетчер графов фильтров не передает это событие в приложение.

## <a name="remarks"></a>Remarks

Модули подготовки видео отправляют это сообщение, когда получают сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) и не имеют данных для отображения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

