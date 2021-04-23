---
title: Сообщение WM_CHANGEUISTATE (Winuser. h)
description: Приложение отправляет \_ сообщение WM чанжеуистате, чтобы указать, что необходимо изменить состояние пользовательского интерфейса.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803838"
---
# <a name="wm_changeuistate-message"></a><span data-ttu-id="bb62e-104">\_Сообщение ЧАНЖЕУИСТАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="bb62e-104">WM\_CHANGEUISTATE message</span></span>

<span data-ttu-id="bb62e-105">Приложение отправляет сообщение **WM \_ чанжеуистате** , чтобы указать, что необходимо изменить состояние пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bb62e-105">An application sends the **WM\_CHANGEUISTATE** message to indicate that the UI state should be changed.</span></span>


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a><span data-ttu-id="bb62e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb62e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb62e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb62e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb62e-108">Слово нижнего порядка указывает выполняемое действие.</span><span class="sxs-lookup"><span data-stu-id="bb62e-108">The low-order word specifies the action to be taken.</span></span> <span data-ttu-id="bb62e-109">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bb62e-109">This member can be one of the following values.</span></span>



| <span data-ttu-id="bb62e-110">Значение</span><span class="sxs-lookup"><span data-stu-id="bb62e-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="bb62e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="bb62e-111">Meaning</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="bb62e-112"><dt>**Пользовательский интерфейс \_ ОЧИСТИТЬ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="bb62e-113">Флаги состояния пользовательского интерфейса, указанные в слове высокого порядка, должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="bb62e-113">The UI state flags specified by the high-order word should be cleared.</span></span><br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="bb62e-114"><dt>**Пользовательский интерфейс \_ ИНИЦИАЛИЗАЦИя**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="bb62e-115">Флаги состояния пользовательского интерфейса, заданные с помощью слова высокого порядка, должны быть изменены на основе последнего события ввода.</span><span class="sxs-lookup"><span data-stu-id="bb62e-115">The UI state flags specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="bb62e-116">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="bb62e-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="bb62e-117"><dt>**Пользовательский интерфейс \_ НАБОР**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="bb62e-118">Необходимо задать флаги состояния пользовательского интерфейса, указанные в слове с высоким порядком.</span><span class="sxs-lookup"><span data-stu-id="bb62e-118">The UI state flags specified by the high-order word should be set.</span></span><br/>                                                                      |



 

<span data-ttu-id="bb62e-119">Слово с высоким порядковым числом указывает, какие элементы состояния пользовательского интерфейса затрагиваются, или стиль элемента управления.</span><span class="sxs-lookup"><span data-stu-id="bb62e-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="bb62e-120">Этот элемент может иметь одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bb62e-120">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="bb62e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bb62e-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="bb62e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bb62e-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="bb62e-123"><dt>**Уисф \_ Активный**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="bb62e-124">Элемент управления должен быть нарисован в стиле, используемом для активных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="bb62e-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="bb62e-125"><dt>**Уисф \_ ХИДЕАКЦЕЛ**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="bb62e-126">Сочетания клавиш скрыты.</span><span class="sxs-lookup"><span data-stu-id="bb62e-126">Keyboard accelerators are hidden.</span></span><br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="bb62e-127"><dt>**Уисф \_ ХИДЕФОКУС**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="bb62e-128">Индикаторы фокуса скрыты.</span><span class="sxs-lookup"><span data-stu-id="bb62e-128">Focus indicators are hidden.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="bb62e-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb62e-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb62e-130">Этот параметр не используется и должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="bb62e-130">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb62e-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb62e-131">Remarks</span></span>

<span data-ttu-id="bb62e-132">Окно должно отправить это сообщение в себя или его родительский элемент, если он должен изменить элементы состояния пользовательского интерфейса всех окон в той же иерархии.</span><span class="sxs-lookup"><span data-stu-id="bb62e-132">A window should send this message to itself or its parent when it must change the UI state elements of all windows in the same hierarchy.</span></span> <span data-ttu-id="bb62e-133">Процедура окна должна позволить [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) обрабатывать это сообщение, чтобы все дерево окон соответствовало состоянию пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bb62e-133">The window procedure must let [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) process this message so that the entire window tree has a consistent UI state.</span></span> <span data-ttu-id="bb62e-134">Когда окно верхнего уровня получает сообщение **WM \_ чанжеуистате** , оно отправляет сообщение [**WM \_ упдатеуистате**](wm-updateuistate.md) с теми же параметрами, что и все дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="bb62e-134">When the top-level window receives the **WM\_CHANGEUISTATE** message, it sends a [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with the same parameters to all child windows.</span></span> <span data-ttu-id="bb62e-135">Когда система обрабатывает сообщение **WM \_ упдатеуистате** , она вносит изменения в состояние пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bb62e-135">When the system processes the **WM\_UPDATEUISTATE** message, it makes the change in the UI state.</span></span>

<span data-ttu-id="bb62e-136">Если слово с низким приоритетом *wParam* является ПОЛЬЗОВАТЕЛЬским интерфейсом \_ , система отправит сообщение [**WM \_ упдатеуистате**](wm-updateuistate.md) с состоянием пользовательского интерфейса на основе последнего события ввода.</span><span class="sxs-lookup"><span data-stu-id="bb62e-136">If the low-order word of *wParam* is UIS\_INITIALIZE, the system will send the [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with a UI state based on the last input event.</span></span> <span data-ttu-id="bb62e-137">Например, если последний ввод поступил от мыши, система скрывает подсказки клавиатуры. И, если последний ввод поступил с клавиатуры, система покажет подсказки клавиатуры. Если состояние, полученное в результате обработки **WM \_ чанжеуистате** , совпадает со старым состоянием, [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) не отправляет это сообщение.</span><span class="sxs-lookup"><span data-stu-id="bb62e-137">For example, if the last input came from the mouse, the system will hide the keyboard cues. And, if the last input came from the keyboard, the system will show the keyboard cues. If the state that results from processing **WM\_CHANGEUISTATE** is the same as the old state, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not send this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb62e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="bb62e-138">Requirements</span></span>



| <span data-ttu-id="bb62e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="bb62e-139">Requirement</span></span> | <span data-ttu-id="bb62e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="bb62e-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb62e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb62e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bb62e-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb62e-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bb62e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb62e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bb62e-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb62e-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb62e-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bb62e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb62e-146"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb62e-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb62e-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb62e-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb62e-148">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="bb62e-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="bb62e-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bb62e-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="bb62e-150">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bb62e-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bb62e-151">**WM \_ куерюистате**</span><span class="sxs-lookup"><span data-stu-id="bb62e-151">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="bb62e-152">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="bb62e-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb62e-153">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="bb62e-153">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

