---
description: Возвращает тип шины ввода-вывода, используемой для отправки данных в GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423550"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a><span data-ttu-id="9e30d-103">D3DAUTHENTICATEDQUERY \_ акцессибилитяттрибутес</span><span class="sxs-lookup"><span data-stu-id="9e30d-103">D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES</span></span>

<span data-ttu-id="9e30d-104">Возвращает тип шины ввода-вывода, используемой для отправки данных в GPU.</span><span class="sxs-lookup"><span data-stu-id="9e30d-104">Returns the type of I/O bus used to send data to the GPU.</span></span>



| <span data-ttu-id="9e30d-105">Требование</span><span class="sxs-lookup"><span data-stu-id="9e30d-105">Requirement</span></span> | <span data-ttu-id="9e30d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="9e30d-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e30d-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="9e30d-107">Query GUID</span></span>  | <span data-ttu-id="9e30d-108">**D3DAUTHENTICATEDQUERY \_ акцессибилитяттрибутес**</span><span class="sxs-lookup"><span data-stu-id="9e30d-108">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>                                                           |
| <span data-ttu-id="9e30d-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9e30d-109">Input data</span></span>  | [<span data-ttu-id="9e30d-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9e30d-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="9e30d-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="9e30d-111">Return data</span></span> | [<span data-ttu-id="9e30d-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеринфобустипе**</span><span class="sxs-lookup"><span data-stu-id="9e30d-112">**D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="9e30d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e30d-113">Remarks</span></span>

<span data-ttu-id="9e30d-114">Этот запрос также возвращает сведения о доступности содержимого при помещении в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="9e30d-114">This query also returns information about how accessible the content is when put into video memory.</span></span>

<span data-ttu-id="9e30d-115">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="9e30d-115">The following channel types support this query:</span></span>

-   <span data-ttu-id="9e30d-116">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9e30d-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="9e30d-117">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="9e30d-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="9e30d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9e30d-118">Requirements</span></span>



| <span data-ttu-id="9e30d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9e30d-119">Requirement</span></span> | <span data-ttu-id="9e30d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9e30d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e30d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e30d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e30d-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9e30d-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9e30d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e30d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e30d-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e30d-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9e30d-125">Header</span><span class="sxs-lookup"><span data-stu-id="9e30d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e30d-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e30d-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e30d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e30d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e30d-128">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="9e30d-128">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="9e30d-129">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="9e30d-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="9e30d-130">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9e30d-130">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




