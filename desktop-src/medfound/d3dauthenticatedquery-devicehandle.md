---
description: Возвращает маркер устройства, связанного с этим каналом с проверкой подлинности.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692053"
---
# <a name="d3dauthenticatedquery_devicehandle"></a><span data-ttu-id="b657c-103">D3DAUTHENTICATEDQUERY \_ девицехандле</span><span class="sxs-lookup"><span data-stu-id="b657c-103">D3DAUTHENTICATEDQUERY\_DEVICEHANDLE</span></span>

<span data-ttu-id="b657c-104">Возвращает маркер устройства, связанного с этим каналом с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="b657c-104">Returns a handle to the device that is associated with this authenticated channel.</span></span> <span data-ttu-id="b657c-105">Этот обработчик можно использовать, чтобы проверить, взаимодействуют ли два прошедших проверку подлинности канала с одним и тем же устройством.</span><span class="sxs-lookup"><span data-stu-id="b657c-105">You can use this handle to verify whether two authenticated channels are communicating with the same device.</span></span>



| <span data-ttu-id="b657c-106">Требование</span><span class="sxs-lookup"><span data-stu-id="b657c-106">Requirement</span></span> | <span data-ttu-id="b657c-107">Значение</span><span class="sxs-lookup"><span data-stu-id="b657c-107">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b657c-108">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="b657c-108">Query GUID</span></span>  | <span data-ttu-id="b657c-109">**D3DAUTHENTICATEDQUERY \_ девицехандле**</span><span class="sxs-lookup"><span data-stu-id="b657c-109">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>                                                                        |
| <span data-ttu-id="b657c-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b657c-110">Input data</span></span>  | [<span data-ttu-id="b657c-111">**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**</span><span class="sxs-lookup"><span data-stu-id="b657c-111">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                           |
| <span data-ttu-id="b657c-112">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="b657c-112">Return data</span></span> | [<span data-ttu-id="b657c-113">**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеридевицехандле**</span><span class="sxs-lookup"><span data-stu-id="b657c-113">**D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="b657c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b657c-114">Remarks</span></span>

<span data-ttu-id="b657c-115">Этот запрос действителен для всех типов каналов.</span><span class="sxs-lookup"><span data-stu-id="b657c-115">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="b657c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b657c-116">Requirements</span></span>



| <span data-ttu-id="b657c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b657c-117">Requirement</span></span> | <span data-ttu-id="b657c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b657c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b657c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b657c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b657c-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b657c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b657c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b657c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b657c-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b657c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b657c-123">Header</span><span class="sxs-lookup"><span data-stu-id="b657c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b657c-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b657c-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b657c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b657c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b657c-126">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="b657c-126">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="b657c-127">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="b657c-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="b657c-128">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="b657c-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




