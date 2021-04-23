---
description: Возвращает число типов шифрования, которые можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808123"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a><span data-ttu-id="2eced-103">D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуидкаунт</span><span class="sxs-lookup"><span data-stu-id="2eced-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span></span>

<span data-ttu-id="2eced-104">Возвращает число типов шифрования, которые можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.</span><span class="sxs-lookup"><span data-stu-id="2eced-104">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="2eced-105">Требование</span><span class="sxs-lookup"><span data-stu-id="2eced-105">Requirement</span></span> | <span data-ttu-id="2eced-106">Значение</span><span class="sxs-lookup"><span data-stu-id="2eced-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eced-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="2eced-107">Query GUID</span></span>  | <span data-ttu-id="2eced-108">**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуидкаунт**</span><span class="sxs-lookup"><span data-stu-id="2eced-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>                                                                                 |
| <span data-ttu-id="2eced-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2eced-109">Input data</span></span>  | [<span data-ttu-id="2eced-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="2eced-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="2eced-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="2eced-111">Return data</span></span> | [<span data-ttu-id="2eced-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуидкаунт**</span><span class="sxs-lookup"><span data-stu-id="2eced-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="2eced-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2eced-113">Remarks</span></span>

<span data-ttu-id="2eced-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="2eced-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="2eced-115">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="2eced-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="2eced-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="2eced-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="2eced-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2eced-117">Requirements</span></span>



| <span data-ttu-id="2eced-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2eced-118">Requirement</span></span> | <span data-ttu-id="2eced-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2eced-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eced-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2eced-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2eced-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2eced-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2eced-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2eced-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2eced-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2eced-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2eced-124">Header</span><span class="sxs-lookup"><span data-stu-id="2eced-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eced-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eced-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eced-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2eced-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eced-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="2eced-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="2eced-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="2eced-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="2eced-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="2eced-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




