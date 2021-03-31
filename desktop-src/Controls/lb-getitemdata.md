---
title: Сообщение LB_GETITEMDATA (Winuser. h)
description: Возвращает определяемое приложением значение, связанное с указанным элементом списка.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- Элементы управления Windows для LB_GETITEMDATA сообщений
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137439"
---
# <a name="lb_getitemdata-message"></a><span data-ttu-id="8385b-104">Сообщение жетитемдата балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="8385b-104">LB\_GETITEMDATA message</span></span>

<span data-ttu-id="8385b-105">Возвращает определяемое приложением значение, связанное с указанным элементом списка.</span><span class="sxs-lookup"><span data-stu-id="8385b-105">Gets the application-defined value associated with the specified list box item.</span></span>

## <a name="parameters"></a><span data-ttu-id="8385b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8385b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8385b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8385b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8385b-108">Индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="8385b-108">The index of the item.</span></span>

<span data-ttu-id="8385b-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="8385b-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="8385b-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="8385b-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="8385b-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="8385b-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="8385b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8385b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8385b-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="8385b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8385b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8385b-114">Return value</span></span>

<span data-ttu-id="8385b-115">Возвращаемое значение — это значение, связанное с элементом, или ошибка балансировки нагрузки \_ при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="8385b-115">The return value is the value associated with the item, or LB\_ERR if an error occurs.</span></span> <span data-ttu-id="8385b-116">Если элемент находится в списке, рисуемом владельцем, и был создан без [**\_ Хасстрингс стиля фунта**](list-box-styles.md) , это значение было указано в параметре *lParam* сообщения [**\_ ADDSTRING**](lb-addstring.md) или [**фунтов \_ инсертстринг**](lb-insertstring.md) , которое добавляло элемент в список.</span><span class="sxs-lookup"><span data-stu-id="8385b-116">If the item is in an owner-drawn list box and was created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this value was in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span> <span data-ttu-id="8385b-117">В противном случае это значение параметра *lParam* сообщения [**\_ сетитемдата балансировки нагрузки**](lb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="8385b-117">Otherwise, it is the value in the *lParam* of the [**LB\_SETITEMDATA**](lb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8385b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8385b-118">Requirements</span></span>



| <span data-ttu-id="8385b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8385b-119">Requirement</span></span> | <span data-ttu-id="8385b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8385b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8385b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8385b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8385b-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8385b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8385b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8385b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8385b-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8385b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8385b-125">Header</span><span class="sxs-lookup"><span data-stu-id="8385b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8385b-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8385b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8385b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8385b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8385b-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8385b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8385b-129">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="8385b-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="8385b-130">**инсертстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="8385b-130">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="8385b-131">**сетитемдата балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="8385b-131">**LB\_SETITEMDATA**</span></span>](lb-setitemdata.md)
</dt> </dl>

 

 





