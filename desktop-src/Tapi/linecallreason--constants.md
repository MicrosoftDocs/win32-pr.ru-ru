---
description: '\_Константы побитового флага линекаллреасон описывают причину вызова.'
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Константы LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674895"
---
# <a name="linecallreason_-constants"></a>\_Константы линекаллреасон

Константы побитового флага **линекаллреасон \_** описывают причину вызова.

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**ЛИНЕКАЛЛРЕАСОН \_ каллкомплетион**
</dt> <dd> <dl> <dt>



Вызов был результатом запроса на завершение вызова.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**ЛИНЕКАЛЛРЕАСОН \_ кампедон**
</dt> <dd> <dl> <dt>



В адресе был включен звонок. Обычно он отображается изначально в состоянии onhold и может быть переключен на использование [**линесвафолд**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold). Если активный вызов переходит в состояние простоя, вызов с включенным параметром "в состоянии" может измениться на "предложение", а устройство начнет звонить.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**ЛИНЕКАЛЛРЕАСОН \_ Direct**
</dt> <dd> <dl> <dt>



Это прямой входящий или исходящий вызов.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**ЛИНЕКАЛЛРЕАСОН \_ фвдбуси**
</dt> <dd> <dl> <dt>



Этот вызов был перенаправлен от другого расширения, которое было занято во время вызова.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**ЛИНЕКАЛЛРЕАСОН \_ фвдноансвер**
</dt> <dd> <dl> <dt>



Вызов был перенаправлен от другого расширения, которое не ответило на вызов после некоторого числа колец.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**ЛИНЕКАЛЛРЕАСОН \_ фвдунконд**
</dt> <dd> <dl> <dt>



Вызов был перенаправлен безусловно из другого числа.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**ЛИНЕКАЛЛРЕАСОН \_ атака**
</dt> <dd> <dl> <dt>



Вызов, появляющийся в строке с помощью действия завершения вызова, вызванного другой станцией или действием оператора. В зависимости от реализации переключателя вызов может находиться либо в состоянии Connected, либо на Конференции с существующим активным вызовом в строке.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**ЛИНЕКАЛЛРЕАСОН \_ приостановлено**
</dt> <dd> <dl> <dt>



Звонок был приостановлен по адресу. Обычно он отображается изначально в состоянии onholdии.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**\_Отправка линекаллреасон**
</dt> <dd> <dl> <dt>



Вызов был выбран из другого расширения.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**Перенаправление ЛИНЕКАЛЛРЕАСОН \_**
</dt> <dd> <dl> <dt>



Вызов перенаправляется на эту станцию.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**\_напоминание линекаллреасон**
</dt> <dd> <dl> <dt>



Вызов — это напоминание (или «отзыв») о том, что пользователь придерживается или удерживается (потенциально) длительное время.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**ЛИНЕКАЛЛРЕАСОН \_ раутерекуест**
</dt> <dd> <dl> <dt>



Вызов отображается по адресу, так как параметру требуются инструкции по маршрутизации из приложения. Приложение должно проверить элемент **калледид** в [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)и использовать функцию [**линередирект**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) для предоставления нового набора адресов для вызова. Если вместо этого вызов будет заблокирован, приложение может вызвать [**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop). Если приложению не удается выполнить действие в течение определенного времени ожидания, будет предпринято действие по умолчанию. Поставщик услуг может использовать эту константу только в том случае, если согласованная версия в строке 2,0 или выше. В противном случае поставщик услуг должен заменить ЛИНЕКАЛЛРЕАСОН \_ .


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_Перенос линекаллреасон**
</dt> <dd> <dl> <dt>



Вызов был передан из другого числа.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**ЛИНЕКАЛЛРЕАСОН \_ НЕсвободно**
</dt> <dd> <dl> <dt>



Причина вызова недоступна и не будет известна позже.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**ЛИНЕКАЛЛРЕАСОН \_ неизвестный**
</dt> <dd> <dl> <dt>



Причина вызова в настоящее время неизвестна, но может быть известна позже.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**\_НЕприпаркованный линекаллреасон**
</dt> <dd> <dl> <dt>



Вызов был получен как приостановленный вызов.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

\_Константы линекаллреасон используются в элементе **параметр dwReason** структуры данных [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**линередирект**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[**линесвафолд**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




