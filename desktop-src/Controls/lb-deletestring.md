---
title: Сообщение LB_DELETESTRING (Winuser. h)
description: Удаляет строку из списка.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- Элементы управления Windows для LB_DELETESTRING сообщений
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892389"
---
# <a name="lb_deletestring-message"></a><span data-ttu-id="a86cc-104">Сообщение делетестринг балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="a86cc-104">LB\_DELETESTRING message</span></span>

<span data-ttu-id="a86cc-105">Удаляет строку из списка.</span><span class="sxs-lookup"><span data-stu-id="a86cc-105">Deletes a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="a86cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a86cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a86cc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a86cc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a86cc-108">Отсчитываемый от нуля индекс удаляемой строки.</span><span class="sxs-lookup"><span data-stu-id="a86cc-108">The zero-based index of the string to be deleted.</span></span>

<span data-ttu-id="a86cc-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="a86cc-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="a86cc-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="a86cc-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="a86cc-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="a86cc-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="a86cc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a86cc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a86cc-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="a86cc-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a86cc-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a86cc-114">Return value</span></span>

<span data-ttu-id="a86cc-115">Возвращаемое значение — это количество строк, остающихся в списке.</span><span class="sxs-lookup"><span data-stu-id="a86cc-115">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="a86cc-116">Возвращаемое значение — это ошибка балансировки нагрузки, \_ Если параметр *wParam* задает индекс, превышающий число элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="a86cc-116">The return value is LB\_ERR if the *wParam* parameter specifies an index greater than the number of items in the list.</span></span>

## <a name="remarks"></a><span data-ttu-id="a86cc-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a86cc-117">Remarks</span></span>

<span data-ttu-id="a86cc-118">Если приложение создает список с помощью стиля, рисуемого владельцем, но без стиля [**фунта \_ хасстрингс**](list-box-styles.md) , система отправляет владельцу списка сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) , чтобы приложение могла освобождать любые дополнительные данные, связанные с элементом.</span><span class="sxs-lookup"><span data-stu-id="a86cc-118">If an application creates the list box with an owner-drawn style but without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the list box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="a86cc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a86cc-119">Requirements</span></span>



| <span data-ttu-id="a86cc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a86cc-120">Requirement</span></span> | <span data-ttu-id="a86cc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a86cc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a86cc-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a86cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a86cc-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a86cc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a86cc-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a86cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a86cc-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a86cc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a86cc-126">Header</span><span class="sxs-lookup"><span data-stu-id="a86cc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a86cc-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a86cc-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a86cc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a86cc-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a86cc-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a86cc-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a86cc-130">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="a86cc-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="a86cc-131">**инсертстринг балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="a86cc-131">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="a86cc-132">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="a86cc-132">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





