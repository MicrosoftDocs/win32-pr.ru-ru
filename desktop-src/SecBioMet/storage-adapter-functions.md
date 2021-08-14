---
title: служба хранилища Функции адаптера
description: Адаптер хранилища управляет шаблонами баз данных.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7072847c6d1ca653bd9e8edad9c51b7736354b447feeafda7c465973d4c25aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911806"
---
# <a name="storage-adapter-functions"></a>служба хранилища Функции адаптера

Адаптер хранилища управляет шаблонами баз данных. Разработчик адаптера должен реализовать следующие функции. они вызываются биометрической службой Windows.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                         | Описание                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**сторажеадаптерактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | дает адаптеру служба хранилища возможность выполнять любую работу, необходимую для перевода компонента хранилища из состояния простоя.<br/>         |
| [**сторажеадаптераддрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Добавляет шаблон в базу данных.<br/>                                                                                             |
| [**сторажеадаптераттач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Добавляет адаптер хранилища в конвейер обработки биометрического блока.<br/>                                                     |
| [**сторажеадаптерклеарконтекст**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Подготавливает конвейер обработки биометрического блока для новой операции.<br/>                                                  |
| [**сторажеадаптерклоседатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Закрывает базу данных, связанную с конвейером, и освобождает все связанные с ней ресурсы.<br/>                                            |
| [**сторажеадаптерконтролунит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Выполняет определяемую поставщиком операцию элемента управления, которая не требует повышенных привилегий.<br/>                                        |
| [**сторажеадаптерконтролунитпривилежед**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Выполняет определяемую поставщиком операцию элемента управления, для которой требуются повышенные привилегии.<br/>                                                |
| [**сторажеадаптеркреатедатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Создает и настраивает новую базу данных.<br/>                                                                                       |
| [**сторажеадаптердеактивате**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | дает адаптеру служба хранилища возможность выполнять любую работу, необходимую для перевода компонента хранилища в состояние простоя.<br/>             |
| [**сторажеадаптерделетерекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Удаляет один или несколько шаблонов из базы данных.<br/>                                                                             |
| [**сторажеадаптердетач**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Освобождает ресурсы, относящиеся к адаптеру, присоединенные к конвейеру.<br/>                                                                |
| [**сторажеадаптерераседатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Удаляет базу данных и помечает ее для удаления.<br/>                                                                               |
| [**сторажеадаптерфирстрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Помещает курсор результирующего набора на первую запись в наборе.<br/>                                                              |
| [**сторажеадаптержеткуррентрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Извлекает содержимое текущей записи в результирующем наборе конвейера.<br/>                                                     |
| [**сторажеадаптержетдатабасесизе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Извлекает размер базы данных и доступное пространство.<br/>                                                                             |
| [**сторажеадаптержетдатаформат**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Извлекает сведения о формате и версии, используемые текущей базой данных, связанной с конвейером.<br/>                          |
| [**сторажеадаптержетрекордкаунт**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Возвращает количество записей шаблона в результирующем наборе конвейера.<br/>                                                         |
| [**сторажеадаптернекстрекорд**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Перемещает курсор результирующего набора на одну запись.<br/>                                                                                |
| [*сторажеадаптернотифиповерчанже*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Получает уведомление об изменении состояния электропитания компьютера и соответствующим образом подготавливает адаптер хранилища.<br/>               |
| [**сторажеадаптеропендатабасе**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Открывает базу данных для использования адаптером хранилища.<br/>                                                                             |
| [**сторажеадаптерпипелинеклеануп**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | дает адаптеру служба хранилища возможность выполнять любые действия по очистке при подготовке к закрытию базы данных шаблонов.<br/>                |
| [**сторажеадаптерпипелинеинит**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | дает адаптеру служба хранилища возможность выполнить инициализацию, которая остается незавершенной.<br/>                                  |
| [**сторажеадаптеркуерибиконтент**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Запрашивает базу данных, которая открыта в данный момент для шаблонов, связанных с указанным вектором индекса.<br/>                          |
| [**сторажеадаптеркуерибисубжект**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Запрашивает базу данных, которая открыта в данный момент для шаблонов, связанных с указанным удостоверением и вложенным фактором.<br/>               |
| [**сторажеадаптеркуерекстендединфо**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Определяет возможности и ограничения компонента биометрического хранилища.<br/>                                              |
| [**вбиокуеристоражеинтерфаце**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Получает указатель на структуру [**\_ \_ интерфейса хранилища винбио**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) для адаптера хранилища.<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции подключаемых модулей](plug-in-functions.md)
</dt> </dl>

 

 





