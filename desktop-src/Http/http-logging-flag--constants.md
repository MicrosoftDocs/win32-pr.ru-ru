---
title: Константы HTTP_LOGGING_FLAG_ (HTTP. h)
description: Определите параметры для настройки ведения журнала в API-интерфейсе HTTP Server.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae84697d84295d137f929bcf0d65c2e49fc6754aa7c1110d3b341bb471cbcb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981444"
---
# <a name="http_logging_flag_-constants"></a>\_ \_ Константы флага ведения журнала HTTP \_

Константы **\_ \_ флага \_ ведения журнала HTTP** определяют параметры для настройки ведения журнала в API-интерфейсе сервера HTTP.

Эти константы используются в структуре [**\_ \_ сведений о ведении журнала HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_флаг ведения журнала HTTP — \_ \_ Локальная \_ \_ Смена времени**
</dt> <dd> <dl> <dt>



Операция переключения на файл журнала основана на местном времени. По умолчанию смена файлов журнала основана на времени в формате UTC.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Протокол HTTP \_ Флаг ведения журнала \_ \_ использование \_ \_ преобразования UTF8**
</dt> <dd> <dl> <dt>



При записи в файлы журнала поля Юникода преобразуются в кодировки UTF8 (многобайты). По умолчанию файлы журнала записываются с помощью локального преобразования кодовой страницы.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_флаг ведения журнала HTTP — \_ \_ \_ только ошибки журнала \_**
</dt> <dd> <dl> <dt>



Файлы журнала содержат только сведения об ошибках. По умолчанию в журнал записываются как ответы об ошибках, так и успешные запросы. Если ни один **из \_ флагов ведения журнала HTTP не имеет значения \_ \_ только для журнала \_ ошибок \_** или **\_ \_ \_ \_ \_ только для флага журнала HTTP** , то регистрируются как ошибки, так и сведения об успешном выполнении.

Этот флаг не может быть установлен, если установлен флаг " **\_ \_ \_ Журнал \_ \_ только флагов регистрации HTTP** ". Эти два флага являются взаимоисключающими.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Протокол HTTP \_ \_Журнал флагов ведения журнала \_ \_ \_ только успешно выполнен**
</dt> <dd> <dl> <dt>



В файлы журнала входят только сведения об успешном выполнении. По умолчанию регистрируются ошибки и успешные транзакции. Если ни один **из \_ флагов ведения журнала HTTP не имеет значения \_ \_ только для журнала \_ ошибок \_** или **\_ \_ \_ \_ \_ только для флага журнала HTTP** , то регистрируются как ошибки, так и сведения об успешном выполнении.

Этот флаг не может быть установлен, если установлен флаг "журнал **\_ \_ \_ \_ ошибок \_ только флагов регистрации HTTP** ". Эти два флага являются взаимоисключающими.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>HTTP. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Константы API сервера HTTP версии 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_сведения о ведении журнала HTTP \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**хттпкуерюрлграуппроперти**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**хттпкуерисерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





