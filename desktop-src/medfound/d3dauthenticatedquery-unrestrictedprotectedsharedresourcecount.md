---
description: Возвращает количество защищенных общих ресурсов, которые могут быть открыты любым процессом без ограничений.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662113"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a><span data-ttu-id="268b8-103">D3DAUTHENTICATEDQUERY \_ унрестриктедпротектедшаредресаурцекаунт</span><span class="sxs-lookup"><span data-stu-id="268b8-103">D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span></span>

<span data-ttu-id="268b8-104">Возвращает количество защищенных общих ресурсов, которые могут быть открыты любым процессом без ограничений.</span><span class="sxs-lookup"><span data-stu-id="268b8-104">Returns the number of protected shared resources that can be opened by any process without restrictions.</span></span>



| <span data-ttu-id="268b8-105">Требование</span><span class="sxs-lookup"><span data-stu-id="268b8-105">Requirement</span></span> | <span data-ttu-id="268b8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="268b8-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="268b8-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="268b8-107">Query GUID</span></span>  | <span data-ttu-id="268b8-108">**D3DAUTHENTICATEDQUERY \_ унрестриктедпротектедшаредресаурцекаунт**</span><span class="sxs-lookup"><span data-stu-id="268b8-108">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>                                                                                                    |
| <span data-ttu-id="268b8-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="268b8-109">Input data</span></span>  | [<span data-ttu-id="268b8-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="268b8-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                                   |
| <span data-ttu-id="268b8-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="268b8-111">Return data</span></span> | [<span data-ttu-id="268b8-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерюнрестриктедпротектедшаредресаурцекаунт**</span><span class="sxs-lookup"><span data-stu-id="268b8-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="268b8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="268b8-113">Remarks</span></span>

<span data-ttu-id="268b8-114">Единственным типом канала, поддерживающим этот запрос, является **D3DAUTHENTICATEDCHANNEL \_ Driver \_ Software**.</span><span class="sxs-lookup"><span data-stu-id="268b8-114">The only channel type that supports this query is **D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="268b8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="268b8-115">Requirements</span></span>



| <span data-ttu-id="268b8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="268b8-116">Requirement</span></span> | <span data-ttu-id="268b8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="268b8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="268b8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="268b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="268b8-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="268b8-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="268b8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="268b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="268b8-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="268b8-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="268b8-122">Header</span><span class="sxs-lookup"><span data-stu-id="268b8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="268b8-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="268b8-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="268b8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="268b8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268b8-125">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="268b8-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="268b8-126">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="268b8-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="268b8-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="268b8-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




