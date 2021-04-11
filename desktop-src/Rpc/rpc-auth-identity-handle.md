---
title: RPC_AUTH_IDENTITY_HANDLE (Рпкдце. h)
description: '\_Тип данных обработчика проверки подлинности RPC \_ \_ объявляет маркер, указывающий на структуру, содержащую учетные данные проверки подлинности и авторизации клиента, указанные для удаленных вызовов процедур.'
ms.assetid: 06e45348-a392-45be-9f8a-e77ef887f26c
keywords:
- RPC_AUTH_IDENTITY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86559e7852172d34898d48f13bb2975ed792d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137703"
---
# <a name="rpc_auth_identity_handle"></a><span data-ttu-id="a9a49-104">\_ \_ маркер идентификации RPC \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="a9a49-104">RPC\_AUTH\_IDENTITY\_HANDLE</span></span>

<span data-ttu-id="a9a49-105">Тип **данных \_ \_ \_ обработчика проверки подлинности RPC** объявляет маркер, указывающий на структуру, содержащую учетные данные проверки подлинности и авторизации клиента, указанные для удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="a9a49-105">The **RPC\_AUTH\_IDENTITY\_HANDLE** data type declares a handle that points to a structure containing the client's authentication and authorization credentials specified for remote procedure calls.</span></span>


```C++
typedef void* RPC_AUTH_IDENTITY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="a9a49-106">Требования</span><span class="sxs-lookup"><span data-stu-id="a9a49-106">Requirements</span></span>



| <span data-ttu-id="a9a49-107">Требование</span><span class="sxs-lookup"><span data-stu-id="a9a49-107">Requirement</span></span> | <span data-ttu-id="a9a49-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a9a49-108">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a49-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9a49-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a49-110">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9a49-110">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a9a49-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9a49-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a49-112">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9a49-112">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9a49-113">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a9a49-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9a49-114"><dt>Рпкдце. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a49-114"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a49-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9a49-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a49-116">**рпкбиндингинкаусинфо**</span><span class="sxs-lookup"><span data-stu-id="a9a49-116">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="a9a49-117">**рпкбиндингсетаусинфо**</span><span class="sxs-lookup"><span data-stu-id="a9a49-117">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> </dl>

 

 





