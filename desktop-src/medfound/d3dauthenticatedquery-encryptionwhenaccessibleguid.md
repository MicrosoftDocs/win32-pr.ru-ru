---
description: Возвращает один из типов шифрования, который можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692052"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a><span data-ttu-id="3920f-103">D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид</span><span class="sxs-lookup"><span data-stu-id="3920f-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID</span></span>

<span data-ttu-id="3920f-104">Возвращает один из типов шифрования, который можно использовать для шифрования содержимого до того, как оно станет доступным для ЦП или шины.</span><span class="sxs-lookup"><span data-stu-id="3920f-104">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="3920f-105">Требование</span><span class="sxs-lookup"><span data-stu-id="3920f-105">Requirement</span></span> | <span data-ttu-id="3920f-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3920f-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3920f-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="3920f-107">Query GUID</span></span>  | <span data-ttu-id="3920f-108">**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**</span><span class="sxs-lookup"><span data-stu-id="3920f-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>                                                                            |
| <span data-ttu-id="3920f-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3920f-109">Input data</span></span>  | [<span data-ttu-id="3920f-110">**\_ \_ Входные данные куеревиктионенкриптионгуид D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="3920f-110">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| <span data-ttu-id="3920f-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="3920f-111">Return data</span></span> | [<span data-ttu-id="3920f-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуид**</span><span class="sxs-lookup"><span data-stu-id="3920f-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="3920f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3920f-113">Remarks</span></span>

<span data-ttu-id="3920f-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="3920f-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="3920f-115">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="3920f-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="3920f-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="3920f-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="3920f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3920f-117">Requirements</span></span>



| <span data-ttu-id="3920f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3920f-118">Requirement</span></span> | <span data-ttu-id="3920f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3920f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3920f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3920f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3920f-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3920f-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3920f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3920f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3920f-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3920f-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3920f-124">Header</span><span class="sxs-lookup"><span data-stu-id="3920f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3920f-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3920f-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3920f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3920f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3920f-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="3920f-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="3920f-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="3920f-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="3920f-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="3920f-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




