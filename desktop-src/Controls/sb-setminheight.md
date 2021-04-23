---
title: Сообщение SB_SETMINHEIGHT (Коммктрл. h)
description: Задает минимальную высоту области отображения окна состояния.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Элементы управления Windows для SB_SETMINHEIGHT сообщений
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989072"
---
# <a name="sb_setminheight-message"></a><span data-ttu-id="04562-104">\_Сообщение SB сетминхеигхт</span><span class="sxs-lookup"><span data-stu-id="04562-104">SB\_SETMINHEIGHT message</span></span>

<span data-ttu-id="04562-105">Задает минимальную высоту области отображения окна состояния.</span><span class="sxs-lookup"><span data-stu-id="04562-105">Sets the minimum height of a status window's drawing area.</span></span>

## <a name="parameters"></a><span data-ttu-id="04562-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04562-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04562-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04562-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04562-108">Минимальная высота окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="04562-108">Minimum height, in pixels, of the window.</span></span>

</dd> <dt>

<span data-ttu-id="04562-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04562-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="04562-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="04562-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04562-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04562-111">Return value</span></span>

<span data-ttu-id="04562-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="04562-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04562-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04562-113">Remarks</span></span>

<span data-ttu-id="04562-114">Минимальная высота — это сумма параметра *wParam* и удвоенная ширина (в пикселях) вертикальной границы окна состояния.</span><span class="sxs-lookup"><span data-stu-id="04562-114">The minimum height is the sum of *wParam* and twice the width, in pixels, of the vertical border of the status window.</span></span> <span data-ttu-id="04562-115">Приложение должно отправить сообщение [**\_ размером WM**](/windows/desktop/winmsg/wm-size) в окно состояния, чтобы перерисовать окно.</span><span class="sxs-lookup"><span data-stu-id="04562-115">An application must send the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to the status window to redraw the window.</span></span> <span data-ttu-id="04562-116">Параметры *wParam* и *lParam* сообщения **\_ размера WM** должны иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="04562-116">The *wParam* and *lParam* parameters of the **WM\_SIZE** message should be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="04562-117">Требования</span><span class="sxs-lookup"><span data-stu-id="04562-117">Requirements</span></span>



| <span data-ttu-id="04562-118">Требование</span><span class="sxs-lookup"><span data-stu-id="04562-118">Requirement</span></span> | <span data-ttu-id="04562-119">Значение</span><span class="sxs-lookup"><span data-stu-id="04562-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04562-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04562-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04562-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04562-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04562-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04562-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04562-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04562-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04562-124">Header</span><span class="sxs-lookup"><span data-stu-id="04562-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="04562-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="04562-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

