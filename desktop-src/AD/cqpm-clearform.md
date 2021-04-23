---
title: Сообщение CQPM_CLEARFORM (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок запроса на страницу расширения, когда необходимо сбросить содержимое страницы до значений по умолчанию.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_CLEARFORM Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988274"
---
# <a name="cqpm_clearform-message"></a><span data-ttu-id="99d65-104">\_Сообщение ККПМ клеарформ</span><span class="sxs-lookup"><span data-stu-id="99d65-104">CQPM\_CLEARFORM message</span></span>

<span data-ttu-id="99d65-105">Сообщение **ККПМ \_ клеарформ** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) запроса на страницу расширения, когда необходимо сбросить содержимое страницы до значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="99d65-105">The **CQPM\_CLEARFORM** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query for extension page when the contents of the page should be reset to the default values.</span></span>

## <a name="parameters"></a><span data-ttu-id="99d65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99d65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99d65-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99d65-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99d65-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="99d65-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="99d65-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99d65-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99d65-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="99d65-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99d65-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99d65-111">Return value</span></span>

<span data-ttu-id="99d65-112">Возвращает **значение \_ ОК** , если успешно, или стандартный код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="99d65-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="99d65-113">Требования</span><span class="sxs-lookup"><span data-stu-id="99d65-113">Requirements</span></span>



| <span data-ttu-id="99d65-114">Требование</span><span class="sxs-lookup"><span data-stu-id="99d65-114">Requirement</span></span> | <span data-ttu-id="99d65-115">Значение</span><span class="sxs-lookup"><span data-stu-id="99d65-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99d65-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99d65-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99d65-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99d65-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="99d65-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99d65-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99d65-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99d65-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="99d65-120">Header</span><span class="sxs-lookup"><span data-stu-id="99d65-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99d65-121"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="99d65-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99d65-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99d65-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d65-123">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="99d65-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





