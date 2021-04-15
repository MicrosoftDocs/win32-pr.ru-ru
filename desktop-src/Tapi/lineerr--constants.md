---
description: Ниже приведен список кодов ошибок, которые может возвращать TAPI при вызове операций в строках, адресах или вызовах.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Константы LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689472"
---
# <a name="lineerr_-constants"></a>\_Константы линирр

Ниже приведен список кодов ошибок, которые может возвращать TAPI при вызове операций в строках, адресах или вызовах. Дополнительные сведения о том, как определить, какие из этих кодов ошибок может возвращать конкретная функция, см. в описании отдельных функций.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**ЛИНИРР \_ аддрессблоккед**
</dt> <dd> <dl> <dt>



Указанный адрес заблокирован из-за указанного вызова.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**ЛИНИРР \_ аддрессблоккед**
</dt> <dd> <dl> <dt>



Для целевого адреса вызова включена блокировка вызовов.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**ЛИНИРР \_ выделен**
</dt> <dd> <dl> <dt>



Строка не может быть открыта из-за устойчивого состояния, например в том, что последовательный порт открыт в монопольном режиме другим процессом.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**ЛИНИРР \_ баддевицеид**
</dt> <dd> <dl> <dt>



Указанный идентификатор устройства или строки идентификатора устройства, например в параметре *двдевицеид* , является недопустимым или выходит за пределы допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**ЛИНИРР \_ беарермодеунаваил**
</dt> <dd> <dl> <dt>



Недопустимый член режима носителя в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , режим носителя, указанный в **линекаллпарамс** , недоступен, или режим носителя вызова не может быть изменен на указанный режим носителя.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**ЛИНИРР \_ биллингрежектед**
</dt> <dd> <dl> <dt>



Режим выставления счетов для вызова был отклонен.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**ЛИНИРР \_ каллунаваил**
</dt> <dd> <dl> <dt>



Все представления вызовов по указанному адресу сейчас используются.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**ЛИНИРР \_ комплетионоверрун**
</dt> <dd> <dl> <dt>



Превышено максимальное число незавершенных завершений вызова.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**ЛИНИРР \_ конференцефулл**
</dt> <dd> <dl> <dt>



Достигнуто максимальное число сторон для Конференции, или запрошенное число сторон не может быть удовлетворено.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**ЛИНИРР \_ диалбиллинг**
</dt> <dd> <dl> <dt>



Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**ЛИНИРР \_ диалдиалтоне**
</dt> <dd> <dl> <dt>



Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**ЛИНИРР \_ диалпромпт**
</dt> <dd> <dl> <dt>



Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**ЛИНИРР \_ диалкуиет**
</dt> <dd> <dl> <dt>



Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**ЛИНИРР \_ диалвоицедетект**
</dt> <dd> <dl> <dt>



Использование модификатора набора номера (:) не поддерживается. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**ЛИНИРР \_ отключен**
</dt> <dd> <dl> <dt>



Вызов был отключен. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,2 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**ЛИНИРР \_ инкомпатиблеапиверсион**
</dt> <dd> <dl> <dt>



Приложение запросило версию или диапазон версий TAPI, которые либо несовместимы с, либо не поддерживаются в, реализацией API телефонии и соответствующим поставщиком услуг.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**ЛИНИРР \_ инкомпатибликстверсион**
</dt> <dd> <dl> <dt>



Приложение запросило диапазон версий расширения, которое либо недопустимо, либо не может поддерживаться соответствующим поставщиком услуг.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**ЛИНИРР \_ инифилекоррупт**
</dt> <dd> <dl> <dt>



TAPI-файл не может быть правильно прочитан или понят из-за внутренних несоответствий или ошибок форматирования. Telephon.ini Например, \[ \] раздел расположения, \[ карточки \] или \[ страны \] Telephon.ini файла может быть поврежден или непоследовательен.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**ЛИНИРР \_ INUSE**
</dt> <dd> <dl> <dt>



Линейное устройство используется и сейчас не может быть настроено, допускает добавление стороны, позволяет получить ответ на вызов, разрешить помещение вызова или разрешить передачу вызова.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**ЛИНИРР \_ инваладдресс**
</dt> <dd> <dl> <dt>



Указанный адрес недопустим или запрещен. Если значение недопустимо, адрес содержит недопустимые символы или цифры, либо адрес назначения содержит управляющие символы набора номера (W, @, $ или?), которые не поддерживаются поставщиком услуг. Если не разрешено, указанный адрес либо не назначается указанной строке, либо недопустим для перенаправления адреса.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**ЛИНИРР \_ инваладдрессид**
</dt> <dd> <dl> <dt>



