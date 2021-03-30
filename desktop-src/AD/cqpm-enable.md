---
title: Сообщение CQPM_ENABLE (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок на странице расширения формы запроса для включения или отключения страницы.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071263"
---
# <a name="cqpm_enable-message"></a><span data-ttu-id="de1bb-104">\_Сообщение о включении ККПМ</span><span class="sxs-lookup"><span data-stu-id="de1bb-104">CQPM\_ENABLE message</span></span>

<span data-ttu-id="de1bb-105">Сообщение **ККПМ \_ Enable** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса для включения или отключения страницы.</span><span class="sxs-lookup"><span data-stu-id="de1bb-105">The **CQPM\_ENABLE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to enable or disable the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="de1bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de1bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1bb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de1bb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de1bb-108">Содержит нуль для отключения страницы или ненулевого значения для включения страницы.</span><span class="sxs-lookup"><span data-stu-id="de1bb-108">Contains zero to disable the page or nonzero to enable the page.</span></span>

</dd> <dt>

<span data-ttu-id="de1bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de1bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de1bb-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="de1bb-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de1bb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de1bb-111">Return value</span></span>

<span data-ttu-id="de1bb-112">Возвращаемое значение для этого сообщения игнорируется.</span><span class="sxs-lookup"><span data-stu-id="de1bb-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="de1bb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="de1bb-113">Requirements</span></span>



| <span data-ttu-id="de1bb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="de1bb-114">Requirement</span></span> | <span data-ttu-id="de1bb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="de1bb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de1bb-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de1bb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de1bb-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de1bb-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="de1bb-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de1bb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de1bb-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de1bb-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="de1bb-120">Header</span><span class="sxs-lookup"><span data-stu-id="de1bb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de1bb-121"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="de1bb-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de1bb-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de1bb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1bb-123">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="de1bb-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





