---
description: 'При работе с енклавес, которые используются для создания доверенных сред выполнения, используются следующие структуры:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Доверенные структуры выполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9349c8c4e4c04ecc664ccab668abe55cdca1e1720b6fa17fd35bb7139f53f19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386255"
---
# <a name="trusted-execution-structures"></a>Доверенные структуры выполнения

При работе с енклавес, которые используются для создания доверенных сред выполнения, используются следующие структуры:

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                         | Описание                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ сведения о создании анклава \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Содержит сведения об архитектуре, используемые для создания анклава, если тип анклава — **анклава \_ Type \_ SGX**, который указывает анклава для расширения архитектуры Intel Software Guard (SGX).<br/>     |
| [**АНКЛАВА \_ \_ сведения о создании \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Содержит сведения об архитектуре, используемые для создания анклава, если тип анклава — **анклава \_ Type \_ vbs**, который указывает безопасность на основе виртуализации (VBS) анклава.<br/>                                       |
| [**\_удостоверение анклава**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Описывает идентификатор основного модуля анклава. <br/>                                                                                                                                                                 |
| [**\_сведения о анклава**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Содержит сведения о выполняемом в данный момент анклава.<br/>                                                                                                                                                                  |
| [**АНКЛАВА \_ \_ сведения о инициализации \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Содержит сведения об архитектуре, используемые для инициализации анклава, если тип анклава — **анклава \_ типа \_ SGX**, который указывает анклава для расширения архитектуры Intel Software Guard (SGX).<br/> |
| [**АНКЛАВА \_ \_ сведения о инициализации \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Содержит сведения об архитектуре, используемые для инициализации анклава, если тип анклава — **анклава \_ Type \_ vbs**, который указывает безопасность на основе виртуализации (VBS) анклава.<br/>                                   |
| [**IMAGE \_ анклава \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Определяет формат конфигурации анклава для систем с 32-разрядным Windows.<br/>                                                                                                                                          |
| [**IMAGE \_ анклава \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Определяет формат конфигурации анклава для систем с 64-разрядным Windows.<br/>                                                                                                                                          |
| [**\_Импорт АНКЛАВА \_ изображения**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Определяет запись в массиве изображений, которые может импортировать анклава.<br/>                                                                                                                                                           |
| [**\_отчет vbs анклава \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Описывает формат подписанной инструкции, содержащейся в отчете, созданном путем вызова функции [**енклавежетаттестатионрепорт**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                     |
| [**\_ \_ Модуль отчета vbs \_ анклава**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Описывает модуль, загруженный для анклава.<br/>                                                                                                                                                                                   |
| [**\_ \_ заголовок Reporting \_ анклава \_ для vbs**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Описывает содержимое отчета, созданного путем вызова функции [**енклавежетаттестатионрепорт**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                                                     |
| [**\_ \_ \_ заголовок вардата отчета vbs \_ анклава**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Описывает формат блока данных переменной, содержащегося в отчете, создаваемом функцией [**енклавежетаттестатионрепорт**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                          |



 

 

 
