---
description: Возвращает текущий уровень защиты для устройства.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262797"
---
# <a name="d3dauthenticatedquery_protection"></a><span data-ttu-id="884a5-103">\_Защита D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="884a5-103">D3DAUTHENTICATEDQUERY\_PROTECTION</span></span>

<span data-ttu-id="884a5-104">Возвращает текущий уровень защиты для устройства.</span><span class="sxs-lookup"><span data-stu-id="884a5-104">Returns the current protection level for the device.</span></span>



| <span data-ttu-id="884a5-105">Требование</span><span class="sxs-lookup"><span data-stu-id="884a5-105">Requirement</span></span> | <span data-ttu-id="884a5-106">Значение</span><span class="sxs-lookup"><span data-stu-id="884a5-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="884a5-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="884a5-107">Query GUID</span></span>  | <span data-ttu-id="884a5-108">**\_Защита D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="884a5-108">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>                                                                      |
| <span data-ttu-id="884a5-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="884a5-109">Input data</span></span>  | [<span data-ttu-id="884a5-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="884a5-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                       |
| <span data-ttu-id="884a5-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="884a5-111">Return data</span></span> | [<span data-ttu-id="884a5-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерипротектион**</span><span class="sxs-lookup"><span data-stu-id="884a5-112">**D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="884a5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="884a5-113">Remarks</span></span>

<span data-ttu-id="884a5-114">Этот запрос действителен для всех типов каналов.</span><span class="sxs-lookup"><span data-stu-id="884a5-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="884a5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="884a5-115">Requirements</span></span>



| <span data-ttu-id="884a5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="884a5-116">Requirement</span></span> | <span data-ttu-id="884a5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="884a5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="884a5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="884a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="884a5-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="884a5-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="884a5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="884a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="884a5-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="884a5-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="884a5-122">Header</span><span class="sxs-lookup"><span data-stu-id="884a5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="884a5-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="884a5-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884a5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="884a5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884a5-125">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="884a5-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="884a5-126">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="884a5-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="884a5-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="884a5-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




