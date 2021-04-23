---
title: Сообщение LB_GETITEMHEIGHT (Winuser. h)
description: Возвращает высоту элементов в поле со списком.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- Элементы управления Windows для LB_GETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891785"
---
# <a name="lb_getitemheight-message"></a><span data-ttu-id="59994-104">Сообщение GETITEMHEIGHT балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="59994-104">LB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="59994-105">Возвращает высоту элементов в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="59994-105">Gets the height of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="59994-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59994-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59994-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59994-108">Отсчитываемый от нуля индекс элемента списка.</span><span class="sxs-lookup"><span data-stu-id="59994-108">The zero-based index of the list box item.</span></span> <span data-ttu-id="59994-109">Этот индекс используется только в том случае, если список имеет стиль [**фунта \_ овнердраввариабле**](list-box-styles.md) . в противном случае он должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="59994-109">This index is used only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, it must be zero.</span></span>

<span data-ttu-id="59994-110">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="59994-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="59994-111">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="59994-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="59994-112">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="59994-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="59994-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59994-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59994-114">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="59994-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59994-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59994-115">Return value</span></span>

<span data-ttu-id="59994-116">Возвращаемое значение — это высота (в пикселях) каждого элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="59994-116">The return value is the height, in pixels, of each item in the list box.</span></span> <span data-ttu-id="59994-117">Возвращаемое значение — это высота элемента, заданного параметром *wParam* , если список имеет стиль [**фунта \_ овнердраввариабле**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="59994-117">The return value is the height of the item specified by the *wParam* parameter if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style.</span></span> <span data-ttu-id="59994-118">Возвращаемое значение — это ошибка балансировки нагрузки \_ при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="59994-118">The return value is LB\_ERR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="59994-119">Требования</span><span class="sxs-lookup"><span data-stu-id="59994-119">Requirements</span></span>



| <span data-ttu-id="59994-120">Требование</span><span class="sxs-lookup"><span data-stu-id="59994-120">Requirement</span></span> | <span data-ttu-id="59994-121">Значение</span><span class="sxs-lookup"><span data-stu-id="59994-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59994-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59994-122">Minimum supported client</span></span><br/> | <span data-ttu-id="59994-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59994-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="59994-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59994-124">Minimum supported server</span></span><br/> | <span data-ttu-id="59994-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59994-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59994-126">Header</span><span class="sxs-lookup"><span data-stu-id="59994-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="59994-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59994-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59994-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59994-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59994-129">**сетитемхеигхт балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="59994-129">**LB\_SETITEMHEIGHT**</span></span>](lb-setitemheight.md)
</dt> </dl>

 

 





