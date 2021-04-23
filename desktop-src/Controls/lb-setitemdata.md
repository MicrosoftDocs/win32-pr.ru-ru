---
title: Сообщение LB_SETITEMDATA (Winuser. h)
description: Задает значение, связанное с указанным элементом в поле со списком.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- Элементы управления Windows для LB_SETITEMDATA сообщений
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137134"
---
# <a name="lb_setitemdata-message"></a><span data-ttu-id="5beb4-104">Сообщение сетитемдата балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="5beb4-104">LB\_SETITEMDATA message</span></span>

<span data-ttu-id="5beb4-105">Задает значение, связанное с указанным элементом в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="5beb4-105">Sets a value associated with the specified item in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5beb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5beb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5beb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5beb4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5beb4-108">Указывает отсчитываемый от нуля индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="5beb4-108">Specifies the zero-based index of the item.</span></span> <span data-ttu-id="5beb4-109">Если это значение равно-1, то значение *lParam* применяется ко всем элементам списка.</span><span class="sxs-lookup"><span data-stu-id="5beb4-109">If this value is -1, the *lParam* value applies to all items in the list box.</span></span>

<span data-ttu-id="5beb4-110">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="5beb4-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5beb4-111">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="5beb4-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5beb4-112">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="5beb4-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5beb4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5beb4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5beb4-114">Указывает значение, которое должно быть связано с элементом.</span><span class="sxs-lookup"><span data-stu-id="5beb4-114">Specifies the value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5beb4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5beb4-115">Return value</span></span>

<span data-ttu-id="5beb4-116">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="5beb4-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5beb4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5beb4-117">Remarks</span></span>

<span data-ttu-id="5beb4-118">Если элемент находится в списке, созданном владельцем, без стиля [**фунта \_ хасстрингс**](list-box-styles.md) , это сообщение заменяет значение, содержащееся в параметре *lParam* сообщения [**\_ ADDSTRING**](lb-addstring.md) или [**\_ инсертстринг**](lb-insertstring.md) , которое добавляет элемент в список.</span><span class="sxs-lookup"><span data-stu-id="5beb4-118">If the item is in an owner-drawn list box created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this message replaces the value contained in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5beb4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5beb4-119">Requirements</span></span>



| <span data-ttu-id="5beb4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5beb4-120">Requirement</span></span> | <span data-ttu-id="5beb4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5beb4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5beb4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5beb4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5beb4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5beb4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5beb4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5beb4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5beb4-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5beb4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5beb4-126">Header</span><span class="sxs-lookup"><span data-stu-id="5beb4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5beb4-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5beb4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5beb4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5beb4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5beb4-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5beb4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5beb4-130">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="5beb4-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5beb4-131">**жетитемдата балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="5beb4-131">**LB\_GETITEMDATA**</span></span>](lb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="5beb4-132">**инсертстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="5beb4-132">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





