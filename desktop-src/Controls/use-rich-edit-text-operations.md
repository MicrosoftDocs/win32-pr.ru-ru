---
title: Как использовать широкие операции редактирования текста
description: Приложение может отсылать сообщения для получения или поиска текста в элементе управления Rich Edit. Можно получить выделенный текст или указанный фрагмент текста.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987931"
---
# <a name="how-to-use-rich-edit-text-operations"></a><span data-ttu-id="56dd1-104">Как использовать широкие операции редактирования текста</span><span class="sxs-lookup"><span data-stu-id="56dd1-104">How to Use Rich Edit Text Operations</span></span>

<span data-ttu-id="56dd1-105">Приложение может отсылать сообщения для получения или поиска текста в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="56dd1-105">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="56dd1-106">Можно получить выделенный текст или указанный фрагмент текста.</span><span class="sxs-lookup"><span data-stu-id="56dd1-106">You can retrieve either the selected text or a specified range of text.</span></span>

<span data-ttu-id="56dd1-107">Чтобы получить выделенный текст в элементе управления Rich Edit, используйте сообщение [**EM \_ жетселтекст**](em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="56dd1-107">To get the selected text in a rich edit control, use the [**EM\_GETSELTEXT**](em-getseltext.md) message.</span></span> <span data-ttu-id="56dd1-108">Текст копируется в указанный массив символов.</span><span class="sxs-lookup"><span data-stu-id="56dd1-108">The text is copied to the specified character array.</span></span> <span data-ttu-id="56dd1-109">Необходимо убедиться, что массив достаточно велик, чтобы вместить выделенный текст, а также завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="56dd1-109">You must ensure that the array is large enough to hold the selected text plus a terminating null character.</span></span>

<span data-ttu-id="56dd1-110">Чтобы получить указанный диапазон текста, используйте сообщение [**EM \_ жеттекстранже**](em-gettextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="56dd1-110">To retrieve a specified range of text, use the [**EM\_GETTEXTRANGE**](em-gettextrange.md) message.</span></span> <span data-ttu-id="56dd1-111">Структура [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) , используемая с этим сообщением, указывает диапазон текста для извлечения и указывает на массив символов, который получает текст.</span><span class="sxs-lookup"><span data-stu-id="56dd1-111">The [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure used with this message specifies the text range to retrieve and points to a character array that receives the text.</span></span> <span data-ttu-id="56dd1-112">В этом случае приложение должно обеспечить достаточно большой размер массива для указанного текста и завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="56dd1-112">Here again, the application must ensure that the array is large enough for the specified text plus a terminating null character.</span></span>

<span data-ttu-id="56dd1-113">Вы можете выполнять поиск строки в элементе управления Rich Edit с помощью сообщений [**EM \_ строки FindText**](em-findtext.md) или [**EM \_ финдтекстекс**](em-findtextex.md) или их эквивалентов в Юникоде, [**EM \_ финдтекств**](em-findtextw.md) и [**EM \_ финдтекстексв**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="56dd1-113">You can search for a string in a rich edit control by using the [**EM\_FINDTEXT**](em-findtext.md) or [**EM\_FINDTEXTEX**](em-findtextex.md) messages, or their Unicode equivalents, [**EM\_FINDTEXTW**](em-findtextw.md) and [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span> <span data-ttu-id="56dd1-114">Структура [**строки FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) , используемая с нерасширенными версиями, задает текстовый диапазон для поиска и искомую строку.</span><span class="sxs-lookup"><span data-stu-id="56dd1-114">The [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure that is used with the nonextended versions specifies the text range to search and the string to search for.</span></span> <span data-ttu-id="56dd1-115">В расширенных версиях используется структура [**финдтекстекс**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , которая задает одни и те же сведения, а также начальную и конечную точки диапазона символов найденного текста.</span><span class="sxs-lookup"><span data-stu-id="56dd1-115">The extended versions use a [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, which specifies the same information and also receives the start and end points of the character range of the found text.</span></span> <span data-ttu-id="56dd1-116">Можно также указать такие параметры, как при поиске с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="56dd1-116">You can also specify such options as whether the search is case sensitive.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="56dd1-117">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="56dd1-117">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="56dd1-118">Технологии</span><span class="sxs-lookup"><span data-stu-id="56dd1-118">Technologies</span></span>

-   [<span data-ttu-id="56dd1-119">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="56dd1-119">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="56dd1-120">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="56dd1-120">Prerequisites</span></span>

-   <span data-ttu-id="56dd1-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="56dd1-121">C/C++</span></span>
-   <span data-ttu-id="56dd1-122">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="56dd1-122">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="56dd1-123">Инструкции</span><span class="sxs-lookup"><span data-stu-id="56dd1-123">Instructions</span></span>

### <a name="use-a-rich-edit-text-operation"></a><span data-ttu-id="56dd1-124">Использование операции расширенного ввода текста</span><span class="sxs-lookup"><span data-stu-id="56dd1-124">Use a Rich Edit Text Operation</span></span>

<span data-ttu-id="56dd1-125">Следующий пример функции находит указанный текст в выделенном тексте в элементе управления Rich Edit, поддерживающем Юникод.</span><span class="sxs-lookup"><span data-stu-id="56dd1-125">The following example function finds the specified text within the selected text in a rich edit control that supports Unicode.</span></span> <span data-ttu-id="56dd1-126">Если целевой объект найден, он становится новым выбором.</span><span class="sxs-lookup"><span data-stu-id="56dd1-126">If the target is found, it becomes the new selection.</span></span>


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a><span data-ttu-id="56dd1-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56dd1-127">Remarks</span></span>

<span data-ttu-id="56dd1-128">Microsoft Rich Edit 3,0 также поддерживает функцию редактора метода ввода (IME) Хекстауникоде, позволяющую пользователю выполнять преобразование между шестнадцатеричными и Юникод с помощью горячих клавиш.</span><span class="sxs-lookup"><span data-stu-id="56dd1-128">Microsoft Rich Edit 3.0 also supports the HexToUnicode Input Method Editor (IME) function, which allows a user to convert between hexadecimal and Unicode by using hot keys.</span></span> <span data-ttu-id="56dd1-129">Дополнительные сведения см. в разделе [ХЕКСТАУНИКОДЕ IME](/windows/desktop/Intl/hextounicode-ime).</span><span class="sxs-lookup"><span data-stu-id="56dd1-129">For more information, see [HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56dd1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="56dd1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56dd1-131">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="56dd1-131">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="56dd1-132">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="56dd1-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 