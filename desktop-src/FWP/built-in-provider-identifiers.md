---
title: Идентификаторы встроенных поставщиков (Фвпму. h)
description: идентификаторы для поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.
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
ms.openlocfilehash: c8982fe6ebbe3f4cf5135f2b67f07826ddf9d3f970ca0568c7095931c617cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951313"
---
# <a name="built-in-provider-identifiers"></a>Встроенные идентификаторы поставщиков

идентификаторы для поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.

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
> доступно только в Windows 7 и Windows Server 2008 R2.

 


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
> доступно только для Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





