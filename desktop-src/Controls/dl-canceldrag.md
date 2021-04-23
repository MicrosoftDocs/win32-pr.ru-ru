---
title: Код уведомления DL_CANCELDRAG (Коммктрл. h)
description: Сигнализирует, что пользователь отменил операцию перетаскивания, щелкнув правой кнопкой мыши или нажав клавишу ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- DL_CANCELDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137906"
---
# <a name="dl_canceldrag-notification-code"></a><span data-ttu-id="244d0-104">\_Код уведомления канцелдраг списка рассылки</span><span class="sxs-lookup"><span data-stu-id="244d0-104">DL\_CANCELDRAG notification code</span></span>

<span data-ttu-id="244d0-105">Сигнализирует, что пользователь отменил операцию перетаскивания, щелкнув правой кнопкой мыши или нажав клавишу ESC.</span><span class="sxs-lookup"><span data-stu-id="244d0-105">Signals that the user has canceled a drag operation by clicking the right mouse button or pressing the ESC key.</span></span> <span data-ttu-id="244d0-106">Поле со списком перетаскивания отправляет этот код уведомления в его родительское окно в виде сообщения списка перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="244d0-106">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="244d0-107">Дополнительные сведения см. в статье [перетаскивание сообщений в поле со списком](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="244d0-107">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="244d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="244d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244d0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="244d0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="244d0-110">Указатель на структуру [**драглистинфо**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , содержащую \_ код уведомления DL канцелдраг, маркер для списка перетаскивания и позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="244d0-110">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_CANCELDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244d0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="244d0-111">Return value</span></span>

<span data-ttu-id="244d0-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="244d0-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="244d0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="244d0-113">Remarks</span></span>

<span data-ttu-id="244d0-114">Обрабатывая \_ код уведомления канцелдраг списка рассылки, приложение может сбросить свое внутреннее состояние, чтобы указать, что перетаскивание не действует.</span><span class="sxs-lookup"><span data-stu-id="244d0-114">By processing the DL\_CANCELDRAG notification code, an application can reset its internal state to indicate that dragging is not in effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="244d0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="244d0-115">Requirements</span></span>



| <span data-ttu-id="244d0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="244d0-116">Requirement</span></span> | <span data-ttu-id="244d0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="244d0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="244d0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="244d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="244d0-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="244d0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="244d0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="244d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="244d0-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="244d0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="244d0-122">Header</span><span class="sxs-lookup"><span data-stu-id="244d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="244d0-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="244d0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





