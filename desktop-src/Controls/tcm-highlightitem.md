---
title: Сообщение TCM_HIGHLIGHTITEM (Коммктрл. h)
description: Задает состояние выделения элемента вкладки. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл хигхлигхтитем.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- Элементы управления Windows для TCM_HIGHLIGHTITEM сообщений
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892525"
---
# <a name="tcm_highlightitem-message"></a><span data-ttu-id="484e1-105">\_Сообщение ХИГХЛИГХТИТЕМ TCM</span><span class="sxs-lookup"><span data-stu-id="484e1-105">TCM\_HIGHLIGHTITEM message</span></span>

<span data-ttu-id="484e1-106">Задает состояние выделения элемента вкладки.</span><span class="sxs-lookup"><span data-stu-id="484e1-106">Sets the highlight state of a tab item.</span></span> <span data-ttu-id="484e1-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ хигхлигхтитем**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .</span><span class="sxs-lookup"><span data-stu-id="484e1-107">You can send this message explicitly or by using the [**TabCtrl\_HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="484e1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="484e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="484e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="484e1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="484e1-110">Значение **типа int** , указывающее Отсчитываемый от нуля индекс элемента управления вкладки.</span><span class="sxs-lookup"><span data-stu-id="484e1-110">An **INT** value that specifies the zero-based index of a tab control item.</span></span>

</dd> <dt>

<span data-ttu-id="484e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="484e1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="484e1-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, определяющее выделенное состояние выделения.</span><span class="sxs-lookup"><span data-stu-id="484e1-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** specifying the highlight state to be set.</span></span> <span data-ttu-id="484e1-113">Если это значение равно **true**, вкладка выделена; Если **значение равно false**, то для вкладки задано состояние по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="484e1-113">If this value is **TRUE**, the tab is highlighted; if **FALSE**, the tab is set to its default state.</span></span> <span data-ttu-id="484e1-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="484e1-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="484e1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="484e1-115">Return value</span></span>

<span data-ttu-id="484e1-116">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="484e1-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="484e1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="484e1-117">Remarks</span></span>

<span data-ttu-id="484e1-118">В Comctl32.dll версии 6,0 это сообщение не отображается, если тема активна.</span><span class="sxs-lookup"><span data-stu-id="484e1-118">In Comctl32.dll version 6.0, this message has no visible effect when a theme is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="484e1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="484e1-119">Requirements</span></span>



| <span data-ttu-id="484e1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="484e1-120">Requirement</span></span> | <span data-ttu-id="484e1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="484e1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="484e1-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="484e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="484e1-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="484e1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="484e1-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="484e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="484e1-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="484e1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="484e1-126">Header</span><span class="sxs-lookup"><span data-stu-id="484e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="484e1-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="484e1-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

