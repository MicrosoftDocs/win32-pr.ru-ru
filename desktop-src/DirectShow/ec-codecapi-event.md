---
description: '\_ \_ Событие КОДЕКАПИ события EC отправляется кодировщиком для сигнализации о событии кодирования. Клиент регистрируется для события кодировщика путем вызова метода Икодекапи:: Регистерфоревент.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675571"
---
# <a name="ec_codecapi_event"></a>\_событие EC кодекапи \_

\_ \_ Событие КОДЕКАПИ события EC отправляется кодировщиком для сигнализации о событии кодирования. Клиент регистрируется для события кодировщика путем вызова метода [**икодекапи:: регистерфоревент**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Данные пользователя. Значением этого параметра является указатель, указанный вызывающим объектом в параметре *UserData* метода [**регистерфоревент**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Указатель на данные события. Эти данные выделяются кодировщиком и должны быть освобождены приложением с помощью функции **CoTaskMemFree** . Блок данных начинается со структуры [**кодекапиевентдата**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; Приведите параметр *lParam2* к указателю на эту структуру.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет действия по умолчанию.

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

 

 




