---
title: Сообщение RB_BEGINDRAG (Коммктрл. h)
description: Помещает элемент управления главной панели в режим перетаскивания. Это сообщение не приводит к \_ отправке уведомления РБН бегиндраг.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Элементы управления Windows для RB_BEGINDRAG сообщений
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491781"
---
# <a name="rb_begindrag-message"></a><span data-ttu-id="9128d-105">\_Сообщение БЕГИНДРАГ RB</span><span class="sxs-lookup"><span data-stu-id="9128d-105">RB\_BEGINDRAG message</span></span>

<span data-ttu-id="9128d-106">Помещает элемент управления главной панели в режим перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="9128d-106">Puts the rebar control in drag-and-drop mode.</span></span> <span data-ttu-id="9128d-107">Это сообщение не приводит к отправке уведомления [РБН \_ бегиндраг](rbn-begindrag.md) .</span><span class="sxs-lookup"><span data-stu-id="9128d-107">This message does not cause a [RBN\_BEGINDRAG](rbn-begindrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="9128d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9128d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9128d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9128d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9128d-110">Отсчитываемый от нуля индекс диапазона, на который будет влиять операция перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="9128d-110">Zero-based index of the band that the drag-and-drop operation will affect.</span></span>

</dd> <dt>

<span data-ttu-id="9128d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9128d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9128d-112">Значение **типа DWORD** , содержащее начальные координаты мыши.</span><span class="sxs-lookup"><span data-stu-id="9128d-112">**DWORD** value that contains the starting mouse coordinates.</span></span> <span data-ttu-id="9128d-113">Горизонтальная координата содержится в ЛОВОРД, а вертикальная координата содержится в HIWORD.</span><span class="sxs-lookup"><span data-stu-id="9128d-113">The horizontal coordinate is contained in the LOWORD and the vertical coordinate is contained in the HIWORD.</span></span> <span data-ttu-id="9128d-114">Если передать (**DWORD**) значение 1, элемент управления "Главная панель" будет использовать расположение мыши во время последнего потока элемента управления [**с именем "**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)".</span><span class="sxs-lookup"><span data-stu-id="9128d-114">If you pass (**DWORD**)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9128d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9128d-115">Return value</span></span>

<span data-ttu-id="9128d-116">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="9128d-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9128d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9128d-117">Remarks</span></span>

<span data-ttu-id="9128d-118">Сообщения **RB \_ бегиндраг**, [**RB \_ драгмове**](rb-dragmove.md)и [**RB \_ енддраг**](rb-enddrag.md) позволяют реализовать интерфейс [**интерфейс IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) для элемента управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="9128d-118">The **RB\_BEGINDRAG**, [**RB\_DRAGMOVE**](rb-dragmove.md), and [**RB\_ENDDRAG**](rb-enddrag.md) messages allow you to implement an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface for a rebar control.</span></span> <span data-ttu-id="9128d-119">Вы отправляете **сообщение \_ RB бегиндраг** в ответ на [**интерфейс IDropTarget::D ражентер**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), отправляете сообщение **RB \_ Драгмове** в ответ на [**интерфейс IDropTarget::D Раговер**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), а сообщение **RB \_ Енддраг** в ответ на [**интерфейс IDropTarget::D верхнем**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) и [**интерфейс IDropTarget::D раглеаве**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span><span class="sxs-lookup"><span data-stu-id="9128d-119">You send the **RB\_BEGINDRAG** message in response to [**IDropTarget::DragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), send the **RB\_DRAGMOVE** message in response to [**IDropTarget::DragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), and the **RB\_ENDDRAG** message in response to [**IDropTarget::Drop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) and [**IDropTarget::DragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span></span>

## <a name="requirements"></a><span data-ttu-id="9128d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9128d-120">Requirements</span></span>



| <span data-ttu-id="9128d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9128d-121">Requirement</span></span> | <span data-ttu-id="9128d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9128d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9128d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9128d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9128d-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9128d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9128d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9128d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9128d-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9128d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9128d-127">Header</span><span class="sxs-lookup"><span data-stu-id="9128d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9128d-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9128d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

