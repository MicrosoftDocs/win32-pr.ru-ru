---
title: Сообщение LVM_APPROXIMATEVIEWRECT (Коммктрл. h)
description: Вычисляет приблизительную ширину и высоту, необходимые для вывода заданного числа элементов. Это сообщение можно отправить явным образом или использовать \_ макрос Аппроксиматевиеврект ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- Элементы управления Windows для LVM_APPROXIMATEVIEWRECT сообщений
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988206"
---
# <a name="lvm_approximateviewrect-message"></a><span data-ttu-id="ec9cd-105">\_Сообщение LVM аппроксиматевиеврект</span><span class="sxs-lookup"><span data-stu-id="ec9cd-105">LVM\_APPROXIMATEVIEWRECT message</span></span>

<span data-ttu-id="ec9cd-106">Вычисляет приблизительную ширину и высоту, необходимые для вывода заданного числа элементов.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-106">Calculates the approximate width and height required to display a given number of items.</span></span> <span data-ttu-id="ec9cd-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ аппроксиматевиеврект ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .</span><span class="sxs-lookup"><span data-stu-id="ec9cd-107">You can send this message explicitly or use the [**ListView\_ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec9cd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec9cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec9cd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec9cd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec9cd-110">Число элементов, отображаемых в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-110">The number of items to be displayed in the control.</span></span> <span data-ttu-id="ec9cd-111">Если этот параметр имеет значение-1, то в сообщении используется общее число элементов в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-111">If this parameter is set to -1, the message uses the total number of items in the control.</span></span>

</dd> <dt>

<span data-ttu-id="ec9cd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec9cd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec9cd-113">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это предлагаемое по оси x измерение элемента управления в пикселях.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the proposed x-dimension of the control, in pixels.</span></span> <span data-ttu-id="ec9cd-114">Этот параметр можно установить в значение-1, чтобы разрешить сообщению использовать текущее значение ширины.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-114">This parameter can be set to -1 to allow the message to use the current width value.</span></span>

<span data-ttu-id="ec9cd-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это предлагаемое по оси y измерение элемента управления (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="ec9cd-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the proposed y-dimension of the control, in pixels.</span></span> <span data-ttu-id="ec9cd-116">Этот параметр можно установить в значение-1, чтобы разрешить сообщению использовать текущее значение высоты.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-116">This parameter can be set to -1 to allow the message to use the current height value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec9cd-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec9cd-117">Return value</span></span>

<span data-ttu-id="ec9cd-118">Возвращает значение **типа DWORD** , которое содержит приблизительную ширину (в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) и высоту (в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))), необходимую для вывода элементов в пикселях.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-118">Returns a **DWORD** value that holds the approximate width (in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) and height (in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) needed to display the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec9cd-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec9cd-119">Remarks</span></span>

<span data-ttu-id="ec9cd-120">Установка размера элемента управления "представление списка" на основе измерений, предоставляемых этим сообщением, может оптимизировать перерисовку и уменьшить мерцание.</span><span class="sxs-lookup"><span data-stu-id="ec9cd-120">Setting the size of the list-view control based on the dimensions provided by this message can optimize redraw and reduce flicker.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec9cd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ec9cd-121">Requirements</span></span>



| <span data-ttu-id="ec9cd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ec9cd-122">Requirement</span></span> | <span data-ttu-id="ec9cd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ec9cd-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec9cd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec9cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ec9cd-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec9cd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec9cd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec9cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ec9cd-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec9cd-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec9cd-128">Header</span><span class="sxs-lookup"><span data-stu-id="ec9cd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec9cd-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec9cd-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

