---
description: Возвращает тип шифрования, который применяется до того, как содержимое становится доступным для ЦП или шины.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262800"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a><span data-ttu-id="4e4e6-103">D3DAUTHENTICATEDQUERY \_ куррентенкриптионвхенакцессибле</span><span class="sxs-lookup"><span data-stu-id="4e4e6-103">D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="4e4e6-104">Возвращает тип шифрования, который применяется до того, как содержимое становится доступным для ЦП или шины.</span><span class="sxs-lookup"><span data-stu-id="4e4e6-104">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="4e4e6-105">Требование</span><span class="sxs-lookup"><span data-stu-id="4e4e6-105">Requirement</span></span> | <span data-ttu-id="4e4e6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="4e4e6-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4e6-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="4e4e6-107">Query GUID</span></span>  | <span data-ttu-id="4e4e6-108">**D3DAUTHENTICATEDQUERY \_ куррентенкриптионвхенакцессибле**</span><span class="sxs-lookup"><span data-stu-id="4e4e6-108">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>                                                                                   |
| <span data-ttu-id="4e4e6-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4e4e6-109">Input data</span></span>  | [<span data-ttu-id="4e4e6-110">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="4e4e6-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="4e4e6-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="4e4e6-111">Return data</span></span> | [<span data-ttu-id="4e4e6-112">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерюнкомпресседенкриптионлевел**</span><span class="sxs-lookup"><span data-stu-id="4e4e6-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="4e4e6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e4e6-113">Remarks</span></span>

<span data-ttu-id="4e4e6-114">Этот запрос поддерживают следующие типы каналов:</span><span class="sxs-lookup"><span data-stu-id="4e4e6-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="4e4e6-115">**\_Оборудование драйвера \_ D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="4e4e6-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="4e4e6-116">**\_ \_ Программное обеспечение драйвера D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="4e4e6-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="4e4e6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4e4e6-117">Requirements</span></span>



| <span data-ttu-id="4e4e6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4e4e6-118">Requirement</span></span> | <span data-ttu-id="4e4e6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4e4e6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4e6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e4e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e4e6-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e4e6-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4e4e6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e4e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e4e6-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e4e6-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4e4e6-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e4e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e4e6-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e4e6-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e4e6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e4e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e4e6-127">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="4e4e6-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="4e4e6-128">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="4e4e6-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="4e4e6-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="4e4e6-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




