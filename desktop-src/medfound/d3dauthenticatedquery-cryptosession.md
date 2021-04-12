---
description: Возвращает дескрипторы криптографического сеанса и устройства Direct3D, связанные с указанным устройством декодера DirectX Video Acceleration 2 (ДКСВА-2).
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262799"
---
# <a name="d3dauthenticatedquery_cryptosession"></a><span data-ttu-id="981e4-103">D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="981e4-103">D3DAUTHENTICATEDQUERY\_CRYPTOSESSION</span></span>

<span data-ttu-id="981e4-104">Возвращает дескрипторы криптографического сеанса и устройства Direct3D, связанные с указанным устройством декодера DirectX Video Acceleration 2 (ДКСВА-2).</span><span class="sxs-lookup"><span data-stu-id="981e4-104">Returns handles to the cryptographic session and Direct3D device that are associated with a specified DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>



| <span data-ttu-id="981e4-105">Требование</span><span class="sxs-lookup"><span data-stu-id="981e4-105">Requirement</span></span> | <span data-ttu-id="981e4-106">Значение</span><span class="sxs-lookup"><span data-stu-id="981e4-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="981e4-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="981e4-107">Query GUID</span></span>  | <span data-ttu-id="981e4-108">**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="981e4-108">**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**</span></span>                                                                         |
| <span data-ttu-id="981e4-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="981e4-109">Input data</span></span>  | [<span data-ttu-id="981e4-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="981e4-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                             |
| <span data-ttu-id="981e4-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="981e4-111">Return data</span></span> | [<span data-ttu-id="981e4-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерикриптосессион**</span><span class="sxs-lookup"><span data-stu-id="981e4-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT**</span></span>](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="981e4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="981e4-113">Remarks</span></span>

<span data-ttu-id="981e4-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="981e4-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="981e4-115">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="981e4-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="981e4-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="981e4-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="981e4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="981e4-117">Requirements</span></span>



| <span data-ttu-id="981e4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="981e4-118">Requirement</span></span> | <span data-ttu-id="981e4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="981e4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="981e4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="981e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="981e4-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="981e4-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="981e4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="981e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="981e4-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="981e4-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="981e4-124">Header</span><span class="sxs-lookup"><span data-stu-id="981e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="981e4-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="981e4-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="981e4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="981e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981e4-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="981e4-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="981e4-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="981e4-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="981e4-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="981e4-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




