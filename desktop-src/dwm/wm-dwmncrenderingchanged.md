---
title: Сообщение WM_DWMNCRENDERINGCHANGED (Winuser. h)
description: Посылается, когда изменилась политика отрисовки области, не являющейся клиентской.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- Сообщение WM_DWMNCRENDERINGCHANGED диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988737"
---
# <a name="wm_dwmncrenderingchanged-message"></a><span data-ttu-id="105ba-104">\_Сообщение ДВМНКРЕНДЕРИНГЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="105ba-104">WM\_DWMNCRENDERINGCHANGED message</span></span>

<span data-ttu-id="105ba-105">Посылается, когда изменилась политика отрисовки области, не являющейся клиентской.</span><span class="sxs-lookup"><span data-stu-id="105ba-105">Sent when the non-client area rendering policy has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="105ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="105ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="105ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="105ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="105ba-108">Указывает, включена ли визуализация DWM для области окна, не являющейся клиентской.</span><span class="sxs-lookup"><span data-stu-id="105ba-108">Specifies whether DWM rendering is enabled for the non-client area of the window.</span></span> <span data-ttu-id="105ba-109">**Значение true** , если включено; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="105ba-109">**TRUE** if enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="105ba-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="105ba-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="105ba-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="105ba-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="105ba-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="105ba-112">Return value</span></span>

<span data-ttu-id="105ba-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="105ba-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="105ba-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="105ba-114">Remarks</span></span>

<span data-ttu-id="105ba-115">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="105ba-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="105ba-116">Функции [**двмжетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) и [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) используются для получения или задания политики отрисовки без клиента.</span><span class="sxs-lookup"><span data-stu-id="105ba-116">The [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions are used to get or set the non-client rendering policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="105ba-117">Требования</span><span class="sxs-lookup"><span data-stu-id="105ba-117">Requirements</span></span>



| <span data-ttu-id="105ba-118">Требование</span><span class="sxs-lookup"><span data-stu-id="105ba-118">Requirement</span></span> | <span data-ttu-id="105ba-119">Значение</span><span class="sxs-lookup"><span data-stu-id="105ba-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="105ba-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="105ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="105ba-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="105ba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="105ba-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="105ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="105ba-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="105ba-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="105ba-124">Header</span><span class="sxs-lookup"><span data-stu-id="105ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="105ba-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="105ba-125"><dt>Winuser.h</dt></span></span> </dl> |



 

