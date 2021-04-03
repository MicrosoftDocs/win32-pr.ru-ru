---
title: Флаги регистрации интерфейса (Рпкдце. h)
description: В параметре Flags функций RpcServerRegisterIf2 и Рпксерверрегистерифекс используются следующие константы.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137246"
---
# <a name="interface-registration-flags"></a>Флаги регистрации интерфейса

В параметре *flags* функций [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) и [**рпксерверрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) используются следующие константы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>0,0</strong></dt> </dl></td>
<td style="text-align: left;">Стандартная семантика интерфейса.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">При регистрации этого флага интерфейса Среда выполнения RPC вызывает зарегистрированный обратный вызов безопасности для всех вызовов, независимо от удостоверения, последовательности протокола или уровня проверки подлинности клиента.<br/>
<blockquote>
[!Note]<br />
Этот флаг доступен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1). Если этот флаг не установлен, RPC автоматически фильтрует все вызовы, не прошедшие проверку подлинности, прежде чем они достигли обратного вызова безопасности.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Когда этот флаг интерфейса зарегистрирован, среда выполнения RPC отклоняет вызовы, выполняемые удаленными клиентами. Все локальные вызовы с использованием последовательностей протоколов ncadg_ * и ncacn_ * также отклоняются, за исключением ncacn_np. RPC разрешает ncacn_NP вызовы только в том случае, если вызов не получен из SRV. Вызовы из нкалрпк всегда обрабатываются.<br/>
<blockquote>
[!Note]<br />
Этот флаг доступен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">Это интерфейс <strong>автоматического прослушивания</strong> . Время выполнения начинает ожидать вызовов сразу после регистрации первого интерфейса автопрослушивания и прекращает прослушивание при отмене регистрации последнего интерфейса автопрослушивания.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <dt><strong>RPC_IF_OLE</strong></dt> </dl></td>
<td style="text-align: left;">Зарезервировано для OLE. Не используйте этот флаг.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </dl></td>
<td style="text-align: left;">В настоящий момент не реализовано.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Ограничивает соединения с клиентами, которые используют уровень авторизации выше RPC_C_AUTHN_LEVEL_NONE. Указание этого флага позволяет клиентам проходить через <strong>пустой</strong> сеанс. В Windows XP и Windows Server 2003 такие клиенты не разрешены. Клиенты, не прошедшие RPC_IF_ALLOW_SECURE_ONLY тест, получают ошибку RPC_S_ACCESS_DENIED. Использование флага RPC_IF_ALLOW_SECURE_ONLY не подразумевает или не гарантирует высокий уровень привилегий в части вызывающего пользователя. RPC проверяет наличие действительных учетных данных у пользователя. вызывающий пользователь может использовать учетную запись гостя или другие учетные записи с низкими привилегиями. Не представим высокий уровень привилегий при использовании RPC_IF_ALLOW_SECURE_ONLY.<br/> <strong>Windows NT 4,0 и Windows Me/98/95:  </strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">Отключает кэширование обратного вызова безопасности, принудительное применение обратного вызова безопасности для каждого вызова RPC для данного интерфейса.<br/>
<blockquote>
[!Note]<br />
Этот флаг доступен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1).
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Рпкдце. h</dt> </dl> |



 

 





