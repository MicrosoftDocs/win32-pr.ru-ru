---
title: TS_ATTRID (Текстстор. h)
description: '\_Тип данных TS ATTRID используется для задания текстового атрибута.'
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800988"
---
# <a name="ts_attrid"></a><span data-ttu-id="a3d55-104">\_ATTRID TS</span><span class="sxs-lookup"><span data-stu-id="a3d55-104">TS\_ATTRID</span></span>

<span data-ttu-id="a3d55-105">Тип данных **TS \_ ATTRID** используется для задания текстового атрибута.</span><span class="sxs-lookup"><span data-stu-id="a3d55-105">The **TS\_ATTRID** data type is used to identify a text attribute.</span></span>


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a><span data-ttu-id="a3d55-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3d55-106">Remarks</span></span>

<span data-ttu-id="a3d55-107">Список стандартных идентификаторов GUID для TS \_ ATTRID находится в тсаттрс. h.</span><span class="sxs-lookup"><span data-stu-id="a3d55-107">A list of predefined GUIDs for TS\_ATTRID is in tsattrs.h.</span></span>

<span data-ttu-id="a3d55-108">Идентификаторы GUID ТСАТТРИД \_ Text \_ ВЕРТИКАЛВРИТИНГ и тсаттрид \_ \_ полезны для того, чтобы приложения соответствовали вводимому тексту, который должен быть исправлен.</span><span class="sxs-lookup"><span data-stu-id="a3d55-108">The GUIDs TSATTRID\_Text\_VerticalWriting and TSATTRID\_Text\_Orientation are useful for applications to match input text that is to be corrected.</span></span> <span data-ttu-id="a3d55-109">Можно создать дополнительные идентификаторы GUID, определяемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="a3d55-109">Additional user-defined GUIDs can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d55-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a3d55-110">Requirements</span></span>



| <span data-ttu-id="a3d55-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a3d55-111">Requirement</span></span> | <span data-ttu-id="a3d55-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a3d55-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d55-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3d55-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a3d55-114">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="a3d55-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3d55-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a3d55-116">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="a3d55-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a3d55-117">Redistributable</span></span><br/>          | <span data-ttu-id="a3d55-118">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="a3d55-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="a3d55-119">Header</span><span class="sxs-lookup"><span data-stu-id="a3d55-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3d55-120"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3d55-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3d55-121">IDL</span><span class="sxs-lookup"><span data-stu-id="a3d55-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3d55-122"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3d55-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d55-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3d55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d55-124">**ITextStoreACP:: Финднекстаттртранситион**</span><span class="sxs-lookup"><span data-stu-id="a3d55-124">**ITextStoreACP::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="a3d55-125">**ITextStoreACP:: Рекуестаттрсатпоситион**</span><span class="sxs-lookup"><span data-stu-id="a3d55-125">**ITextStoreACP::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="a3d55-126">**ITextStoreACP:: Рекуестаттрстранситионингатпоситион**</span><span class="sxs-lookup"><span data-stu-id="a3d55-126">**ITextStoreACP::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="a3d55-127">**ITextStoreACP:: Рекуестсуппортедаттрс**</span><span class="sxs-lookup"><span data-stu-id="a3d55-127">**ITextStoreACP::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="a3d55-128">**ITextStoreACPSink:: Онаттрсчанже**</span><span class="sxs-lookup"><span data-stu-id="a3d55-128">**ITextStoreACPSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="a3d55-129">**Итекстстореанчор:: Финднекстаттртранситион**</span><span class="sxs-lookup"><span data-stu-id="a3d55-129">**ITextStoreAnchor::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="a3d55-130">**Итекстстореанчор:: Рекуестаттрсатпоситион**</span><span class="sxs-lookup"><span data-stu-id="a3d55-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="a3d55-131">**Итекстстореанчор:: Рекуестаттрстранситионингатпоситион**</span><span class="sxs-lookup"><span data-stu-id="a3d55-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="a3d55-132">**Итекстстореанчор:: Рекуестсуппортедаттрс**</span><span class="sxs-lookup"><span data-stu-id="a3d55-132">**ITextStoreAnchor::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="a3d55-133">**Итекстстореанчорсинк:: Онаттрсчанже**</span><span class="sxs-lookup"><span data-stu-id="a3d55-133">**ITextStoreAnchorSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="a3d55-134">**\_АТТРВАЛ TS**</span><span class="sxs-lookup"><span data-stu-id="a3d55-134">**TS\_ATTRVAL**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





