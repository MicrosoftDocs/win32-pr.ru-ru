---
title: Идентификаторы контекста фильтра (Фвпму. h)
description: Идентификаторы для контекстов фильтра, встроенных в платформу фильтрации Windows.
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661973"
---
# <a name="filter-context-identifiers"></a>Фильтровать идентификаторы контекста

Идентификаторы контекстов фильтров, встроенных в платформу фильтрации Windows, определяются следующим образом.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**ФВПМ \_ контекст \_ \_ входящего трафика IPSec \_ , фвпм \_ контекст \_ IPSec \_ для \_ входящего \_ подключения сохранить \_ безопасность, \_ фвпм \_ контекст \_ входящего трафика IPSec \_ зарезервирован**
</dt> <dd> <dl> <dt>



Контексты фильтра транспорта IPsec на входящем уровне.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**ФВПМ \_ контекст \_ IPSec для \_ исходящей \_ согласованности \_ обнаружения, фвпм \_ контекст \_ IPSec \_ \_ исключать \_ согласование**
</dt> <dd> <dl> <dt>



Контексты фильтра транспорта IPsec на исходящем уровне.

> [!Note]  
> В Windows 7 Используйте **контекст фвпм \_ контексте \_ IPSec \_ \_ исключать \_ согласование**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**для \_ \_ \_ подключения к набору ALE контекста фвпм \_ \_ требуется \_ \_ безопасность IPSec, фвпм. \_ \_ \_ Установка \_ подключения " \_ ленивый \_ SD \_ "**
</dt> <dd> <dl> <dt>



Контексты фильтра, используемые на уровне соединения ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**для \_ \_ \_ подключения к набору ALE контекста фвпм \_ \_ требуется \_ \_ шифрование IPSec, \_ \_ Подключение набора ALE контекста фвпм — \_ \_ \_ Разрешить \_ первый входящий незашифрованный общедоступный маркер общедоступного \_ \_ \_ контекста, фвпм \_ контекст \_ \_ \_ проверки подлинности \_**
</dt> <dd> <dl> <dt>



Контексты фильтра, используемые на уровне соединения или принятия ALE.

> [!Note]  
> Для Windows 7 Используйте **\_ \_ Подключение Set ALE фвпм \_ , \_ \_ разрешающее получение \_ первого \_ входящего \_ \_ незашифрованного** или **фвпм \_ контекста, \_ \_ разрешающего \_ \_ встроенное по проверки подлинности**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_контекст фвпм \_ \_ \_ , включение разгрузки TCP CHIMNEY \_ , \_ Отключение контекста фвпм \_ TCP \_ Chimney \_ \_ Disable**
</dt> <dd> <dl> <dt>



Контексты, используемые выносками разгрузки TCP Chimney.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_ \_ Аудит RPC context \_ фвпм \_ включен**
</dt> <dd> <dl> <dt>



Контексты, используемые в подуровне аудита RPC.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





