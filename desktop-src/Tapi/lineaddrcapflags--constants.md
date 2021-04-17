---
description: '\_Константы битового флага линеаддркапфлагс используются в элементе дваддркапфлагс структуры данных линеаддресскапс для описания различных возможностей логического адреса.'
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Константы LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685340"
---
# <a name="lineaddrcapflags_-constants"></a>\_Константы линеаддркапфлагс

 \_ Константы битового флага линеаддркапфлагс используются в элементе **дваддркапфлагс** структуры данных [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) для описания различных возможностей логического адреса.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**ЛИНЕАДДРКАПФЛАГС \_ акцепттоалерт**
</dt> <dd> <dl> <dt>



**Значение true** , если вызов предложения должен быть принят с помощью [**линеакцепт**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) , чтобы начать предупреждать пользователей на обоих концах вызова; в противном случае — **значение false**. Обычно это используется только с ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**ЛИНЕАДДРКАПФЛАГС \_ акдграуп**
</dt> <dd> <dl> <dt>



Адрес поддерживает [ACD Groups](about-call-center-controls.md#acd-group-object) в связи с операциями центра обработки вызовов. Дополнительные сведения о ACDных группах см. в разделе [об элементах управления центра обработки вызовов](./about-call-center-controls.md) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**ЛИНЕАДДРКАПФЛАГС \_ аутореконнект**
</dt> <dd> <dl> <dt>



Указывает, будет ли автоматически повторно подключаться к вызову на удержании консультации. **Значение true** , если повторное соединение происходит автоматически; в противном случае — **значение false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**ЛИНЕАДДРКАПФЛАГС \_ блоккиддефаулт**
</dt> <dd> <dl> <dt>



Указывает, отправляет ли сеть по умолчанию или блокирует сведения об ИДЕНТИФИКАТОРе вызывающего объекта при выполнении вызова по этому адресу. Если **значение — true**, сведения об идентификаторе блокируются по умолчанию; Если **значение равно false**, сведения об идентификаторе передаются по умолчанию.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**ЛИНЕАДДРКАПФЛАГС \_ блоккидоверриде**
</dt> <dd> <dl> <dt>



Указывает, можно ли переопределить параметр по умолчанию для отправки или блокировки сведений об ИДЕНТИФИКАТОРе вызывающего объекта по вызову. При **значении true** переопределение возможно; Если **значение равно false**, переопределение невозможно.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**ЛИНЕАДДРКАПФЛАГС \_ комплетионид**
</dt> <dd> <dl> <dt>



Указывает, являются ли идентификаторы завершения, возвращаемые [**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) , полезными и уникальными. **Значение true** , если полезно; в противном случае — **значение false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**ЛИНЕАДДРКАПФЛАГС \_ конфдроп**
</dt> <dd> <dl> <dt>



**Значение true** , если [**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop) на родительском вызове Конференции также имеет побочный результат удаления (то есть отсоединения) с другими сторонами, участвующими в вызове конференции; **Значение false** , если вызов конференции по-прежнему позволяет другим сторонам общаться друг с другом.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**ЛИНЕАДДРКАПФЛАГС \_ конференцехелд**
</dt> <dd> <dl> <dt>



Указывает, можно ли выполнить принудительное обращение к нежестко удерживаемому вызову. Часто в качестве вызова конференции можно добавить только вызовы с удержанием на консультации.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**ЛИНЕАДДРКАПФЛАГС \_ конференцемаке**
</dt> <dd> <dl> <dt>



Указывает, можно ли установить полностью новый вызов для использования в качестве вызова консультации (для добавления) на Конференции.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**ЛИНЕАДДРКАПФЛАГС \_ дестоффхук**
</dt> <dd> <dl> <dt>



Указывает, может ли телефон вызываемой стороны автоматически принудительно оффхук при совершении вызовов.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**ЛИНЕАДДРКАПФЛАГС \_ набор**
</dt> <dd> <dl> <dt>



Указывает, можно ли набрать адрес назначения по этому адресу для выполнения вызова. **Значение true** , если адрес назначения должен быть набран; **Значение false** , если адрес назначения фиксирован (как и "горячий телефон").


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдбусинааддр**
</dt> <dd> <dl> <dt>



Указывает, могут ли пересылать вызовы для занятости и без ответов использовать разные адреса перенаправления. Этот флаг имеет смысл только в том случае, если перенаправление в состояние «занято» и «без ответа» можно контролировать отдельно. Этот флаг имеет **значение true** , если пересылка в занятом состоянии и без ответа может использовать другие адреса назначения. в противном случае — **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдконсулт**
</dt> <dd> <dl> <dt>



Указывает, включает ли переадресация вызовов установку вызова консультации.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдинтекстаддр**
</dt> <dd> <dl> <dt>



Указывает, могут ли внутренние и внешние вызовы перенаправляться на разные адреса пересылки. Этот флаг имеет смысл только в том случае, если переадресация внутренних и внешних вызовов может осуществляться отдельно. Этот флаг имеет **значение true** , если внутренние и внешние вызовы могут перенаправляться на разные адреса назначения. в противном случае — **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвднумрингс**
</dt> <dd> <dl> <dt>



Указывает, можно ли указать число колец для ответного вызова без ответа при пересылке вызовов без ответа. Если **значение — true**, допустимый диапазон указывается в элементах **двминфвднумрингс** и **двмаксфвднумрингс** структуры [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдстатусвалид**
</dt> <dd> <dl> <dt>



Указывает, является ли состояние перенаправления в структуре [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) для этого адреса допустимым или не является наиболее подходящей оценкой, указанным отсутствием точного подтверждения коммутатором или сетью.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**ЛИНЕАДДРКАПФЛАГС \_ холдмакеснев**
</dt> <dd> <dl> <dt>



Когда вызов по этому адресу помещается в удержание (с помощью [**линехолд**](/windows/desktop/api/Tapi/nf-tapi-linehold) или внешнего действия), автоматически создается новый вызов (скорее всего, в линекаллстате \_ диалтоне).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**ЛИНЕАДДРКАПФЛАГС \_ ноекстерналкаллс**
</dt> <dd> <dl> <dt>



Адрес связан с внутренней линией УАТС, которая ограничена таким образом, что она не может использоваться для размещения вызовов к адресу за пределами коммутатора (например, это внутренней). Приложение может использовать эту индикацию, чтобы помочь пользователю выбрать правильный внешний вид вызова, который будет использоваться для выполнения вызова. Если этот бит отключен, он не обязательно указывает, что адрес можно использовать для выполнения внешних вызовов, так как поставщик услуг может не компания cognizant тип строки.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**ЛИНЕАДДРКАПФЛАГС \_ ноинтерналкаллс**
</dt> <dd> <dl> <dt>



Адрес связан с прямой СОВМЕСТНОй линией (магистральным каналом) и не может использоваться для выполнения внутренних вызовов УАТС. Приложение может использовать эту индикацию, чтобы помочь пользователю выбрать правильный внешний вид вызова, который будет использоваться для выполнения вызова. Если этот бит отключен, он не обязательно указывает, что адрес можно использовать для выполнения внутренних вызовов, так как поставщик услуг может не компания cognizant тип строки.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**ЛИНЕАДДРКАПФЛАГС \_ нопстнаддресстранслатион**
</dt> <dd> <dl> <dt>



Этот адрес не поддерживает преобразование адресов телефонной сети с открытым коммутируемым адресом. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**ЛИНЕАДДРКАПФЛАГС \_ оригоффхук**
</dt> <dd> <dl> <dt>



Указывает, может ли телефон исходной стороны автоматически принимать оффхук при выполнении вызовов.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**ЛИНЕАДДРКАПФЛАГС \_ партиалдиал**
</dt> <dd> <dl> <dt>



Указывает, доступен ли частичный набор.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**ЛИНЕАДДРКАПФЛАГС \_ пиккупкаллваит**
</dt> <dd> <dl> <dt>



**Значение true** , если [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) можно использовать для получения вызова, обнаруженного пользователем как вызов с ожиданием вызова; в противном случае — **значение false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**ЛИНЕАДДРКАПФЛАГС \_ пиккупграупид**
</dt> <dd> <dl> <dt>



Указывает, требуется ли идентификатор группы для отправки вызова.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**ЛИНЕАДДРКАПФЛАГС \_ предиктиведиалер**
</dt> <dd> <dl> <dt>



Этот адрес содержит расширенные возможности мониторинга хода вызова, которые можно применять к исходящим вызовам для определения состояний вызова, таких как *звонка*, *Busy*, *спеЦиалинфо* и *Connected*, или типа носителя устройства, отвечающего на вызов. Она также может иметь возможность автоматически передавать исходящие вызовы на другой адрес, когда вызов достигает какого-либо предопределенного набора состояний.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_очередь линеаддркапфлагс**
</dt> <dd> <dl> <dt>



Этот адрес не связан с конкретной станцией или физическим устройством, но является местом хранения, где вызовы ожидают дальнейшей обработки. Вызовы, помещаемые в очередь, могут получить определенную обработку. Они также могут автоматически передаваться при доступности определенного ресурса (например, если очередь является ACD-очередью, а вызовы ожидают доступного агента).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**ЛИНЕАДДРКАПФЛАГС \_ раутепоинт**
</dt> <dd> <dl> <dt>



Этот адрес не связан с конкретной станцией или физическим устройством, но является местом хранения, где вызовы ожидают маршрутизации приложением (приложение проверяет вызываемый адрес и может перенаправить вызов на другой адрес). Вызов также может быть автоматически передан в случае истечения времени ожидания маршрутизации (обычно параметр предполагает маршрутизацию по умолчанию).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**ЛИНЕАДДРКАПФЛАГС \_ безопасность**
</dt> <dd> <dl> <dt>



Указывает, можно ли обеспечить безопасность вызовов в этом адресе во время настройки вызова.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**ЛИНЕАДДРКАПФЛАГС \_ сеткаллингид**
</dt> <dd> <dl> <dt>



Приложение может выбрать установку элемента **каллингпартид** в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) при вызове [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) и других функций, которые принимают структуру **линекаллпарамс** . Поставщик услуг, если содержимое идентификатора приемлемо и доступен путь, передайте идентификатор вызываемой стороне, чтобы указать удостоверение вызывающей стороны.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**ЛИНЕАДДРКАПФЛАГС \_ сетупконфнулл**
</dt> <dd> <dl> <dt>



Указывает, начинается ли настройка вызова конференции с начальным вызовом (**false**) или без начального вызова (**true**).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**ЛИНЕАДДРКАПФЛАГС \_ трансферхелд**
</dt> <dd> <dl> <dt>



Указывает, можно ли передать жестко Удерживаемый вызов. Часто могут быть переданы только вызовы с удержанием на консультации.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**ЛИНЕАДДРКАПФЛАГС \_ трансфермаке**
</dt> <dd> <dl> <dt>



Указывает, можно ли установить полностью новый вызов для использования в качестве вызова консультации при перемещении.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линеакцепт**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**линехолд**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

