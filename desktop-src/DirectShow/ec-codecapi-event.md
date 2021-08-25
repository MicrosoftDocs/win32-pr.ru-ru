---
description: '\_ \_ Событие КОДЕКАПИ события EC отправляется кодировщиком для сигнализации о событии кодирования. Клиент регистрируется для события кодировщика путем вызова метода Икодекапи:: Регистерфоревент.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5765c2a1156653e66c5d3685cacfdd551cd22032eea34463f5450dc6d4fbea3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965944"
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
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




