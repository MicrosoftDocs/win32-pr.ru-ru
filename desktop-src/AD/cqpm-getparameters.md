---
title: Сообщение CQPM_GETPARAMETERS (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок на странице расширения формы запроса для получения данных о запросе, выполняемом страницей.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_GETPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891565"
---
# <a name="cqpm_getparameters-message"></a><span data-ttu-id="f551e-104">\_Сообщение ККПМ Parameters</span><span class="sxs-lookup"><span data-stu-id="f551e-104">CQPM\_GETPARAMETERS message</span></span>

<span data-ttu-id="f551e-105">Сообщение **ККПМ \_ Parameters** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса для получения данных о запросе, выполняемом страницей.</span><span class="sxs-lookup"><span data-stu-id="f551e-105">The **CQPM\_GETPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to retrieve data about the query performed by the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="f551e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f551e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f551e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f551e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f551e-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f551e-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f551e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f551e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f551e-110">Указатель на значение [**лпдскуерипарамс**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) , которое получает данные о запросе, выполняемом страницей.</span><span class="sxs-lookup"><span data-stu-id="f551e-110">Pointer to a [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) value that receives data about the query performed by the page.</span></span> <span data-ttu-id="f551e-111">Если этот параметр имеет **значение NULL**, то расширение структуры **дскуерипарамс** должно быть выделено расширением с помощью функции [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .</span><span class="sxs-lookup"><span data-stu-id="f551e-111">If this parameter is **NULL**, the **DSQUERYPARAMS** structure must be allocated by the extension using the [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f551e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f551e-112">Return value</span></span>

<span data-ttu-id="f551e-113">Возвращает **значение \_ ОК** , если успешно, или стандартный код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f551e-113">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f551e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f551e-114">Requirements</span></span>



| <span data-ttu-id="f551e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f551e-115">Requirement</span></span> | <span data-ttu-id="f551e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f551e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f551e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f551e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f551e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f551e-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="f551e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f551e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f551e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f551e-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="f551e-121">Header</span><span class="sxs-lookup"><span data-stu-id="f551e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f551e-122"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="f551e-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f551e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f551e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f551e-124">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="f551e-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="f551e-125">**дскуерипарамс**</span><span class="sxs-lookup"><span data-stu-id="f551e-125">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[<span data-ttu-id="f551e-126">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="f551e-126">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

