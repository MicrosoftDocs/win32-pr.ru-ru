---
title: Сообщение TTM_RELAYEVENT (Коммктрл. h)
description: Передает сообщение мыши элементу управления ToolTip для обработки.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Элементы управления Windows для TTM_RELAYEVENT сообщений
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353252"
---
# <a name="ttm_relayevent-message"></a><span data-ttu-id="6b76b-104">\_Сообщение ТТМ релайевент</span><span class="sxs-lookup"><span data-stu-id="6b76b-104">TTM\_RELAYEVENT message</span></span>

<span data-ttu-id="6b76b-105">Передает сообщение мыши элементу управления ToolTip для обработки.</span><span class="sxs-lookup"><span data-stu-id="6b76b-105">Passes a mouse message to a tooltip control for processing.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b76b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b76b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b76b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b76b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b76b-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6b76b-108">Must be zero.</span></span> <span data-ttu-id="6b76b-109">**Windows 7 и более поздние версии:** Если позиция подсказки смещена от позиции курсора (в порядке, когда палец или указывающее устройство не затронула), этот параметр может содержать дополнительные сведения, взятые из сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="6b76b-109">**Windows 7 and later:** If the position of the tooltip is offset from the cursor position (in order not be obstructed by a finger or pointing device), this parameter can contain extra information taken from the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="6b76b-110">Извлеките эту лишнюю информацию с помощью [**жетмессажеекстраинфо**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span><span class="sxs-lookup"><span data-stu-id="6b76b-110">Retrieve this extra information with [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span></span>

</dd> <dt>

<span data-ttu-id="6b76b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b76b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b76b-112">Указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую сообщение для ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="6b76b-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to relay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b76b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b76b-113">Return value</span></span>

<span data-ttu-id="6b76b-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="6b76b-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b76b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b76b-115">Remarks</span></span>

<span data-ttu-id="6b76b-116">Элемент управления ToolTip обрабатывает только следующие сообщения, переданные в него сообщением **ТТМ \_ релайевент** :</span><span class="sxs-lookup"><span data-stu-id="6b76b-116">A tooltip control processes only the following messages passed to it by the **TTM\_RELAYEVENT** message:</span></span>

-   <span data-ttu-id="6b76b-117">WM \_ лбуттондовн</span><span class="sxs-lookup"><span data-stu-id="6b76b-117">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="6b76b-118">WM \_ лбуттонуп</span><span class="sxs-lookup"><span data-stu-id="6b76b-118">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="6b76b-119">WM \_ мбуттондовн</span><span class="sxs-lookup"><span data-stu-id="6b76b-119">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="6b76b-120">WM \_ мбуттонуп</span><span class="sxs-lookup"><span data-stu-id="6b76b-120">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="6b76b-121">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="6b76b-121">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="6b76b-122">WM \_ нкмаусемове</span><span class="sxs-lookup"><span data-stu-id="6b76b-122">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="6b76b-123">WM \_ рбуттондовн</span><span class="sxs-lookup"><span data-stu-id="6b76b-123">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="6b76b-124">WM \_ рбуттонуп</span><span class="sxs-lookup"><span data-stu-id="6b76b-124">WM\_RBUTTONUP</span></span>

<span data-ttu-id="6b76b-125">Все остальные сообщения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="6b76b-125">All other messages are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b76b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6b76b-126">Requirements</span></span>



| <span data-ttu-id="6b76b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6b76b-127">Requirement</span></span> | <span data-ttu-id="6b76b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6b76b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b76b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b76b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6b76b-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b76b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b76b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b76b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6b76b-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b76b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b76b-133">Header</span><span class="sxs-lookup"><span data-stu-id="6b76b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b76b-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b76b-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

