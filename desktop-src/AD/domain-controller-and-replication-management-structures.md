---
title: Структуры управления репликацией и контроллером домена
description: В контроллерах домена и функциях управления репликацией используются следующие структуры.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afe084e4285f4851457f9a519e747952e3bbd67
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890436"
---
# <a name="domain-controller-and-replication-management-structures"></a>Структуры управления репликацией и контроллером домена

Контроллеры домена и функции управления репликацией используют следующие структуры:

-   [**\_ \_ Сведения об контроллере домена DS \_ \_ 1**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [**\_ \_ Сведения о контроллере домена DS \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [**\_ \_ Сведения об контроллере домена DS \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [**\_результат имени \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [**\_ \_ элемент результата имени \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [**\_ \_ метаданные attr для DS REPL \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [**Службы DS \_ REPL, \_ \_ метаданные \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [**\_BLOB- \_ \_ \_ объект метаданных attr \_ для DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [**\_ \_ \_ метаданные значения attr \_ \_ для DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [**\_Метаданные для \_ значения attr для DS REPL \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [**\_ \_ \_ \_ расширение МЕТАДАННЫХ значения \_ attr \_ для DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [**\_курсор REPL в DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [**DS \_ REPL, \_ курсор \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [**\_Курсор репликации \_ DS \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [**\_BLOB- \_ объект курсора REPL DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [**\_курсоры REPL в DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [**DS \_ REPL, \_ курсоры \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [**\_Курсоры REPL в DS \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [**\_сбой проверки \_ согласованности DS \_ DSA \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [**\_сбои проверки \_ согласованности DS \_ DSA \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [**DS \_ REPL \_ KCC \_ DSA \_ фаилурев \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [**\_сосед DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [**\_соседи DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [**DS \_ REPL \_ неигхборв, \_ большой двоичный объект**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [**\_ \_ метаданные obj- \_ \_ данных DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [**DS \_ REPL \_ , \_ метаданные obj- \_ данных \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [**DS \_ REPL, \_ операция**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [**\_ \_ \_ большой двоичный объект для печати DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [**\_ \_ ожидающих операций DS REPL \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [**DS \_ REPL \_ очереди \_ статистиксв**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   [**\_BLOB- \_ \_ объект статистиксв очереди DS REPL \_**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))
-   [**\_ \_ метаданные значения REPL \_ для \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [**\_Метаданные для значения репликации DS REPL \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [**\_ \_ \_ расширение МЕТАДАННЫХ значения \_ \_ репликации DS REPL**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [**\_BLOB- \_ \_ \_ \_ объект метаданных значения REPL для DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [**\_ \_ \_ \_ \_ ext BLOB-объектов метаданных значения \_ репликации DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [**DS \_ репсинкалл \_ ерринфо**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [**\_Синхронизация РЕПСИНКАЛЛ \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [**\_Обновление РЕПСИНКАЛЛ \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [**\_ \_ Таблица GUID схемы \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [**\_ \_ сведения о стоимости сайта DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [**Расписание**](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [**\_заголовок расписания**](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Структуры в службах домен Active Directory Services](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 