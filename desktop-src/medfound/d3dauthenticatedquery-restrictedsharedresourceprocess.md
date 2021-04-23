---
description: Возвращает сведения о процессе, которому разрешено открывать общие ресурсы с ограниченным доступом.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710829"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a><span data-ttu-id="35097-103">D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесс</span><span class="sxs-lookup"><span data-stu-id="35097-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS</span></span>

<span data-ttu-id="35097-104">Возвращает сведения о процессе, которому разрешено открывать общие ресурсы с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="35097-104">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="35097-105">Требование</span><span class="sxs-lookup"><span data-stu-id="35097-105">Requirement</span></span> | <span data-ttu-id="35097-106">Значение</span><span class="sxs-lookup"><span data-stu-id="35097-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35097-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="35097-107">Query GUID</span></span>  | <span data-ttu-id="35097-108">**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесс**</span><span class="sxs-lookup"><span data-stu-id="35097-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>                                                                                           |
| <span data-ttu-id="35097-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="35097-109">Input data</span></span>  | [<span data-ttu-id="35097-110">**\_ \_ Входные данные куерирестриктедшаредресаурцепроцесс D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="35097-110">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| <span data-ttu-id="35097-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="35097-111">Return data</span></span> | [<span data-ttu-id="35097-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс**</span><span class="sxs-lookup"><span data-stu-id="35097-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="35097-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35097-113">Remarks</span></span>

<span data-ttu-id="35097-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="35097-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="35097-115">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="35097-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="35097-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="35097-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="35097-117">Требования</span><span class="sxs-lookup"><span data-stu-id="35097-117">Requirements</span></span>



| <span data-ttu-id="35097-118">Требование</span><span class="sxs-lookup"><span data-stu-id="35097-118">Requirement</span></span> | <span data-ttu-id="35097-119">Значение</span><span class="sxs-lookup"><span data-stu-id="35097-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35097-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35097-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35097-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="35097-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="35097-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35097-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35097-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35097-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="35097-124">Header</span><span class="sxs-lookup"><span data-stu-id="35097-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="35097-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="35097-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35097-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35097-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35097-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="35097-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="35097-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="35097-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="35097-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="35097-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




