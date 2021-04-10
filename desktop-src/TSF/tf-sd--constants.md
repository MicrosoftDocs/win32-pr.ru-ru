---
title: Константы TF_SD_ (Мсктф. h)
description: '\_ \_ Константы TF SD \ описывают состояние документа.'
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135247"
---
# <a name="tf_sd_-constants"></a><span data-ttu-id="d6aea-103">\_ \_ \* Константы TF SD</span><span class="sxs-lookup"><span data-stu-id="d6aea-103">TF\_SD\_\* Constants</span></span>

<span data-ttu-id="d6aea-104">\_ \_ \* Константы TF SD описывают состояние документа.</span><span class="sxs-lookup"><span data-stu-id="d6aea-104">The TF\_SD\_\* constants describe the document status.</span></span>



| <span data-ttu-id="d6aea-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="d6aea-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="d6aea-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d6aea-106">Description</span></span>                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <span data-ttu-id="d6aea-107"><dt>**Tf \_ \_только SD ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt></span><span class="sxs-lookup"><span data-stu-id="d6aea-107"><dt>**TF\_SD\_READONLY**</dt> <dt>( TS\_SD\_READONLY )</dt></span></span> </dl> | <span data-ttu-id="d6aea-108">Документ доступен только для чтения и не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="d6aea-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <span data-ttu-id="d6aea-109"><dt>**Tf \_ \_Загрузка SD**</dt> <dt>( \_ Загрузка SD служб терминалов \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="d6aea-109"><dt>**TF\_SD\_LOADING**</dt> <dt>( TS\_SD\_LOADING )</dt></span></span> </dl>     | <span data-ttu-id="d6aea-110">Документ загружается и может быть неполным.</span><span class="sxs-lookup"><span data-stu-id="d6aea-110">The document is loading and can be incomplete.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="d6aea-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6aea-111">Remarks</span></span>

<span data-ttu-id="d6aea-112">Элемент **двдинамикфлагс** структуры [ \_ состояния TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) использует эти константы.</span><span class="sxs-lookup"><span data-stu-id="d6aea-112">The **dwDynamicFlags** member of the [TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6aea-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d6aea-113">Requirements</span></span>



| <span data-ttu-id="d6aea-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d6aea-114">Requirement</span></span> | <span data-ttu-id="d6aea-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d6aea-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6aea-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6aea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d6aea-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d6aea-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d6aea-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6aea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d6aea-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d6aea-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d6aea-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d6aea-120">Redistributable</span></span><br/>          | <span data-ttu-id="d6aea-121">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="d6aea-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="d6aea-122">Header</span><span class="sxs-lookup"><span data-stu-id="d6aea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6aea-123"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6aea-123"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6aea-124">IDL</span><span class="sxs-lookup"><span data-stu-id="d6aea-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6aea-125"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6aea-125"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6aea-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6aea-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6aea-127">[TF \_ status](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6aea-127">[TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d6aea-128">\_Константы SD служб терминалов \_ \*</span><span class="sxs-lookup"><span data-stu-id="d6aea-128">TS\_SD\_\* Constants</span></span>](ts-sd--constants.md)
</dt> <dt>

[<span data-ttu-id="d6aea-129">Итфконтекстовнер::/Status</span><span class="sxs-lookup"><span data-stu-id="d6aea-129">ITfContextOwner::GetStatus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[<span data-ttu-id="d6aea-130">Итфконтекстовнерсервицес:: Онстатусчанже</span><span class="sxs-lookup"><span data-stu-id="d6aea-130">ITfContextOwnerServices::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[<span data-ttu-id="d6aea-131">ITextStoreACP::/Status</span><span class="sxs-lookup"><span data-stu-id="d6aea-131">ITextStoreACP::GetStatus</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[<span data-ttu-id="d6aea-132">Итфстатуссунк:: Онстатусчанже</span><span class="sxs-lookup"><span data-stu-id="d6aea-132">ITfStatusSunk::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

