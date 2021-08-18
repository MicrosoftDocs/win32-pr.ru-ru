---
title: Структуры API службы удаленных рабочих столов
description: Содержит структуры, используемые с API службы удаленных рабочих столов.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3161d7c8e8b295e42930af1edcc79b7c60d83b61097b4d02661c1b11b5f1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000104"
---
# <a name="remote-desktop-services-api-structures"></a>Структуры API службы удаленных рабочих столов

С службы удаленных рабочих столов API используются следующие структуры.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**DEF по КАНАЛу \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Содержит имя и параметры виртуального канала службы удаленных рабочих столов.

</dd> <dt>

[**\_точки входа \_ каналов**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Содержит указатели на функции, вызываемые клиентской библиотекой DLL для доступа к виртуальным каналам.

</dd> <dt>

[**\_заголовок канала PDU \_**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Содержит сведения о блоке данных, получаемом серверным концом виртуального канала.

</dd> <dt>

[**лскэйпакк**](lskeypack.md)
</dt> <dd>

Содержит сведения о конкретном пакете лицензионных ключей службы удаленных рабочих столов.

</dd> <dt>

[**лслиценсе**](lslicense.md)
</dt> <dd>

Содержит сведения о конкретной лицензии службы удаленных рабочих столов.

</dd> <dt>

[**втсклиент**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Содержит сведения о клиенте подключение к удаленному рабочему столу (RDC).

</dd> <dt>

[**втсконфигинфо**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Содержит сведения о службы удаленных рабочих столов сеансе.

</dd> <dt>

[**втсинфо**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Содержит сведения о службы удаленных рабочих столов сеансе.

</dd> <dt>

[**втсинфоекс**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Содержит [**втсинфоекс на \_ уровне**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) объединения, который содержит расширенные сведения о сеансе службы удаленных рабочих столов.

</dd> <dt>

[**ВТСИНФОЕКС \_ level1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Содержит расширенные сведения о службы удаленных рабочих столов сеансе.

</dd> <dt>

[**втслистенерконфиг**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Содержит сведения о прослушивателе службы удаленных рабочих столов.

</dd> <dt>

[**ВТССБКС \_ IP- \_ адрес**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Содержит сведения о IP-адресе сетевого ресурса.

</dd> <dt>

[**\_ \_ сведения о подключении к втссбкс машине \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Содержит сведения о компьютере, принимающем удаленные подключения.

</dd> <dt>

[**\_ \_ сведения о компьютере втссбкс**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Содержит сведения о компьютере и его текущем состоянии.

</dd> <dt>

[**\_сведения о сеансе втссбкс \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Содержит сведения о сеансах, доступных для подключение к удаленному рабочему столу Broker (RDCB).

</dd> <dt>

[**\_уведомление втссессион**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Предоставляет сведения о уведомлении об изменении сеанса. Служба получает эту структуру в своей функции [*хандлерекс*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) в ответ на событие изменения сеанса.

</dd> <dt>

[**втсусерконфиг**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Содержит сведения о конфигурации пользователя на контроллере домена или на сервере узла сеансов удаленный рабочий стол.

</dd> <dt>

[**WTS \_ \_адрес клиента**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Содержит сетевой адрес клиента службы удаленных рабочих столов сеанса.

</dd> <dt>

[**WTS \_ \_Отображение клиента**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Содержит сведения о дисплее клиента подключение к удаленному рабочему столу (RDC).

</dd> <dt>

[**WTS \_ \_сведения о процессе**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Содержит сведения о процессе, выполняющемся на сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**WTS \_ \_сведения о процессе ( \_ ex)**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Содержит расширенные сведения о процессе, работающем на сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**WTS \_ \_сведения о продукте**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Сведения о лицензии продукта, необходимой для подключения к серверу терминалов.

</dd> <dt>

[**WTS \_ \_сведения о сервере**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Содержит сведения о конкретном сервере службы удаленных рабочих столов.

</dd> <dt>

[**WTS \_ \_адрес сеанса**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Содержит виртуальный IP-адрес, назначенный сеансу.

</dd> <dt>

[**WTS \_ \_сведения о сеансе**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Содержит сведения о клиентском сеансе на сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**WTS \_ \_Сведения о сеансе \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Содержит расширенные сведения о клиентском сеансе на сервере узла сеансов удаленных рабочих столов или на сервере узла виртуализации удаленных рабочих столов (Узел виртуализации удаленных рабочих столов).

</dd> </dl>

 

 