---
description: Для создания и обслуживания файлов заполнителей и каталогов используются следующие структуры.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Структуры фильтрации в облаке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebe6623ad3d9d348d624f8ab8da3427416d4742
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656091"
---
# <a name="cloud-filter-structures"></a>Структуры фильтрации в облаке

Для создания и обслуживания файлов заполнителей и каталогов используются следующие структуры.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                   | Описание                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_сведения о обратном вызове CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Содержит общие сведения о обратном вызове.<br/>                                                                                          |
| [**\_Параметры обратного вызова CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Содержит параметры обратного вызова, такие как смещение файла, длина, флаги и т. д.<br/>                                                 |
| [**\_Регистрация обратного вызова CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Обратные вызовы, регистрируемые поставщиком синхронизации.<br/>                                                                           |
| [**\_диапазон файлов \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Задает диапазон данных в файле заполнителя.<br/>                                                                               |
| [**\_ \_ буфер диапазона файлов \_ CF**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Структура для описания расположения и диапазона данных в файле.<br/>                                                              |
| [**\_метаданные CF FS \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Файл заполнителя или метаданные каталога.<br/>                                                                                        |
| [**\_Политика РАСКОНСЕРВАЦИИ \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Указывает основную политику расконсервации и ее модификатор.<br/>                                                                       |
| [**\_ \_ сведения об операции CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Сведения об операции с файлом заполнителя или папкой.<br/>                                                                |
| [**\_параметры операции \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Параметры операции с файлом заполнителя или папкой.<br/>                                                                    |
| [**\_ \_ Базовая информация заполнителя \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Основные сведения о заполнителе.<br/>                                                                                                 |
| [**\_ \_ сведения о создании заполнителя CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Содержит сведения о заполнителе для создания новых файлов заполнителей или каталогов. <br/>                                           |
| [**заполнитель CF \_ \_ стандартные \_ сведения**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Сведения о стандартных заполнителях.<br/>                                                                                              |
| [**\_ \_ сведения о платформе CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Возвращает сведения о платформе облачных файлов. Это предназначено для поставщиков синхронизации, работающих в нескольких версиях Windows.<br/> |
| [**\_Политика заполнения \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Указывает основную политику заполнения и ее модификатор.<br/>                                                                      |
| [**\_ \_ сведения о процессе CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Содержит сведения о пользовательском процессе.<br/>                                                                                     |
| [**\_политики синхронизации \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Определяет политики синхронизации, используемые корнем синхронизации.<br/>                                                                                 |
| [**\_Регистрация синхронизации \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Сведения о поставщике синхронизации и корне синхронизации для регистрации.<br/>                                                               |
| [**\_ \_ корневая \_ Базовая \_ информация о синхронизации CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Основные сведения об корневой синхронизации.<br/>                                                                                                   |
| [**\_ \_ \_ сведения о корневом ПОСТАВЩИКе синхронизации CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Синхронизация сведений о корневом поставщике.<br/>                                                                                                |
| [**\_ \_ \_ сведения о корневом СТАНДАРТе синхронизации CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Стандартные корневые сведения синхронизации.<br/>                                                                                                |
| [**\_состояние синхронизации \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Используется в структуре [**\_ \_ сведений операции CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) для описания состояния указанного корня синхронизации.<br/>     |



 

 

