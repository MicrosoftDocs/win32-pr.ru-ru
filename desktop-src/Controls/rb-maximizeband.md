---
title: Сообщение RB_MAXIMIZEBAND (Коммктрл. h)
description: Изменяет размер полосы в элементе управления главной панели до его идеального или самого крупного размера.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- Элементы управления Windows для RB_MAXIMIZEBAND сообщений
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892277"
---
# <a name="rb_maximizeband-message"></a><span data-ttu-id="fbcef-104">\_Сообщение МАКСИМИЗЕБАНД RB</span><span class="sxs-lookup"><span data-stu-id="fbcef-104">RB\_MAXIMIZEBAND message</span></span>

<span data-ttu-id="fbcef-105">Изменяет размер полосы в элементе управления главной панели до его идеального или самого крупного размера.</span><span class="sxs-lookup"><span data-stu-id="fbcef-105">Resizes a band in a rebar control to either its ideal or largest size.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbcef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbcef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbcef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbcef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbcef-108">Отсчитываемый от нуля индекс диапазона, который необходимо развернуть.</span><span class="sxs-lookup"><span data-stu-id="fbcef-108">Zero-based index of the band to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="fbcef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbcef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbcef-110">Указывает, следует ли использовать идеальную ширину полосы, если полоса развернута.</span><span class="sxs-lookup"><span data-stu-id="fbcef-110">Indicates if the ideal width of the band should be used when the band is maximized.</span></span> <span data-ttu-id="fbcef-111">Если это значение не равно нулю, будет использоваться идеальная ширина.</span><span class="sxs-lookup"><span data-stu-id="fbcef-111">If this value is nonzero, the ideal width will be used.</span></span> <span data-ttu-id="fbcef-112">Если это значение равно нулю, то полоса будет максимально велика.</span><span class="sxs-lookup"><span data-stu-id="fbcef-112">If this value is zero, the band will be made as large as possible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbcef-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbcef-113">Return value</span></span>

<span data-ttu-id="fbcef-114">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="fbcef-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbcef-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fbcef-115">Requirements</span></span>



| <span data-ttu-id="fbcef-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fbcef-116">Requirement</span></span> | <span data-ttu-id="fbcef-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fbcef-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbcef-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbcef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fbcef-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbcef-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbcef-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbcef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fbcef-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fbcef-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbcef-122">Header</span><span class="sxs-lookup"><span data-stu-id="fbcef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbcef-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbcef-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbcef-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbcef-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="fbcef-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fbcef-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fbcef-126">**\_СЕТБАНДИНФО RB**</span><span class="sxs-lookup"><span data-stu-id="fbcef-126">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





