---
title: Константы TS_LF_ (Текстстор. h)
description: '\_ \_ Константы TS LF \ определяют тип блокировки документа.'
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681750"
---
# <a name="ts_lf_-constants"></a><span data-ttu-id="089b5-103">\_ \_ \* Константы TS LF</span><span class="sxs-lookup"><span data-stu-id="089b5-103">TS\_LF\_\* Constants</span></span>

<span data-ttu-id="089b5-104">\_ \_ \* Константы перевода TS указывают тип блокировки документа.</span><span class="sxs-lookup"><span data-stu-id="089b5-104">The TS\_LF\_\* constants specify the type of document lock.</span></span>



| <span data-ttu-id="089b5-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="089b5-105">Constant/value</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="089b5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="089b5-106">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <span data-ttu-id="089b5-107"><dt>**TS \_ \_Синхронизация LF**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="089b5-107"><dt>**TS\_LF\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                | <span data-ttu-id="089b5-108">Документ имеет синхронную блокировку, если этот флаг сочетается с другими флагами.</span><span class="sxs-lookup"><span data-stu-id="089b5-108">The document has a synchronous-lock if this flag is combined with other flags.</span></span><br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <span data-ttu-id="089b5-109"><dt>**TS \_ \_Чтение LF**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="089b5-109"><dt>**TS\_LF\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                | <span data-ttu-id="089b5-110">Документ имеет блокировку только для чтения и не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="089b5-110">The document has a read-only lock and cannot be modified.</span></span><br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <span data-ttu-id="089b5-111"><dt>**TS \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="089b5-111"><dt>**TS\_LF\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl> | <span data-ttu-id="089b5-112">Документ имеет блокировку чтения и записи и может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="089b5-112">The document has a read/write lock and can be modified.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="089b5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="089b5-113">Requirements</span></span>



| <span data-ttu-id="089b5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="089b5-114">Requirement</span></span> | <span data-ttu-id="089b5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="089b5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="089b5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="089b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="089b5-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="089b5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="089b5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="089b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="089b5-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="089b5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="089b5-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="089b5-120">Redistributable</span></span><br/>          | <span data-ttu-id="089b5-121">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="089b5-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="089b5-122">Header</span><span class="sxs-lookup"><span data-stu-id="089b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="089b5-123"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="089b5-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="089b5-124">IDL</span><span class="sxs-lookup"><span data-stu-id="089b5-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="089b5-125"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="089b5-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089b5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="089b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089b5-127">Блокировки документов</span><span class="sxs-lookup"><span data-stu-id="089b5-127">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="089b5-128">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="089b5-128">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="089b5-129">ITextStoreACPSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="089b5-129">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="089b5-130">Итекстстореанчор:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="089b5-130">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="089b5-131">Итекстстореанчорсинк:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="089b5-131">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





