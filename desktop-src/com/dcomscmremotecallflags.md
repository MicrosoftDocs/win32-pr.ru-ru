---
title: дкомскмремотекаллфлагс
description: Управляет поведением вызовов из локального диспетчера управления службами DCOM (ДКОМСКМ) на удаленный ДКОМСКМ.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- COM-значение реестра Дкомскмремотекаллфлагс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070676"
---
# <a name="dcomscmremotecallflags"></a><span data-ttu-id="8cd5c-104">дкомскмремотекаллфлагс</span><span class="sxs-lookup"><span data-stu-id="8cd5c-104">DCOMSCMRemoteCallFlags</span></span>

<span data-ttu-id="8cd5c-105">Управляет поведением вызовов из локального диспетчера управления службами DCOM (ДКОМСКМ) на удаленный ДКОМСКМ.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-105">Controls the behavior of calls from the local DCOM Service Control Manager (DCOMSCM) to a remote DCOMSCM.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8cd5c-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="8cd5c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a><span data-ttu-id="8cd5c-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cd5c-107">Remarks</span></span>

<span data-ttu-id="8cd5c-108">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8cd5c-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="8cd5c-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd5c-109">Value</span></span> | <span data-ttu-id="8cd5c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8cd5c-110">Description</span></span>                                       |
|-------|---------------------------------------------------|
| <span data-ttu-id="8cd5c-111">0x1</span><span class="sxs-lookup"><span data-stu-id="8cd5c-111">0x1</span></span>   | <span data-ttu-id="8cd5c-112">**\_Активация дкомскм \_ использовать \_ All \_ ауснсервицес**</span><span class="sxs-lookup"><span data-stu-id="8cd5c-112">**DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES**</span></span>  |
| <span data-ttu-id="8cd5c-113">0x2</span><span class="sxs-lookup"><span data-stu-id="8cd5c-113">0x2</span></span>   | <span data-ttu-id="8cd5c-114">**\_Активация дкомскм \_ запрещает \_ небезопасный \_ вызов**</span><span class="sxs-lookup"><span data-stu-id="8cd5c-114">**DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL**</span></span> |
| <span data-ttu-id="8cd5c-115">0x4</span><span class="sxs-lookup"><span data-stu-id="8cd5c-115">0x4</span></span>   | <span data-ttu-id="8cd5c-116">**ДКОМСКМ \_ Разрешить \_ использовать \_ все \_ ауснсервицес**</span><span class="sxs-lookup"><span data-stu-id="8cd5c-116">**DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES**</span></span>     |
| <span data-ttu-id="8cd5c-117">0x8</span><span class="sxs-lookup"><span data-stu-id="8cd5c-117">0x8</span></span>   | <span data-ttu-id="8cd5c-118">**ДКОМСКМ \_ Resolve \_ запрет \_ небезопасного \_ вызова**</span><span class="sxs-lookup"><span data-stu-id="8cd5c-118">**DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL**</span></span>    |
| <span data-ttu-id="8cd5c-119">0x10</span><span class="sxs-lookup"><span data-stu-id="8cd5c-119">0x10</span></span>  | <span data-ttu-id="8cd5c-120">**ДКОМСКМ \_ ping \_ USE \_ MID \_ ауснсервице**</span><span class="sxs-lookup"><span data-stu-id="8cd5c-120">**DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE**</span></span>         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a><span data-ttu-id="8cd5c-121">ДКОМСКМ \_ Activation \_ использовать \_ \_ Описание ALL ауснсервицес</span><span class="sxs-lookup"><span data-stu-id="8cd5c-121">DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="8cd5c-122">Когда клиент выдает запрос на активацию, который использует параметры безопасности по умолчанию, локальный ДКОМСКМ использует службу проверки подлинности Negotiate при активации вызова RPC для удаленной ДКОМСКМ.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-122">When the client issues an activation request that uses the default security settings, the local DCOMSCM uses the Negotiate authentication service when making the activation RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="8cd5c-123">Если вызов завершается неудачно, локальный ДКОМСКМ делает вызов RPC активации без защиты.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-123">If the call fails, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="8cd5c-124">**Windows Server 2003 и Windows XP/2000:** Если вызов RPC активации, использующий службу проверки подлинности Negotiate, завершается сбоем, локальная ДКОМСКМ выполняет вызов RPC с помощью Kerberos, NTLM или других настроенных поставщиков безопасности.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-124">**Windows Server 2003 and Windows XP/2000:** If the activation RPC call that uses the Negotiate authentication service fails, the local DCOMSCM makes the activation RPC call using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="8cd5c-125">Если поставщики безопасности не работают, локальная ДКОМСКМ делает вызов RPC активации без защиты.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-125">If no security providers work, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="8cd5c-126">Устанавливая этот флаг, локальная ДКОМСКМ в Windows Vista или более поздней версии может работать как в системах, предшествующих Vista.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-126">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="8cd5c-127">Не рекомендуется устанавливать этот флаг, если это не требуется в целях совместимости.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-127">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a><span data-ttu-id="8cd5c-128">ДКОМСКМ \_ Activation \_ запрещает \_ небезопасное \_ Описание вызова</span><span class="sxs-lookup"><span data-stu-id="8cd5c-128">DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="8cd5c-129">Если установлен **флаг \_ \_ \_ небезопасного \_ вызова дкомскм Activation** , локальный дкомскм не делает вызов RPC небезопасной активации.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-129">If the **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure activation RPC call.</span></span> <span data-ttu-id="8cd5c-130">Чтобы разрешить клиентам выполнять запросы на активацию с параметрами безопасности, отличными от значений по умолчанию, укажите структуру [**коаусинфо**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) при выполнении запроса на активацию.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-130">To enable clients to make activation requests with non-default security settings, specify the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure when making the activation request.</span></span> <span data-ttu-id="8cd5c-131">В этом случае **\_ Активация дкомскм \_ использует \_ All \_ ауснсервицес** и **дкомскм Activation, \_ \_ запрещающие \_ небезопасные \_** флаги вызовов игнорируются.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-131">In this case, the **DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES** and **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flags are ignored.</span></span>

