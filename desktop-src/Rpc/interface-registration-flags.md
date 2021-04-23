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
# <a name="interface-registration-flags"></a><span data-ttu-id="2fead-103">Флаги регистрации интерфейса</span><span class="sxs-lookup"><span data-stu-id="2fead-103">Interface Registration Flags</span></span>

<span data-ttu-id="2fead-104">В параметре *flags* функций [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) и [**рпксерверрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="2fead-104">The following constants are used in the *Flags* parameter of the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) and [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) functions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2fead-105">Константа</span><span class="sxs-lookup"><span data-stu-id="2fead-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2fead-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2fead-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <span data-ttu-id="2fead-107"><dt><strong>0,0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-107"><dt><strong>0</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-108">Стандартная семантика интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2fead-108">Standard interface semantics.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <span data-ttu-id="2fead-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-110">При регистрации этого флага интерфейса Среда выполнения RPC вызывает зарегистрированный обратный вызов безопасности для всех вызовов, независимо от удостоверения, последовательности протокола или уровня проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="2fead-110">When this interface flag is registered, the RPC runtime invokes the registered security callback for all calls, regardless of identity, protocol sequence, or authentication level of the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2fead-111">Этот флаг доступен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2fead-111">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="2fead-112">Если этот флаг не установлен, RPC автоматически фильтрует все вызовы, не прошедшие проверку подлинности, прежде чем они достигли обратного вызова безопасности.</span><span class="sxs-lookup"><span data-stu-id="2fead-112">When this flag is not set, RPC automatically filters all unauthenticated calls before they reach the security callback.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <span data-ttu-id="2fead-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-114">Когда этот флаг интерфейса зарегистрирован, среда выполнения RPC отклоняет вызовы, выполняемые удаленными клиентами.</span><span class="sxs-lookup"><span data-stu-id="2fead-114">When this interface flag is registered, the RPC runtime rejects calls made by remote clients.</span></span> <span data-ttu-id="2fead-115">Все локальные вызовы с использованием последовательностей протоколов ncadg_ \* и ncacn_ \* также отклоняются, за исключением ncacn_np.</span><span class="sxs-lookup"><span data-stu-id="2fead-115">All local calls using ncadg_\* and ncacn_\* protocol sequences are also rejected, with the exception of ncacn_np.</span></span> <span data-ttu-id="2fead-116">RPC разрешает ncacn_NP вызовы только в том случае, если вызов не получен из SRV.</span><span class="sxs-lookup"><span data-stu-id="2fead-116">RPC allows ncacn_NP calls only if the call does not come from SRV.</span></span> <span data-ttu-id="2fead-117">Вызовы из нкалрпк всегда обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="2fead-117">Calls from ncalrpc are always processed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2fead-118">Этот флаг доступен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2fead-118">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <span data-ttu-id="2fead-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-120">Это интерфейс <strong>автоматического прослушивания</strong> .</span><span class="sxs-lookup"><span data-stu-id="2fead-120">This is an <strong>auto-listen</strong> interface.</span></span> <span data-ttu-id="2fead-121">Время выполнения начинает ожидать вызовов сразу после регистрации первого интерфейса автопрослушивания и прекращает прослушивание при отмене регистрации последнего интерфейса автопрослушивания.</span><span class="sxs-lookup"><span data-stu-id="2fead-121">The run time begins listening for calls as soon as the first autolisten interface is registered, and stops listening when the last autolisten interface is unregistered.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <span data-ttu-id="2fead-122"><dt><strong>RPC_IF_OLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-122"><dt><strong>RPC_IF_OLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-123">Зарезервировано для OLE.</span><span class="sxs-lookup"><span data-stu-id="2fead-123">Reserved for OLE.</span></span> <span data-ttu-id="2fead-124">Не используйте этот флаг.</span><span class="sxs-lookup"><span data-stu-id="2fead-124">Do not use this flag.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <span data-ttu-id="2fead-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-126">В настоящий момент не реализовано.</span><span class="sxs-lookup"><span data-stu-id="2fead-126">Currently not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <span data-ttu-id="2fead-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-128">Ограничивает соединения с клиентами, которые используют уровень авторизации выше RPC_C_AUTHN_LEVEL_NONE.</span><span class="sxs-lookup"><span data-stu-id="2fead-128">Limits connections to clients that use an authorization level higher than RPC_C_AUTHN_LEVEL_NONE.</span></span> <span data-ttu-id="2fead-129">Указание этого флага позволяет клиентам проходить через <strong>пустой</strong> сеанс.</span><span class="sxs-lookup"><span data-stu-id="2fead-129">Specifying this flag allows clients to come through on the <strong>NULL</strong> session.</span></span> <span data-ttu-id="2fead-130">В Windows XP и Windows Server 2003 такие клиенты не разрешены.</span><span class="sxs-lookup"><span data-stu-id="2fead-130">On Windows XP and Windows Server 2003, such clients are not allowed.</span></span> <span data-ttu-id="2fead-131">Клиенты, не прошедшие RPC_IF_ALLOW_SECURE_ONLY тест, получают ошибку RPC_S_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="2fead-131">Clients that fail the RPC_IF_ALLOW_SECURE_ONLY test receive an RPC_S_ACCESS_DENIED error.</span></span> <span data-ttu-id="2fead-132">Использование флага RPC_IF_ALLOW_SECURE_ONLY не подразумевает или не гарантирует высокий уровень привилегий в части вызывающего пользователя.</span><span class="sxs-lookup"><span data-stu-id="2fead-132">Using the RPC_IF_ALLOW_SECURE_ONLY flag does not imply or guarantee a high level of privilege on the part of the calling user.</span></span> <span data-ttu-id="2fead-133">RPC проверяет наличие действительных учетных данных у пользователя. вызывающий пользователь может использовать учетную запись гостя или другие учетные записи с низкими привилегиями.</span><span class="sxs-lookup"><span data-stu-id="2fead-133">RPC only checks that the user has valid credentials; the calling user may be using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="2fead-134">Не представим высокий уровень привилегий при использовании RPC_IF_ALLOW_SECURE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="2fead-134">Do not assume high privilege when RPC_IF_ALLOW_SECURE_ONLY is used.</span></span><br/> <span data-ttu-id="2fead-135"><strong>Windows NT 4,0 и Windows Me/98/95:  </strong></span><span class="sxs-lookup"><span data-stu-id="2fead-135"><strong>Windows NT 4.0 and Windows Me/98/95:  </strong></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <span data-ttu-id="2fead-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2fead-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2fead-137">Отключает кэширование обратного вызова безопасности, принудительное применение обратного вызова безопасности для каждого вызова RPC для данного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2fead-137">Disables security callback caching, forcing a security callback for each RPC call on a given interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2fead-138">Этот флаг доступен в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2fead-138">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="2fead-139">Требования</span><span class="sxs-lookup"><span data-stu-id="2fead-139">Requirements</span></span>



| <span data-ttu-id="2fead-140">Требование</span><span class="sxs-lookup"><span data-stu-id="2fead-140">Requirement</span></span> | <span data-ttu-id="2fead-141">Значение</span><span class="sxs-lookup"><span data-stu-id="2fead-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2fead-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2fead-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2fead-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2fead-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2fead-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2fead-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2fead-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2fead-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2fead-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2fead-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fead-147"><dt>Рпкдце. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fead-147"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





