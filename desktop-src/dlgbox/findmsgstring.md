---
title: Сообщение ФИНДМСГСТРИНГ (Коммдлг. h)
description: Диалоговое окно Поиск или замена отправляет зарегистрированное сообщение ФИНДМСГСТРИНГ в процедуру окна своего окна-владельца, когда пользователь нажимает кнопку Найти далее, заменить или заменить все или закрывает диалоговое окно.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Диалоговые окна сообщения ФИНДМСГСТРИНГ
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535261"
---
# <a name="findmsgstring-message"></a><span data-ttu-id="59a32-104">Сообщение ФИНДМСГСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="59a32-104">FINDMSGSTRING message</span></span>

<span data-ttu-id="59a32-105">Диалоговое окно **Поиск** или **Замена** отправляет зарегистрированное сообщение **финдмсгстринг** в процедуру окна своего окна-владельца, когда пользователь нажимает кнопку **Найти далее**, **заменить** или **заменить все** или закрывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="59a32-105">A **Find** or **Replace** dialog box sends the **FINDMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Find Next**, **Replace**, or **Replace All** button, or closes the dialog box.</span></span>


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a><span data-ttu-id="59a32-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59a32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a32-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59a32-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59a32-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="59a32-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59a32-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59a32-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59a32-110">Указатель на структуру [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .</span><span class="sxs-lookup"><span data-stu-id="59a32-110">A pointer to a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span> <span data-ttu-id="59a32-111">Члены этой структуры содержат последние введенные пользователем данные, включая строку для поиска, строку замены (если таковые имеются) и параметры поиска и замены.</span><span class="sxs-lookup"><span data-stu-id="59a32-111">The members of this structure contain the latest user input, including the string to search for, the replacement string (if any) and the search-and-replacement options.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a32-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59a32-112">Return value</span></span>

<span data-ttu-id="59a32-113">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="59a32-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a32-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59a32-114">Remarks</span></span>

<span data-ttu-id="59a32-115">Чтобы получить идентификатор сообщения, отправленного диалоговым окном, необходимо указать константу **финдмсгстринг** в вызове функции [**регистервиндовмессаже**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) .</span><span class="sxs-lookup"><span data-stu-id="59a32-115">You must specify the **FINDMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="59a32-116">При создании диалогового окна используйте элемент **хвндовнер** структуры [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) для указания окна, получающего сообщения **финдмсгстринг** .</span><span class="sxs-lookup"><span data-stu-id="59a32-116">When you create the dialog box, use the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to identify the window to receive **FINDMSGSTRING** messages.</span></span>

