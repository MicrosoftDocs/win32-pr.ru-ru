---
title: Сообщение CB_RESETCONTENT (Winuser. h)
description: Удаляет все элементы из списка и элементы управления поля со списком.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Элементы управления Windows для CB_RESETCONTENT сообщений
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891917"
---
# <a name="cb_resetcontent-message"></a><span data-ttu-id="2555f-104">\_Сообщение РЕСЕТКОНТЕНТ CB</span><span class="sxs-lookup"><span data-stu-id="2555f-104">CB\_RESETCONTENT message</span></span>

<span data-ttu-id="2555f-105">Удаляет все элементы из списка и элементы управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="2555f-105">Removes all items from the list box and edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2555f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2555f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2555f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2555f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2555f-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2555f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2555f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2555f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2555f-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2555f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2555f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2555f-111">Return value</span></span>

<span data-ttu-id="2555f-112">Это сообщение всегда возвращает значение CB \_ .</span><span class="sxs-lookup"><span data-stu-id="2555f-112">This message always returns CB\_OKAY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2555f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2555f-113">Remarks</span></span>

<span data-ttu-id="2555f-114">Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , владелец поля со списком получает сообщение [**WM \_ DELETEITEM**](wm-deleteitem.md) для каждого элемента в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="2555f-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the owner of the combo box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2555f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2555f-115">Requirements</span></span>



| <span data-ttu-id="2555f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2555f-116">Requirement</span></span> | <span data-ttu-id="2555f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2555f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2555f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2555f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2555f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2555f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2555f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2555f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2555f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2555f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2555f-122">Header</span><span class="sxs-lookup"><span data-stu-id="2555f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2555f-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2555f-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2555f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2555f-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="2555f-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2555f-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2555f-126">**\_ДЕЛЕТЕСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="2555f-126">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="2555f-127">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="2555f-127">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





