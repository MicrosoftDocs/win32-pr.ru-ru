---
description: Возвращает один из идентификаторов вывода, связанный с указанным сеансом шифрования и устройством Direct3D.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808122"
---
# <a name="d3dauthenticatedquery_outputid"></a><span data-ttu-id="282c7-103">D3DAUTHENTICATEDQUERY \_ аутпутид</span><span class="sxs-lookup"><span data-stu-id="282c7-103">D3DAUTHENTICATEDQUERY\_OUTPUTID</span></span>

<span data-ttu-id="282c7-104">Возвращает один из идентификаторов вывода, связанный с указанным сеансом шифрования и устройством Direct3D.</span><span class="sxs-lookup"><span data-stu-id="282c7-104">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="282c7-105">Требование</span><span class="sxs-lookup"><span data-stu-id="282c7-105">Requirement</span></span> | <span data-ttu-id="282c7-106">Значение</span><span class="sxs-lookup"><span data-stu-id="282c7-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="282c7-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="282c7-107">Query GUID</span></span>  | <span data-ttu-id="282c7-108">**D3DAUTHENTICATEDQUERY \_ аутпутид**</span><span class="sxs-lookup"><span data-stu-id="282c7-108">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>                                                                    |
| <span data-ttu-id="282c7-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="282c7-109">Input data</span></span>  | [<span data-ttu-id="282c7-110">**\_ \_ Входные данные куерйоутпутид D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="282c7-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-input.md)   |
| <span data-ttu-id="282c7-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="282c7-111">Return data</span></span> | [<span data-ttu-id="282c7-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерйоутпутид**</span><span class="sxs-lookup"><span data-stu-id="282c7-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="282c7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="282c7-113">Remarks</span></span>

<span data-ttu-id="282c7-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="282c7-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="282c7-115">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="282c7-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="282c7-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="282c7-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="282c7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="282c7-117">Requirements</span></span>



| <span data-ttu-id="282c7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="282c7-118">Requirement</span></span> | <span data-ttu-id="282c7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="282c7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="282c7-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="282c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="282c7-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="282c7-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="282c7-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="282c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="282c7-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="282c7-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="282c7-124">Header</span><span class="sxs-lookup"><span data-stu-id="282c7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="282c7-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="282c7-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="282c7-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="282c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="282c7-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="282c7-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="282c7-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="282c7-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="282c7-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="282c7-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




