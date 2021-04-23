---
title: Сообщение LB_SETTOPINDEX (Winuser. h)
description: Гарантирует, что указанный элемент в окне списка будет видимым.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_settopindex.htm
keywords:
- Элементы управления Windows для LB_SETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- LB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b415c2369ccc7963a5139ab001159bdba7d6326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137127"
---
# <a name="lb_settopindex-message"></a><span data-ttu-id="f8869-104">Сообщение сеттопиндекс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="f8869-104">LB\_SETTOPINDEX message</span></span>

<span data-ttu-id="f8869-105">Гарантирует, что указанный элемент в окне списка будет видимым.</span><span class="sxs-lookup"><span data-stu-id="f8869-105">Ensures that the specified item in a list box is visible.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8869-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8869-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8869-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8869-108">Отсчитываемый от нуля индекс элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="f8869-108">The zero-based index of the item in the list box.</span></span>

<span data-ttu-id="f8869-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="f8869-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="f8869-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="f8869-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="f8869-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="f8869-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="f8869-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8869-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8869-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="f8869-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8869-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8869-114">Return value</span></span>

<span data-ttu-id="f8869-115">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f8869-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8869-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8869-116">Remarks</span></span>

<span data-ttu-id="f8869-117">Система прокручивает содержимое списка таким образом, чтобы указанный элемент появился в верхней части окна списка или был достигнут максимальный диапазон прокрутки.</span><span class="sxs-lookup"><span data-stu-id="f8869-117">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8869-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f8869-118">Requirements</span></span>



| <span data-ttu-id="f8869-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f8869-119">Requirement</span></span> | <span data-ttu-id="f8869-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f8869-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8869-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8869-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f8869-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8869-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f8869-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8869-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f8869-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8869-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8869-125">Header</span><span class="sxs-lookup"><span data-stu-id="f8869-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8869-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8869-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8869-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8869-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8869-128">**жеттопиндекс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="f8869-128">**LB\_GETTOPINDEX**</span></span>](lb-gettopindex.md)
</dt> </dl>

 

 





