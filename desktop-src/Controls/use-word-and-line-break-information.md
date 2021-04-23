---
title: Использование сведений о разрывах слов и строк
description: Форматированный элемент управления "поле ввода" вызывает функцию, называемую процедурой разрыва слов, чтобы найти разрывы между словами и определить, где она может разбивать строки.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654377"
---
# <a name="how-to-use-word-and-line-break-information"></a><span data-ttu-id="094f2-103">Использование сведений о разрывах слов и строк</span><span class="sxs-lookup"><span data-stu-id="094f2-103">How to Use Word and Line Break Information</span></span>

<span data-ttu-id="094f2-104">Форматированный элемент управления "поле ввода" вызывает функцию, называемую процедурой разрыва слов, чтобы найти разрывы между словами и определить, где она может разбивать строки.</span><span class="sxs-lookup"><span data-stu-id="094f2-104">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="094f2-105">Этот элемент управления использует эти сведения при выполнении операций переноса по словам и при обработке сочетания клавиш CTRL + стрелка влево и CTRL + стрелка вправо.</span><span class="sxs-lookup"><span data-stu-id="094f2-105">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="094f2-106">Приложение может отправить сообщения в элемент управления Rich Edit, чтобы заменить процедуру разбиения по словам по умолчанию, получить сведения о разрыве слов и определить линию, на которую попадает заданный символ.</span><span class="sxs-lookup"><span data-stu-id="094f2-106">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="094f2-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="094f2-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="094f2-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="094f2-108">Technologies</span></span>

