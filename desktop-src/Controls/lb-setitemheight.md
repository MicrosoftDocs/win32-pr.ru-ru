---
title: Сообщение LB_SETITEMHEIGHT (Winuser. h)
description: Задает высоту (в пикселях) элементов в поле со списком. Если список имеет стиль ФУНТа \_ овнердраввариабле, это сообщение задает высоту элемента, указанного параметром wParam. В противном случае это сообщение задает высоту всех элементов в списке.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- Элементы управления Windows для LB_SETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492432"
---
# <a name="lb_setitemheight-message"></a><span data-ttu-id="753bb-106">Сообщение сетитемхеигхт балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="753bb-106">LB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="753bb-107">Задает высоту (в пикселях) элементов в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="753bb-107">Sets the height, in pixels, of items in a list box.</span></span> <span data-ttu-id="753bb-108">Если список имеет стиль [**фунта \_ овнердраввариабле**](list-box-styles.md) , это сообщение задает высоту элемента, указанного параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="753bb-108">If the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style, this message sets the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="753bb-109">В противном случае это сообщение задает высоту всех элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="753bb-109">Otherwise, this message sets the height of all items in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="753bb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="753bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="753bb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="753bb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="753bb-112">Указывает отсчитываемый от нуля индекс элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="753bb-112">Specifies the zero-based index of the item in the list box.</span></span> <span data-ttu-id="753bb-113">Используйте этот параметр, только если список имеет стиль [**фунта \_ овнердраввариабле**](list-box-styles.md) . в противном случае установите его в ноль.</span><span class="sxs-lookup"><span data-stu-id="753bb-113">Use this parameter only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, set it to zero.</span></span>

<span data-ttu-id="753bb-114">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="753bb-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="753bb-115">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="753bb-115">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="753bb-116">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="753bb-116">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="753bb-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="753bb-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="753bb-118">Задает высоту элемента в пикселях.</span><span class="sxs-lookup"><span data-stu-id="753bb-118">Specifies the height, in pixels, of the item.</span></span> <span data-ttu-id="753bb-119">Максимальная высота составляет 255 пикселей.</span><span class="sxs-lookup"><span data-stu-id="753bb-119">The maximum height is 255 pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="753bb-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="753bb-120">Return value</span></span>

<span data-ttu-id="753bb-121">Если индекс или высота являются недопустимыми, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="753bb-121">If the index or height is invalid, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="753bb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="753bb-122">Requirements</span></span>



| <span data-ttu-id="753bb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="753bb-123">Requirement</span></span> | <span data-ttu-id="753bb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="753bb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="753bb-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="753bb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="753bb-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="753bb-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="753bb-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="753bb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="753bb-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="753bb-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="753bb-129">Header</span><span class="sxs-lookup"><span data-stu-id="753bb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="753bb-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="753bb-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="753bb-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="753bb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="753bb-132">**GETITEMHEIGHT балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="753bb-132">**LB\_GETITEMHEIGHT**</span></span>](lb-getitemheight.md)
</dt> </dl>

 

 





