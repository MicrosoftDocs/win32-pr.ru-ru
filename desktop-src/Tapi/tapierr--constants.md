---
description: '\_Константы тапиерр предоставляют сведения о сбоях выполнения функций.'
ms.assetid: 6d1cf18b-efeb-4703-9b8e-fce59b61b63f
title: Константы TAPIERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e8a60e2a625ff456a4a8aa2730b80000e92ff54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675174"
---
# <a name="tapierr_-constants"></a>\_Константы тапиерр

**\_ Константы тапиерр** предоставляют сведения о сбоях выполнения функций.

<dl> <dt>

<span id="TAPIERR_CONNECTED"></span><span id="tapierr_connected"></span>**ТАПИЕРР \_ подключен**
</dt> <dd> <dl> <dt>



Операция не может быть выполнена, пока состояние вызова — Connected.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTBUSY"></span><span id="tapierr_destbusy"></span>**ТАПИЕРР \_ дестбуси**
</dt> <dd> <dl> <dt>



Назначение вызова занято.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTNOANSWER"></span><span id="tapierr_destnoanswer"></span>**ТАПИЕРР \_ дестноансвер**
</dt> <dd> <dl> <dt>



Назначение вызова не отвечает.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTUNAVAIL"></span><span id="tapierr_destunavail"></span>**ТАПИЕРР \_ дестунаваил**
</dt> <dd> <dl> <dt>



Назначение вызова недоступно.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICECLASSUNAVAIL"></span><span id="tapierr_deviceclassunavail"></span>**ТАПИЕРР \_ девицеклассунаваил**
</dt> <dd> <dl> <dt>



Необходимый класс устройства недоступен.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEIDUNAVAIL"></span><span id="tapierr_deviceidunavail"></span>**ТАПИЕРР \_ девицеидунаваил**
</dt> <dd> <dl> <dt>



Необходимый идентификатор устройства недоступен.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEINUSE"></span><span id="tapierr_deviceinuse"></span>**ТАПИЕРР \_ девицеинусе**
</dt> <dd> <dl> <dt>



Необходимое устройство уже используется.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DROPPED"></span><span id="tapierr_dropped"></span>**ТАПИЕРР \_ удален**
</dt> <dd> <dl> <dt>



Вызов удален.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDESTADDRESS"></span><span id="tapierr_invaldestaddress"></span>**ТАПИЕРР \_ инвалдестаддресс**
</dt> <dd> <dl> <dt>



Недопустимый указатель на адрес назначения, имеет **значение NULL** или строка конечного адреса слишком длинна.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICECLASS"></span><span id="tapierr_invaldeviceclass"></span>**ТАПИЕРР \_ инвалдевицекласс**
</dt> <dd> <dl> <dt>



Запрошен недопустимый класс устройства.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICEID"></span><span id="tapierr_invaldeviceid"></span>**ТАПИЕРР \_ инвалдевицеид**
</dt> <dd> <dl> <dt>



Запрошен недопустимый идентификатор класса устройства.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALPOINTER"></span><span id="tapierr_invalpointer"></span>**ТАПИЕРР \_ инвалпоинтер**
</dt> <dd> <dl> <dt>



Указатель не ссылается на допустимое расположение в памяти. Один или несколько указателей *лпсздестаддресс*, *лпсзаппнаме*, *лпсзкалледпарти* или *лпсзкоммент* были указаны, но являются недопустимыми.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALWINDOWHANDLE"></span><span id="tapierr_invalwindowhandle"></span>**ТАПИЕРР \_ инвалвиндовхандле**
</dt> <dd> <dl> <dt>



Недопустимый маркер окна.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOREQUESTRECIPIENT"></span><span id="tapierr_norequestrecipient"></span>**ТАПИЕРР \_ норекуестреЦипиент**
</dt> <dd> <dl> <dt>



Для выполнения запроса не доступно ни одного приложения получателя. Пользователь должен запустить приложение получателя и повторить попытку.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOTADMIN"></span><span id="tapierr_notadmin"></span>**ТАПИЕРР \_ нотадмин**
</dt> <dd> <dl> <dt>



Для запрошенной операции требуются права администратора.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTCANCELLED"></span><span id="tapierr_requestcancelled"></span>**ТАПИЕРР \_ рекуестканцеллед**
</dt> <dd> <dl> <dt>



Запрос на поддержку телефонии был отменен.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTFAILED"></span><span id="tapierr_requestfailed"></span>**ТАПИЕРР \_ рекуестфаилед**
</dt> <dd> <dl> <dt>



Запрос не выполнен по неопределенным причинам.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTQUEUEFULL"></span><span id="tapierr_requestqueuefull"></span>**ТАПИЕРР \_ рекуесткуеуефулл**
</dt> <dd> <dl> <dt>



Приложение-получатель активно, но очередь запросов заполнена, или недостаточно памяти для расширения очереди. Приложение может повторить попытку позже.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNREQUESTID"></span><span id="tapierr_unknownrequestid"></span>**ТАПИЕРР \_ ункновнрекуестид**
</dt> <dd> <dl> <dt>



Недопустимый идентификатор запроса, на который указывает ссылка.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNWINHANDLE"></span><span id="tapierr_unknownwinhandle"></span>**ТАПИЕРР \_ ункновнвинхандле**
</dt> <dd> <dl> <dt>



Ссылка на неизвестный маркер окна.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Все остальные \_ значения тапиерр являются устаревшими и не должны использоваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




