---
description: Транзакционные структуры NTFS (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Структуры TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662609"
---
# <a name="txf-structures"></a>Структуры TxF

Транзакционная NTFS (TxF) предоставляет следующие структуры.

## <a name="in-this-section"></a>Содержание раздела



| Структура                                                                                                    | Описание                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ сведения о создании тксфс мини \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Содержит сведения о версии мини, созданной с помощью [**фсктл \_ тксфс \_ Create \_ мини**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion).<br/>                                            |
| [**ТКСФС \_ Получение \_ \_ сведений о \_ метаданных**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Содержит сведения о версии создаваемой мини-версии.<br/>                                                                                                                 |
| [**\_идентификатор TxF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Представляет уникальный идентификатор в контексте диспетчер ресурсов.<br/>                                                                                                              |
| [**ТКСФС \_ получить \_ версию транзакционной транзакции \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Содержит сведения о базовой и последней версии указанного файла.<br/>                                                                                                      |
| [**ТКСФС \_ список \_ \_ заблокированных \_ файлов транзакций**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Содержит список файлов, заблокированных транзакционным модулем записи.<br/>                                                                                                                                 |
| [**\_ \_ \_ запись заблокированных \_ файлов транзакции списка \_ тксфс**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Содержит сведения о заблокированной транзакции.<br/>                                                                                                                                        |
| [**ТКСФС \_ список \_ транзакций**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Содержит список транзакций.<br/>                                                                                                                                                        |
| [**\_запись тксфс списка \_ транзакций \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Содержит сведения о транзакции.<br/>                                                                                                                                               |
| [**\_ \_ \_ файл затронутых записей журнала TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Содержит сведения о файле, затронутом транзакцией.<br/>                                                                                                                     |
| [**\_ \_ база записи журнала \_ TxF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Содержит основные сведения о записи.<br/>                                                                                                                                                  |
| [**\_ \_ усечение записи журнала \_ TxF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Содержит запись для операции усечения.<br/>                                                                                                                                           |
| [**запись \_ журнала \_ TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Содержит запись для операции записи.<br/>                                                                                                                                              |
| [**ТКСФС \_ изменить \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Содержит сведения, необходимые при изменении параметров журнала и режима ведения журнала для дополнительного диспетчера ресурсов.<br/>                                                                      |
| [**ТКСФС \_ запрос \_ \_ сведений о диспетчере ресурсов**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Содержит сведения о диспетчере ресурсов (RM).<br/>                                                                                                                                   |
| [**ТКСФС \_ Чтение \_ резервной копии \_ данных \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Содержит определенную транзакционную структуру NTFS (TxF). Эти сведения следует использовать только при вызове [**тксфс \_ записи \_ резервной копии \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information).<br/>    |
| [**\_сведения о тксфс точке сохранения \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | Структура [**\_ \_ \_ сведений о точке сохранения фсктл тксфс**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) определяет действие, которое необходимо выполнить, и на какую транзакцию.<br/>                                      |
| [**\_ \_ Активная \_ информация о транзакции тксфс**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Содержит флаг, указывающий, активны ли транзакции при создании моментального снимка.<br/>                                                                                     |
| [**ТКСФС \_ запись \_ сведений о резервной копии \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Содержит определенную транзакционную структуру NTFS (TxF). Эти сведения следует использовать только при вызове [**тксфс \_ записи \_ резервной копии \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out).<br/> |



 

 

