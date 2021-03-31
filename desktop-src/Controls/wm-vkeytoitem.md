---
title: Сообщение WM_VKEYTOITEM (Winuser. h)
description: Посылается списком с \_ ванткэйбоардинпут в качестве владельца в ответ на \_ сообщение WM KeyDown.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- Элементы управления Windows для WM_VKEYTOITEM сообщений
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "104351732"
---
# <a name="wm_vkeytoitem-message"></a><span data-ttu-id="fb9e1-104">\_Сообщение ВКЭЙТОИТЕМ WM</span><span class="sxs-lookup"><span data-stu-id="fb9e1-104">WM\_VKEYTOITEM message</span></span>

<span data-ttu-id="fb9e1-105">Посылается списком с [**\_ ванткэйбоардинпут**](list-box-styles.md) в качестве владельца в ответ на сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="fb9e1-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span>


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fb9e1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb9e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb9e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb9e1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb9e1-108">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает код виртуального ключа нажатой пользователем клавиши.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the virtual-key code of the key the user pressed.</span></span> <span data-ttu-id="fb9e1-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает текущую позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="fb9e1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb9e1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb9e1-111">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb9e1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb9e1-112">Return value</span></span>

<span data-ttu-id="fb9e1-113">Возвращаемое значение указывает действие, выполненное приложением в ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="fb9e1-114">Возвращаемое значение, равное-2, указывает, что приложение обработало все аспекты выбора элемента и не требует дальнейших действий, выполняемых списком.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-114">A return value of -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="fb9e1-115">(См. раздел Примечания.) Возвращаемое значение, равное-1, указывает, что окно списка должно выполнять действие по умолчанию в ответ на нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-115">(See Remarks.) A return value of -1 indicates that the list box should perform the default action in response to the keystroke.</span></span> <span data-ttu-id="fb9e1-116">Возвращаемое значение 0 или выше указывает индекс элемента в списке и указывает, что поле списка должно выполнять действие по умолчанию для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-116">A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb9e1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb9e1-117">Remarks</span></span>

<span data-ttu-id="fb9e1-118">Возвращаемое значение-2 допустимо только для ключей, которые не преобразуются в символы в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="fb9e1-118">A return value of -2 is valid only for keys that are not translated into characters by the list box control.</span></span> <span data-ttu-id="fb9e1-119">Если сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) преобразуется в сообщение [**WM \_ char**](/windows/desktop/inputdev/wm-char) и приложение обрабатывает сообщение **WM \_ вкэйтоитем** , созданное в результате нажатия клавиши, то в поле со списком игнорируется возвращаемое значение и выполняется обработка по умолчанию для этого символа.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-119">If the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message translates to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message and the application processes the **WM\_VKEYTOITEM** message generated as a result of the key press, the list box ignores the return value and does the default processing for that character).</span></span> <span data-ttu-id="fb9e1-120">**WM \_ Сообщения KEYDOWN** , созданные такими ключами, как VK \_ Up, VK \_ Down, VK \_ Next и VK \_ Previous, не преобразуются в сообщения **WM \_ char** .</span><span class="sxs-lookup"><span data-stu-id="fb9e1-120">**WM\_KEYDOWN** messages generated by keys such as VK\_UP, VK\_DOWN, VK\_NEXT, and VK\_PREVIOUS are not translated to **WM\_CHAR** messages.</span></span> <span data-ttu-id="fb9e1-121">В таких случаях перехват сообщения **\_ вкэйтоитем WM** и возврат-2 не позволит списку выполнить обработку по умолчанию для этого ключа.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-121">In such cases, trapping the **WM\_VKEYTOITEM** message and returning -2 prevents the list box from doing the default processing for that key.</span></span>

<span data-ttu-id="fb9e1-122">Для перехвата ключей, создающих сообщение типа char и обрабатывающих специальную обработку, приложение должно создать подкласс списка, захватывать сообщения [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) и [**WM \_ char**](/windows/desktop/inputdev/wm-char) , а также обрабатывать сообщения соответствующим образом в процедуре подкласса.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-122">To trap keys that generate a char message and do special processing, the application must subclass the list box, trap both the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages, and process the messages appropriately in the subclass procedure.</span></span>

<span data-ttu-id="fb9e1-123">Предыдущие примечания применяются к обычным спискам, созданным с использованием стиля [**фунта \_ ванткэйбоардинпут**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fb9e1-123">The preceding remarks apply to regular list boxes that are created with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style.</span></span> <span data-ttu-id="fb9e1-124">Если окно списка является рисуемым владельцем, приложение должно обработать сообщение [**WM \_ чартоитем**](wm-chartoitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fb9e1-124">If the list box is owner-drawn, the application must process the [**WM\_CHARTOITEM**](wm-chartoitem.md) message.</span></span>

<span data-ttu-id="fb9e1-125">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="fb9e1-126">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к **логическому** типу и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-126">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="fb9e1-127">\_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fb9e1-127">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb9e1-128">Требования</span><span class="sxs-lookup"><span data-stu-id="fb9e1-128">Requirements</span></span>



| <span data-ttu-id="fb9e1-129">Требование</span><span class="sxs-lookup"><span data-stu-id="fb9e1-129">Requirement</span></span> | <span data-ttu-id="fb9e1-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fb9e1-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9e1-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb9e1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9e1-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb9e1-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fb9e1-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb9e1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9e1-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb9e1-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb9e1-135">Header</span><span class="sxs-lookup"><span data-stu-id="fb9e1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb9e1-136"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb9e1-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb9e1-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb9e1-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb9e1-138">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fb9e1-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fb9e1-139">**WM \_ чартоитем**</span><span class="sxs-lookup"><span data-stu-id="fb9e1-139">**WM\_CHARTOITEM**</span></span>](wm-chartoitem.md)
</dt> <dt>

<span data-ttu-id="fb9e1-140">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="fb9e1-140">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="fb9e1-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb9e1-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fb9e1-142">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb9e1-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fb9e1-143">**WM \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="fb9e1-143">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

