---
title: Сообщение CB_DELETESTRING (Winuser. h)
description: Удаляет строку из списка в поле со списком.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Элементы управления Windows для CB_DELETESTRING сообщений
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137447"
---
# <a name="cb_deletestring-message"></a><span data-ttu-id="92c15-104">\_Сообщение ДЕЛЕТЕСТРИНГ CB</span><span class="sxs-lookup"><span data-stu-id="92c15-104">CB\_DELETESTRING message</span></span>

<span data-ttu-id="92c15-105">Удаляет строку из списка в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="92c15-105">Deletes a string in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="92c15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92c15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c15-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92c15-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92c15-108">Отсчитываемый от нуля индекс удаляемой строки.</span><span class="sxs-lookup"><span data-stu-id="92c15-108">The zero-based index of the string to delete.</span></span>

</dd> <dt>

<span data-ttu-id="92c15-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92c15-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92c15-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="92c15-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c15-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92c15-111">Return value</span></span>

<span data-ttu-id="92c15-112">Возвращаемое значение — это количество строк, остающихся в списке.</span><span class="sxs-lookup"><span data-stu-id="92c15-112">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="92c15-113">Если параметр *wParam* задает индекс, превышающий число элементов в списке, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="92c15-113">If the *wParam* parameter specifies an index greater than the number of items in the list, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c15-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92c15-114">Remarks</span></span>

<span data-ttu-id="92c15-115">Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , система отправит сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) владельцу поля со списком, чтобы приложение могла освобождать любые дополнительные данные, связанные с элементом.</span><span class="sxs-lookup"><span data-stu-id="92c15-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the combo box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c15-116">Требования</span><span class="sxs-lookup"><span data-stu-id="92c15-116">Requirements</span></span>



| <span data-ttu-id="92c15-117">Требование</span><span class="sxs-lookup"><span data-stu-id="92c15-117">Requirement</span></span> | <span data-ttu-id="92c15-118">Значение</span><span class="sxs-lookup"><span data-stu-id="92c15-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c15-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92c15-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92c15-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92c15-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="92c15-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92c15-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92c15-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92c15-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="92c15-123">Header</span><span class="sxs-lookup"><span data-stu-id="92c15-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="92c15-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92c15-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c15-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92c15-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="92c15-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="92c15-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="92c15-127">**\_РЕСЕТКОНТЕНТ CB**</span><span class="sxs-lookup"><span data-stu-id="92c15-127">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="92c15-128">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="92c15-128">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





