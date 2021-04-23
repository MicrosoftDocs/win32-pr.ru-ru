---
title: Код уведомления DL_DROPPED (Коммктрл. h)
description: Сигнализирует, что пользователь завершил операцию перетаскивания, Отпустив левую кнопку мыши. Поле со списком перетаскивания отправляет этот код уведомления в его родительское окно в виде сообщения списка перетаскивания. Дополнительные сведения см. в статье перетаскивание сообщений в поле со списком.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892849"
---
# <a name="dl_dropped-notification-code"></a><span data-ttu-id="806c0-106">\_Отброшенный код уведомления списка рассылки</span><span class="sxs-lookup"><span data-stu-id="806c0-106">DL\_DROPPED notification code</span></span>

<span data-ttu-id="806c0-107">Сигнализирует, что пользователь завершил операцию перетаскивания, Отпустив левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="806c0-107">Signals that the user has completed a drag operation by releasing the left mouse button.</span></span> <span data-ttu-id="806c0-108">Поле со списком перетаскивания отправляет этот код уведомления в его родительское окно в виде сообщения списка перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="806c0-108">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="806c0-109">Дополнительные сведения см. в статье [перетаскивание сообщений в поле со списком](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="806c0-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="806c0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="806c0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="806c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="806c0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="806c0-112">Указатель на структуру [**драглистинфо**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , содержащую \_ отброшенный код уведомления DL, маркер для списка перетаскивания и позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="806c0-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DROPPED notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="806c0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="806c0-113">Return value</span></span>

<span data-ttu-id="806c0-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="806c0-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="806c0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="806c0-115">Remarks</span></span>

<span data-ttu-id="806c0-116">Этот код уведомления обычно обрабатывается путем вставки элемента, перетаскиваемого в список перед элементом под курсором.</span><span class="sxs-lookup"><span data-stu-id="806c0-116">This notification code is normally processed by inserting the item being dragged into the list in front of the item under the cursor.</span></span> <span data-ttu-id="806c0-117">Чтобы получить индекс элемента в позиции курсора, используйте функцию [**лбитемфромпт**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="806c0-117">To retrieve the index of the item at the cursor position, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="806c0-118">Обратите внимание, что \_ отброшенный код уведомления рассылки отправляется, даже если курсор не находится на элементе списка.</span><span class="sxs-lookup"><span data-stu-id="806c0-118">Note that the DL\_DROPPED notification code is sent even if the cursor is not on a list item.</span></span> <span data-ttu-id="806c0-119">В этом случае **лбитемфромпт** возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="806c0-119">In that case, **LBItemFromPt** returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="806c0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="806c0-120">Requirements</span></span>



| <span data-ttu-id="806c0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="806c0-121">Requirement</span></span> | <span data-ttu-id="806c0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="806c0-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="806c0-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="806c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="806c0-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="806c0-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="806c0-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="806c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="806c0-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="806c0-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="806c0-127">Header</span><span class="sxs-lookup"><span data-stu-id="806c0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="806c0-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="806c0-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





