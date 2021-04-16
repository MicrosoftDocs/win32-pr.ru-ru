---
description: В API теневого копирования томов определены следующие перечисления.
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: Перечисления API теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ade0af4637e9c057c9743dfaf0778e86b3d81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692388"
---
# <a name="volume-shadow-copy-api-enumerations"></a>Перечисления API теневого копирования томов

В API теневого копирования томов определены следующие перечисления.



| Имя                                                                           | Описание                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_состояние альтернативного \_ модуля записи VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | Определяет набор допустимых состояний, используемых для указания того, имеет ли модуль записи связанный альтернативный модуль записи.                                                              |
| [**\_уровень приложения \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | Определяет набор допустимых уровней приложения.                                                                                                                       |
| [**\_схема резервного копирования VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | Определяет набор схем резервного копирования — операции, в которых может участвовать модуль записи.                                                                                          |
| [**\_тип резервного копирования VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | Определяет набор типов резервных копий.                                                                                                                                   |
| [**\_ \_ Флаги компонента VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | Указывает поддержку автоматического восстановления.                                                                                                                               |
| [**\_тип компонента \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | Определяет набор типов компонентов.                                                                                                                                |
| [**\_ \_ состояние восстановления файлов \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | Определяет набор состояний операции восстановления файла.                                                                                                           |
| [**\_ \_ \_ тип резервного копирования спецификации файла VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | Определяет набор операций резервного копирования, поддерживаемых модулями записи.                                                                                                         |
| [**\_\_Параметры оборудования \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | Определяет флаги теневого копирования LUN.                                                                                                                                     |
| [**\_ \_ тип объекта для руководства по VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | Discriminant для объединения [**\_ объектов службы \_ \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001) с объединением в [**структуре \_ \_ \_ prop объекта для службы VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . |
| [**\_тип объекта \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | Используется для обнаружения объекта в виде набора теневых копий, теневого копирования или поставщика.                                                                                         |
| [**\_сбой защиты \_ VSS**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | Определяет набор сбоев защиты теневого копирования.                                                                                                                  |
| [**\_уровень защиты \_ VSS**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | Определяет набор уровней защиты теневого копирования томов.                                                                                                           |
| [**\_возможности поставщика \_ VSS**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | Зарезервировано для последующего использования.                                                                                                                                           |
| [**\_тип поставщика \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | Определяет набор типов поставщиков.                                                                                                                                 |
| [**\_Параметры восстановления \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | Используется инициатором запроса для указания способа выполнения операции повторной синхронизации.                                                                               |
| [**\_ \_ целевой объект восстановления VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | Определяет набор целевых объектов восстановления.                                                                                                                                |
| [**\_тип восстановления \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | Определяет набор операций восстановления, которые необходимо выполнить.                                                                                                              |
| [**\_перечисление РЕСТОРЕМЕСОД VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | Определяет набор методов восстановления файлов по умолчанию для модуля записи.                                                                                                      |
| [**\_тип НАКАТУ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | Используется инициатором запроса для указания типа операции наката, которую он собирается выполнить.                                                                         |
| [**\_Совместимость моментальных снимков VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | Определяет набор элементов управления громкостью или файловых операций ввода-вывода, которые могут быть отключены для тома, для которого была создана теневая копия.                                            |
| [**\_\_контекст моментальных снимков VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | Указывает, как создается, запрашивается или удаляется теневая копия, а также степень вовлечения в модуль записи.                                                            |
| [**\_состояние моментального снимка VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | Определяет набор состояний для операции теневого копирования.                                                                                                              |
| [**\_тип источника \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | Определяет набор типов данных, которыми может управлять модуль записи.                                                                                                         |
| [**\_Маска подписки \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | Определяет набор событий, которые может получить модуль записи.                                                                                                               |
| [**\_тип использования \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | Указывает, как хост-система использует данные, управляемые модулем записи.                                                                                                   |
| [**\_\_ \_ атрибуты моментального снимка тома VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | Определяет набор атрибутов теневой копии.                                                                                                                    |
| [**\_состояние модуля записи VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | Определяет набор состояний модуля записи.                                                                                                                           |
| [**\_перечисление ВРИТЕРРЕСТОРЕ VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | Определяет набор условий, при котором модуль записи будет выполнять обработку событий, созданных во время операции восстановления.                                                        |



 

 

 



