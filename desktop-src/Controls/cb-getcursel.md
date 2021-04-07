---
title: Сообщение CB_GETCURSEL (Winuser. h)
description: Приложение отправляет \_ сообщение с индексом CB для получения индекса выбранного в данный момент элемента в поле со списком.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- Элементы управления Windows для CB_GETCURSEL сообщений
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892850"
---
# <a name="cb_getcursel-message"></a><span data-ttu-id="68461-104">Сообщение с нерекурсивным превышем CB \_</span><span class="sxs-lookup"><span data-stu-id="68461-104">CB\_GETCURSEL message</span></span>

<span data-ttu-id="68461-105">Приложение отправляет сообщение с индексом **CB \_** для получения индекса выбранного в данный момент элемента в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="68461-105">An application sends a **CB\_GETCURSEL** message to retrieve the index of the currently selected item, if any, in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="68461-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68461-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68461-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68461-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68461-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="68461-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="68461-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68461-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68461-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="68461-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68461-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68461-111">Return value</span></span>

<span data-ttu-id="68461-112">Возвращаемое значение — это Отсчитываемый от нуля индекс текущего выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="68461-112">The return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="68461-113">Если элемент не выбран, это значение равно CB \_ .</span><span class="sxs-lookup"><span data-stu-id="68461-113">If no item is selected, it is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="68461-114">Требования</span><span class="sxs-lookup"><span data-stu-id="68461-114">Requirements</span></span>



| <span data-ttu-id="68461-115">Требование</span><span class="sxs-lookup"><span data-stu-id="68461-115">Requirement</span></span> | <span data-ttu-id="68461-116">Значение</span><span class="sxs-lookup"><span data-stu-id="68461-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68461-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68461-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68461-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68461-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="68461-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68461-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68461-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68461-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="68461-121">Header</span><span class="sxs-lookup"><span data-stu-id="68461-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68461-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68461-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68461-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68461-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="68461-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="68461-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68461-125">**\_СЕЛЕКТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="68461-125">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="68461-126">**\_СЕТКУРСЕЛ CB**</span><span class="sxs-lookup"><span data-stu-id="68461-126">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> </dl>

 

 