Указанный идентификатор адреса недопустим или выходит за пределы допустимого диапазона.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**ЛИНИРР \_ инваладдрессмоде**
</dt> <dd> <dl> <dt>



Указан недопустимый режим адреса.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**ЛИНИРР \_ инваладдрессстате**
</dt> <dd> <dl> <dt>



Указанное состояние адреса содержит один или несколько битов, которые не являются [**\_ константами линеаддрессстате**](lineaddressstate--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**ЛИНИРР \_ инваладдресстипе**
</dt> <dd> <dl> <dt>



Приложение ссылается на недопустимый тип адреса. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 3,0 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**ЛИНИРР \_ инвалажентактивити**
</dt> <dd> <dl> <dt>



Указанное действие агента недопустимо.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**ЛИНИРР \_ инвалажентактивити**
</dt> <dd> <dl> <dt>



Приложение, вызывающее эту операцию, является целевым объектом косвенной передачи. То есть TAPI определил, что вызывающее приложение также является приложением с наивысшим приоритетом для данного типа носителя. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**ЛИНИРР \_ инвалажентграуп**
</dt> <dd> <dl> <dt>



Указанные сведения о группе агентов недопустимы или содержат ошибки. Запрошенное действие не выполнено.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**ЛИНИРР \_ инвалажентграуп**
</dt> <dd> <dl> <dt>



Приложение ссылается на недопустимую группу агентов. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**ЛИНИРР \_ инвалажентид**
</dt> <dd> <dl> <dt>



Указан недопустимый идентификатор агента.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**ЛИНИРР \_ инвалажентид**
</dt> <dd> <dl> <dt>



Использован недопустимый идентификатор агента. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**ЛИНИРР \_ инвалажентсессионстате**
</dt> <dd> <dl> <dt>



Недопустимое состояние сеанса агента. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,2 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**ЛИНИРР \_ инвалажентстате**
</dt> <dd> <dl> <dt>



Указанное состояние агента недопустимо или содержит ошибки. В состояние агента указанного адреса не внесены изменения.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**ЛИНИРР \_ инвалажентстате**
</dt> <dd> <dl> <dt>



Приложение ссылается на недопустимое состояние агента. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**ЛИНИРР \_ инвалапфандле**
</dt> <dd> <dl> <dt>



Недопустимый маркер приложения (например, заданный параметром *хлинеапп* ) или регистрационный маркер приложения.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**ЛИНИРР \_ инвалаппнаме**
</dt> <dd> <dl> <dt>



Указано недопустимое имя приложения. Если имя приложения задано приложением, предполагается, что строка не содержит какие-либо символы, которые не удается воспроизвести, и завершается нулем.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**ЛИНИРР \_ инвалбеарермоде**
</dt> <dd> <dl> <dt>



Указан недопустимый режим носителя.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**ЛИНИРР \_ инвалкаллкомплмоде**
</dt> <dd> <dl> <dt>



Указано недопустимое завершение.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**ЛИНИРР \_ инвалкаллхандле**
</dt> <dd> <dl> <dt>



Указан недопустимый маркер вызова. Например, маркер не равен **null** , но не принадлежит данной строке. В некоторых случаях указанный маркер устройства вызова является недопустимым.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**ЛИНИРР \_ инвалкаллпарамс**
</dt> <dd> <dl> <dt>



Указаны недопустимые параметры вызова.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**ЛИНИРР \_ инвалкаллпривилеже**
</dt> <dd> <dl> <dt>



Указанный параметр привилегии вызова недопустим.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**ЛИНИРР \_ инвалкаллселект**
</dt> <dd> <dl> <dt>



Указан недопустимый параметр SELECT.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**ЛИНИРР \_ инвалкаллстате**
</dt> <dd> <dl> <dt>



Текущее состояние вызова находится в недопустимом состоянии для запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**ЛИНИРР \_ инвалкаллстателист**
</dt> <dd> <dl> <dt>



Указан недопустимый список состояний вызова.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**ЛИНИРР \_ инвалкард**
</dt> <dd> <dl> <dt>



Не удалось найти постоянный идентификатор карты, указанный в *двкард* , в любой записи в \[ разделе "карточки" \] в реестре.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**ЛИНИРР \_ инвалкомплетионид**
</dt> <dd> <dl> <dt>



Недопустимый идентификатор завершения.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**ЛИНИРР \_ инвалконфкаллхандле**
</dt> <dd> <dl> <dt>



Указанный маркер вызова для вызова конференции является недопустимым или не является обработчиком для вызова конференции.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**ЛИНИРР \_ инвалконсулткаллхандле**
</dt> <dd> <dl> <dt>



Указан недопустимый описатель вызова консультации.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**ЛИНИРР \_ инвалкаунтрикоде**
</dt> <dd> <dl> <dt>



Указан недопустимый код страны или региона.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**ЛИНИРР \_ инвалдевицекласс**
</dt> <dd> <dl> <dt>



Устройство линии не имеет связанного устройства для данного класса устройств, или указанная строка не поддерживает указанный класс устройства.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**ЛИНИРР \_ инвалдевицехандле**
</dt> <dd> <dl> <dt>



Недопустимый маркер устройства линии.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**ЛИНИРР \_ инвалдиалпарамс**
</dt> <dd> <dl> <dt>



Недопустимые параметры набора номера.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**ЛИНИРР \_ инвалдигитлист**
</dt> <dd> <dl> <dt>



Указан недопустимый список цифр.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**ЛИНИРР \_ инвалдигитмоде**
</dt> <dd> <dl> <dt>



Указан недопустимый цифровой режим.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**ЛИНИРР \_ инвалдигитс**
</dt> <dd> <dl> <dt>



Указаны недопустимые цифры завершения.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**ЛИНИРР \_ инвалекстверсион**
</dt> <dd> <dl> <dt>



Недопустимый номер версии расширения поставщика услуг.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**ЛИНИРР \_ инвалфеатуре**
</dt> <dd> <dl> <dt>



Недопустимый параметр *двфеатуре* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**ЛИНИРР \_ инвалфеатуре**
</dt> <dd> <dl> <dt>



Приложение вызвало функцию, недоступную в этой строке.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**ЛИНИРР \_ инвалграупид**
</dt> <dd> <dl> <dt>



Указан недопустимый идентификатор группы.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**ЛИНИРР \_ инваллинехандле**
</dt> <dd> <dl> <dt>



Указанный вызов, устройство, устройство линии или маркер строки недопустимы.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**ЛИНИРР \_ инваллинестате**
</dt> <dd> <dl> <dt>



Конфигурация устройства не может быть изменена в текущем состоянии строки. Строка может использоваться другим приложением, или параметр *двлинестатес* содержит один или несколько битов, которые не являются [ \_ константами линедевстате](linedevstate--constants.md). Значение **линирр \_ инваллинестате** также может указывать на то, что устройство отключено или находится вне обслуживания. Эти состояния обозначаются заданием битов, соответствующих значениям *линедевстатусфлагс \_ Connected* и *линедевстатусфлагсing \_* , равными 0 в элементе **Двдевстатусфлагс** структуры [**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) , возвращаемой функцией [**линежетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**ЛИНИРР \_ инваллокатион**
</dt> <dd> <dl> <dt>



Не удалось найти постоянный идентификатор расположения, указанный в *двлокатион* , ни в одной записи в \[ разделе Locations \] в реестре.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**ЛИНИРР \_ инвалмедиалист**
</dt> <dd> <dl> <dt>



Указан недопустимый список носителей.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**ЛИНИРР \_ инвалмедиамоде**
</dt> <dd> <dl> <dt>



Список типов мультимедиа (режимов) для отслеживания содержит недопустимые данные, указанный параметр типа носителя является недопустимым, или поставщик услуг не поддерживает указанный тип носителя. Типы мультимедиа, поддерживаемые в строке, перечислены в элементе **двмедиамодес** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**ЛИНИРР \_ инвалмессажеид**
</dt> <dd> <dl> <dt>



Число, заданное в *двмессажеид* , находится вне диапазона, заданного элементом **Двнумкомплетионмессажес** в структуре [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**ЛИНИРР \_ инвалпарам**
</dt> <dd> <dl> <dt>



Параметр или структура, на которые указывает параметр, содержит недопустимые сведения, код страны или региона недопустим, недопустимый указатель окна или указанный параметр прямого списка содержит недопустимые данные.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**ЛИНИРР \_ инвалпаркид**
</dt> <dd> <dl> <dt>



Недопустимый идентификатор парковки.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**ЛИНИРР \_ инвалпаркмоде**
</dt> <dd> <dl> <dt>



Указан недопустимый режим парковки.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**ЛИНИРР \_ инвалпассворд**
</dt> <dd> <dl> <dt>



Указан неправильный пароль, запрошенное действие не выполнено.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**ЛИНИРР \_ инвалпассворд**
</dt> <dd> <dl> <dt>



Приложение использовало недопустимый пароль. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**ЛИНИРР \_ инвалпоинтер**
</dt> <dd> <dl> <dt>



Один или несколько указанных параметров указателя (например, *лпкалллист*, *лпдвапиверсион*, *лпекстенсионид*, *лпдвекстверсион*, *лфикон*, *лплинедевкапс* и *Лптонелист*) недопустимы, или необходим указатель на выходной параметр **со значением NULL**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**ЛИНИРР \_ инвалпривселект**
</dt> <dd> <dl> <dt>



Для параметра *двпривилежес* был задан недопустимый флаг или сочетание флагов.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**ЛИНИРР \_ инвалрате**
</dt> <dd> <dl> <dt>



Указана недопустимая скорость.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**ЛИНИРР \_ инвалрекуестмоде**
</dt> <dd> <dl> <dt>



Недопустимый индикатор [**линерекуестмоде**](linerequestmode--constants.md) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**ЛИНИРР \_ инвалтерминалид**
</dt> <dd> <dl> <dt>



Указан недопустимый идентификатор терминала.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**ЛИНИРР \_ инвалтерминалмоде**
</dt> <dd> <dl> <dt>



Указан недопустимый параметр режимов терминала.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**ЛИНИРР \_ инвалтимеаут**
</dt> <dd> <dl> <dt>



Значения времени ожидания не поддерживаются, или значение выходит за пределы допустимого диапазона, указанного в [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**ЛИНИРР \_ инвалтоне**
</dt> <dd> <dl> <dt>



Указанный пользовательский тон не представляет допустимый тон или состоит из слишком большого числа частот или если указанная структура тона не описывает допустимый тон.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**ЛИНИРР \_ инвалтонелист**
</dt> <dd> <dl> <dt>



Указан недопустимый список тонов.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**ЛИНИРР \_ инвалтонемоде**
</dt> <dd> <dl> <dt>



Указан недопустимый параметр "тоновый режим".


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**ЛИНИРР \_ инвалтрансфермоде**
</dt> <dd> <dl> <dt>



Указан недопустимый параметр режима пересылки.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**ЛИНИРР \_ линемапперфаилед**
</dt> <dd> <dl> <dt>



ЛИНЕМАППЕР было передано значение, переданное в параметре *двдевицеид* , но строки, соответствующие требованиям, указанным в параметре *лпкаллпарамс* , не найдены.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**ЛИНИРРная \_ Конференция**
</dt> <dd> <dl> <dt>



Указанный вызов не является обработчиком вызова конференции или вызовом участника.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**\_устройство линирр**
</dt> <dd> <dl> <dt>



Указанный идентификатор устройства, который ранее был действителен, больше не принимается, так как связанное устройство было удалено из системы с момента последней инициализации TAPI. Кроме того, устройство линии не имеет связанного устройства для данного класса устройств.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**ЛИНИРР \_ Drive**
</dt> <dd> <dl> <dt>



Не удалось найти Tapiaddr.dll или поставщик телефонной службы для указанного устройства обнаружил, что один из его компонентов отсутствует или поврежден, так как он не был обнаружен во время инициализации. Чтобы устранить проблему, пользователю рекомендуется использовать панель управления телефонии.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**ЛИНИРР \_ номем**
</dt> <dd> <dl> <dt>



Недостаточно памяти для выполнения операции или не удалось заблокировать память.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**ЛИНИРР \_ номултиплеинстанце**
</dt> <dd> <dl> <dt>



Поставщик услуг телефонии, который не поддерживает несколько экземпляров, несколько раз указан в \[ \] разделе поставщиков в реестре. Приложение должно рекомендовать пользователю использовать панель управления телефонии для удаления повторяющегося драйвера.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**ЛИНИРР \_ номултиплеинстанце**
</dt> <dd> <dl> <dt>



Несколько экземпляров этого поставщика услуг не допускаются.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**ЛИНИРР, \_ запрос**
</dt> <dd> <dl> <dt>



В настоящее время нет запроса, ожидающего указанного режима, или приложение больше не является приложением с наивысшим приоритетом для указанного режима запроса.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**ЛИНИРР \_**
</dt> <dd> <dl> <dt>



Приложение не имеет прав владельца на указанный вызов.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**ЛИНИРР \_ зарегистрировано**
</dt> <dd> <dl> <dt>



Приложение не зарегистрировано как получатель запроса для указанного режима запроса.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**ЛИНИРР \_ оператионфаилед**
</dt> <dd> <dl> <dt>



Не удалось выполнить операцию по неопределенной или неизвестной причине.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**ЛИНИРР \_ оператионунаваил**
</dt> <dd> <dl> <dt>



Операция недоступна, например для данного устройства или указанной строки.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**ЛИНИРР \_ ратеунаваил**
</dt> <dd> <dl> <dt>



В настоящее время поставщик услуг не имеет достаточной пропускной способности, доступной для указанной скорости.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**ЛИНИРР \_ REinit**
</dt> <dd> <dl> <dt>



Если была запрошена повторная инициализация TAPI, например, в результате добавления или удаления поставщика услуг телефонии, то запросы [**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)или [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) отклоняются с этой ошибкой до тех пор, пока Последнее приложение не завершит использование API (с помощью [**линешутдовн**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), когда новая конфигурация вступит в силу и приложения снова смогут вызвать **линеинитиализе** или **линеинитиализикс**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**ЛИНИРР \_ REinit**
</dt> <dd> <dl> <dt>



Приложение попыталось инициализировать TAPI дважды.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**ЛИНИРР \_ рекуестоверрун**
</dt> <dd> <dl> <dt>



Количество запросов в ожидании, чем устройство может быть обработано.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**ЛИНИРР \_ ресаурцеунаваил**
</dt> <dd> <dl> <dt>



Недостаточно ресурсов для завершения операции. Например, строку нельзя открыть из-за перерасхода динамических ресурсов.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**ЛИНИРР \_ структуретусмалл**
</dt> <dd> <dl> <dt>



Элемент **двтоталсизе** структуры не указывает достаточно памяти для хранения фиксированной части указанной структуры.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**ЛИНИРР \_ таржетнотфаунд**
</dt> <dd> <dl> <dt>



Не найден целевой объект для перенаправления вызова. Это может произойти, если именованное приложение не открывало бы ту же строку с \_ битом владельца линекаллпривилеже в  параметре двпривилежес [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen). Или, в случае передачи в режиме мультимедиа, ни одно приложение не открывало в \_ параметре *двпривилежес* [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) и тип мультимедиа, указанный в *параметре* *ДВМЕДИАМОДЕС* [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen), ни одна строка с битом линекаллпривилеже Owner.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**ЛИНИРР \_ таржетселф**
</dt> <dd> <dl> <dt>



Приложение, вызывающее эту операцию, является целевым объектом косвенной передачи. То есть TAPI определил, что вызывающее приложение также является приложением с наивысшим приоритетом для данного типа носителя.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**ЛИНИРР не \_ инициализирован**
</dt> <dd> <dl> <dt>



Операция была вызвана до любого приложения с именем [**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) или [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**ЛИНИРР \_ усерканцеллед**
</dt> <dd> <dl> <dt>



Пользователь отменил вызов. Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,2 или более поздней.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**ЛИНИРР \_ усерусеринфотубиг**
</dt> <dd> <dl> <dt>



Строка, содержащая сведения о пользователе пользователя, превышает максимальное число байтов, указанное в элементе **двууиакцептсизе**, **двууиансверсизе**, **двууидропсизе**, **двууимакекаллсизе** или **двууисендусерусеринфосизе** в [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), либо строка, содержащая сведения о пользователе пользователя, слишком длинная.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Значения 0xC0000000 до 0xFFFFFFFF доступны для расширений устройств. Значения от 0x80000000 до 0xBFFFFFFF зарезервированы, а в качестве идентификаторов запросов используется 0x00000000 – 0x7FFFFFFF.

Если приложение получает сообщение об ошибке, возвращающее, что оно не обрабатывается специально (например, сообщение об ошибке, определенное расширением конкретного устройства), оно должно рассматривать ошибку как ЛИНИРР \_ оператионфаилед (по неизвестной причине).

При вызове констант ЛИНИРР, которые \_ являются новыми для TAPI 3,0, необходимо обновить файл Tapierr.MC новыми сообщениями.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**линежетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**линешутдовн**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