<span data-ttu-id="8cd5c-132">Не рекомендуется устанавливать этот флаг, если все клиенты и серверы в сети полностью не прошли проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-132">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_resolve_use_all_authnservices-description"></a><span data-ttu-id="8cd5c-133">ДКОМСКМ \_ Разрешить \_ использовать \_ все \_ ауснсервицес описание</span><span class="sxs-lookup"><span data-stu-id="8cd5c-133">DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="8cd5c-134">Когда клиент выполняет детрансляцию ссылки на объект, локальная ДКОМСКМ использует службу проверки подлинности Negotiate при выполнении вызова RPC для разрешения оксид удаленного ДКОМСКМ.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-134">When the client unmarshals an object reference, the local DCOMSCM uses the Negotiate authentication service when making the OXID Resolution RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="8cd5c-135">Если вызов завершается неудачно, локальный ДКОМСКМ делает вызов RPC для разрешения оксид, не используя безопасность.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-135">If the call fails, the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="8cd5c-136">**Windows Server 2003 и Windows XP/2000:** Если вызов RPC для разрешения оксид с помощью службы проверки подлинности Negotiate завершается сбоем, локальный ДКОМСКМ делает вызов RPC разрешения оксид с помощью Kerberos, NTLM или других настроенных поставщиков безопасности.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-136">**Windows Server 2003 and Windows XP/2000:** If the OXID Resolution RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the OXID Resolution RPC call by using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="8cd5c-137">Если поставщики безопасности не работают, локальный ДКОМСКМ делает вызов RPC для разрешения оксид, не используя безопасность.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-137">If no security providers work, then the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="8cd5c-138">Устанавливая этот флаг, локальная ДКОМСКМ в Windows Vista или более поздней версии может работать как в системах, предшествующих Vista.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-138">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="8cd5c-139">Не рекомендуется устанавливать этот флаг, если это не требуется в целях совместимости.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-139">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a><span data-ttu-id="8cd5c-140">ДКОМСКМ \_ Resolve \_ запрет \_ небезопасного \_ вызова</span><span class="sxs-lookup"><span data-stu-id="8cd5c-140">DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="8cd5c-141">Если установлен флаг **дкомскм \_ Resolve \_ ЗАПРЕТа \_ небезопасного \_ вызова** , локальный дкомскм не делает вызов RPC незащищенным оксид разрешением.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-141">If the **DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure OXID Resolution RPC call.</span></span> <span data-ttu-id="8cd5c-142">Кроме того, локальный ДКОМСКМ не выполняет вызов RPC для проверки связи с небезопасным сбором мусора.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-142">In addition, the local DCOMSCM does not make an unsecure garbage collection Ping RPC call.</span></span> <span data-ttu-id="8cd5c-143">Не рекомендуется устанавливать этот флаг, если все клиенты и серверы в сети полностью не прошли проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-143">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_ping_use_mid_authnservice-description"></a><span data-ttu-id="8cd5c-144">ДКОМСКМ \_ ping \_ USE \_ ПСТР \_ ауснсервице Description</span><span class="sxs-lookup"><span data-stu-id="8cd5c-144">DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE Description</span></span>

