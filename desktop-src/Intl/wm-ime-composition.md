---
description: Отправляется в приложение, когда редактор IME изменяет состояние композиции в результате нажатия клавиши. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Сообщение WM_IME_COMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999684"
---
# <a name="wm_ime_composition-message"></a><span data-ttu-id="4f230-104">\_ \_ Сообщение композиции IME WM</span><span class="sxs-lookup"><span data-stu-id="4f230-104">WM\_IME\_COMPOSITION message</span></span>

<span data-ttu-id="4f230-105">Отправляется в приложение, когда редактор IME изменяет состояние композиции в результате нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="4f230-105">Sent to an application when the IME changes composition status as a result of a keystroke.</span></span> <span data-ttu-id="4f230-106">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4f230-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a><span data-ttu-id="4f230-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f230-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f230-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="4f230-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4f230-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="4f230-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="4f230-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f230-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f230-111">Символ DBCS, представляющий Последнее изменение в строке композиции.</span><span class="sxs-lookup"><span data-stu-id="4f230-111">DBCS character representing the latest change to the composition string.</span></span>

</dd> <dt>

<span data-ttu-id="4f230-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f230-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f230-113">Значение, указывающее, как изменилась строка композиции или символ.</span><span class="sxs-lookup"><span data-stu-id="4f230-113">Value specifying how the composition string or character changed.</span></span> <span data-ttu-id="4f230-114">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4f230-114">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="4f230-115">Дополнительные сведения об этих значениях см. в разделе [строковые значения композиции IME](ime-composition-string-values.md).</span><span class="sxs-lookup"><span data-stu-id="4f230-115">For more information about these values, see [IME Composition String Values](ime-composition-string-values.md).</span></span>

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

<span data-ttu-id="4f230-116">**\_КОМПАТТР GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-116">**GCS\_COMPATTR**</span></span>
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

<span data-ttu-id="4f230-117">**\_КОМПКЛАУСЕ GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-117">**GCS\_COMPCLAUSE**</span></span>
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

<span data-ttu-id="4f230-118">**\_КОМПРЕАДСТР GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-118">**GCS\_COMPREADSTR**</span></span>
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

<span data-ttu-id="4f230-119">**\_КОМПРЕАДАТТР GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-119">**GCS\_COMPREADATTR**</span></span>
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

<span data-ttu-id="4f230-120">**\_КОМПРЕАДКЛАУСЕ GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-120">**GCS\_COMPREADCLAUSE**</span></span>
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

<span data-ttu-id="4f230-121">**\_КОМПСТР GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-121">**GCS\_COMPSTR**</span></span>
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

<span data-ttu-id="4f230-122">**\_КУРСОРПОС GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-122">**GCS\_CURSORPOS**</span></span>
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

<span data-ttu-id="4f230-123">**\_ДЕЛТАСТАРТ GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-123">**GCS\_DELTASTART**</span></span>
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

<span data-ttu-id="4f230-124">**\_РЕСУЛТКЛАУСЕ GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-124">**GCS\_RESULTCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

<span data-ttu-id="4f230-125">**\_РЕСУЛТРЕАДКЛАУСЕ GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-125">**GCS\_RESULTREADCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

<span data-ttu-id="4f230-126">**\_РЕСУЛТРЕАДСТР GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-126">**GCS\_RESULTREADSTR**</span></span>
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

<span data-ttu-id="4f230-127">**\_РЕСУЛТСТР GC**</span><span class="sxs-lookup"><span data-stu-id="4f230-127">**GCS\_RESULTSTR**</span></span>
</dt> </dl>

<span data-ttu-id="4f230-128">Параметр *lParam* также может иметь одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4f230-128">The *lParam* parameter can also have one or more of the following values.</span></span>



