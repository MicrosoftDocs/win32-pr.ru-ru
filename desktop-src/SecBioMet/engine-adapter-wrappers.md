---
title: Оболочки адаптера подсистемы
description: Функции, которые можно использовать для вызова функций в адаптере подсистемы. Эти функции определены в Винбио \_ Adapter. h.
ms.assetid: b3d6d617-e423-4ed5-9d29-be72c5dd8b49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ec0fcc3b6ea358e8238061bc74e2933d8bf87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681502"
---
# <a name="engine-adapter-wrappers"></a>Оболочки адаптера подсистемы

В Винбио Adapter. h определены следующие функции-оболочки \_ . Их можно использовать для вызова функций в адаптере подсистемы.



| Функция                                           | Описание                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| вбиоенгинеакцептсампледата<br/>              | Вызывает функцию [**енгинеадаптеракцептсампледата**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn) .<br/>                                                                                                 |
| вбиоенгинеактивате<br/>                      | Вызывает функцию [**енгинеадаптерактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                                           |
| вбиоенгинеаттач<br/>                        | Вызывает функцию [**енгинеадаптераттач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn) .<br/>                                                                                                                     |
| вбиоенгинечеккфордупликате<br/>             | Вызывает функцию [**енгинеадаптерчеккфордупликате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn) .<br/>                                                                                               |
| вбиоенгинеклеарконтекст<br/>                  | Вызывает функцию [**енгинеадаптерклеарконтекст**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn) .<br/>                                                                                                         |
| вбиоенгинекоммитенроллмент<br/>              | Вызывает функцию [**енгинеадаптеркоммитенроллмент**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn) .<br/>                                                                                                 |
| вбиоенгинеконтролунит<br/>                   | Вызывает функцию [**енгинеадаптерконтролунит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn) .<br/>                                                                                                           |
| вбиоенгинеконтролунитпривилежед<br/>         | Вызывает функцию [**енгинеадаптерконтролунитпривилежед**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn) .<br/>                                                                                       |
| вбиоенгинекреатинроллмент<br/>              | Вызывает функцию [**енгинеадаптеркреатинроллмент**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn) .<br/>                                                                                                 |
| вбиоенгинедеактивате<br/>                    | Вызывает функцию [**енгинеадаптердеактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                                       |
| вбиоенгинедетач<br/>                        | Вызывает функцию [**енгинеадаптердетач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn) .<br/>                                                                                                                     |
| вбиоенгинедискарденроллмент<br/>             | Вызывает функцию [**енгинеадаптердискарденроллмент**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn) .<br/>                                                                                               |
| вбиоенгиникспортенгинедата<br/>              | Вызывает функцию [**енгинеадаптерекспортенгинедата**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn) .<br/>                                                                                                 |
| вбиоенгинежетенроллменсаш<br/>             | Вызывает функцию [**енгинеадаптержетенроллменсаш**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn) .<br/>                                                                                               |
| вбиоенгинежетенроллментстатус<br/>           | Вызывает функцию [**енгинеадаптержетенроллментстатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn) .<br/>                                                                                           |
| вбиоенгинеидентифялл<br/>                   | Вызывает функцию [**енгинеадаптеридентифялл**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                                     |
| вбиоенгинеидентифифеатуресет<br/>            | Вызывает функцию [**енгинеадаптеридентифифеатуресет**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn) .<br/>                                                                                             |
| вбиоенгиненотифиповерчанже<br/>             | Вызывает функцию [*енгинеадаптернотифиповерчанже*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 8.<br/>                            |
| вбиоенгинепипелинеклеануп<br/>               | Вызывает функцию [**енгинеадаптерпипелинеклеануп**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                             |
| вбиоенгинепипелинеинит<br/>                  | Вызывает функцию [**енгинеадаптерпипелинеинит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                                   |
| вбиоенгинекуерикалибратиондата<br/>          | Вызывает функцию [**енгинеадаптеркуерикалибратиондата**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                   |
| вбиоенгинекуерекстендеденроллментстатус<br/> | Вызывает функцию [**енгинеадаптеркуерекстендеденроллментстатус**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/> |
| вбиоенгинекуерекстендединфо<br/>             | Вызывает функцию [**енгинеадаптеркуерекстендединфо**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                         |
| вбиоенгинекуерихашалгорисмс<br/>           | Вызывает функцию [**енгинеадаптеркуерихашалгорисмс**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn) .<br/>                                                                                           |
| вбиоенгинекуериндексвекторсизе<br/>          | Вызывает функцию [**енгинеадаптеркуериндексвекторсизе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn) .<br/>                                                                                         |
| вбиоенгинекуерипреферредформат<br/>          | Вызывает функцию [**енгинеадаптеркуерипреферредформат**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn) .<br/>                                                                                         |
| вбиоенгинекуерисамплехинт<br/>               | Вызывает функцию [**енгинеадаптеркуерисамплехинт**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn) .<br/>                                                                                                   |
| вбиоенгинерефрешкаче<br/>                  | Вызывает функцию [**енгинеадаптеррефрешкаче**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                                   |
| вбиоенгинеселекткалибратионформат<br/>       | Вызывает функцию [**енгинеадаптерселекткалибратионформат**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>             |
| вбиоенгинесетаккаунтполици<br/>              | Вызывает функцию [**енгинеадаптерсетаккаунтполици**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                           |
| вбиоенгинесетенроллментпараметерс<br/>       | Вызывает функцию [**енгинеадаптерсетенроллментпараметерс**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>             |
| вбиоенгинесетенроллментселектор<br/>         | Вызывает функцию [**енгинеадаптерсетенроллментселектор**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn) .<br/> Эта функция-оболочка поддерживается начиная с Windows 10.<br/>                 |
| вбиоенгинесесашалгорисм<br/>              | Вызывает функцию [**енгинеадаптерсесашалгорисм**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) .<br/>                                                                                                 |
| вбиоенгинеупдатинроллмент<br/>              | Вызывает функцию [**енгинеадаптерупдатинроллмент**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn) .<br/>                                                                                                 |
| вбиоенгиневерифифеатуресет<br/>              | Вызывает функцию [**енгинеадаптерверифифеатуресет**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn) .<br/>                                                                                                 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции адаптера ядра](engine-adapter-functions.md)
</dt> <dt>

[Функции подключаемых модулей](plug-in-functions.md)
</dt> </dl>

 

 





