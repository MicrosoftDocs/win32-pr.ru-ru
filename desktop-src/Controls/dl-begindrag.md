---
title: Код уведомления DL_BEGINDRAG (Коммктрл. h)
description: Сообщает родительскому окну поля списка перетаскивания, что пользователь щелкнул левую кнопку мыши на элементе. Поле со списком перетаскивания отправляет этот код уведомления в виде сообщения списка перетаскивания. Дополнительные сведения см. в статье перетаскивание сообщений в поле со списком.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892846"
---
# <a name="dl_begindrag-notification-code"></a><span data-ttu-id="46545-106">\_Код уведомления бегиндраг списка рассылки</span><span class="sxs-lookup"><span data-stu-id="46545-106">DL\_BEGINDRAG notification code</span></span>

<span data-ttu-id="46545-107">Сообщает родительскому окну поля списка перетаскивания, что пользователь щелкнул левую кнопку мыши на элементе.</span><span class="sxs-lookup"><span data-stu-id="46545-107">Notifies the drag list box's parent window that the user has clicked the left mouse button on an item.</span></span> <span data-ttu-id="46545-108">Поле со списком перетаскивания отправляет этот код уведомления в виде сообщения списка перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="46545-108">A drag list box sends this notification code in the form of a drag list message.</span></span> <span data-ttu-id="46545-109">Дополнительные сведения см. в статье [перетаскивание сообщений в поле со списком](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="46545-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="46545-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="46545-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46545-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46545-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46545-112">Указатель на структуру [**драглистинфо**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , содержащую \_ код уведомления DL бегиндраг, маркер для списка перетаскивания и позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="46545-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_BEGINDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46545-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46545-113">Return value</span></span>

<span data-ttu-id="46545-114">Возвращает **значение true** , чтобы начать операцию перетаскивания, или **false** , чтобы предотвратить операцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="46545-114">Return **TRUE** to begin the drag operation, or **FALSE** to prevent the drag operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="46545-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46545-115">Remarks</span></span>

<span data-ttu-id="46545-116">При обработке этого кода уведомления процедура окна обычно определяет элемент списка в указанной позиции курсора с помощью функции [**лбитемфромпт**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="46545-116">When processing this notification code, a window procedure typically determines the list item at the specified cursor position by using the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="46545-117">Затем он возвращает **значение true** или **false** в зависимости от того, следует ли перетаскивать элемент.</span><span class="sxs-lookup"><span data-stu-id="46545-117">It then returns **TRUE** or **FALSE**, depending on whether the item should be dragged.</span></span> <span data-ttu-id="46545-118">Перед возвращением значения **true** процедура Window должна сохранить индекс элемента списка, чтобы приложение знало, какой элемент нужно переместить или скопировать после завершения операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="46545-118">Before returning **TRUE**, the window procedure should save the index of the list item so the application knows which item to move or copy when the drag operation is completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="46545-119">Требования</span><span class="sxs-lookup"><span data-stu-id="46545-119">Requirements</span></span>



| <span data-ttu-id="46545-120">Требование</span><span class="sxs-lookup"><span data-stu-id="46545-120">Requirement</span></span> | <span data-ttu-id="46545-121">Значение</span><span class="sxs-lookup"><span data-stu-id="46545-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46545-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46545-122">Minimum supported client</span></span><br/> | <span data-ttu-id="46545-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46545-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46545-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46545-124">Minimum supported server</span></span><br/> | <span data-ttu-id="46545-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46545-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46545-126">Header</span><span class="sxs-lookup"><span data-stu-id="46545-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="46545-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="46545-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





