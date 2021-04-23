---
title: RPC_EP_INQ_HANDLE (Рпкасинк. h)
description: '\_ \_ \_ Тип данных Handle инк для RPC EP объявляет маркер для контекста запроса. Приложения RPC используют его для просмотра сведений об адресе сервера, хранящегося на карте конечных точек.'
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416009"
---
# <a name="rpc_ep_inq_handle"></a><span data-ttu-id="61041-105">RPC \_ EP \_ инк, \_ обработчик</span><span class="sxs-lookup"><span data-stu-id="61041-105">RPC\_EP\_INQ\_HANDLE</span></span>

<span data-ttu-id="61041-106">Тип **данных \_ \_ \_ Handle инк для RPC EP** объявляет маркер для контекста запроса.</span><span class="sxs-lookup"><span data-stu-id="61041-106">The **RPC\_EP\_INQ\_HANDLE** data type declares a handle for an inquiry context.</span></span> <span data-ttu-id="61041-107">Приложения RPC используют его для просмотра сведений об адресе сервера, хранящегося на карте конечных точек.</span><span class="sxs-lookup"><span data-stu-id="61041-107">RPC applications use it to view server address information stored in the endpoint map.</span></span>


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="61041-108">Требования</span><span class="sxs-lookup"><span data-stu-id="61041-108">Requirements</span></span>



| <span data-ttu-id="61041-109">Требование</span><span class="sxs-lookup"><span data-stu-id="61041-109">Requirement</span></span> | <span data-ttu-id="61041-110">Значение</span><span class="sxs-lookup"><span data-stu-id="61041-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61041-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61041-111">Minimum supported client</span></span><br/> | <span data-ttu-id="61041-112">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61041-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="61041-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61041-113">Minimum supported server</span></span><br/> | <span data-ttu-id="61041-114">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61041-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="61041-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="61041-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="61041-116"><dt>Рпкасинк. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61041-116"><dt>Rpcasync.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61041-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61041-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61041-118">**рпкмгмтепелтинкбегин**</span><span class="sxs-lookup"><span data-stu-id="61041-118">**RpcMgmtEpEltInqBegin**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[<span data-ttu-id="61041-119">**рпкмгмтепелтинкнекст**</span><span class="sxs-lookup"><span data-stu-id="61041-119">**RpcMgmtEpEltInqNext**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[<span data-ttu-id="61041-120">**рпкмгмтепелтинкдоне**</span><span class="sxs-lookup"><span data-stu-id="61041-120">**RpcMgmtEpEltInqDone**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