<span data-ttu-id="8cd5c-145">Локальная ДКОМСКМ использует службу проверки подлинности Negotiate при выполнении вызова RPC для проверки связи мусора с удаленным ДКОМСКМ.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-145">The local DCOMSCM uses the Negotiate authentication service when making the garbage-collection Ping RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="8cd5c-146">Если вызов завершается неудачно, локальный ДКОМСКМ делает вызов RPC-сборки с помощью команды ping без защиты.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-146">If the call fails, the local DCOMSCM makes the garbage-collection Ping RPC call using no security.</span></span>

<span data-ttu-id="8cd5c-147">**Windows Server 2003 и Windows XP/2000:** Если RPC-вызов сбора мусора с помощью службы проверки подлинности Negotiate завершается неудачно, локальный ДКОМСКМ выполняет вызов RPC для проверки связи при сборке мусора с помощью Kerberos, NTLM и других настроенных поставщиков безопасности.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-147">**Windows Server 2003 and Windows XP/2000:** If the garbage-collection Ping RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the garbage collection Ping RPC call by using Kerberos, NTLM, and other configured security providers.</span></span> <span data-ttu-id="8cd5c-148">Если поставщики безопасности не работают, локальный ДКОМСКМ делает вызов RPC с помощью команды ping для сбора мусора без защиты.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-148">If no security providers work, then the local DCOMSCM makes the garbage collection Ping RPC call using no security.</span></span>

<span data-ttu-id="8cd5c-149">Устанавливая этот флаг, локальная ДКОМСКМ в Windows Vista или более поздней версии может работать как в системах, предшествующих Vista.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-149">By setting this flag, the local DCOMSCM on Windows Vista or above can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="8cd5c-150">Не рекомендуется задавать флаг **дкомскм \_ ping \_ USE \_ MID \_ ауснсервице** , если это не требуется в целях обеспечения совместимости.</span><span class="sxs-lookup"><span data-stu-id="8cd5c-150">It is not recommended to set the **DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE** flag unless required for compatibility reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cd5c-151">См. также</span><span class="sxs-lookup"><span data-stu-id="8cd5c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd5c-152">Проверка подлинности для удаленных подключений</span><span class="sxs-lookup"><span data-stu-id="8cd5c-152">Authentication for Remote Connections</span></span>](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[<span data-ttu-id="8cd5c-153">енабледком</span><span class="sxs-lookup"><span data-stu-id="8cd5c-153">EnableDCOM</span></span>](enabledcom.md)
</dt> <dt>

[<span data-ttu-id="8cd5c-154">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="8cd5c-154">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="8cd5c-155">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="8cd5c-155">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 