---
title: Сообщение WM_CHARTOITEM (Winuser. h)
description: Отправляется списком со стилем ФУНТа \_ ванткэйбоардинпут в ответ на \_ сообщение WM char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Элементы управления Windows для WM_CHARTOITEM сообщений
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353915"
---
# <a name="wm_chartoitem-message"></a><span data-ttu-id="1ec65-104">\_Сообщение ЧАРТОИТЕМ WM</span><span class="sxs-lookup"><span data-stu-id="1ec65-104">WM\_CHARTOITEM message</span></span>

<span data-ttu-id="1ec65-105">Отправляется списком со стилем [**фунта \_ ванткэйбоардинпут**](list-box-styles.md) в ответ на сообщение [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="1ec65-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1ec65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec65-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ec65-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec65-108">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает код символа нажатой пользователем клавиши.</span><span class="sxs-lookup"><span data-stu-id="1ec65-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the character code of the key the user pressed.</span></span> <span data-ttu-id="1ec65-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает текущую позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="1ec65-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="1ec65-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ec65-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec65-111">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="1ec65-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec65-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec65-112">Return value</span></span>

<span data-ttu-id="1ec65-113">Возвращаемое значение указывает действие, выполненное приложением в ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="1ec65-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="1ec65-114">Возвращаемое значение-1 или-2 означает, что приложение обработало все аспекты выбора элемента и не требует дальнейших действий по списку.</span><span class="sxs-lookup"><span data-stu-id="1ec65-114">A return value of -1 or -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="1ec65-115">Возвращаемое значение 0 или больше Указывает отсчитываемый от нуля индекс элемента в списке и указывает, что поле списка должно выполнять действие по умолчанию для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="1ec65-115">A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec65-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ec65-116">Remarks</span></span>

<span data-ttu-id="1ec65-117">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="1ec65-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="1ec65-118">Это сообщение могут получить только рисуемые владельцем списки, у которых нет стиля [**фунта \_ хасстрингс**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec65-118">Only owner-drawn list boxes that do not have the [**LBS\_HASSTRINGS**](list-box-styles.md) style can receive this message.</span></span>

<span data-ttu-id="1ec65-119">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к **логическому** типу и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="1ec65-119">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="1ec65-120">Значение *\_ мсгресулт DWL* , заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1ec65-120">The *DWL\_MSGRESULT* value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec65-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec65-121">Requirements</span></span>



| <span data-ttu-id="1ec65-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec65-122">Requirement</span></span> | <span data-ttu-id="1ec65-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec65-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec65-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ec65-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec65-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ec65-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ec65-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ec65-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec65-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ec65-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ec65-128">Header</span><span class="sxs-lookup"><span data-stu-id="1ec65-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec65-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec65-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec65-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ec65-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ec65-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1ec65-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ec65-132">**WM \_ вкэйтоитем**</span><span class="sxs-lookup"><span data-stu-id="1ec65-132">**WM\_VKEYTOITEM**</span></span>](wm-vkeytoitem.md)
</dt> <dt>

<span data-ttu-id="1ec65-133">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="1ec65-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1ec65-134">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="1ec65-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="1ec65-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ec65-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1ec65-136">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ec65-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1ec65-137">**WM \_ char**</span><span class="sxs-lookup"><span data-stu-id="1ec65-137">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

