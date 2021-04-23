---
title: Сообщение WM_DWMWINDOWMAXIMIZEDCHANGE (Winuser. h)
description: Посылается, когда развернутое окно диспетчер окон рабочего стола (DWM) развернуто.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Сообщение WM_DWMWINDOWMAXIMIZEDCHANGE диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415608"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a><span data-ttu-id="b8f11-104">\_Сообщение ДВМВИНДОВМАКСИМИЗЕДЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="b8f11-104">WM\_DWMWINDOWMAXIMIZEDCHANGE message</span></span>

<span data-ttu-id="b8f11-105">Посылается, когда развернутое окно диспетчер окон рабочего стола (DWM) развернуто.</span><span class="sxs-lookup"><span data-stu-id="b8f11-105">Sent when a Desktop Window Manager (DWM) composed window is maximized.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8f11-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8f11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f11-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8f11-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f11-108">Задайте значение true, чтобы указать, что окно развернуто.</span><span class="sxs-lookup"><span data-stu-id="b8f11-108">Set to true to specify that the window has been maximized.</span></span>

</dd> <dt>

<span data-ttu-id="b8f11-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8f11-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f11-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b8f11-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f11-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8f11-111">Return value</span></span>

<span data-ttu-id="b8f11-112">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="b8f11-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f11-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8f11-113">Remarks</span></span>

<span data-ttu-id="b8f11-114">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8f11-114">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f11-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b8f11-115">Requirements</span></span>



| <span data-ttu-id="b8f11-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b8f11-116">Requirement</span></span> | <span data-ttu-id="b8f11-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f11-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f11-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8f11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f11-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8f11-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b8f11-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8f11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f11-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8f11-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8f11-122">Header</span><span class="sxs-lookup"><span data-stu-id="b8f11-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f11-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f11-123"><dt>Winuser.h</dt></span></span> </dl> |



 