| <span data-ttu-id="4f230-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4f230-129">Value</span></span>                                                                                                                                                            | <span data-ttu-id="4f230-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4f230-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <span data-ttu-id="4f230-131"><dt>**CS \_ инсертчар**</dt></span><span class="sxs-lookup"><span data-stu-id="4f230-131"><dt>**CS\_INSERTCHAR**</dt></span></span> </dl>    | <span data-ttu-id="4f230-132">Вставка символа композиции *wParam* в текущей точке вставки.</span><span class="sxs-lookup"><span data-stu-id="4f230-132">Insert the *wParam* composition character at the current insertion point.</span></span> <span data-ttu-id="4f230-133">Приложение должно отображать символ композиции, если он обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="4f230-133">An application should display the composition character if it processes this message.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <span data-ttu-id="4f230-134"><dt>**CS \_ номовекарет**</dt></span><span class="sxs-lookup"><span data-stu-id="4f230-134"><dt>**CS\_NOMOVECARET**</dt></span></span> </dl> | <span data-ttu-id="4f230-135">Не перемещайте положение курсора в результате обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f230-135">Do not move the caret position as a result of processing the message.</span></span> <span data-ttu-id="4f230-136">Например, если редактор IME задает сочетание CS \_ инсертчар и CS \_ номовекарет, приложение должно вставить указанный символ в текущую положение курсора, но не должен перемещать курсор к следующей позиции.</span><span class="sxs-lookup"><span data-stu-id="4f230-136">For example, if an IME specifies a combination of CS\_INSERTCHAR and CS\_NOMOVECARET, the application should insert the specified character at the current caret position but should not move the caret to the next position.</span></span> <span data-ttu-id="4f230-137">Последующее \_ сообщение композиции редактора WM IME \_ с GC \_ ресултстр заменит этот символ.</span><span class="sxs-lookup"><span data-stu-id="4f230-137">A subsequent WM\_IME\_COMPOSITION message with GCS\_RESULTSTR will replace this character.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f230-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f230-138">Return value</span></span>

<span data-ttu-id="4f230-139">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4f230-139">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f230-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f230-140">Remarks</span></span>

<span data-ttu-id="4f230-141">Приложение должно обработать это сообщение, если оно отображает сами символы композиции.</span><span class="sxs-lookup"><span data-stu-id="4f230-141">An application should process this message if it displays composition characters itself.</span></span> <span data-ttu-id="4f230-142">В противном случае он должен отправить сообщение в окно IME.</span><span class="sxs-lookup"><span data-stu-id="4f230-142">Otherwise, it should send the message to the IME window.</span></span>

<span data-ttu-id="4f230-143">Если приложение создало окно IME, оно должно передать это сообщение в это окно.</span><span class="sxs-lookup"><span data-stu-id="4f230-143">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="4f230-144">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  обрабатывает это сообщение, передавая его в окно IME по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4f230-144">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span> <span data-ttu-id="4f230-145">Окно IME обрабатывает это сообщение, обновляя его внешний вид в зависимости от указанного флага изменения.</span><span class="sxs-lookup"><span data-stu-id="4f230-145">The IME window processes this message by updating its appearance based on the change flag specified.</span></span> <span data-ttu-id="4f230-146">Приложение может вызвать [**иммжеткомпоситионстринг**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) для получения нового состояния композиции.</span><span class="sxs-lookup"><span data-stu-id="4f230-146">An application can call [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) to retrieve the new composition status.</span></span>

<span data-ttu-id="4f230-147">Если ни одно из значений глобальных каталогов \_ не задано, сообщение указывает, что Текущая композиция отменена, и приложения, которые рисуют строку композиции, должны удалить строку.</span><span class="sxs-lookup"><span data-stu-id="4f230-147">If none of the GCS\_ values are set, the message indicates that the current composition has been canceled and applications that draw the composition string should delete the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f230-148">Требования</span><span class="sxs-lookup"><span data-stu-id="4f230-148">Requirements</span></span>



| <span data-ttu-id="4f230-149">Требование</span><span class="sxs-lookup"><span data-stu-id="4f230-149">Requirement</span></span> | <span data-ttu-id="4f230-150">Значение</span><span class="sxs-lookup"><span data-stu-id="4f230-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f230-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f230-151">Minimum supported client</span></span><br/> | <span data-ttu-id="4f230-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f230-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4f230-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f230-153">Minimum supported server</span></span><br/> | <span data-ttu-id="4f230-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f230-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4f230-155">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4f230-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f230-156"><dt>Winuser. h (включает Windows. h); </dt> <dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f230-156"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f230-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f230-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f230-158">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="4f230-158">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4f230-159">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="4f230-159">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="4f230-160">**иммжеткомпоситионстринг**</span><span class="sxs-lookup"><span data-stu-id="4f230-160">**ImmGetCompositionString**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
