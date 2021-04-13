---
title: Константы Authorization-Service (Рпкдце. h)
description: Константы службы авторизации представляют службы авторизации, передаваемые различным функциям времени выполнения.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535597"
---
# <a name="authorization-service-constants"></a><span data-ttu-id="c59b2-103">Константы Authorization-Service</span><span class="sxs-lookup"><span data-stu-id="c59b2-103">Authorization-Service Constants</span></span>

<span data-ttu-id="c59b2-104">Константы службы авторизации представляют службы авторизации, передаваемые различным функциям времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="c59b2-104">The authorization service constants represent the authorization services passed to various run-time functions.</span></span>

<span data-ttu-id="c59b2-105">Следующие константы являются допустимыми значениями для параметра *аусзсвк* .</span><span class="sxs-lookup"><span data-stu-id="c59b2-105">The following constants are valid values for the *AuthzSvc* parameter.</span></span> <span data-ttu-id="c59b2-106">Большинство приложений находят \_ \_ недостаточный вызов RPC C AUTHZ \_ .</span><span class="sxs-lookup"><span data-stu-id="c59b2-106">Most applications find RPC\_C\_AUTHZ\_NON sufficient.</span></span>



| <span data-ttu-id="c59b2-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="c59b2-107">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="c59b2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c59b2-108">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="c59b2-109"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c59b2-109"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="c59b2-110">Сервер не выполняет авторизацию.</span><span class="sxs-lookup"><span data-stu-id="c59b2-110">Server performs no authorization.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="c59b2-111"><dt>**RPC \_ C \_ AUTHZ \_ имя**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c59b2-111"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="c59b2-112">Сервер выполняет авторизацию на основе имени участника клиента.</span><span class="sxs-lookup"><span data-stu-id="c59b2-112">Server performs authorization based on the client's principal name.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="c59b2-113"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c59b2-113"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="c59b2-114">Сервер выполняет проверку авторизации с помощью сведений о сертификате ключа доступа DCE, которые отправляются на сервер при каждом вызове удаленной процедуры с помощью маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="c59b2-114">Server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="c59b2-115">Как правило, доступ проверяется по спискам управления доступом DCE ([ACL](/windows/desktop/api/winnt/ns-winnt-acl)).</span><span class="sxs-lookup"><span data-stu-id="c59b2-115">Generally, access is checked against DCE access control lists ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)).</span></span><br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="c59b2-116"><dt>**RPC \_ C \_ AUTHZ \_ по умолчанию**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="c59b2-116"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="c59b2-117">Сервер использует службу авторизации по умолчанию для текущего поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="c59b2-117">Server uses the default authorization service for the current SSP.</span></span><br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="c59b2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c59b2-118">Requirements</span></span>



| <span data-ttu-id="c59b2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c59b2-119">Requirement</span></span> | <span data-ttu-id="c59b2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c59b2-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c59b2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c59b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c59b2-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c59b2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c59b2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c59b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c59b2-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c59b2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c59b2-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c59b2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c59b2-126"><dt>Рпкдце. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59b2-126"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59b2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c59b2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59b2-128">**рпкбиндингинкаусинфо**</span><span class="sxs-lookup"><span data-stu-id="c59b2-128">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="c59b2-129">**рпкбиндингсетаусинфо**</span><span class="sxs-lookup"><span data-stu-id="c59b2-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="c59b2-130">**рпкбиндингинкаусклиент**</span><span class="sxs-lookup"><span data-stu-id="c59b2-130">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="c59b2-131">**рпкбиндингинкаусклиентекс**</span><span class="sxs-lookup"><span data-stu-id="c59b2-131">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="c59b2-132">**рпкбиндингсетаусинфоекс**</span><span class="sxs-lookup"><span data-stu-id="c59b2-132">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="c59b2-133">**рпкбиндингинкаусинфоекс**</span><span class="sxs-lookup"><span data-stu-id="c59b2-133">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[<span data-ttu-id="c59b2-134">**рпкмгмтинкдефаултпротектлевел**</span><span class="sxs-lookup"><span data-stu-id="c59b2-134">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

