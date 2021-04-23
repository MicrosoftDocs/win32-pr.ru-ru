---
title: Константы Authentication-Service (Рпкдце. h)
description: Константы службы проверки подлинности представляют службы проверки подлинности, передаваемые различным функциям времени выполнения.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535111"
---
# <a name="authentication-service-constants"></a><span data-ttu-id="6bfea-103">Константы Authentication-Service</span><span class="sxs-lookup"><span data-stu-id="6bfea-103">Authentication-Service Constants</span></span>

<span data-ttu-id="6bfea-104">Константы службы проверки подлинности представляют службы проверки подлинности, передаваемые различным функциям времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="6bfea-104">The authentication service constants represent the authentication services passed to various run-time functions.</span></span>

<span data-ttu-id="6bfea-105">Следующие константы являются допустимыми значениями для параметра *ауснсвк* .</span><span class="sxs-lookup"><span data-stu-id="6bfea-105">The following constants are valid values for the *AuthnSvc* parameter.</span></span>



| <span data-ttu-id="6bfea-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="6bfea-106">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="6bfea-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6bfea-107">Description</span></span>                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="6bfea-108"><dt>**RPC \_ C \_ AUTHN \_ нет**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-108"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="6bfea-109">Без проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6bfea-109">No authentication.</span></span><br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="6bfea-110"><dt>**RPC \_ C \_ AUTHN \_ DCE \_ частный**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-110"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="6bfea-111">Используйте проверку подлинности с закрытым ключом среды распределенных вычислений (DCE).</span><span class="sxs-lookup"><span data-stu-id="6bfea-111">Use Distributed Computing Environment (DCE) private key authentication.</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="6bfea-112"><dt>**RPC \_ C \_ AUTHN \_ DCE \_ Public**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-112"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="6bfea-113">Проверка подлинности с открытым ключом DCE (зарезервировано для будущего использования).</span><span class="sxs-lookup"><span data-stu-id="6bfea-113">DCE public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="6bfea-114"><dt>**RPC \_ C \_ AUTHN \_ Dec \_**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-114"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="6bfea-115">Аутентификация с открытым ключом DEC (зарезервировано для будущего использования).</span><span class="sxs-lookup"><span data-stu-id="6bfea-115">DEC public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="6bfea-116"><dt>**RPC \_ C \_ AUTHN \_ GSS — \_ согласование**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="6bfea-117">Используйте [поставщик общих служб Майкрософт для согласования](/windows/desktop/SecAuthN/microsoft-negotiate).</span><span class="sxs-lookup"><span data-stu-id="6bfea-117">Use the [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span></span> <span data-ttu-id="6bfea-118">Этот поставщик общих служб согласовывает использование протоколов NTLM и протокола безопасности Kerberos (SSP).</span><span class="sxs-lookup"><span data-stu-id="6bfea-118">This SSP negotiates between the use of the NTLM and Kerberos protocol Security Support Providers (SSP).</span></span><br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="6bfea-119"><dt>**RPC \_ C \_ AUTHN \_ WinNT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-119"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="6bfea-120">Используйте [SSP Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).</span><span class="sxs-lookup"><span data-stu-id="6bfea-120">Use the [Microsoft NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm).</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="6bfea-121"><dt>**RPC \_ C \_ AUTHN \_ GSS \_ SChannel**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-121"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="6bfea-122">Используйте для этого [поставщик общих служб SChannel](/windows/desktop/SecAuthN/secure-channel).</span><span class="sxs-lookup"><span data-stu-id="6bfea-122">Use the [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span></span> <span data-ttu-id="6bfea-123">Этот поставщик общих служб поддерживает протокол SSL, технологию частной связи (PCT) и безопасность на транспортном уровне (TLS).</span><span class="sxs-lookup"><span data-stu-id="6bfea-123">This SSP supports Secure Socket Layer (SSL), private communication technology (PCT), and transport level security (TLS).</span></span><br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="6bfea-124"><dt>**RPC \_ C \_ AUTHN \_ GSS \_ Kerberos**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-124"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="6bfea-125">Используйте [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span><span class="sxs-lookup"><span data-stu-id="6bfea-125">Use the [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span></span><br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="6bfea-126"><dt>**RPC \_ C \_ AUTHN \_ DPA**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-126"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="6bfea-127">Используйте распределенную проверку пароля (DPA).</span><span class="sxs-lookup"><span data-stu-id="6bfea-127">Use Distributed Password Authentication (DPA).</span></span><br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="6bfea-128"><dt>**RPC \_ C \_ AUTHN \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-128"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="6bfea-129">SSP протокола проверки подлинности, используемый для сети Microsoft (MSN).</span><span class="sxs-lookup"><span data-stu-id="6bfea-129">Authentication protocol SSP used for the Microsoft Network (MSN).</span></span><br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="6bfea-130"><dt>**RPC \_ C \_ AUTHN \_ Digest**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-130"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="6bfea-131">Windows XP или более поздней версии: используйте [дайджест-поставщик Microsoft Digest](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span><span class="sxs-lookup"><span data-stu-id="6bfea-131">Windows XP or later: Use the [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span></span><br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="6bfea-132"><dt>**RPC \_ \_ \_ \_ Расширитель C AUTHN него**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-132"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="6bfea-133">Windows 7 или более поздней версии: зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="6bfea-133">Windows 7 or later: Reserved.</span></span> <span data-ttu-id="6bfea-134">Не использовать</span><span class="sxs-lookup"><span data-stu-id="6bfea-134">Do not use</span></span><br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="6bfea-135"><dt>**RPC \_ C \_ AUTHN \_ MQ**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-135"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="6bfea-136">Этот поставщик общих служб предоставляет совместимую с SSPI оболочку для протокола транспортного уровня очереди сообщений Майкрософт (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="6bfea-136">This SSP provides an SSPI-compatible wrapper for the Microsoft Message Queue (MSMQ) transport-level protocol.</span></span><br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="6bfea-137"><dt>**RPC \_ C \_ AUTHN \_ по умолчанию**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-137"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl>            | <span data-ttu-id="6bfea-138">Используйте службу проверки подлинности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6bfea-138">Use the default authentication service.</span></span><br/>                                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="6bfea-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bfea-139">Remarks</span></span>

<span data-ttu-id="6bfea-140">Укажите RPC \_ C \_ AUTHN \_ None, чтобы отключить проверку подлинности для вызовов удаленных процедур, выполненных на основе маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="6bfea-140">Specify RPC\_C\_AUTHN\_NONE to turn off authentication for remote procedure calls made over a binding handle.</span></span> <span data-ttu-id="6bfea-141">При указании RPC \_ c \_ AUTHN \_ по умолчанию библиотека времени выполнения RPC использует \_ \_ \_ службу проверки подлинности RPC c AUTHN WinNT для удаленных вызовов процедур, выполненных с помощью маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="6bfea-141">When you specify RPC\_C\_AUTHN\_DEFAULT, the RPC run-time library uses the RPC\_C\_AUTHN\_WINNT authentication service for remote procedure calls made using the binding handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bfea-142">Требования</span><span class="sxs-lookup"><span data-stu-id="6bfea-142">Requirements</span></span>



| <span data-ttu-id="6bfea-143">Требование</span><span class="sxs-lookup"><span data-stu-id="6bfea-143">Requirement</span></span> | <span data-ttu-id="6bfea-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6bfea-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfea-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bfea-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6bfea-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6bfea-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6bfea-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bfea-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6bfea-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6bfea-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6bfea-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6bfea-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bfea-150"><dt>Рпкдце. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bfea-150"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bfea-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bfea-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfea-152">**рпкбиндингинкаусинфо**</span><span class="sxs-lookup"><span data-stu-id="6bfea-152">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="6bfea-153">**рпкбиндингсетаусинфо**</span><span class="sxs-lookup"><span data-stu-id="6bfea-153">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="6bfea-154">**рпкбиндингинкаусклиент**</span><span class="sxs-lookup"><span data-stu-id="6bfea-154">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="6bfea-155">**рпкбиндингинкаусклиентекс**</span><span class="sxs-lookup"><span data-stu-id="6bfea-155">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="6bfea-156">**рпкбиндингсетаусинфоекс**</span><span class="sxs-lookup"><span data-stu-id="6bfea-156">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="6bfea-157">**рпкбиндингинкаусинфоекс**</span><span class="sxs-lookup"><span data-stu-id="6bfea-157">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

