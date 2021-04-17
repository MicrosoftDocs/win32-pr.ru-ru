---
description: Возвращает число процессов, которым разрешено открывать общие ресурсы с ограниченным доступом.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710828"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a><span data-ttu-id="f9c85-103">D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесскаунт</span><span class="sxs-lookup"><span data-stu-id="f9c85-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span></span>

<span data-ttu-id="f9c85-104">Возвращает число процессов, которым разрешено открывать общие ресурсы с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="f9c85-104">Returns the number of processes that are allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="f9c85-105">Требование</span><span class="sxs-lookup"><span data-stu-id="f9c85-105">Requirement</span></span> | <span data-ttu-id="f9c85-106">Значение</span><span class="sxs-lookup"><span data-stu-id="f9c85-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c85-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="f9c85-107">Query GUID</span></span>  | <span data-ttu-id="f9c85-108">**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесскаунт**</span><span class="sxs-lookup"><span data-stu-id="f9c85-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span></span>                                                                                                |
| <span data-ttu-id="f9c85-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f9c85-109">Input data</span></span>  | [<span data-ttu-id="f9c85-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="f9c85-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                           |
| <span data-ttu-id="f9c85-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="f9c85-111">Return data</span></span> | [<span data-ttu-id="f9c85-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесскаунт**</span><span class="sxs-lookup"><span data-stu-id="f9c85-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="f9c85-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9c85-113">Remarks</span></span>

<span data-ttu-id="f9c85-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="f9c85-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="f9c85-115">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="f9c85-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="f9c85-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="f9c85-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c85-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f9c85-117">Requirements</span></span>



| <span data-ttu-id="f9c85-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f9c85-118">Requirement</span></span> | <span data-ttu-id="f9c85-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f9c85-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c85-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9c85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c85-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f9c85-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f9c85-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9c85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c85-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9c85-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f9c85-124">Header</span><span class="sxs-lookup"><span data-stu-id="f9c85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9c85-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9c85-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c85-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9c85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c85-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="f9c85-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="f9c85-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="f9c85-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="f9c85-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="f9c85-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




