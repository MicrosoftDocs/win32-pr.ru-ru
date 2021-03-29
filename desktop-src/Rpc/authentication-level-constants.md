---
title: Константы Authentication-Level (Рпкдце. h)
description: Константы уровня проверки подлинности представляют уровни проверки подлинности, передаваемые различным функциям времени выполнения.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535114"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="fedf5-103">Константы уровня проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="fedf5-103">Authentication-Level Constants</span></span>

<span data-ttu-id="fedf5-104">Константы уровня проверки подлинности представляют уровни проверки подлинности, передаваемые различным функциям времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="fedf5-104">The authentication-level constants represent authentication levels passed to various run-time functions.</span></span> <span data-ttu-id="fedf5-105">Эти уровни перечислены в порядке повышения уровня проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fedf5-105">These levels are listed in order of increasing authentication.</span></span> <span data-ttu-id="fedf5-106">Каждый новый уровень добавляет к проверке подлинности, обеспечиваемой предыдущим уровнем.</span><span class="sxs-lookup"><span data-stu-id="fedf5-106">Each new level adds to the authentication provided by the previous level.</span></span> <span data-ttu-id="fedf5-107">Если библиотека времени выполнения RPC не поддерживает указанный уровень, она автоматически обновляется до следующего более высокого поддерживаемого уровня.</span><span class="sxs-lookup"><span data-stu-id="fedf5-107">If the RPC run-time library does not support the specified level, it automatically upgrades to the next higher supported level.</span></span>



| <span data-ttu-id="fedf5-108">Константа</span><span class="sxs-lookup"><span data-stu-id="fedf5-108">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="fedf5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fedf5-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="fedf5-110"><dt>**\_ \_ \_ по умолчанию на уровне RPC C AUTHN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-110"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt></span></span> </dl>                    | <span data-ttu-id="fedf5-111">Использует уровень проверки подлинности по умолчанию для заданной службы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fedf5-111">Uses the default authentication level for the specified authentication service.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="fedf5-112"><dt>**\_уровень RPC \_ C \_ AUTHN \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="fedf5-113">Не выполняет проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="fedf5-113">Performs no authentication.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="fedf5-114"><dt>**\_подключение на уровне RPC C \_ AUTHN \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt></span></span> </dl>                    | <span data-ttu-id="fedf5-115">Проверка проходит успешно только в том случае, когда клиент устанавливает соединение с сервером.</span><span class="sxs-lookup"><span data-stu-id="fedf5-115">Authenticates only when the client establishes a relationship with a server.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="fedf5-116"><dt>**\_ \_ \_ вызов уровня RPC C \_ AUTHN**</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-116"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt></span></span> </dl>                             | <span data-ttu-id="fedf5-117">Проверка подлинности выполняется только в начале каждого удаленного вызова процедуры, когда сервер получает запрос.</span><span class="sxs-lookup"><span data-stu-id="fedf5-117">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="fedf5-118">Не применяется к удаленным вызовам процедур, выполненным с помощью последовательностей протоколов на основе подключений (которые начинаются с префикса "нкакн").</span><span class="sxs-lookup"><span data-stu-id="fedf5-118">Does not apply to remote procedure calls made using the connection-based protocol sequences (those that start with the prefix "ncacn").</span></span> <span data-ttu-id="fedf5-119">Если последовательность протокола в маркере привязки является последовательностью протокола на основе соединения и указан этот уровень, то эта подпрограмма использует \_ \_ \_ константу PKT уровня RPC C AUTHN \_ .</span><span class="sxs-lookup"><span data-stu-id="fedf5-119">If the protocol sequence in a binding handle is a connection-based protocol sequence and you specify this level, this routine instead uses the RPC\_C\_AUTHN\_LEVEL\_PKT constant.</span></span><br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="fedf5-120"><dt>**\_PKT на уровне RPC C \_ AUTHN \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt></span></span> </dl>                                | <span data-ttu-id="fedf5-121">Выполняет проверку подлинности только тех данных, которые получены от ожидаемого клиента.</span><span class="sxs-lookup"><span data-stu-id="fedf5-121">Authenticates only that all data received is from the expected client.</span></span> <span data-ttu-id="fedf5-122">Не проверяет сами данные.</span><span class="sxs-lookup"><span data-stu-id="fedf5-122">Does not validate the data itself.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="fedf5-123"><dt>**\_ \_ \_ \_ целостность PKT RPC C AUTHN Level \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-123"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt></span></span> </dl> | <span data-ttu-id="fedf5-124">Проверка подлинности и проверка того, что ни один из данных, передаваемых между клиентом и сервером, не был изменен.</span><span class="sxs-lookup"><span data-stu-id="fedf5-124">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="fedf5-125"><dt>**\_Конфиденциальность RPC C \_ AUTHN \_ Level \_ PKT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-125"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt></span></span> </dl>       | <span data-ttu-id="fedf5-126">Включает все предыдущие уровни и гарантирует, что данные с открытым текстом могут быть видны только отправителю и получателю.</span><span class="sxs-lookup"><span data-stu-id="fedf5-126">Includes all previous levels, and ensures clear text data can only be seen by the sender and the receiver.</span></span> <span data-ttu-id="fedf5-127">В локальном случае это подразумевает использование безопасного канала.</span><span class="sxs-lookup"><span data-stu-id="fedf5-127">In the local case, this involves using a secure channel.</span></span> <span data-ttu-id="fedf5-128">В удаленном случае это подразумевает шифрование значения аргумента для каждого удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="fedf5-128">In the remote case, this involves encrypting the argument value of each remote procedure call.</span></span><br/>                                                                                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="fedf5-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fedf5-129">Remarks</span></span>

<span data-ttu-id="fedf5-130">Независимо от значения, заданного константой, **нкалрпк** всегда использует \_ безопасность RPC C AUTHN на \_ \_ уровне \_ \_ безопасности PKT.</span><span class="sxs-lookup"><span data-stu-id="fedf5-130">Regardless of the value specified by the constant, **ncalrpc** always uses RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fedf5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="fedf5-131">Requirements</span></span>



| <span data-ttu-id="fedf5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="fedf5-132">Requirement</span></span> | <span data-ttu-id="fedf5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="fedf5-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fedf5-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fedf5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fedf5-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fedf5-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fedf5-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fedf5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fedf5-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fedf5-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fedf5-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fedf5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fedf5-139"><dt>Рпкдце. h</dt></span><span class="sxs-lookup"><span data-stu-id="fedf5-139"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fedf5-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fedf5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedf5-141">**рпкбиндингинкаусинфо**</span><span class="sxs-lookup"><span data-stu-id="fedf5-141">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="fedf5-142">**рпкбиндингсетаусинфо**</span><span class="sxs-lookup"><span data-stu-id="fedf5-142">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="fedf5-143">**рпкмгмтинкдефаултпротектлевел**</span><span class="sxs-lookup"><span data-stu-id="fedf5-143">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[<span data-ttu-id="fedf5-144">**рпкбиндингинкаусклиент**</span><span class="sxs-lookup"><span data-stu-id="fedf5-144">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="fedf5-145">**рпкбиндингинкаусклиентекс**</span><span class="sxs-lookup"><span data-stu-id="fedf5-145">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="fedf5-146">**рпкбиндингсетаусинфоекс**</span><span class="sxs-lookup"><span data-stu-id="fedf5-146">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="fedf5-147">**рпкбиндингинкаусинфоекс**</span><span class="sxs-lookup"><span data-stu-id="fedf5-147">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





