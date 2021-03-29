---
title: Код уведомления DL_DRAGGING (Коммктрл. h)
description: Сигнализирует, что пользователь переместил указатель мыши при перетаскивании элемента.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535651"
---
# <a name="dl_dragging-notification-code"></a><span data-ttu-id="536dc-104">\_Код уведомления для перетаскивания списка рассылки</span><span class="sxs-lookup"><span data-stu-id="536dc-104">DL\_DRAGGING notification code</span></span>

<span data-ttu-id="536dc-105">Сигнализирует, что пользователь переместил указатель мыши при перетаскивании элемента.</span><span class="sxs-lookup"><span data-stu-id="536dc-105">Signals that the user has moved the mouse while dragging an item.</span></span> <span data-ttu-id="536dc-106">\_Перетаскивание DL также периодически отправляется во время перетаскивания, даже если мышь не перемещена.</span><span class="sxs-lookup"><span data-stu-id="536dc-106">DL\_DRAGGING is also sent periodically during dragging even if the mouse is not moved.</span></span> <span data-ttu-id="536dc-107">Поле со списком перетаскивания отправляет этот код уведомления в его родительское окно в виде сообщения списка перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="536dc-107">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="536dc-108">Дополнительные сведения см. в статье [перетаскивание сообщений в поле со списком](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="536dc-108">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="536dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="536dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="536dc-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="536dc-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="536dc-111">Идентификатор элемента управления поля со списком перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="536dc-111">The control identifier of the drag list box.</span></span>

</dd> <dt>

<span data-ttu-id="536dc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="536dc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="536dc-113">Указатель на структуру [**драглистинфо**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , содержащую \_ код уведомления для перетаскивания списка рассылки, маркер в поле со списком перетаскивания и позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="536dc-113">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DRAGGING notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="536dc-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="536dc-114">Return value</span></span>

<span data-ttu-id="536dc-115">Возвращаемое значение определяет тип курсора мыши, который должен быть установлен в списке перетаскивания. Это может быть значение списка рассылки \_ стопкурсор, DL \_ КОПИКУРСОР или DL \_ мовекурсор.</span><span class="sxs-lookup"><span data-stu-id="536dc-115">The return value determines the type of mouse cursor that the drag list should set; it can be the DL\_STOPCURSOR, DL\_COPYCURSOR, or DL\_MOVECURSOR value.</span></span> <span data-ttu-id="536dc-116">Если возвращается любое другое значение, курсор не изменяется.</span><span class="sxs-lookup"><span data-stu-id="536dc-116">If any other value is returned, the cursor does not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="536dc-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="536dc-117">Remarks</span></span>

<span data-ttu-id="536dc-118">Как правило, процедура окна обрабатывает \_ код уведомления для перетаскивания списка рассылки, определяя элемент под курсором и вырисуя значок вставки.</span><span class="sxs-lookup"><span data-stu-id="536dc-118">A window procedure typically processes the DL\_DRAGGING notification code by determining the item under the cursor and then drawing an insert icon.</span></span> <span data-ttu-id="536dc-119">Чтобы получить элемент под курсором, используйте функцию [**лбитемфромпт**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , указав **значение true** для параметра *баутоскролл* .</span><span class="sxs-lookup"><span data-stu-id="536dc-119">To retrieve the item under the cursor, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function, specifying **TRUE** for the *bAutoScroll* parameter.</span></span> <span data-ttu-id="536dc-120">Этот параметр приводит к периодической прокрутке окна списка перетаскивания, если курсор находится выше или ниже области клиента.</span><span class="sxs-lookup"><span data-stu-id="536dc-120">This option causes the drag list box to scroll periodically if the cursor is above or below its client area.</span></span> <span data-ttu-id="536dc-121">Чтобы нарисовать значок вставки, используйте функцию [**дравинсерт**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .</span><span class="sxs-lookup"><span data-stu-id="536dc-121">To draw the insert icon, use the [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="536dc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="536dc-122">Requirements</span></span>



| <span data-ttu-id="536dc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="536dc-123">Requirement</span></span> | <span data-ttu-id="536dc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="536dc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="536dc-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="536dc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="536dc-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="536dc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="536dc-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="536dc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="536dc-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="536dc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="536dc-129">Header</span><span class="sxs-lookup"><span data-stu-id="536dc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="536dc-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="536dc-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





