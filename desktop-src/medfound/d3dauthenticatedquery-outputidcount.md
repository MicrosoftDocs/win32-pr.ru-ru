---
description: Возвращает число идентификаторов вывода, связанных с указанным сеансом шифрования и устройством Direct3D.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808117"
---
# <a name="d3dauthenticatedquery_outputidcount"></a><span data-ttu-id="9ec53-103">D3DAUTHENTICATEDQUERY \_ аутпутидкаунт</span><span class="sxs-lookup"><span data-stu-id="9ec53-103">D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT</span></span>

<span data-ttu-id="9ec53-104">Возвращает число идентификаторов вывода, связанных с указанным сеансом шифрования и устройством Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9ec53-104">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="9ec53-105">Требование</span><span class="sxs-lookup"><span data-stu-id="9ec53-105">Requirement</span></span> | <span data-ttu-id="9ec53-106">Значение</span><span class="sxs-lookup"><span data-stu-id="9ec53-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec53-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="9ec53-107">Query GUID</span></span>  | <span data-ttu-id="9ec53-108">**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**</span><span class="sxs-lookup"><span data-stu-id="9ec53-108">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>                                                                         |
| <span data-ttu-id="9ec53-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9ec53-109">Input data</span></span>  | [<span data-ttu-id="9ec53-110">**\_ \_ Входные данные куерйоутпутидкаунт D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9ec53-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| <span data-ttu-id="9ec53-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="9ec53-111">Return data</span></span> | [<span data-ttu-id="9ec53-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерйоутпутидкаунт**</span><span class="sxs-lookup"><span data-stu-id="9ec53-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="9ec53-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ec53-113">Remarks</span></span>

<span data-ttu-id="9ec53-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="9ec53-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="9ec53-115">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9ec53-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="9ec53-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9ec53-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec53-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9ec53-117">Requirements</span></span>



| <span data-ttu-id="9ec53-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9ec53-118">Requirement</span></span> | <span data-ttu-id="9ec53-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9ec53-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec53-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ec53-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec53-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9ec53-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ec53-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ec53-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec53-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ec53-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ec53-124">Header</span><span class="sxs-lookup"><span data-stu-id="9ec53-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ec53-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ec53-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec53-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ec53-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec53-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="9ec53-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="9ec53-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="9ec53-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="9ec53-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9ec53-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




