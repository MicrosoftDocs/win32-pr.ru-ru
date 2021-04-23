---
title: RPC_AUTHZ_HANDLE (Рпкдце. h)
description: '\_Тип данных "обработчик RPC AUTHZ" \_ объявляет маркер авторизации. Этот маркер указывает сведения о привилегиях для клиентского приложения, которое сделал удаленный вызов процедуры.'
ms.assetid: 35b6a3f4-1703-4244-98fd-fad7de48b262
keywords:
- RPC_AUTHZ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b095100e1e224590ef6a285785da632e198e1b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137702"
---
# <a name="rpc_authz_handle"></a><span data-ttu-id="501f0-105">\_обработчик RPC AUTHZ \_</span><span class="sxs-lookup"><span data-stu-id="501f0-105">RPC\_AUTHZ\_HANDLE</span></span>

<span data-ttu-id="501f0-106">Тип данных " **\_ \_ обработчик RPC AUTHZ** " объявляет маркер авторизации.</span><span class="sxs-lookup"><span data-stu-id="501f0-106">The **RPC\_AUTHZ\_HANDLE** data type declares an authorization handle.</span></span> <span data-ttu-id="501f0-107">Этот маркер указывает сведения о привилегиях для клиентского приложения, которое сделал удаленный вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="501f0-107">This handle points to the privileges information for the client application that made the remote procedure call.</span></span>


```C++
typedef void* RPC_AUTHZ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="501f0-108">Требования</span><span class="sxs-lookup"><span data-stu-id="501f0-108">Requirements</span></span>



| <span data-ttu-id="501f0-109">Требование</span><span class="sxs-lookup"><span data-stu-id="501f0-109">Requirement</span></span> | <span data-ttu-id="501f0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="501f0-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="501f0-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="501f0-111">Minimum supported client</span></span><br/> | <span data-ttu-id="501f0-112">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="501f0-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="501f0-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="501f0-113">Minimum supported server</span></span><br/> | <span data-ttu-id="501f0-114">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="501f0-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="501f0-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="501f0-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="501f0-116"><dt>Рпкдце. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="501f0-116"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="501f0-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="501f0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501f0-118">**рпкбиндингинкаусклиент**</span><span class="sxs-lookup"><span data-stu-id="501f0-118">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> </dl>

 

 





