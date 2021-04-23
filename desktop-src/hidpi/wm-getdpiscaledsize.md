---
title: Сообщение WM_GETDPISCALEDSIZE (Winuser. h)
description: Это сообщение сообщает операционной системе, что размер окна будет изменяться по сравнению с размерами по умолчанию.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE высокое разрешение для сообщения
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490749"
---
# <a name="wm_getdpiscaledsize-message"></a><span data-ttu-id="8b149-104">\_Сообщение ЖЕТДПИСКАЛЕДСИЗЕ WM</span><span class="sxs-lookup"><span data-stu-id="8b149-104">WM\_GETDPISCALEDSIZE message</span></span>

<span data-ttu-id="8b149-105">Это сообщение сообщает операционной системе, что размер окна будет изменяться по сравнению с размерами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b149-105">This message tells the operating system that the window will be sized to dimensions other than the default.</span></span>

<span data-ttu-id="8b149-106">Это сообщение отправляется в окна верхнего уровня с [ \_ \_ контекстом осведомленности о dpi](dpi-awareness-context.md) для каждого монитора версии 2 перед отправкой сообщения [**\_ DPICHANGED WM**](wm-dpichanged.md) и позволяет окну вычислять требуемый размер для ожидающего изменения dpi.</span><span class="sxs-lookup"><span data-stu-id="8b149-106">This message is sent to top-level windows with a [DPI\_AWARENESS\_CONTEXT](dpi-awareness-context.md) of Per Monitor v2 before a [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent, and allows the window to compute its desired size for the pending DPI change.</span></span> <span data-ttu-id="8b149-107">Так как масштабирование с линейным разрешением используется по умолчанию, это полезно только в тех случаях, когда окно пытается масштабироваться не линейно.</span><span class="sxs-lookup"><span data-stu-id="8b149-107">As linear DPI scaling is the default behavior, this is only useful in scenarios where the window wants to scale non-linearly.</span></span> <span data-ttu-id="8b149-108">Если приложение отвечает на это сообщение, полученный размер будет прямоугольником-кандидатом Send to **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="8b149-108">If the application responds to this message, the resulting size will be the candidate rectangle send to **WM\_DPICHANGED**.</span></span>

<span data-ttu-id="8b149-109">Это сообщение используется для изменения размера Rect, который предоставляется с помощью [**WM \_ DPICHANGED**](wm-dpichanged.md).</span><span class="sxs-lookup"><span data-stu-id="8b149-109">Use this message to alter the size of the rect that is provided with [**WM\_DPICHANGED**](wm-dpichanged.md).</span></span>


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a><span data-ttu-id="8b149-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b149-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b149-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b149-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b149-112">Параметр WPARAM содержит значение DPI.</span><span class="sxs-lookup"><span data-stu-id="8b149-112">The WPARAM contains a DPI value.</span></span> <span data-ttu-id="8b149-113">Масштабируемый размер окна, который будет задан приложением, должен быть вычислен так, как будто окно переключается на это значение DPI.</span><span class="sxs-lookup"><span data-stu-id="8b149-113">The scaled window size that the application would set needs to be computed as if the window were to switch to this DPI.</span></span>

</dd> <dt>

<span data-ttu-id="8b149-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b149-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b149-115">LPARAM — это указатель в/out для структуры размера.</span><span class="sxs-lookup"><span data-stu-id="8b149-115">The LPARAM is an in/out pointer to a SIZE struct.</span></span> <span data-ttu-id="8b149-116">\_Значение in в \_ lParam — это ожидающий размер окна после перемещения, инициированного пользователем, или вызова [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="8b149-116">The \_In\_ value in the LPARAM is the pending size of the window after a user-initiated move or a call to [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="8b149-117">При изменении размера окна этот размер не обязательно должен совпадать с текущим размером окна на момент получения этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8b149-117">If the window is being resized, this size is not necessarily the same as the window's current size at the time this message is received.</span></span>

<span data-ttu-id="8b149-118">\_Значение out \_ в lParam должно быть записано приложением, чтобы указать требуемый размер масштабированного окна, соответствующий указанному значению dpi в параметре wParam.</span><span class="sxs-lookup"><span data-stu-id="8b149-118">The \_Out\_ value in the LPARAM should be written to by the application to specify the desired scaled window size corresponding to the provided DPI value in the WPARAM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b149-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b149-119">Return value</span></span>

<span data-ttu-id="8b149-120">Функция возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="8b149-120">The function returns a BOOL.</span></span> <span data-ttu-id="8b149-121">Возврат значения TRUE означает, что был вычислен новый размер.</span><span class="sxs-lookup"><span data-stu-id="8b149-121">Returning TRUE indicates that a new size has been computed.</span></span> <span data-ttu-id="8b149-122">Возврат значения FALSE означает, что сообщение не будет обработано, а масштабирование линейного DPI по умолчанию будет применено к окну.</span><span class="sxs-lookup"><span data-stu-id="8b149-122">Returning FALSE indicates that the message will not be handled, and the default linear DPI scaling will apply to the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b149-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b149-123">Remarks</span></span>

<span data-ttu-id="8b149-124">Это сообщение отправляется только в окна верхнего уровня с контекстом осведомленности о DPI для каждого монитора версии 2.</span><span class="sxs-lookup"><span data-stu-id="8b149-124">This message is only sent to top-level windows which have a DPI awareness context of Per Monitor v2.</span></span>

<span data-ttu-id="8b149-125">Это событие необходимо для того, чтобы обеспечить корректное нелинейное масштабирование и гарантировать, что расположение Windows остается постоянным в связи с курсором и при перемещении между мониторами.</span><span class="sxs-lookup"><span data-stu-id="8b149-125">This event is necessary to facilitate graceful non-linear scaling, and ensures that the windows's position remains constant in relationship to the cursor and when moving back and forth across monitors.</span></span>

<span data-ttu-id="8b149-126">По умолчанию в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca)не определена обработка этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8b149-126">There is no specific default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="8b149-127">Как и для всех сообщений, которые он не обрабатывает явно, [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) возвратит ноль для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="8b149-127">As for all messages it does not explicitly handle, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will return zero for this message.</span></span> <span data-ttu-id="8b149-128">Как отмечалось выше, этот возврат сообщает системе, что используется линейное поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b149-128">As noted above, this return tells the system to use the default linear behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b149-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8b149-129">Requirements</span></span>



| <span data-ttu-id="8b149-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8b149-130">Requirement</span></span> | <span data-ttu-id="8b149-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8b149-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b149-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b149-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8b149-133">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="8b149-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8b149-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b149-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8b149-135">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8b149-135">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8b149-136">Header</span><span class="sxs-lookup"><span data-stu-id="8b149-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b149-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b149-137"><dt>Winuser.h</dt></span></span> </dl> |



 

