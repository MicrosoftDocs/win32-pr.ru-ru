---
description: Возвращает тип канала, прошедшего проверку подлинности.
ms.assetid: eec4b117-a9f2-479d-99d7-e5d4053cf6b4
title: D3DAUTHENTICATEDQUERY_CHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 58ac84a0caca5a5709c74adbca567633e12daa10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710833"
---
# <a name="d3dauthenticatedquery_channeltype"></a><span data-ttu-id="d0c69-103">D3DAUTHENTICATEDQUERY \_ чаннелтипе</span><span class="sxs-lookup"><span data-stu-id="d0c69-103">D3DAUTHENTICATEDQUERY\_CHANNELTYPE</span></span>

<span data-ttu-id="d0c69-104">Возвращает тип канала, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="d0c69-104">Returns the type of authenticated channel.</span></span>



| <span data-ttu-id="d0c69-105">Требование</span><span class="sxs-lookup"><span data-stu-id="d0c69-105">Requirement</span></span> | <span data-ttu-id="d0c69-106">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c69-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c69-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="d0c69-107">Query GUID</span></span>  | <span data-ttu-id="d0c69-108">**D3DAUTHENTICATEDQUERY \_ чаннелтипе**</span><span class="sxs-lookup"><span data-stu-id="d0c69-108">**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**</span></span>                                                                       |
| <span data-ttu-id="d0c69-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d0c69-109">Input data</span></span>  | [<span data-ttu-id="d0c69-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="d0c69-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="d0c69-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="d0c69-111">Return data</span></span> | [<span data-ttu-id="d0c69-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеричаннелтипе**</span><span class="sxs-lookup"><span data-stu-id="d0c69-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querychanneltype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="d0c69-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0c69-113">Remarks</span></span>

<span data-ttu-id="d0c69-114">Этот запрос действителен для всех типов каналов.</span><span class="sxs-lookup"><span data-stu-id="d0c69-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c69-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d0c69-115">Requirements</span></span>



| <span data-ttu-id="d0c69-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d0c69-116">Requirement</span></span> | <span data-ttu-id="d0c69-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c69-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c69-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0c69-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c69-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d0c69-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d0c69-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0c69-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c69-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0c69-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0c69-122">Header</span><span class="sxs-lookup"><span data-stu-id="d0c69-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c69-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c69-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c69-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0c69-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c69-125">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="d0c69-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="d0c69-126">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="d0c69-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="d0c69-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="d0c69-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




