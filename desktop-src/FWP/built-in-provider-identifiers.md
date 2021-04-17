---
title: Идентификаторы встроенных поставщиков (Фвпму. h)
description: Идентификаторы для поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661951"
---
# <a name="built-in-provider-identifiers"></a>Встроенные идентификаторы поставщиков

Идентификаторы для поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.

Эти идентификаторы определяются следующим образом.

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_IKEEXT поставщика \_ фвпм**
</dt> <dd> <dl> <dt>

{10ad9216-ccde-456c-8b16-e9f04e60a90b}
</dt> <dt>



Используется для обнаружения всех фильтров, добавленных IKE/AuthIP.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_Конфигурация фвпм поставщика \_ IPSec для \_ DOS \_**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



Используется для обнаружения всех фильтров, добавленных функцией защиты IPsec в DoS.

> [!Note]  
> Доступно только в Windows 7 и Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_ \_ \_ разгрузка TCP \_ CHIMNEY поставщика фвпм**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84b9}
</dt> <dt>



Используется для обнаружения всех фильтров, добавленных разгрузкой TCP Chimney.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**\_ \_ шаблоны TCP поставщика \_ фвпм**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432d-bed3-441ae50e63c3}
</dt> <dt>



Используется для поиска всех фильтров, добавленных с помощью шаблонов TCP.

> [!Note]  
> Доступно только в Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





