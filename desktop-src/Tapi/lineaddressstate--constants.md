---
description: '\_Константы побитового флага линеаддрессстате описывают различные элементы состояния адреса.'
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Константы LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddf746d98328df51497374b990eb23f3885516ee1374d9cfdafb8799d016fb74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761856"
---
# <a name="lineaddressstate_-constants"></a>\_Константы линеаддрессстате

Константы побитового флага **линеаддрессстате \_** описывают различные элементы состояния адреса.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**ЛИНЕАДДРЕСССТАТЕ \_ капсчанже**
</dt> <dd> <dl> <dt>



Указывает, что из-за изменений, внесенных в конфигурацию пользователем или в других обстоятельствах, изменился один или несколько элементов структуры [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) для адреса. Приложение должно использовать [**линежетаддресскапс**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) для чтения обновленной структуры. Если поставщик услуг отправляет сообщение [**Line \_ аддрессстате**](line-addressstate.md) , содержащее это значение в TAPI, TAPI передает его приложениям, имеющим согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, получают [**строки \_ ЛИНЕДЕВСТАТЕ**](line-linedevstate.md) сообщения, указывающие линедевстате \_ reinit, что требует от них завершения работы и повторной инициализации подключения к TAPI для получения обновленной информации.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**ЛИНЕАДДРЕСССТАТЕ \_ девспеЦифик**
</dt> <dd> <dl> <dt>



Изменился элемент состояния адреса, относящийся к конкретному устройству.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**ЛИНЕАДДРЕСССТАТЕ \_ вперед**
</dt> <dd> <dl> <dt>



Состояние пересылки адреса изменилось, включая, возможно, число колец для определения условия "без ответа". Приложение должно проверить состояние адреса, чтобы определить сведения о текущем состоянии пересылки адреса.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**ЛИНЕАДДРЕСССТАТЕ \_ инусемани**
</dt> <dd> <dl> <dt>



Отслеживаемый или переданный мостский адрес был изменен с помощью одной станции, чтобы она использовалась несколькими станциями.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**ЛИНЕАДДРЕСССТАТЕ \_ инусеоне**
</dt> <dd> <dl> <dt>



Адрес изменен с режима простоя или используется многими станциями, которые используют мост для использования только одной станцией.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**ЛИНЕАДДРЕСССТАТЕ \_ инусезеро**
</dt> <dd> <dl> <dt>



Адрес был изменен на бездействие (он не используется ни одной из станций).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**ЛИНЕАДДРЕСССТАТЕ \_ нумкаллс**
</dt> <dd> <dl> <dt>



Число вызовов в адресе изменилось. Это результат таких событий, как новый входящий вызов, исходящий вызов по адресу или вызов, изменяющий состояние его удержания. Этот флаг охватывает изменения в любом из членов **двнумактивекаллс**, **двнумонхолдкаллс** и **двнумонхолдпендингкаллс** в структуре [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) . Приложение должно проверить все три из этих членов при получении сообщения [**Line \_ аддрессстате**](line-addressstate.md) (нумкаллс).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**ЛИНЕАДДРЕСССТАТЕ \_**
</dt> <dd> <dl> <dt>



Address — изменились элементы состояния, отличные от перечисленных ниже. Приложение должно проверить состояние текущего адреса, чтобы определить, какие элементы были изменены.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**ЛИНЕАДДРЕСССТАТЕ \_ терминалов**
</dt> <dd> <dl> <dt>



Параметры терминала для адреса были изменены.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Без расширяемости. Все 32 бит зарезервированы.

Приложение получает уведомление об изменениях этих элементов состояния в [**строке сообщения \_ аддрессстате**](line-addressstate.md) . Возможности устройства для адресации указывают на то, какие изменения состояния адресов могут быть переданы по этому адресу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Строка \_ аддрессстате**](line-addressstate.md)
</dt> <dt>

[**Строка \_ линедевстате**](line-linedevstate.md)
</dt> <dt>

[**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**линежетаддресскапс**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




