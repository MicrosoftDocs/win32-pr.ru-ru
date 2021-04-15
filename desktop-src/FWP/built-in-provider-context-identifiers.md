---
title: Встроенные идентификаторы контекста поставщика (Фвпму. h)
description: Встроенные контексты поставщика указывают политики по умолчанию для использования с защищенными сокетами.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488997"
---
# <a name="built-in-provider-context-identifiers"></a>Встроенные идентификаторы контекста поставщика

Идентификаторы для контекстов поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются идентификаторами GUID. Эти встроенные контексты поставщика указывают политики по умолчанию для использования с защищенными сокетами.

Эти идентификаторы определяются следующим образом.

<dl> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**\_контекст поставщика \_ фвпм \_ безопасный \_ сокет \_ AUTHIP**
</dt> <dd> <dl> <dt>



Политика по умолчанию для протокола AuthIP в основном режиме для защищенных сокетов.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_ \_ \_ защищенный \_ сокет IPSec контекста \_ поставщика фвпм**
</dt> <dd> <dl> <dt>



Политика по умолчанию быстрого режима IPsec для защищенных сокетов.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





