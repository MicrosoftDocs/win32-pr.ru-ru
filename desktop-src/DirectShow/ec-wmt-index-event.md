---
description: Отправляется, когда приложение использует фильтр модуля записи WM ASF для индексирования видеофайлов Windows Media.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675443"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (DShow. h)

Отправляется, когда приложение использует фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) для индексирования видеофайлов Windows Media.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Может быть одним из следующих сообщений **\_ о состоянии ВМТ** .



| Значение                | Описание              |
|----------------------|--------------------------|
| ВМТ \_ запущен         | Индексирование начато.      |
| ВМТ \_ закрыт          | Индексирование завершено.  |
| \_ \_ ход выполнения индекса ВМТ | Выполняется индексирование. |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Если *LPARAM1* ВМТ \_ Closed или ВМТ \_ Started, то *lParam2* равен нулю. Если *lParam1* является ВМТ \_ \_ ходом выполнения индекса, то *lParam2* — это **DWORD** , который указывает текущий ход выполнения в процентах от общего размера загрузки.

</dd> </dl>

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

 

 




