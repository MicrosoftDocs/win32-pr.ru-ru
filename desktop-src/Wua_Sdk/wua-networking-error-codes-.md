---
description: Дополнительные сведения см. в статье коды ошибок сети WUA
ms.assetid: 07ff2ed7-09bc-4af7-84f9-66a921c0f53f
title: Коды ошибок сети WUA (Вуеррор. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fb2c027939afda3fe5817a8a860469fc90b766
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708372"
---
# <a name="wua-networking-error-codes"></a>Коды ошибок сети WUA

API Центр обновления Windows Agent (WUA) может возвращать следующие коды ошибок при выполнении сетевых операций, таких как поиск обновлений:



| Константа/значение                                                                                                                                                                                                                                                                                        | Описание                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WU_E_WINHTTP_INVALID_FILE"></span><span id="wu_e_winhttp_invalid_file"></span><dl> <dt>**Wu \_ E \_ WinHTTP \_ Недопустимый \_ файл**</dt> <dt>0x80240038</dt> </dl>                                  | Загруженный файл имеет непредвиденный тип контента.<br/>                                                                                                                               |
| <span id="WU_E_PT_HTTP_STATUS_BAD_REQUEST"></span><span id="wu_e_pt_http_status_bad_request"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ Недопустимый \_ запрос состояния HTTP E PT**</dt> <dt>0x80244016</dt> </dl>              | Совпадение с кодом состояния HTTP 400 — серверу не удалось обработать запрос из-за недопустимого синтаксиса.<br/>                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_DENIED"></span><span id="wu_e_pt_http_status_denied"></span><dl> <dt>**Wu \_ \_Состояние HTTP "E PT" \_ \_ \_ отклонено**</dt> <dt>0x80244017</dt> </dl>                              | Совпадение с кодом состояния HTTP 401 — запрошенный ресурс требует проверки подлинности пользователя.<br/>                                                                                                    |
| <span id="WU_E_PT_HTTP_STATUS_FORBIDDEN"></span><span id="wu_e_pt_http_status_forbidden"></span><dl> <dt>**Wu \_ \_Состояние HTTP "E PT" \_ \_ \_ запрещено**</dt> <dt>0x80244018</dt> </dl>                     | То же, что и состояние HTTP 403 — сервер понимает запрос, но отклоняет его для выполнения.<br/>                                                                                              |
| <span id="WU_E_PT_HTTP_STATUS_NOT_FOUND"></span><span id="wu_e_pt_http_status_not_found"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ Не \_ Найдено состояние HTTP E PT**</dt> <dt>0x80244019</dt> </dl>                    | Совпадение с кодом состояния HTTP 404 — серверу не удается найти запрошенный URI (универсальный идентификатор ресурса).<br/>                                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_BAD_METHOD"></span><span id="wu_e_pt_http_status_bad_method"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ Неправильный \_ метод состояния HTTP E PT**</dt> <dt>0x8024401A</dt> </dl>                 | Совпадение с кодом состояния HTTP 405 — Метод HTTP не разрешен.<br/>                                                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="wu_e_pt_http_status_proxy_auth_req"></span><dl> <dt>**Wu \_ E \_ PT \_ HTTP \_ Status \_ Proxy \_ \_ req**</dt> <dt>0x8024401B</dt> </dl>    | Совпадение с кодом состояния HTTP 407 — требуется проверка подлинности прокси-сервера.<br/>                                                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="wu_e_pt_http_status_request_timeout"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ \_ Время ожидания запроса состояния HTTP E PT**</dt> <dt>0x8024401C</dt> </dl>  | Совпадение с кодом состояния HTTP 408 — истекло время ожидания запроса сервером.<br/>                                                                                                           |
| <span id="WU_E_PT_HTTP_STATUS_CONFLICT"></span><span id="wu_e_pt_http_status_conflict"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ Конфликт состояния HTTP E PT**</dt> <dt>0x8024401D</dt> </dl>                        | Совпадение с кодом состояния HTTP 409 — запрос не был завершен из-за конфликта с текущим состоянием ресурса.<br/>                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_GONE"></span><span id="wu_e_pt_http_status_gone"></span><dl> <dt>**Wu \_ \_ \_ Состояние HTTP E \_ PT \_ пропало**</dt> <dt>0x8024401E</dt> </dl>                                    | Совпадение с кодом состояния HTTP 410 — запрошенный ресурс больше не доступен на сервере.<br/>                                                                                                |
| <span id="WU_E_PT_HTTP_STATUS_SERVER_ERROR"></span><span id="wu_e_pt_http_status_server_error"></span><dl> <dt>**Wu \_ E \_ PT \_ HTTP \_ состояние \_ сервера \_ Ошибка**</dt> <dt>0x8024401F</dt> </dl>           | Совпадение с кодом состояния HTTP 500 — Внутренняя ошибка сервера не позволила удовлетворить запрос.<br/>                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_NOT_SUPPORTED"></span><span id="wu_e_pt_http_status_not_supported"></span><dl> <dt>**Wu \_ \_ \_ Состояние HTTP E \_ PT \_ не \_ поддерживается**</dt> <dt>0x80244020</dt> </dl>        | То же, что и состояние HTTP 501 — сервер не поддерживает функции, необходимые для выполнения запроса. <br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_BAD_GATEWAY"></span><span id="wu_e_pt_http_status_bad_gateway"></span><dl> <dt>**Wu \_ \_Состояние HTTP "E PT" \_ \_ \_ неверный \_ шлюз**</dt> <dt>0x80244021</dt> </dl>              | Совпадение с кодом состояния HTTP 502 — сервер, выполняющий роль шлюза или прокси-сервера, получил недопустимый ответ от вышестоящего сервера, к которому он обращался при попытке выполнить запрос.<br/> |
| <span id="WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="wu_e_pt_http_status_service_unavail"></span><dl> <dt>**Wu \_ Не0x80244022ная \_ \_ \_ \_ Служба \_ состояния HTTP E PT**</dt> <dt></dt> </dl>  | То же, что и состояние HTTP 503 — Служба временно перегружена.<br/>                                                                                                                  |
| <span id="WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="wu_e_pt_http_status_gateway_timeout"></span><dl> <dt>**Wu \_ \_ \_ Шлюз состояния HTTP E PT \_ \_ \_ время ожидания**</dt> <dt>0x80244023</dt> </dl>  | Совпадение с кодом состояния HTTP 504 — истекло время ожидания шлюза для запроса.<br/>                                                                                                        |
| <span id="WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP"></span><span id="wu_e_pt_http_status_version_not_sup"></span><dl> <dt>**Wu \_ \_ \_ Версия состояния HTTP E PT \_ \_ \_ не \_ SUP**</dt> <dt>0x80244024</dt> </dl> | То же, что и состояние HTTP 505 — сервер не поддерживает версию протокола HTTP, используемую для запроса.<br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_NOT_MAPPED"></span><span id="wu_e_pt_http_status_not_mapped"></span><dl> <dt>**Wu \_ \_ \_ Состояние HTTP E \_ PT \_ не \_ сопоставлено**</dt> <dt>0x8024402B</dt> </dl>                 | Не удалось выполнить запрос, так как причина не соответствует ни одному из \_ \_ \_ кодов ошибок HTTP Wu E PT \_ \* .<br/>                                                               |
| <span id="WU_E_PT_WINHTTP_NAME_NOT_RESOLVED"></span><span id="wu_e_pt_winhttp_name_not_resolved"></span><dl> <dt>**Wu \_ \_Имя WinHTTP для E PT \_ \_ \_ не \_ разрешено**</dt> <dt>0x8024402C</dt> </dl>        | Совпадение с \_ ошибкой \_ имя WinHTTP \_ не \_ разрешено — невозможно разрешить имя прокси-сервера или целевого сервера.<br/>                                                                          |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вуеррор. h</dt> </dl> |



 

 




