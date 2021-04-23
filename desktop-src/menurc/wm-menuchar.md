---
title: Сообщение WM_MENUCHAR (Winuser. h)
description: Посылается, когда меню активно, и пользователь нажимает клавишу, которая не соответствует ни одной из назначенных клавиш или сочетанию клавиш. Это сообщение отправляется в окно, которому принадлежит меню.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804024"
---
# <a name="wm_menuchar-message"></a><span data-ttu-id="f2de4-105">\_Сообщение МЕНУЧАР WM</span><span class="sxs-lookup"><span data-stu-id="f2de4-105">WM\_MENUCHAR message</span></span>

<span data-ttu-id="f2de4-106">Посылается, когда меню активно, и пользователь нажимает клавишу, которая не соответствует ни одной из назначенных клавиш или сочетанию клавиш.</span><span class="sxs-lookup"><span data-stu-id="f2de4-106">Sent when a menu is active and the user presses a key that does not correspond to any mnemonic or accelerator key.</span></span> <span data-ttu-id="f2de4-107">Это сообщение отправляется в окно, которому принадлежит меню.</span><span class="sxs-lookup"><span data-stu-id="f2de4-107">This message is sent to the window that owns the menu.</span></span>


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a><span data-ttu-id="f2de4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2de4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2de4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2de4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2de4-110">Слово нижнего порядка указывает код символа, соответствующий ключу, который пользователь нажал.</span><span class="sxs-lookup"><span data-stu-id="f2de4-110">The low-order word specifies the character code that corresponds to the key the user pressed.</span></span>

<span data-ttu-id="f2de4-111">Слово в высоком порядке указывает тип активного меню.</span><span class="sxs-lookup"><span data-stu-id="f2de4-111">The high-order word specifies the active menu type.</span></span> <span data-ttu-id="f2de4-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="f2de4-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f2de4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f2de4-113">Value</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="f2de4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f2de4-114">Meaning</span></span>                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="f2de4-115"><dt>**MF \_ Всплывающее окно**</dt> <dt>0x00000010L</dt></span><span class="sxs-lookup"><span data-stu-id="f2de4-115"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>       | <span data-ttu-id="f2de4-116">Раскрывающееся меню, подменю или контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="f2de4-116">A drop-down menu, submenu, or shortcut menu.</span></span><br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="f2de4-117"><dt>**MF \_ СИСМЕНУ**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="f2de4-117"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl> | <span data-ttu-id="f2de4-118">Меню окно.</span><span class="sxs-lookup"><span data-stu-id="f2de4-118">The window menu.</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="f2de4-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2de4-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2de4-120">Маркер активного меню.</span><span class="sxs-lookup"><span data-stu-id="f2de4-120">A handle to the active menu.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2de4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2de4-121">Return value</span></span>

<span data-ttu-id="f2de4-122">Приложение, обрабатывающее это сообщение, должно возвращать одно из следующих значений в слове возвращаемого значения в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="f2de4-122">An application that processes this message should return one of the following values in the high-order word of the return value.</span></span>



| <span data-ttu-id="f2de4-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f2de4-123">Return code/value</span></span>                                                                                                                                  | <span data-ttu-id="f2de4-124">Описание</span><span class="sxs-lookup"><span data-stu-id="f2de4-124">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2de4-125"><dt>**МНК \_ ЗАКРЫТЬ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f2de4-125"><dt>**MNC\_CLOSE**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="f2de4-126">Информирует систему о том, что необходимо закрыть активное меню.</span><span class="sxs-lookup"><span data-stu-id="f2de4-126">Informs the system that it should close the active menu.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="f2de4-127"><dt>**МНК \_ ВЫПОЛНЕНИЕ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f2de4-127"><dt>**MNC\_EXECUTE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="f2de4-128">Информирует систему о том, что необходимо выбрать элемент, указанный в младшем слове возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f2de4-128">Informs the system that it should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="f2de4-129">Окно-владелец получает сообщение [**\_ командной строки WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="f2de4-129">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span><br/> |
| <dl> <span data-ttu-id="f2de4-130"><dt>**МНК \_ ИГНОРИРОВАТЬ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2de4-130"><dt>**MNC\_IGNORE**</dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="f2de4-131">Информирует систему о том, что необходимо отбросить символ, который пользователь нажал, и создать короткий звуковой сигнал на системном докладчике.</span><span class="sxs-lookup"><span data-stu-id="f2de4-131">Informs the system that it should discard the character the user pressed and create a short beep on the system speaker.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f2de4-132"><dt>**МНК \_ Выберите**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f2de4-132"><dt>**MNC\_SELECT**</dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="f2de4-133">Информирует систему о том, что необходимо выбрать элемент, указанный в младшем слове возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f2de4-133">Informs the system that it should select the item specified in the low-order word of the return value.</span></span> <br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f2de4-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2de4-134">Remarks</span></span>

<span data-ttu-id="f2de4-135">Слово низкого порядка пропускается, если слово в высоком порядке содержит 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="f2de4-135">The low-order word is ignored if the high-order word contains 0 or 1.</span></span>

<span data-ttu-id="f2de4-136">Приложение должно обработать это сообщение, если для выбора пункта меню, отображающего точечный рисунок, используется ускоритель.</span><span class="sxs-lookup"><span data-stu-id="f2de4-136">An application should process this message when an accelerator is used to select a menu item that displays a bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2de4-137">Требования</span><span class="sxs-lookup"><span data-stu-id="f2de4-137">Requirements</span></span>



| <span data-ttu-id="f2de4-138">Требование</span><span class="sxs-lookup"><span data-stu-id="f2de4-138">Requirement</span></span> | <span data-ttu-id="f2de4-139">Значение</span><span class="sxs-lookup"><span data-stu-id="f2de4-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2de4-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2de4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f2de4-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2de4-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2de4-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2de4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f2de4-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2de4-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2de4-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f2de4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2de4-145"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2de4-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2de4-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2de4-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2de4-147">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f2de4-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="f2de4-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2de4-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f2de4-149">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2de4-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f2de4-150">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f2de4-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2de4-151">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="f2de4-151">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

