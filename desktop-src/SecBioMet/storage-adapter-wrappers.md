---
title: Оболочки адаптеров хранилища
description: Функции, которые можно использовать для вызова функций в адаптере хранилища. Эти функции определены в Винбио \_ Adapter. h.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf562546e1520ee85c5a9a0164acdff53904
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411008"
---
# <a name="storage-adapter-wrappers"></a>Оболочки адаптеров хранилища

В Винбио Adapter. h определены следующие функции-оболочки \_ . Их можно использовать для вызова функций в адаптере хранилища.



| Функция                                    | Описание                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| вбиосторажеактивате<br/>              | Вызывает функцию [**сторажеадаптерактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                   |
| вбиосторажеаддрекорд<br/>             | Вызывает функцию [**сторажеадаптераддрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) .<br/>                                                                                       |
| вбиосторажеаттач<br/>                | Вызывает функцию [**сторажеадаптераттач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) .<br/>                                                                                             |
| вбиосторажеклеарконтекст<br/>          | Вызывает функцию [**сторажеадаптерклеарконтекст**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) .<br/>                                                                                 |
| вбиосторажеклоседатабасе<br/>         | Вызывает функцию [**сторажеадаптерклоседатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) .<br/>                                                                               |
| вбиосторажеконтролунит<br/>           | Вызывает функцию [**сторажеадаптерконтролунит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) .<br/>                                                                                   |
| вбиосторажеконтролунитпривилежед<br/> | Вызывает функцию [**сторажеадаптерконтролунитпривилежед**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) .<br/>                                                               |
| вбиосторажекреатедатабасе<br/>        | Вызывает функцию [**сторажеадаптеркреатедатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) .<br/>                                                                             |
| вбиосторажедеактивате<br/>            | Вызывает функцию [**сторажеадаптердеактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>               |
| вбиосторажеделетерекорд<br/>          | Вызывает функцию [**сторажеадаптерделетерекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) .<br/>                                                                                 |
| вбиосторажедетач<br/>                | Вызывает функцию [**сторажеадаптердетач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) .<br/>                                                                                             |
| вбиосторажеераседатабасе<br/>         | Вызывает функцию [**сторажеадаптерераседатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) .<br/>                                                                               |
| вбиосторажефирстрекорд<br/>           | Вызывает функцию [**сторажеадаптерфирстрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) .<br/>                                                                                   |
| вбиосторажежеткуррентрекорд<br/>      | Вызывает функцию [**сторажеадаптержеткуррентрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) .<br/>                                                                         |
| вбиосторажежетдатабасесизе<br/>       | Вызывает функцию [**сторажеадаптержетдатабасесизе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) .<br/>                                                                           |
| вбиосторажежетдатаформат<br/>         | Вызывает функцию [**сторажеадаптержетдатаформат**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) .<br/>                                                                               |
| вбиосторажежетрекордкаунт<br/>        | Вызывает функцию [**сторажеадаптержетрекордкаунт**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) .<br/>                                                                             |
| вбиостораженекстрекорд<br/>            | Вызывает функцию [**сторажеадаптернекстрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) .<br/>                                                                                     |
| вбиостораженотифиповерчанже<br/>     | Вызывает функцию [*сторажеадаптернотифиповерчанже*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 8.<br/>    |
| вбиосторажеопендатабасе<br/>          | Вызывает функцию [**сторажеадаптеропендатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) .<br/>                                                                                 |
| вбиосторажепипелинеклеануп<br/>       | Вызывает функцию [**сторажеадаптерпипелинеклеануп**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>     |
| вбиосторажепипелинеинит<br/>          | Вызывает функцию [**сторажеадаптерпипелинеинит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>           |
| вбиосторажекуерибиконтент<br/>        | Вызывает функцию [**сторажеадаптеркуерибиконтент**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) .<br/>                                                                             |
| вбиосторажекуерибисубжект<br/>        | Вызывает функцию [**сторажеадаптеркуерибисубжект**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) .<br/>                                                                             |
| вбиосторажекуерекстендединфо<br/>     | Вызывает функцию [**сторажеадаптеркуерекстендединфо**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции адаптера хранилища](storage-adapter-functions.md)
</dt> <dt>

[Функции подключаемых модулей](plug-in-functions.md)
</dt> </dl>

 

 





