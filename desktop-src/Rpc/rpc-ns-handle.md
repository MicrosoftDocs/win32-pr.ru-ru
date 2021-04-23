---
title: RPC_NS_HANDLE (Рпкнси. h)
description: Маркер NS для RPC типа данных \_ \_ определяет маркер службы Name-Service.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535105"
---
# <a name="rpc_ns_handle"></a><span data-ttu-id="1cb4d-104">\_маркер NS \_ RPC</span><span class="sxs-lookup"><span data-stu-id="1cb4d-104">RPC\_NS\_HANDLE</span></span>

<span data-ttu-id="1cb4d-105">**\_ \_ Маркер NS для RPC** типа данных определяет маркер службы Name-Service.</span><span class="sxs-lookup"><span data-stu-id="1cb4d-105">The data type **RPC\_NS\_HANDLE** defines a name-service handle.</span></span>


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="1cb4d-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cb4d-106">Remarks</span></span>

<span data-ttu-id="1cb4d-107">Маркер службы имени — это непрозрачная переменная, содержащая сведения, которые используются библиотекой времени выполнения RPC для возврата следующих данных RPC из базы данных Name-Service:</span><span class="sxs-lookup"><span data-stu-id="1cb4d-107">A name-service handle is an opaque variable containing information the RPC run-time library uses to return the following RPC data from the name-service database:</span></span>

-   <span data-ttu-id="1cb4d-108">Дескрипторы привязки сервера</span><span class="sxs-lookup"><span data-stu-id="1cb4d-108">Server-binding handles</span></span>
-   <span data-ttu-id="1cb4d-109">UUID ресурсов, предлагаемых элементами профиля сервера</span><span class="sxs-lookup"><span data-stu-id="1cb4d-109">UUIDs of resources offered by server profile members</span></span>
-   <span data-ttu-id="1cb4d-110">Члены группы</span><span class="sxs-lookup"><span data-stu-id="1cb4d-110">Group members</span></span>

<span data-ttu-id="1cb4d-111">Областью действия маркера имени службы является из процедуры "Begin" с помощью соответствующей процедуры "Done".</span><span class="sxs-lookup"><span data-stu-id="1cb4d-111">The scope of a name-service handle is from a "Begin" routine through the corresponding "Done" routine.</span></span>

<span data-ttu-id="1cb4d-112">Приложения отвечают за управление параллелизмом для дескрипторов службы Name-Service в потоках.</span><span class="sxs-lookup"><span data-stu-id="1cb4d-112">Applications are responsible for concurrency control of name-service handles across threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb4d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1cb4d-113">Requirements</span></span>



| <span data-ttu-id="1cb4d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1cb4d-114">Requirement</span></span> | <span data-ttu-id="1cb4d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1cb4d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb4d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1cb4d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb4d-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1cb4d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1cb4d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1cb4d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb4d-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1cb4d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1cb4d-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1cb4d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cb4d-121"><dt>Рпкнси. h (включение RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cb4d-121"><dt>Rpcnsi.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb4d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cb4d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb4d-123">**рпкнсбиндингимпортбегин**</span><span class="sxs-lookup"><span data-stu-id="1cb4d-123">**RpcNsBindingImportBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[<span data-ttu-id="1cb4d-124">**рпкнсбиндингимпортдоне**</span><span class="sxs-lookup"><span data-stu-id="1cb4d-124">**RpcNsBindingImportDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[<span data-ttu-id="1cb4d-125">**рпкнсбиндингимпортнекст**</span><span class="sxs-lookup"><span data-stu-id="1cb4d-125">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[<span data-ttu-id="1cb4d-126">**рпкнсбиндинглукупбегин**</span><span class="sxs-lookup"><span data-stu-id="1cb4d-126">**RpcNsBindingLookupBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[<span data-ttu-id="1cb4d-127">**рпкнсбиндинглукупдоне**</span><span class="sxs-lookup"><span data-stu-id="1cb4d-127">**RpcNsBindingLookupDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[<span data-ttu-id="1cb4d-128">**рпкнсбиндинглукупнекст**</span><span class="sxs-lookup"><span data-stu-id="1cb4d-128">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





