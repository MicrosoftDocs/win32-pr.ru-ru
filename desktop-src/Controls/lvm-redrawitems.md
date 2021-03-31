---
title: Сообщение LVM_REDRAWITEMS (Коммктрл. h)
description: Заставляет элемент управления "представление списка" перерисовывать диапазон элементов. Это сообщение можно отправить явно или с помощью \_ макроса Редравитемс ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Элементы управления Windows для LVM_REDRAWITEMS сообщений
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071605"
---
# <a name="lvm_redrawitems-message"></a><span data-ttu-id="9e27f-105">\_Сообщение LVM редравитемс</span><span class="sxs-lookup"><span data-stu-id="9e27f-105">LVM\_REDRAWITEMS message</span></span>

<span data-ttu-id="9e27f-106">Заставляет элемент управления "представление списка" перерисовывать диапазон элементов.</span><span class="sxs-lookup"><span data-stu-id="9e27f-106">Forces a list-view control to redraw a range of items.</span></span> <span data-ttu-id="9e27f-107">Это сообщение можно отправить явно или с помощью макроса [**\_ редравитемс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .</span><span class="sxs-lookup"><span data-stu-id="9e27f-107">You can send this message explicitly or by using the [**ListView\_RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e27f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e27f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e27f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e27f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e27f-110">Индекс первого элемента для перерисовки.</span><span class="sxs-lookup"><span data-stu-id="9e27f-110">Index of the first item to redraw.</span></span>

</dd> <dt>

<span data-ttu-id="9e27f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e27f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e27f-112">Индекс последнего элемента для перерисовки.</span><span class="sxs-lookup"><span data-stu-id="9e27f-112">Index of the last item to redraw.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e27f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e27f-113">Return value</span></span>

<span data-ttu-id="9e27f-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9e27f-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e27f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e27f-115">Remarks</span></span>

<span data-ttu-id="9e27f-116">Указанные элементы на самом деле не перерисовывается до тех пор, пока окно списка представлений не получит сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) для перерисовки.</span><span class="sxs-lookup"><span data-stu-id="9e27f-116">The specified items are not actually redrawn until the list-view window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message to repaint.</span></span> <span data-ttu-id="9e27f-117">Для немедленного перерисовки вызовите функцию [**упдатевиндов**](/windows/desktop/api/winuser/nf-winuser-updatewindow) после использования этого макроса.</span><span class="sxs-lookup"><span data-stu-id="9e27f-117">To repaint immediately, call the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function after using this macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e27f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9e27f-118">Requirements</span></span>



| <span data-ttu-id="9e27f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9e27f-119">Requirement</span></span> | <span data-ttu-id="9e27f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9e27f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e27f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e27f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e27f-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e27f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e27f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e27f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e27f-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9e27f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e27f-125">Header</span><span class="sxs-lookup"><span data-stu-id="9e27f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e27f-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e27f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

