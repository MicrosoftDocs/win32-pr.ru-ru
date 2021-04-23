---
title: Сообщение LB_INITSTORAGE (Winuser. h)
description: Выделяет память для хранения элементов списка. Это сообщение используется до того, как приложение добавит большое количество элементов в список.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- Элементы управления Windows для LB_INITSTORAGE сообщений
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490707"
---
# <a name="lb_initstorage-message"></a><span data-ttu-id="e4ba9-105">Сообщение инитстораже балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="e4ba9-105">LB\_INITSTORAGE message</span></span>

<span data-ttu-id="e4ba9-106">Выделяет память для хранения элементов списка.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-106">Allocates memory for storing list box items.</span></span> <span data-ttu-id="e4ba9-107">Это сообщение используется до того, как приложение добавит большое количество элементов в список.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-107">This message is used before an application adds a large number of items to a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4ba9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4ba9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ba9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4ba9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4ba9-110">Число добавляемых элементов.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-110">The number of items to add.</span></span>

<span data-ttu-id="e4ba9-111">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="e4ba9-112">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="e4ba9-113">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="e4ba9-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4ba9-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4ba9-115">Объем памяти в байтах, выделяемой для строк элемента.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-115">The amount of memory, in bytes, to allocate for item strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ba9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4ba9-116">Return value</span></span>

<span data-ttu-id="e4ba9-117">Если сообщение прошло успешно, возвращаемое значение — это общее число элементов, для которых была предварительно распределена память, то есть общее число элементов, добавленных всеми успешными **\_ инитстораже** сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-117">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="e4ba9-118">Если сообщение не выполняется, возвращается значение фунтов \_ еррспаце.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-118">If the message fails, the return value is LB\_ERRSPACE.</span></span>

<span data-ttu-id="e4ba9-119">Microsoft Windows NT 4,0: это сообщение не выделяет указанный объем памяти; Однако он всегда возвращает значение, указанное в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e4ba9-119">Microsoft Windows NT 4.0 : This message does not allocate the specified amount of memory; however, it always returns the value specified in the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ba9-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4ba9-120">Remarks</span></span>

<span data-ttu-id="e4ba9-121">Сообщение **\_ инитстораже балансировки нагрузки** помогает ускорить инициализацию списков с большим количеством элементов (более 100).</span><span class="sxs-lookup"><span data-stu-id="e4ba9-121">The **LB\_INITSTORAGE** message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="e4ba9-122">Он резервирует указанный объем памяти, чтобы последующие [**\_ ADDSTRING нагрузки**](lb-addstring.md), [**балансировки нагрузки \_ инсертстринг**](lb-insertstring.md), [**балансировки \_**](lb-dir.md)нагрузки и [**балансировки \_**](lb-addfile.md) нагрузки занимают максимально короткие сроки.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-122">It reserves the specified amount of memory so that subsequent [**LB\_ADDSTRING**](lb-addstring.md), [**LB\_INSERTSTRING**](lb-insertstring.md), [**LB\_DIR**](lb-dir.md), and [**LB\_ADDFILE**](lb-addfile.md) messages take the shortest possible time.</span></span> <span data-ttu-id="e4ba9-123">Для параметров *wParam* и *lParam* можно использовать оценки.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="e4ba9-124">При чрезмерной оценке выделяется дополнительный объем памяти. Если недооценивать, то для элементов, превышающих запрошенный объем, используется нормальное выделение.</span><span class="sxs-lookup"><span data-stu-id="e4ba9-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ba9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e4ba9-125">Requirements</span></span>



| <span data-ttu-id="e4ba9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e4ba9-126">Requirement</span></span> | <span data-ttu-id="e4ba9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e4ba9-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ba9-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4ba9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ba9-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4ba9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e4ba9-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4ba9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ba9-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4ba9-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4ba9-132">Header</span><span class="sxs-lookup"><span data-stu-id="e4ba9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4ba9-133"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ba9-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ba9-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4ba9-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4ba9-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e4ba9-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e4ba9-136">**ADDFILE балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="e4ba9-136">**LB\_ADDFILE**</span></span>](lb-addfile.md)
</dt> <dt>

[<span data-ttu-id="e4ba9-137">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="e4ba9-137">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e4ba9-138">**Каталог балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="e4ba9-138">**LB\_DIR**</span></span>](lb-dir.md)
</dt> <dt>

[<span data-ttu-id="e4ba9-139">**инсертстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="e4ba9-139">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





