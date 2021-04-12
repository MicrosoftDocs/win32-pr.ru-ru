---
title: Сообщение LB_GETITEMRECT (Winuser. h)
description: Возвращает размеры прямоугольника, который привязывает элемент списка в том виде, в каком он в данный момент отображается в списке.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- Элементы управления Windows для LB_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b66c7c1a3e9f93e90beea40869cecb2081cb20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490206"
---
# <a name="lb_getitemrect-message"></a><span data-ttu-id="22a9f-104">Сообщение жетитемрект балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="22a9f-104">LB\_GETITEMRECT message</span></span>

<span data-ttu-id="22a9f-105">Возвращает размеры прямоугольника, который привязывает элемент списка в том виде, в каком он в данный момент отображается в списке.</span><span class="sxs-lookup"><span data-stu-id="22a9f-105">Gets the dimensions of the rectangle that bounds a list box item as it is currently displayed in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="22a9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22a9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22a9f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22a9f-108">Основанный на нуле индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="22a9f-108">The zero-based index of the item.</span></span>

<span data-ttu-id="22a9f-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="22a9f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="22a9f-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="22a9f-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="22a9f-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="22a9f-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="22a9f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22a9f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22a9f-113">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать клиентские координаты элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="22a9f-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the client coordinates for the item in the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a9f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22a9f-114">Return value</span></span>

<span data-ttu-id="22a9f-115">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="22a9f-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a9f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="22a9f-116">Requirements</span></span>



| <span data-ttu-id="22a9f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="22a9f-117">Requirement</span></span> | <span data-ttu-id="22a9f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="22a9f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a9f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22a9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22a9f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22a9f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="22a9f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22a9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22a9f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22a9f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22a9f-123">Header</span><span class="sxs-lookup"><span data-stu-id="22a9f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="22a9f-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22a9f-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22a9f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22a9f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="22a9f-126">[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22a9f-126">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

