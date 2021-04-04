---
title: Сообщение WM_UPDATEUISTATE (Winuser. h)
description: Приложение отправляет \_ сообщение WM упдатеуистате, чтобы изменить состояние пользовательского интерфейса для указанного окна и всех его дочерних окон.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137747"
---
# <a name="wm_updateuistate-message"></a><span data-ttu-id="1bfcf-104">\_Сообщение УПДАТЕУИСТАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="1bfcf-104">WM\_UPDATEUISTATE message</span></span>

<span data-ttu-id="1bfcf-105">Приложение отправляет сообщение **WM \_ упдатеуистате** , чтобы изменить состояние пользовательского интерфейса для указанного окна и всех его дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-105">An application sends the **WM\_UPDATEUISTATE** message to change the UI state for the specified window and all its child windows.</span></span>


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a><span data-ttu-id="1bfcf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bfcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bfcf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1bfcf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bfcf-108">Слово нижнего порядка указывает выполняемое действие.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-108">The low-order word specifies the action to be performed.</span></span> <span data-ttu-id="1bfcf-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1bfcf-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1bfcf-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="1bfcf-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1bfcf-111">Meaning</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="1bfcf-112"><dt>**Пользовательский интерфейс \_ ОЧИСТИТЬ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcf-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="1bfcf-113">Элемент состояния пользовательского интерфейса, заданный с помощью слова высокого порядка, должен быть скрытым.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-113">The UI state element specified by the high-order word should be hidden.</span></span><br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="1bfcf-114"><dt>**Пользовательский интерфейс \_ ИНИЦИАЛИЗАЦИя**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcf-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="1bfcf-115">Элемент состояния пользовательского интерфейса, заданный с помощью слова высокого порядка, должен быть изменен на основе последнего события ввода.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-115">The UI state element specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="1bfcf-116">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="1bfcf-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="1bfcf-117"><dt>**Пользовательский интерфейс \_ НАБОР**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcf-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="1bfcf-118">Элемент состояния пользовательского интерфейса, заданный с помощью слова высокого порядка, должен быть видимым.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-118">The UI state element specified by the high-order word should be visible.</span></span><br/>                                                                  |



 

<span data-ttu-id="1bfcf-119">Слово с высоким порядковым числом указывает, какие элементы состояния пользовательского интерфейса затрагиваются, или стиль элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="1bfcf-120">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1bfcf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1bfcf-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="1bfcf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1bfcf-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="1bfcf-123"><dt>**Уисф \_ Активный**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcf-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="1bfcf-124">Элемент управления должен быть нарисован в стиле, используемом для активных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="1bfcf-125"><dt>**Уисф \_ ХИДЕАКЦЕЛ**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcf-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="1bfcf-126">Сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-126">Keyboard accelerators.</span></span><br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="1bfcf-127"><dt>**Уисф \_ ХИДЕФОКУС**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcf-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="1bfcf-128">Индикаторы фокуса.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-128">Focus indicators.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="1bfcf-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bfcf-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bfcf-130">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bfcf-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bfcf-131">Remarks</span></span>

<span data-ttu-id="1bfcf-132">Окно должно отправить это сообщение, чтобы изменить состояние пользовательского интерфейса всех его дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-132">A window should send this message to change the UI state of all its child windows.</span></span> <span data-ttu-id="1bfcf-133">В отличие от сообщения [**WM \_ чанжеуистате**](wm-changeuistate.md) , которое является уведомлением, когда [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) обрабатывает сообщение **WM \_ упдатеуистате** , оно изменяет состояние пользовательского интерфейса и распространяет изменения во все дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-133">In contrast to the [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message, which is a notification, when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processes the **WM\_UPDATEUISTATE** message it changes the UI state and propagates the changes to all child windows.</span></span>

<span data-ttu-id="1bfcf-134">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) обновляет состояние пользовательского интерфейса в соответствии со значением параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1bfcf-134">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function updates the UI state according to the *wParam* value.</span></span> <span data-ttu-id="1bfcf-135">Если состояние пользовательского интерфейса изменено, функция отправляет сообщение всем непосредственным дочерним окнам.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-135">If the UI state is modified, the function sends the message to all the immediate child windows.</span></span> <span data-ttu-id="1bfcf-136">**Дефвиндовпрок** также отправляет это сообщение, когда получает сообщение [**WM \_ чанжеуистате**](wm-changeuistate.md) , уведомляющее систему о том, что дочернее окно планирует изменить состояние пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1bfcf-136">**DefWindowProc** also sends this message when it receives a [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message notifying the system that a child window intends to modify the UI state.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bfcf-137">Требования</span><span class="sxs-lookup"><span data-stu-id="1bfcf-137">Requirements</span></span>



| <span data-ttu-id="1bfcf-138">Требование</span><span class="sxs-lookup"><span data-stu-id="1bfcf-138">Requirement</span></span> | <span data-ttu-id="1bfcf-139">Значение</span><span class="sxs-lookup"><span data-stu-id="1bfcf-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfcf-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1bfcf-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1bfcf-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1bfcf-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1bfcf-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1bfcf-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1bfcf-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1bfcf-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1bfcf-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1bfcf-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bfcf-145"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcf-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bfcf-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bfcf-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bfcf-147">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1bfcf-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bfcf-148">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="1bfcf-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1bfcf-149">**WM \_ чанжеуистате**</span><span class="sxs-lookup"><span data-stu-id="1bfcf-149">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="1bfcf-150">**WM \_ куерюистате**</span><span class="sxs-lookup"><span data-stu-id="1bfcf-150">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="1bfcf-151">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1bfcf-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1bfcf-152">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="1bfcf-152">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

