---
title: Сообщение LB_GETSEL (Winuser. h)
description: Возвращает состояние выбора элемента.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- Элементы управления Windows для LB_GETSEL сообщений
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d808935e65a1ea748c59d606aa2cf483748fb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892149"
---
# <a name="lb_getsel-message"></a><span data-ttu-id="d5609-104">Сообщение жетсел балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="d5609-104">LB\_GETSEL message</span></span>

<span data-ttu-id="d5609-105">Возвращает состояние выбора элемента.</span><span class="sxs-lookup"><span data-stu-id="d5609-105">Gets the selection state of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5609-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5609-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5609-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5609-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5609-108">Основанный на нуле индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="d5609-108">The zero-based index of the item.</span></span>

<span data-ttu-id="d5609-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="d5609-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="d5609-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="d5609-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="d5609-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="d5609-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="d5609-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5609-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5609-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="d5609-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5609-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5609-114">Return value</span></span>

<span data-ttu-id="d5609-115">Если выбран элемент, возвращаемое значение больше нуля; в противном случае он равен нулю.</span><span class="sxs-lookup"><span data-stu-id="d5609-115">If an item is selected, the return value is greater than zero; otherwise, it is zero.</span></span> <span data-ttu-id="d5609-116">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d5609-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5609-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d5609-117">Requirements</span></span>



| <span data-ttu-id="d5609-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d5609-118">Requirement</span></span> | <span data-ttu-id="d5609-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d5609-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5609-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5609-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5609-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5609-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d5609-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5609-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5609-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5609-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5609-124">Header</span><span class="sxs-lookup"><span data-stu-id="d5609-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5609-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5609-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5609-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5609-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5609-127">**сетсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="d5609-127">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





