---
title: Сообщение EM_GETEDITSTYLEEX (RichEdit. h)
description: Извлекает текущие расширенные флаги стиля правки.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- Элементы управления Windows для EM_GETEDITSTYLEEX сообщений
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892037"
---
# <a name="em_geteditstyleex-message"></a><span data-ttu-id="12be0-104">\_Сообщение ЖЕТЕДИТСТИЛИКС EM</span><span class="sxs-lookup"><span data-stu-id="12be0-104">EM\_GETEDITSTYLEEX message</span></span>

<span data-ttu-id="12be0-105">Извлекает текущие расширенные флаги стиля правки.</span><span class="sxs-lookup"><span data-stu-id="12be0-105">Retrieves the current extended edit style flags.</span></span>


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a><span data-ttu-id="12be0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12be0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12be0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12be0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12be0-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="12be0-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="12be0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12be0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12be0-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="12be0-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12be0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12be0-111">Return value</span></span>

<span data-ttu-id="12be0-112">Возвращает расширенные флаги стиля редактирования, которые могут включать одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="12be0-112">Returns the extended edit style flags, which can include one or more of the following values.</span></span>



| <span data-ttu-id="12be0-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="12be0-113">Return code</span></span>                                                                                                | <span data-ttu-id="12be0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="12be0-114">Description</span></span>                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12be0-115"><dt>**SES \_ ex \_ хандлефриендлюрл**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-115"><dt>**SES\_EX\_HANDLEFRIENDLYURL**</dt></span></span> </dl>  | <span data-ttu-id="12be0-116">Отображать ссылки на дружественные имена с одним и тем же цветом текста и подчеркиванием в качестве автоматических связей при условии, что временное форматирование не используется или использует автоцвет текста (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="12be0-116">Display friendly name links with the same text color and underlining as automatic links, provided that temporary formatting isn t used or uses text autocolor (default: 0).</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="12be0-117"><dt>**SES \_ ex \_ Мультисенсорная**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-117"><dt>**SES\_EX\_MULTITOUCH**</dt></span></span> </dl>         | <span data-ttu-id="12be0-118">Включите поддержку сенсорного ввода в расширенном редактировании.</span><span class="sxs-lookup"><span data-stu-id="12be0-118">Enable touch support in Rich Edit.</span></span> <span data-ttu-id="12be0-119">Это включает выделение, размещение курсора и вызов контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="12be0-119">This includes selection, caret placement, and context-menu invocation.</span></span> <span data-ttu-id="12be0-120">Если этот флаг не установлен, касание эмулируется командами мыши, которые не принимают особенности сенсорного режима (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="12be0-120">When this flag is not set, touch is emulated by mouse commands, which do not take touch-mode specifics into account (default: 0).</span></span> <br/>      |
| <dl> <span data-ttu-id="12be0-121"><dt>**SES \_ ex \_ ноацетатеселектион**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-121"><dt>**SES\_EX\_NOACETATESELECTION**</dt></span></span> </dl> | <span data-ttu-id="12be0-122">Отображать выделенный текст, используя классический текст и цвета фона, а не фоновый цвет ацетате (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="12be0-122">Display selected text using classic Windows selection text and background colors instead of background acetate color (default: 0).</span></span> <br/>                                                                                                               |
| <dl> <span data-ttu-id="12be0-123"><dt>**SES \_ EX ( \_ нематематический)**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-123"><dt>**SES\_EX\_NOMATH**</dt></span></span> </dl>             | <span data-ttu-id="12be0-124">Отключить вставку математических зон (по умолчанию: 1).</span><span class="sxs-lookup"><span data-stu-id="12be0-124">Disable insertion of math zones (default: 1).</span></span> <span data-ttu-id="12be0-125">Чтобы включить редактирование и отображение математических выражений, отправьте сообщение [**EM \_ сетедитстиликс**](em-seteditstyleex.md) с параметром *wParam* Set в значение 0, а для параметра *lParam* — значение **SES \_ ex \_ Math**.</span><span class="sxs-lookup"><span data-stu-id="12be0-125">To enable math editing and display, send the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message with *wParam* set to 0, and *lParam* set to **SES\_EX\_NOMATH**.</span></span> <br/>                              |
| <dl> <span data-ttu-id="12be0-126"><dt>**\_важные SES \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-126"><dt>**SES\_EX\_NOTABLE**</dt></span></span> </dl>            | <span data-ttu-id="12be0-127">Отключить вставку таблиц.</span><span class="sxs-lookup"><span data-stu-id="12be0-127">Disable insertion of tables.</span></span> <span data-ttu-id="12be0-128">Сообщение [**EM \_ инсерттабле**](em-inserttable.md) возвращает значение **E \_ Fail** , а таблицы RTF пропускаются (значение по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="12be0-128">The [**EM\_INSERTTABLE**](em-inserttable.md) message returns **E\_FAIL** and RTF tables are skipped (default: 0).</span></span> <br/>                                                                                                  |
| <dl> <span data-ttu-id="12be0-129"><dt>**SES \_ ex \_ усесинглелине**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-129"><dt>**SES\_EX\_USESINGLELINE**</dt></span></span> </dl>      | <span data-ttu-id="12be0-130">Включение многострочного элемента управления в качестве однострочного элемента управления с возможностью прокрутки по вертикали, если высота одной строки превышает высоту окна (значение по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="12be0-130">Enable a multiline control to act like a single-line control with the ability to scroll vertically when the single-line height is greater than the window height (default: 0).</span></span> <br/>                                                                   |
| <dl> <span data-ttu-id="12be0-131"><dt>**SES \_ хидетемпформат**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-131"><dt>**SES\_HIDETEMPFORMAT**</dt></span></span> </dl>         | <span data-ttu-id="12be0-132">Скрытие временного форматирования, созданного при вызове [**итекстфонт. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) с **томапплитмп**.</span><span class="sxs-lookup"><span data-stu-id="12be0-132">Hide temporary formatting that is created when [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) is called with **tomApplyTmp**.</span></span> <span data-ttu-id="12be0-133">Например, такое форматирование используется в средствах проверки орфографии для вывода волнистой подчеркивания в словах с ошибками.</span><span class="sxs-lookup"><span data-stu-id="12be0-133">For example, such formatting is used by spell checkers to display a squiggly underline under possibly misspelled words.</span></span><br/> |
| <dl> <span data-ttu-id="12be0-134"><dt>**SES \_ ex \_ усемаусевпарам**</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-134"><dt>**SES\_EX\_USEMOUSEWPARAM**</dt></span></span> </dl>     | <span data-ttu-id="12be0-135">Используйте параметр *wParam* при обработке сообщения [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) и не вызывайте [**жетасинккэйстате**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="12be0-135">Use *wParam* when handling the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message and do not call [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="12be0-136">Требования</span><span class="sxs-lookup"><span data-stu-id="12be0-136">Requirements</span></span>



| <span data-ttu-id="12be0-137">Требование</span><span class="sxs-lookup"><span data-stu-id="12be0-137">Requirement</span></span> | <span data-ttu-id="12be0-138">Значение</span><span class="sxs-lookup"><span data-stu-id="12be0-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12be0-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12be0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="12be0-140">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="12be0-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="12be0-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12be0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="12be0-142">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="12be0-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12be0-143">Header</span><span class="sxs-lookup"><span data-stu-id="12be0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="12be0-144"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="12be0-144"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12be0-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12be0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12be0-146">**EM \_ сетедитстиликс**</span><span class="sxs-lookup"><span data-stu-id="12be0-146">**EM\_SETEDITSTYLEEX**</span></span>](em-seteditstyleex.md)
</dt> </dl>

 

