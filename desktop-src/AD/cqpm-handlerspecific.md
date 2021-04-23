---
title: Сообщение CQPM_HANDLERSPECIFIC (Кмнкуери. h)
description: Базовое значение, используемое для сообщений, являющихся частными для обработчика запросов.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_HANDLERSPECIFIC Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489477"
---
# <a name="cqpm_handlerspecific-message"></a><span data-ttu-id="6533d-104">\_Сообщение ККПМ хандлерспеЦифик</span><span class="sxs-lookup"><span data-stu-id="6533d-104">CQPM\_HANDLERSPECIFIC message</span></span>

<span data-ttu-id="6533d-105">Сообщение **ККПМ \_ хандлерспеЦифик** — это базовое значение, используемое для сообщений, которые являются частными для обработчика запросов.</span><span class="sxs-lookup"><span data-stu-id="6533d-105">The **CQPM\_HANDLERSPECIFIC** message is the base value used for messages that are private to the query handler.</span></span> <span data-ttu-id="6533d-106">Обработчик запросов должен добавить это значение в частные сообщения, чтобы избежать конфликтов сообщений.</span><span class="sxs-lookup"><span data-stu-id="6533d-106">The query handler should add this value to private messages to ensure that message collisions do not occur.</span></span>

## <a name="parameters"></a><span data-ttu-id="6533d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6533d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6533d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6533d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6533d-109">Содержит дополнительные данные сообщения.</span><span class="sxs-lookup"><span data-stu-id="6533d-109">Contains additional message data.</span></span> <span data-ttu-id="6533d-110">Содержимое этого параметра определяется обработчиком запросов.</span><span class="sxs-lookup"><span data-stu-id="6533d-110">The content of this parameter is defined by the query handler.</span></span>

</dd> <dt>

<span data-ttu-id="6533d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6533d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6533d-112">Содержит дополнительные данные сообщения.</span><span class="sxs-lookup"><span data-stu-id="6533d-112">Contains additional message data.</span></span> <span data-ttu-id="6533d-113">Содержимое этого параметра определяется обработчиком запросов.</span><span class="sxs-lookup"><span data-stu-id="6533d-113">The content of this parameter is defined by the query handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6533d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6533d-114">Return value</span></span>

<span data-ttu-id="6533d-115">Значение возвращаемого значения определяется обработчиком запроса.</span><span class="sxs-lookup"><span data-stu-id="6533d-115">The meaning of the return value is defined by the query handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="6533d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6533d-116">Requirements</span></span>



| <span data-ttu-id="6533d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6533d-117">Requirement</span></span> | <span data-ttu-id="6533d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6533d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6533d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6533d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6533d-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6533d-120">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="6533d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6533d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6533d-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6533d-122">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="6533d-123">Header</span><span class="sxs-lookup"><span data-stu-id="6533d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6533d-124"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="6533d-124"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6533d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6533d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6533d-126">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="6533d-126">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





