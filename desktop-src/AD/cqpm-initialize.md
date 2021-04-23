---
title: Сообщение CQPM_INITIALIZE (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок на странице расширения формы запроса при добавлении страницы в форму.
ms.assetid: 29cb39d5-9bc4-472e-8a2f-dc6cd505144a
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_INITIALIZE Active Directory
topic_type:
- apiref
api_name:
- CQPM_INITIALIZE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e95c7087a9cd2d40387c8d7dd07aa93c8f697fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071568"
---
# <a name="cqpm_initialize-message"></a><span data-ttu-id="a1b79-104">\_Сообщение инициализации ККПМ</span><span class="sxs-lookup"><span data-stu-id="a1b79-104">CQPM\_INITIALIZE message</span></span>

<span data-ttu-id="a1b79-105">Сообщение **\_ инициализации ККПМ** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса при добавлении страницы в форму.</span><span class="sxs-lookup"><span data-stu-id="a1b79-105">The **CQPM\_INITIALIZE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is added to a form.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1b79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1b79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b79-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1b79-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b79-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="a1b79-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1b79-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1b79-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b79-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="a1b79-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b79-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1b79-111">Return value</span></span>

<span data-ttu-id="a1b79-112">Возвращаемое значение для этого сообщения игнорируется.</span><span class="sxs-lookup"><span data-stu-id="a1b79-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b79-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a1b79-113">Requirements</span></span>



| <span data-ttu-id="a1b79-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a1b79-114">Requirement</span></span> | <span data-ttu-id="a1b79-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a1b79-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b79-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1b79-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b79-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1b79-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="a1b79-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1b79-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b79-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1b79-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="a1b79-120">Header</span><span class="sxs-lookup"><span data-stu-id="a1b79-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b79-121"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b79-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b79-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1b79-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b79-123">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="a1b79-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





