---
title: Сообщение BM_CLICK (Winuser. h)
description: Имитирует нажатие пользователем кнопки. Это сообщение приводит к тому, что кнопка получает \_ сообщения WM лбуттондовн и WM \_ лбуттонуп, а родительское окно кнопки — для получения млрд доллного \_ кода уведомления.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- Элементы управления Windows для BM_CLICK сообщений
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071330"
---
# <a name="bm_click-message"></a><span data-ttu-id="c7c67-105">BM \_ щелкните сообщение</span><span class="sxs-lookup"><span data-stu-id="c7c67-105">BM\_CLICK message</span></span>

<span data-ttu-id="c7c67-106">Имитирует нажатие пользователем кнопки.</span><span class="sxs-lookup"><span data-stu-id="c7c67-106">Simulates the user clicking a button.</span></span> <span data-ttu-id="c7c67-107">Это сообщение приводит к тому, что кнопка получает сообщения [**WM \_ Лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) и [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) , а родительское окно кнопки — для получения [млрд доллного \_](bn-clicked.md) кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="c7c67-107">This message causes the button to receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) and [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages, and the button's parent window to receive a [BN\_CLICKED](bn-clicked.md) notification code.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7c67-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7c67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c67-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7c67-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c67-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c7c67-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c7c67-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7c67-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c67-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c7c67-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c67-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7c67-113">Return value</span></span>

<span data-ttu-id="c7c67-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c7c67-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c67-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7c67-115">Remarks</span></span>

<span data-ttu-id="c7c67-116">Если кнопка находится в диалоговом окне, а диалоговое окно неактивно, сообщение **BM \_ Click** может завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c7c67-116">If the button is in a dialog box and the dialog box is not active, the **BM\_CLICK** message might fail.</span></span> <span data-ttu-id="c7c67-117">Чтобы обеспечить успешное выполнение в этой ситуации, вызовите функцию [**сетактивевиндов**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) , чтобы активировать диалоговое окно перед отправкой сообщения о **\_ нажатии кнопки BM** .</span><span class="sxs-lookup"><span data-stu-id="c7c67-117">To ensure success in this situation, call the [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) function to activate the dialog box before sending the **BM\_CLICK** message to the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c67-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c7c67-118">Requirements</span></span>



| <span data-ttu-id="c7c67-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c7c67-119">Requirement</span></span> | <span data-ttu-id="c7c67-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c7c67-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c67-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7c67-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c67-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7c67-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c7c67-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7c67-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c67-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7c67-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7c67-125">Header</span><span class="sxs-lookup"><span data-stu-id="c7c67-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c67-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7c67-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

