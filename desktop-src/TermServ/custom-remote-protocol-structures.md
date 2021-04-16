---
title: Структуры поставщика протокол удаленного рабочего стола
description: API настраиваемого удаленного протокола поддерживает следующие структуры.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672011"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Структуры поставщика протокол удаленного рабочего стола

API настраиваемого удаленного протокола поддерживает следующие структуры.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**ТСМФ \_ Поддержка \_ данных \_ в**](tsmf-support-data-in.md)
</dt> <dd>

Содержит сведения о форматах мультимедиа.

</dd> <dt>

[**\_Исходящие \_ данные поддержки тсмф \_**](tsmf-support-data-out.md)
</dt> <dd>

Содержит сведения о форматах мультимедиа.

</dd> <dt>

[**\_Поддержка тсмф \_ нодедата \_ в**](tsmf-support-nodedata-in.md)
</dt> <dd>

Используется в [**\_ данных поддержки тсмф \_ \_ в**](tsmf-support-data-in.md) структуре для хранения сведений о поддерживаемых форматах мультимедиа.

</dd> <dt>

[**ТСМФ \_ Поддержка \_ нодедата \_**](tsmf-support-nodedata-out.md)
</dt> <dd>

Используется в структуре [**\_ \_ \_ out данных поддержки тсмф**](tsmf-support-data-out.md) для хранения сведений о поддерживаемых форматах мультимедиа.

</dd> <dt>

[**\_Параметры подключения \_ врдс**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Содержит сведения о параметрах подключения для удаленного сеанса.

</dd> <dt>

[**\_Параметры подключения \_ врдс \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Содержит сведения о параметрах подключения для удаленного сеанса.

</dd> <dt>

[**\_ \_ сведения о динамическом часовом \_ поясе врдс \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Содержит сведения о динамическом часовом поясе.

</dd> <dt>

[**\_параметры прослушивателя врдс \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Содержит сведения о параметрах прослушивателя для удаленного сеанса.

</dd> <dt>

[**\_Параметры прослушивателя врдс \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Содержит параметры прослушивателя для удаленного сеанса.

</dd> <dt>

[**\_Параметры врдс**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Содержит сведения о параметрах, связанных с политикой, для удаленного сеанса.

</dd> <dt>

[**\_Параметры врдс \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Содержит параметры, связанные с политикой, для удаленного сеанса.

</dd> <dt>

[**\_Статистика кэша \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Содержит статистику кэша протокола.

</dd> <dt>

[**ВТС \_ отобразить \_ ioctl**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Содержит сведения о дисплее клиента.

</dd> <dt>

[**ВТС \_ \_ данные клиента**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Содержит сведения о клиентском подключении.

</dd> <dt>

[**\_возможности лицензии \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Содержит сведения о возможностях лицензирования клиента.

</dd> <dt>

[**\_данные политики \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Содержит сведения о политике, которые передаются службой службы удаленных рабочих столов протоколу.

</dd> <dt>

[**\_значение свойства \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Содержит сведения о значении свойства, которое необходимо получить из протокола.

</dd> <dt>

[**\_кэш протокола \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Содержит число операций чтения и попаданий в кэш.

</dd> <dt>

[**\_ \_ счетчики протокола ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Содержит счетчики производительности протокола.

</dd> <dt>

[**\_состояние протокола \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Содержит сведения о состоянии протокола.

</dd> <dt>

[**\_состояние службы \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Содержит сведения об изменениях в состоянии службы службы удаленных рабочих столов.

</dd> <dt>

[**\_идентификатор сеанса \_ ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Содержит **идентификатор GUID** , который однозначно определяет сеанс.

</dd> <dt>

[**ВТС \_ маленький \_ Rect**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Содержит координаты окна клиента.

</dd> <dt>

[**ВТС \_ SOCKADDR**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Содержит адрес сокета.

</dd> <dt>

[**ВТС \_ SYSTEMTIME**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Указывает сведения о дате и времени для переходов между стандартным и летним временем.

</dd> <dt>

[**\_сведения о часовом \_ ПОЯСе ВТС \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Содержит сведения о часовом поясе клиента.

</dd> <dt>

[**\_ \_ учетные данные пользователя ВТС**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Содержит учетные данные пользователя.

</dd> <dt>

[**ВТС \_ \_ данные пользователя**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Содержит значения свойства "выбор клиента".

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по поставщику протокол удаленного рабочего стола](custom-remote-protocol-reference.md)
</dt> <dt>

[Перечисления поставщика протокол удаленного рабочего стола](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Интерфейсы поставщика протокол удаленного рабочего стола](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Объединения поставщиков протокол удаленного рабочего стола](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




