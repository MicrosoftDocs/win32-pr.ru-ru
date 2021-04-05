---
description: Коды ошибок PNRP NSP
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: Коды ошибок PNRP NSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b02959c921c8e3a468cadfa87dba6fb8d3c29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909760"
---
# <a name="pnrp-nsp-error-codes"></a>Коды ошибок PNRP NSP

Если функция поставщика пространства имен (NSP) возвращает **\_ ошибку сокета**, для получения дополнительных сведений об ошибке необходимо использовать [всажетластеррор](winsock-nsp-reference-links.md) . NSP PNRP возвращает следующие коды ошибок:



| Термин                                                                                                                                                                     | Описание                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ отменено<br/>                                                                         | Операция отменена.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span>WSA \_ E \_ больше \_<br/>                                                                         | Результаты разрешенного запроса не готовы. Это может не быть ошибкой.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span>\_ожидается ввод-вывод WSA \_ <br/>                                                                      | Операция не завершена.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>WSA \_ не \_ хватает \_ памяти<br/>                                                      | Недостаточно памяти для завершения указанного действия.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>\_Операция WSA \_ прервана<br/>                                                       | Операция отменена.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>WSA \_ \_ облако PNRP \_ отключено<br/>                                                | Указанное имя облака отключено.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>WSA \_ PNRP \_ Cloud \_ не \_ Найдено<br/>                                            | Указанное имя облака недоступно.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>WSA \_ PNRP \_ Cloud \_ — \_ \_ только Поиск<br/>                            | Предпринята попытка зарегистрировать имя в облаке, которое было настроено только для разрешения.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>\_ \_ \_ Недопустимый \_ ИД секции \_ клиента WSA PNRP<br/> | Использование PNRP в секции за пределами по умолчанию. PNRP будет работать только в секции по умолчанию.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>WSA \_ PNRP \_ недопустимое \_ удостоверение<br/>                                          | Не удается получить доступ к указанному удостоверению.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>WSA \_ \_ Загрузка слишком \_ большой \_ нагрузки на PNRP<br/>                                                  | Невозможно создать имя однорангового узла, так как у компьютера нет ресурсов для обработки запроса. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>всаефаулт<br/>                                                                                             | Операция недопустима в текущем состоянии.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>всаеинвал<br/>                                                                                             | Указан недопустимый параметр или сочетание параметров.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>всаенетунреач<br/>                                                                              | Подключение к сети будет потеряно.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>всаенотимплементед<br/>                                                                  | Указанная функциональность не реализована с помощью PNRP.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>всаеопнотсупп<br/>                                                                                 | Указанная функциональность не поддерживается протоколом PNRP.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>всаеваулдблокк<br/>                                                                              | Операция не завершена.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> ВСАСЕРВИЦЕ \_ не \_ найден<br/>                                                     | Указанный поставщик, пространство имен или идентификатор службы не поддерживаются.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>всасиснотреади<br/>                                                                              | Служба не запущена.<br/>                                                                             |



 

 

 




