---
title: Константы авторизации (Рпкдце. h)
description: Определяет, что авторизует сервер.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803934"
---
# <a name="authorization-constants"></a><span data-ttu-id="b344f-103">Константы авторизации</span><span class="sxs-lookup"><span data-stu-id="b344f-103">Authorization Constants</span></span>

<span data-ttu-id="b344f-104">Определяет, что авторизует сервер.</span><span class="sxs-lookup"><span data-stu-id="b344f-104">Defines what the server authorizes.</span></span>



| <span data-ttu-id="b344f-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="b344f-105">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="b344f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b344f-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="b344f-107"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b344f-107"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="b344f-108">Сервер не выполняет авторизацию.</span><span class="sxs-lookup"><span data-stu-id="b344f-108">The server performs no authorization.</span></span> <span data-ttu-id="b344f-109">В настоящее время RPC \_ c \_ AUTHN \_ WinNT, RPC \_ c \_ AUTHN \_ GSS \_ SChannel и RPC \_ c \_ AUTHN \_ GSS \_ Kerberos используют только RPC \_ c \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="b344f-109">Currently, RPC\_C\_AUTHN\_WINNT, RPC\_C\_AUTHN\_GSS\_SCHANNEL, and RPC\_C\_AUTHN\_GSS\_KERBEROS all use only RPC\_C\_AUTHZ\_NONE.</span></span><br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="b344f-110"><dt>**RPC \_ C \_ AUTHZ \_ имя**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b344f-110"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="b344f-111">Сервер выполняет авторизацию на основе имени участника клиента.</span><span class="sxs-lookup"><span data-stu-id="b344f-111">The server performs authorization based on the client's principal name.</span></span> <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="b344f-112"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b344f-112"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="b344f-113">Сервер выполняет проверку авторизации, используя сведения о сертификате ключа доступа DCE, которые отправляются на сервер при каждом вызове удаленной процедуры, выполненной с помощью маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="b344f-113">The server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="b344f-114">Как правило, доступ проверяется по спискам управления доступом DCE (ACL).</span><span class="sxs-lookup"><span data-stu-id="b344f-114">Generally, access is checked against DCE access control lists (ACLs).</span></span> <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="b344f-115"><dt>**RPC \_ C \_ AUTHZ \_ по умолчанию**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="b344f-115"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="b344f-116">DCOM может выбрать уровень авторизации с помощью обычного алгоритма согласования безопасности общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b344f-116">DCOM can choose the authorization level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="b344f-117">Дополнительные сведения см. в разделе [Безопасность — общий согласование](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="b344f-117">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="b344f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b344f-118">Remarks</span></span>

<span data-ttu-id="b344f-119">Эти константы используются методами интерфейса [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="b344f-119">These constants are used by methods of the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="b344f-120">Они используются в структуре [**единственной \_ \_ службы проверки подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , которая извлекается функцией [**кокуеряусентикатионсервицес**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .</span><span class="sxs-lookup"><span data-stu-id="b344f-120">They are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structure, which is retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="b344f-121">Они также используются в структуре [**единственной \_ \_ информации для проверки подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , которая, в свою очередь, является членом [**единственной структуры \_ \_ списка проверки подлинности**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) .</span><span class="sxs-lookup"><span data-stu-id="b344f-121">They are also used in the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure, which in turn is a member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) structure.</span></span> <span data-ttu-id="b344f-122">Эта структура представляет собой список служб проверки подлинности, выполняемых ими служб авторизации, а также сведения о проверке подлинности для каждой службы передаются функции [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) и методу [**Иклиентсекурити:: сетбланкет**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .</span><span class="sxs-lookup"><span data-stu-id="b344f-122">This structure, which is a list of authentication services, the authorization services they perform, and the authentication information for each service, is passed to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and the [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b344f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b344f-123">Requirements</span></span>



| <span data-ttu-id="b344f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b344f-124">Requirement</span></span> | <span data-ttu-id="b344f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b344f-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b344f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b344f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b344f-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b344f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b344f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b344f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b344f-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b344f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b344f-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b344f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b344f-131"><dt>Рпкдце. h</dt></span><span class="sxs-lookup"><span data-stu-id="b344f-131"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b344f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b344f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b344f-133">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="b344f-133">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="b344f-134">**кокуеряусентикатионсервицес**</span><span class="sxs-lookup"><span data-stu-id="b344f-134">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="b344f-135">**иклиентсекурити**</span><span class="sxs-lookup"><span data-stu-id="b344f-135">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="b344f-136">**\_сведения о единственной проверке подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="b344f-136">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="b344f-137">**Единственная \_ Служба проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="b344f-137">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

