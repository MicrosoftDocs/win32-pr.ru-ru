---
title: Фильтрация идентификаторов подслоя (Фвпму. h)
description: Константы идентификатора подслоя фильтрации управления API WFP.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d597fa1b75f6c965da9cf8d71bcc3e729d0b0b2f4f4220c984a1be8c94c09d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068884"
---
# <a name="filtering-sublayer-identifiers"></a>Фильтрация идентификаторов подслоя

идентификаторы подслоя платформы фильтрации Windows (WFP) представлены идентификаторами GUID.

Эти идентификаторы определяются следующим образом.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**подслой ФВПМ для \_ \_ обхода краев подслоя \_ фвпм ( \_ \_ TEREDO)**
</dt> <dd> <dl> <dt>



Фильтры обхода узлов добавляются в этот подуровень.

> [!Note]  
> для Windows 7 и более поздних версий используйте **\_ \_ \_ обход фвпм для подслоя**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_Проверка ПОДСЛОЯ \_ фвпм**
</dt> <dd> <dl> <dt>



Это самый низкий взвешенный подуровень. Он используется только для фильтров проверки.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_ПОДУРОВЕНЬ фвпм \_ IPSec \_ досп**
</dt> <dd> <dl> <dt>



Фильтры защиты IPsec DoS добавляются в этот подуровень.

> [!Note]  
> доступно только в Windows Vista с пакетом обновления 1 (SP1), Windows Server 2008 и более поздних версиях.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_ \_ \_ Перенаправление \_ исходящего \_ туннеля IPSec на подуровне фвпм**
</dt> <dd> <dl> <dt>



Фильтры перенаправления исходящих туннелей IPsec добавляются в этот подуровень.

> [!Note]  
> доступно только в Windows 7, Windows Server 2008 R2 и более поздних версиях.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_ \_ Туннелирование IPSec ПОДслоя фвпм \_**
</dt> <dd> <dl> <dt>



Фильтры туннеля IPsec добавляются в этот подуровень.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_пакеты LIP ПОДСЛОЯ фвпм \_**
</dt> <dd> <dl> <dt>



В этот подуровень добавляются устаревшие фильтры IPsec.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_Аудит RPC ПОДСЛОЯ фвпм \_ \_**
</dt> <dd> <dl> <dt>



Фильтры аудита RPC добавляются в этот подуровень. Эти фильтры Произведите аудит входящих вызовов RPC как часть C2 и соответствие стандарту Common условия_отбора.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_ \_ защищенный сокет ПОДслоя фвпм \_**
</dt> <dd> <dl> <dt>



Фильтры защищенных сокетов добавляются в этот подуровень.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ разгрузка TCP \_ CHIMNEY подслоя фвпм \_**
</dt> <dd> <dl> <dt>



Фильтры разгрузки TCP Chimney добавляются в этот подуровень.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_шаблоны TCP ПОДСЛОЯ фвпм \_ \_** 
</dt> <dd> <dl> <dt>



Фильтры шаблонов TCP добавляются в этот подуровень.

> [!Note]  
> доступно только для Windows 8, Windows Server 2012 и более поздних версий.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**\_универсальный ПОДУРОВЕНЬ \_ фвпм**
</dt> <dd> <dl> <dt>



Этот подуровень содержит все фильтры, которые не назначены ни одному из других подслоев.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





