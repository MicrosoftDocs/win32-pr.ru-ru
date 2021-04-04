---
title: Сообщение LB_SETANCHORINDEX (Winuser. h)
description: Задает элемент привязки \ 8212;, т. е. элемент, из которого начинается выбор нескольких элементов. Множественный выбор охватывает все элементы из привязанного элемента в элемент курсора.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- Элементы управления Windows для LB_SETANCHORINDEX сообщений
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137138"
---
# <a name="lb_setanchorindex-message"></a><span data-ttu-id="6a29b-105">Сообщение сетанчориндекс балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="6a29b-105">LB\_SETANCHORINDEX message</span></span>

<span data-ttu-id="6a29b-106">Задает элемент привязки, т. е. элемент, из которого начинается выбор нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="6a29b-106">Sets the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="6a29b-107">Множественный выбор охватывает все элементы из привязанного элемента в элемент курсора.</span><span class="sxs-lookup"><span data-stu-id="6a29b-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a29b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a29b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a29b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a29b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a29b-110">Задает индекс нового элемента привязки.</span><span class="sxs-lookup"><span data-stu-id="6a29b-110">Specifies the index of the new anchor item.</span></span>

<span data-ttu-id="6a29b-111">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="6a29b-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6a29b-112">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="6a29b-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6a29b-113">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="6a29b-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6a29b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a29b-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a29b-115">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="6a29b-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a29b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a29b-116">Return value</span></span>

<span data-ttu-id="6a29b-117">Если сообщение прошло удачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6a29b-117">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="6a29b-118">Если сообщение не выполняется, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6a29b-118">If the message fails, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a29b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6a29b-119">Requirements</span></span>



| <span data-ttu-id="6a29b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6a29b-120">Requirement</span></span> | <span data-ttu-id="6a29b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6a29b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a29b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a29b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6a29b-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a29b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6a29b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a29b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6a29b-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a29b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6a29b-126">Header</span><span class="sxs-lookup"><span data-stu-id="6a29b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a29b-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a29b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a29b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a29b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a29b-129">**жетанчориндекс балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="6a29b-129">**LB\_GETANCHORINDEX**</span></span>](lb-getanchorindex.md)
</dt> </dl>

 

 





