---
title: Константы TS_SD_ (Текстстор. h)
description: '\_Константы служб терминалов SD \_ \ описывают динамические состояния документов, используемые приложением во время выполнения.'
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681854"
---
# <a name="ts_sd_-constants"></a><span data-ttu-id="4e67d-103">\_Константы SD служб терминалов \_ \*</span><span class="sxs-lookup"><span data-stu-id="4e67d-103">TS\_SD\_\* Constants</span></span>

<span data-ttu-id="4e67d-104">Константы SD в службах терминалов \_ \_ \* описывают динамические состояния документов, используемые приложением во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e67d-104">The TS\_SD\_\* constants describe dynamic document states used by an application at runtime.</span></span>



| <span data-ttu-id="4e67d-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="4e67d-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="4e67d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4e67d-106">Description</span></span>                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <span data-ttu-id="4e67d-107"><dt>**TS \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4e67d-107"><dt>**TS\_SD\_READONLY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="4e67d-108">Документ доступен только для чтения и не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="4e67d-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <span data-ttu-id="4e67d-109"><dt>**TS \_ \_Загрузка SD**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="4e67d-109"><dt>**TS\_SD\_LOADING**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                 | <span data-ttu-id="4e67d-110">Документ загружается и может быть неполным.</span><span class="sxs-lookup"><span data-stu-id="4e67d-110">The document is loading and might be incomplete.</span></span><br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <span data-ttu-id="4e67d-111"><dt>**TS \_ SD \_ Маскалл**</dt> <dt>(TS \_ SD \_ только \| для \_ загрузки SD TS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="4e67d-111"><dt>**TS\_SD\_MASKALL**</dt> <dt>( TS\_SD\_READONLY \| TS\_SD\_LOADING )</dt></span></span> </dl> | <span data-ttu-id="4e67d-112">Документ доступен только для чтения и загружается.</span><span class="sxs-lookup"><span data-stu-id="4e67d-112">The document is both read-only and loading.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="4e67d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e67d-113">Remarks</span></span>

<span data-ttu-id="4e67d-114">Элемент **двдинамикфлагс** структуры [ \_ состояния служб терминалов](/windows/desktop/api/Textstor/ns-textstor-ts_status) использует эти константы.</span><span class="sxs-lookup"><span data-stu-id="4e67d-114">The **dwDynamicFlags** member of the [TS\_STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e67d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4e67d-115">Requirements</span></span>



| <span data-ttu-id="4e67d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4e67d-116">Requirement</span></span> | <span data-ttu-id="4e67d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4e67d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e67d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e67d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4e67d-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e67d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4e67d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e67d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4e67d-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e67d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e67d-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4e67d-122">Redistributable</span></span><br/>          | <span data-ttu-id="4e67d-123">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="4e67d-123">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="4e67d-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e67d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e67d-125"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e67d-125"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e67d-126">IDL</span><span class="sxs-lookup"><span data-stu-id="4e67d-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e67d-127"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e67d-127"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e67d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e67d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e67d-129">\_состояние TS</span><span class="sxs-lookup"><span data-stu-id="4e67d-129">TS\_STATUS</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[<span data-ttu-id="4e67d-130">\_ \_ \* Константы TF SD</span><span class="sxs-lookup"><span data-stu-id="4e67d-130">TF\_SD\_\* Constants</span></span>](tf-sd--constants.md)
</dt> </dl>

 

 





