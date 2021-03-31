---
title: Сообщение CQPM_SETDEFAULTPARAMETERS (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок на странице расширения формы запроса, чтобы задать альтернативные параметры по умолчанию для страницы.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_SETDEFAULTPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490383"
---
# <a name="cqpm_setdefaultparameters-message"></a><span data-ttu-id="c4d7a-104">\_Сообщение ККПМ сетдефаултпараметерс</span><span class="sxs-lookup"><span data-stu-id="c4d7a-104">CQPM\_SETDEFAULTPARAMETERS message</span></span>

<span data-ttu-id="c4d7a-105">Сообщение **ККПМ \_ сетдефаултпараметерс** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса, чтобы задать альтернативные параметры по умолчанию для страницы.</span><span class="sxs-lookup"><span data-stu-id="c4d7a-105">The **CQPM\_SETDEFAULTPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to set alternate default parameters for the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4d7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4d7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4d7a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4d7a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4d7a-108">Содержит ненулевое значение, если страница является страницей по умолчанию или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c4d7a-108">Contains nonzero if the page is the default page or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="c4d7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4d7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4d7a-110">Указатель на структуру [**опенкуеривиндов**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) , содержащую данные о диалоговом окне "запрос службы каталогов".</span><span class="sxs-lookup"><span data-stu-id="c4d7a-110">Pointer to an [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) structure that contains data about the directory service query dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4d7a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4d7a-111">Return value</span></span>

<span data-ttu-id="c4d7a-112">Возвращаемое значение для этого сообщения игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c4d7a-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d7a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c4d7a-113">Requirements</span></span>



| <span data-ttu-id="c4d7a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c4d7a-114">Requirement</span></span> | <span data-ttu-id="c4d7a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c4d7a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d7a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4d7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d7a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4d7a-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="c4d7a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4d7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d7a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4d7a-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="c4d7a-120">Header</span><span class="sxs-lookup"><span data-stu-id="c4d7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4d7a-121"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4d7a-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d7a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4d7a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d7a-123">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="c4d7a-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="c4d7a-124">**опенкуеривиндов**</span><span class="sxs-lookup"><span data-stu-id="c4d7a-124">**OPENQUERYWINDOW**</span></span>](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