<span data-ttu-id="59a32-117">Элемент **flags** структуры [**финдреплаце**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) включает один из следующих флагов для указания события, вызвавшего сообщение.</span><span class="sxs-lookup"><span data-stu-id="59a32-117">The **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="59a32-118">Flag</span><span class="sxs-lookup"><span data-stu-id="59a32-118">Flag</span></span>                            | <span data-ttu-id="59a32-119">Значение</span><span class="sxs-lookup"><span data-stu-id="59a32-119">Meaning</span></span>                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a32-120">**Fr \_ ДИАЛОГТЕРМ** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="59a32-120">**FR\_DIALOGTERM** (0x00000040)</span></span> | <span data-ttu-id="59a32-121">Диалоговое окно закрывается.</span><span class="sxs-lookup"><span data-stu-id="59a32-121">The dialog box is closing.</span></span> <span data-ttu-id="59a32-122">После того как окно-владелец обработает это сообщение, маркер диалогового окна становится недействительным.</span><span class="sxs-lookup"><span data-stu-id="59a32-122">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="59a32-123">**Fr \_ FINDNEXT** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="59a32-123">**FR\_FINDNEXT** (0x00000008)</span></span>   | <span data-ttu-id="59a32-124">Пользователь нащелкнул кнопку " **Найти далее** " в диалоговом окне " **найти** или **заменить** ".</span><span class="sxs-lookup"><span data-stu-id="59a32-124">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="59a32-125">Член **лпстрфиндвхат** указывает строку для поиска.</span><span class="sxs-lookup"><span data-stu-id="59a32-125">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="59a32-126">**Fr \_ Replace** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="59a32-126">**FR\_REPLACE** (0x00000010)</span></span>    | <span data-ttu-id="59a32-127">Пользователь нащелкнул кнопку **заменить** в диалоговом окне **заменить** .</span><span class="sxs-lookup"><span data-stu-id="59a32-127">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="59a32-128">Член **лпстрфиндвхат** указывает строку для замены, а член **лпстрреплацевис** указывает замещающую строку.</span><span class="sxs-lookup"><span data-stu-id="59a32-128">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="59a32-129">**Fr \_ REPLACEALL** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="59a32-129">**FR\_REPLACEALL** (0x00000020)</span></span> | <span data-ttu-id="59a32-130">Пользователь щелкнул кнопку **заменить все** в диалоговом окне **заменить** .</span><span class="sxs-lookup"><span data-stu-id="59a32-130">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="59a32-131">Член **лпстрфиндвхат** указывает строку для замены, а член **лпстрреплацевис** указывает замещающую строку.</span><span class="sxs-lookup"><span data-stu-id="59a32-131">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="59a32-132">Для параметра **найти следующее** или **заменить все** сообщение элемент **flags** может включать один или несколько следующих флагов для указания параметров поиска.</span><span class="sxs-lookup"><span data-stu-id="59a32-132">For a **Find Next** or **Replace All** message, the **Flags** member can include one or more of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="59a32-133">Flag</span><span class="sxs-lookup"><span data-stu-id="59a32-133">Flag</span></span>                           | <span data-ttu-id="59a32-134">Значение</span><span class="sxs-lookup"><span data-stu-id="59a32-134">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a32-135">**Fr \_ ВНИЗ** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="59a32-135">**FR\_DOWN** (0x00000001)</span></span>      | <span data-ttu-id="59a32-136">Если этот параметр задан, выбирается кнопка " **вниз** " переключателя направления, указывающая, что пользователь хочет выполнить поиск от текущего расположения до конца документа.</span><span class="sxs-lookup"><span data-stu-id="59a32-136">If set, the **Down** button of the direction radio buttons is selected indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="59a32-137">Если значение **fr \_ Down** не задано, то выбирается кнопка **вверх** , чтобы пользователь хотел выполнить поиск в начале документа.</span><span class="sxs-lookup"><span data-stu-id="59a32-137">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="59a32-138">**Fr \_ МАТЧКАСЕ** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="59a32-138">**FR\_MATCHCASE** (0x00000004)</span></span> | <span data-ttu-id="59a32-139">Установленный флажок **учитывать регистр** означает, что при поиске пользователя требуется учитывать регистр.</span><span class="sxs-lookup"><span data-stu-id="59a32-139">If set, the **Match Case** check box is selected indicating that the user wants the search to be case-sensitive.</span></span> <span data-ttu-id="59a32-140">Если значение **fr \_ матчкасе** не задано, флажок не выбран, поэтому при поиске не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="59a32-140">If **FR\_MATCHCASE** is not set, the check box is unselected so the search should be case-insensitive.</span></span>                                                                         |
| <span data-ttu-id="59a32-141">**Fr \_ ВХОЛЕВОРД** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="59a32-141">**FR\_WHOLEWORD** (0x00000002)</span></span> | <span data-ttu-id="59a32-142">Если задано значение, то устанавливается флажок **только слово целиком** , указывающий, что пользователь хочет искать только целые слова, соответствующие строке поиска.</span><span class="sxs-lookup"><span data-stu-id="59a32-142">If set, the **Match Whole Word Only** check box is selected indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="59a32-143">Если значение **fr \_ вхолеворд** не задано, флажок не выбран, поэтому следует искать фрагменты слов, соответствующие строке поиска.</span><span class="sxs-lookup"><span data-stu-id="59a32-143">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="59a32-144">Требования</span><span class="sxs-lookup"><span data-stu-id="59a32-144">Requirements</span></span>



| <span data-ttu-id="59a32-145">Требование</span><span class="sxs-lookup"><span data-stu-id="59a32-145">Requirement</span></span> | <span data-ttu-id="59a32-146">Значение</span><span class="sxs-lookup"><span data-stu-id="59a32-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a32-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59a32-147">Minimum supported client</span></span><br/> | <span data-ttu-id="59a32-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59a32-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="59a32-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59a32-149">Minimum supported server</span></span><br/> | <span data-ttu-id="59a32-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59a32-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59a32-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="59a32-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="59a32-152"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59a32-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="59a32-153">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="59a32-153">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="59a32-154">**Финдмсгстрингв** (Юникод) и **финдмсгстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="59a32-154">**FINDMSGSTRINGW** (Unicode) and **FINDMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="59a32-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59a32-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="59a32-156">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="59a32-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="59a32-157">**финдреплаце**</span><span class="sxs-lookup"><span data-stu-id="59a32-157">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="59a32-158">**регистервиндовмессаже**</span><span class="sxs-lookup"><span data-stu-id="59a32-158">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="59a32-159">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="59a32-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="59a32-160">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="59a32-160">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