-   [<span data-ttu-id="094f2-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="094f2-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="094f2-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="094f2-110">Prerequisites</span></span>

-   <span data-ttu-id="094f2-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="094f2-111">C/C++</span></span>
-   <span data-ttu-id="094f2-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="094f2-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="094f2-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="094f2-113">Instructions</span></span>

### <a name="use-word-and-line-break-information"></a><span data-ttu-id="094f2-114">Использование сведений о слове и разрыве строки</span><span class="sxs-lookup"><span data-stu-id="094f2-114">Use Word and Line Break Information</span></span>

<span data-ttu-id="094f2-115">Процедуры разбиения по словам для элементов управления с широкими возможностями похожи на элементы управления редактирования, но имеют дополнительные возможности: процедуры разбиения на слова для обоих видов элементов управления могут определить, является ли символ разделителем, и найти ближайшее разрыв слова до или после указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="094f2-115">Word-break procedures for rich edit controls are similar to those for edit controls, but they have additional capabilities: word-break procedures for both kinds of controls can determine whether a character is a delimiter and can find the nearest word break before or after the specified position.</span></span> <span data-ttu-id="094f2-116">Разделитель — это символ, обозначающий конец слова, например пробел.</span><span class="sxs-lookup"><span data-stu-id="094f2-116">A delimiter is a character that marks the end of a word, such as a space.</span></span> <span data-ttu-id="094f2-117">Как правило, в элементе управления "Правка" разрыв слова происходит только после разделителей.</span><span class="sxs-lookup"><span data-stu-id="094f2-117">Usually, in an edit control, a word break occurs only after delimiters.</span></span> <span data-ttu-id="094f2-118">Однако для большинства азиатских языков применяются разные правила.</span><span class="sxs-lookup"><span data-stu-id="094f2-118">However, different rules apply to most Asian languages.</span></span>

<span data-ttu-id="094f2-119">Процедуры разбиения по словам для элементов управления Rich Edit также группируют символы в классы символов, каждый из которых определяется значением в диапазоне от 0x00 до 0x0F.</span><span class="sxs-lookup"><span data-stu-id="094f2-119">Word-break procedures for rich edit controls also group characters into character classes, each identified by a value in the range 0x00 through 0x0F.</span></span> <span data-ttu-id="094f2-120">Перерывы происходят либо после разделителей, либо между символами разных классов.</span><span class="sxs-lookup"><span data-stu-id="094f2-120">Breaks occur either after delimiters or between characters of different classes.</span></span> <span data-ttu-id="094f2-121">Таким образом, процедура разбиения по словам с различными классами для алфавитно-цифровых символов и знаков препинания будет искать два разрыва слов в строке "Win.doc" (до и после точки).</span><span class="sxs-lookup"><span data-stu-id="094f2-121">Thus, a word-break procedure with different classes for alphanumeric and punctuation characters would find two word breaks in the string "Win.doc" (before and after the period).</span></span>

<span data-ttu-id="094f2-122">Класс символа можно сочетать с нулем или несколькими флагами разрыва слов для формирования 8-разрядного значения.</span><span class="sxs-lookup"><span data-stu-id="094f2-122">A character's class can be combined with zero or more word-break flags to form an 8-bit value.</span></span> <span data-ttu-id="094f2-123">При выполнении операций переноса по словам в элементе управления с расширенным редактированием используются флаги разбиения по словам, чтобы определить, где может нарушиться линия.</span><span class="sxs-lookup"><span data-stu-id="094f2-123">When performing word-wrap operations, a rich edit control uses word-break flags to determine where it can break lines.</span></span> <span data-ttu-id="094f2-124">Расширенное редактирование использует следующие флаги разрыва слов.</span><span class="sxs-lookup"><span data-stu-id="094f2-124">Rich Edit uses the following word-break flags.</span></span>



| <span data-ttu-id="094f2-125">Flag</span><span class="sxs-lookup"><span data-stu-id="094f2-125">Flag</span></span>            | <span data-ttu-id="094f2-126">Описание</span><span class="sxs-lookup"><span data-stu-id="094f2-126">Description</span></span>                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="094f2-127">ВБФ \_ BREAKAFTER</span><span class="sxs-lookup"><span data-stu-id="094f2-127">WBF\_BREAKAFTER</span></span> | <span data-ttu-id="094f2-128">Строки могут быть разорваны после символа.</span><span class="sxs-lookup"><span data-stu-id="094f2-128">Lines may be broken after the character.</span></span>                                                                                          |
| <span data-ttu-id="094f2-129">ВБФ \_ бреаклине</span><span class="sxs-lookup"><span data-stu-id="094f2-129">WBF\_BREAKLINE</span></span>  | <span data-ttu-id="094f2-130">Символ является разделителем.</span><span class="sxs-lookup"><span data-stu-id="094f2-130">The character is a delimiter.</span></span> <span data-ttu-id="094f2-131">Разделители означают концы слов.</span><span class="sxs-lookup"><span data-stu-id="094f2-131">Delimiters mark the ends of words.</span></span> <span data-ttu-id="094f2-132">Строки могут быть разорваны после разделителей.</span><span class="sxs-lookup"><span data-stu-id="094f2-132">Lines may be broken after delimiters.</span></span>                            |
| <span data-ttu-id="094f2-133">ВБФ \_</span><span class="sxs-lookup"><span data-stu-id="094f2-133">WBF\_ISWHITE</span></span>    | <span data-ttu-id="094f2-134">Символ является пробелом.</span><span class="sxs-lookup"><span data-stu-id="094f2-134">The character is a white-space character.</span></span> <span data-ttu-id="094f2-135">Замыкающие пробельные символы не включаются в длину строки при переносе.</span><span class="sxs-lookup"><span data-stu-id="094f2-135">Trailing white-space characters are not included in the length of a line when wrapping.</span></span> |



 

<span data-ttu-id="094f2-136">Значение ВБФ \_ BREAKAFTER используется, чтобы разрешить перенос после символа, который не помечает конец слова, например дефис.</span><span class="sxs-lookup"><span data-stu-id="094f2-136">The WBF\_BREAKAFTER value is used to allow wrapping after a character that does not mark the end of a word, such as a hyphen.</span></span>

<span data-ttu-id="094f2-137">Процедуру разрыва слов по умолчанию для элемента управления Rich Edit можно заменить собственной процедурой с помощью сообщения [**EM \_ сетвордбреакпрок**](em-setwordbreakproc.md) .</span><span class="sxs-lookup"><span data-stu-id="094f2-137">You can replace the default word-break procedure for a rich edit control with your own procedure by using the [**EM\_SETWORDBREAKPROC**](em-setwordbreakproc.md) message.</span></span> <span data-ttu-id="094f2-138">Дополнительные сведения о процедурах разбиения по словам см. в описании функции [*едитвордбреакпрок*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .</span><span class="sxs-lookup"><span data-stu-id="094f2-138">For more information about word-break procedures, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="094f2-139">Эта замена не рекомендуется для Microsoft Rich Edit 2,0 и более поздних версий из-за сложности многоязыковой разбивки слов.</span><span class="sxs-lookup"><span data-stu-id="094f2-139">This replacement is not recommended for Microsoft Rich Edit 2.0 and later, due to the complexity of multilingual word breaking.</span></span>

 

<span data-ttu-id="094f2-140">Для Microsoft Rich Edit 1,0 можно использовать сообщение [**EM \_ сетвордбреакпроцекс**](em-setwordbreakprocex.md) , чтобы заменить расширенную процедуру разрыва слов по умолчанию функцией [*едитвордбреакпроцекс*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) .</span><span class="sxs-lookup"><span data-stu-id="094f2-140">For Microsoft Rich Edit 1.0, you can use the [**EM\_SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) message to replace the default extended word-break procedure with an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function.</span></span> <span data-ttu-id="094f2-141">Эта функция предоставляет дополнительные сведения о тексте, например кодировку.</span><span class="sxs-lookup"><span data-stu-id="094f2-141">This function provides additional information about the text, such as the character set.</span></span> <span data-ttu-id="094f2-142">Для получения адреса текущей расширенной процедуры разбиения по словам можно использовать сообщение [**EM \_ жетвордбреакпроцекс**](em-getwordbreakprocex.md) .</span><span class="sxs-lookup"><span data-stu-id="094f2-142">You can use the [**EM\_GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) message to retrieve the address of the current extended word-break procedure.</span></span> <span data-ttu-id="094f2-143">Обратите внимание, что Microsoft Rich Edit 2,0 и более поздние версии не поддерживают *едитвордбреакпроцекс*, **EM \_ жетвордбреакпроцекс** и **EM \_ сетвордбреакпроцекс**.</span><span class="sxs-lookup"><span data-stu-id="094f2-143">Note that Microsoft Rich Edit 2.0 and later do not support *EditWordBreakProcEx*, **EM\_GETWORDBREAKPROCEX**, and **EM\_SETWORDBREAKPROCEX**.</span></span>

<span data-ttu-id="094f2-144">Сообщение [**EM \_ финдвордбреак**](em-findwordbreak.md) можно использовать для поиска разрывов слов или для определения класса символа и флагов разрыва слов.</span><span class="sxs-lookup"><span data-stu-id="094f2-144">You can use the [**EM\_FINDWORDBREAK**](em-findwordbreak.md) message to find word breaks or to determine a character's class and word-break flags.</span></span> <span data-ttu-id="094f2-145">В свою очередь, элемент управления вызывает процедуру разбиения на слова, чтобы получить запрошенную информацию.</span><span class="sxs-lookup"><span data-stu-id="094f2-145">In turn, the control calls its word-break procedure to get the requested information.</span></span>

<span data-ttu-id="094f2-146">Чтобы определить, на какой строке заданный символ попадает, можно использовать сообщение [**\_ екслинефромчар EM**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="094f2-146">To determine which line a given character falls on, you can use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="094f2-147">См. также</span><span class="sxs-lookup"><span data-stu-id="094f2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="094f2-148">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="094f2-148">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="094f2-149">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="094f2-149">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 