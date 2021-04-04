---
title: Как взаимодействовать с текущим выделением
description: Пользователь может выбрать текст в элементе управления Rich Edit с помощью мыши или клавиатуры.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789360"
---
# <a name="how-to-interact-with-the-current-selection"></a><span data-ttu-id="bbb55-103">Как взаимодействовать с текущим выделением</span><span class="sxs-lookup"><span data-stu-id="bbb55-103">How to Interact with the Current Selection</span></span>

<span data-ttu-id="bbb55-104">Пользователь может выбрать текст в элементе управления Rich Edit с помощью мыши или клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="bbb55-104">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="bbb55-105">*Текущий выделенный фрагмент* — это диапазон выбранных символов или позиция точки вставки, если ни одна из символов не выбрана.</span><span class="sxs-lookup"><span data-stu-id="bbb55-105">The *current selection* is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="bbb55-106">Приложение может получить сведения о текущем выделении, задать его, определить, когда оно изменяется, а также показать или скрыть выделение выделения.</span><span class="sxs-lookup"><span data-stu-id="bbb55-106">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bbb55-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="bbb55-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bbb55-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="bbb55-108">Technologies</span></span>

-   [<span data-ttu-id="bbb55-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="bbb55-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bbb55-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="bbb55-110">Prerequisites</span></span>

-   <span data-ttu-id="bbb55-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="bbb55-111">C/C++</span></span>
-   <span data-ttu-id="bbb55-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="bbb55-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bbb55-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="bbb55-113">Instructions</span></span>

### <a name="interact-with-the-current-selection"></a><span data-ttu-id="bbb55-114">Взаимодействие с текущим выделением</span><span class="sxs-lookup"><span data-stu-id="bbb55-114">Interact with the Current Selection</span></span>

<span data-ttu-id="bbb55-115">Чтобы определить текущее выделение в элементе управления Rich Edit, используйте сообщение [**EM \_ ексжетсел**](em-exgetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-115">To determine the current selection in a rich edit control, use the [**EM\_EXGETSEL**](em-exgetsel.md) message.</span></span> <span data-ttu-id="bbb55-116">Чтобы задать текущее выделение, используйте сообщение [**EM \_ екссетсел**](em-exsetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-116">To set the current selection, use the [**EM\_EXSETSEL**](em-exsetsel.md) message.</span></span> <span data-ttu-id="bbb55-117">Структура [**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange) используется с обоими сообщениями и задает диапазон символов.</span><span class="sxs-lookup"><span data-stu-id="bbb55-117">The [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure is used with both messages and specifies a range of characters.</span></span> <span data-ttu-id="bbb55-118">Чтобы получить сведения о содержимом текущего выделения, можно использовать сообщение [**EM \_ селектионтипе**](em-selectiontype.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-118">To retrieve information about the contents of the current selection, you can use the [**EM\_SELECTIONTYPE**](em-selectiontype.md) message.</span></span>

<span data-ttu-id="bbb55-119">Приложение может обнаружить, когда текущее выделение изменится, обрабатывая код уведомления [en \_ селчанже](en-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-119">An application can detect when the current selection changes by processing the [EN\_SELCHANGE](en-selchange.md) notification code.</span></span> <span data-ttu-id="bbb55-120">Код уведомления указывает структуру [**селчанже**](/windows/desktop/api/Richedit/ns-richedit-selchange) , содержащую сведения о новом выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="bbb55-120">The notification code specifies a [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that contains information about the new selection.</span></span> <span data-ttu-id="bbb55-121">Форматированный элемент управления "поле ввода" отправляет этот код уведомления только в том случае, если он включен с помощью сообщения [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-121">A rich edit control sends this notification code only if you enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="bbb55-122">По умолчанию элемент управления с расширенным редактированием показывает и скрывает выделение выделения при получении и потере фокуса.</span><span class="sxs-lookup"><span data-stu-id="bbb55-122">By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus.</span></span> <span data-ttu-id="bbb55-123">Выделение выделения можно показать или скрыть в любое время с помощью сообщения [**EM \_ хидеселектион**](em-hideselection.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-123">You can show or hide the selection highlight at any time by using the [**EM\_HIDESELECTION**](em-hideselection.md) message.</span></span> <span data-ttu-id="bbb55-124">Например, приложение может предоставить диалоговое окно поиска для поиска текста в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bbb55-124">For example, an application might provide a Search dialog box to find text in a rich edit control.</span></span> <span data-ttu-id="bbb55-125">Приложение может выбрать соответствующий текст, не закрывая диалоговое окно. в этом случае для выделения выбранного фрагмента необходимо использовать сообщение **EM \_ хидеселектион** .</span><span class="sxs-lookup"><span data-stu-id="bbb55-125">The application might select matching text without closing the dialog box, in which case it must use the **EM\_HIDESELECTION** message to highlight the selection.</span></span>

<span data-ttu-id="bbb55-126">Как и в случае с элементами управления "поле ввода", можно задать стиль окна [**ES \_ нохидесел**](edit-control-styles.md) , чтобы запретить элементу управления Rich Edit выделение выделения при потере фокуса.</span><span class="sxs-lookup"><span data-stu-id="bbb55-126">As with edit controls, you can specify the [**ES\_NOHIDESEL**](edit-control-styles.md) window style to prevent a rich edit control from hiding the selection highlight when it loses the focus.</span></span>

<span data-ttu-id="bbb55-127">В качестве альтернативы использованию сообщений [**EM \_ Ексжетсел**](em-exgetsel.md) и [**EM \_ екссетсел**](em-exsetsel.md) можно получить и установить текущий выбор с помощью управляющих сообщений [**EM \_ жетсел**](em-getsel.md) и [**EM \_ сетсел**](em-setsel.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-127">As an alternative to using the [**EM\_EXGETSEL**](em-exgetsel.md) and [**EM\_EXSETSEL**](em-exsetsel.md) messages, you can retrieve and set the current selection by using the [**EM\_GETSEL**](em-getsel.md) and [**EM\_SETSEL**](em-setsel.md) edit control messages.</span></span> <span data-ttu-id="bbb55-128">Пакеты **\_ жетсел** сообщений с пакетом EM 2 16-разрядные индексы в 32-битное возвращаемое значение и, следовательно, работают только для выбора, которые полностью находятся в пределах первых 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="bbb55-128">The **EM\_GETSEL** message packs two 16-bit character indexes into its 32-bit return value and therefore, works only for selections that fall entirely within the first 64K.</span></span> <span data-ttu-id="bbb55-129">Тем не менее, элемент управления "поле ввода" никогда не будет содержать более 32 000 символов текста, если не расширить это ограничение с помощью сообщения [**EM \_ Лимиттекст**](em-limittext.md) или [**EM \_ екслимиттекст**](em-exlimittext.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb55-129">However, a rich edit control will never contain more than 32K characters of text, unless you extend this limit by using the [**EM\_LIMITTEXT**](em-limittext.md) or [**EM\_EXLIMITTEXT**](em-exlimittext.md) message.</span></span> <span data-ttu-id="bbb55-130">Для выбора, который выходит за пределы первых 64 КБ текста, **сообщение \_ жетсел EM** возвращает значение – 1.</span><span class="sxs-lookup"><span data-stu-id="bbb55-130">For selections that extend beyond the first 64 KB of text, the **EM\_GETSEL** message returns –1.</span></span> <span data-ttu-id="bbb55-131">В этом случае можно по-прежнему использовать значения, возвращаемые в *wParam* и *lParam* , для поиска начального и конечного символов выделения.</span><span class="sxs-lookup"><span data-stu-id="bbb55-131">In such a case you can still use the values that are returned in *wParam* and *lParam* to find the start and end characters of the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbb55-132">См. также</span><span class="sxs-lookup"><span data-stu-id="bbb55-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbb55-133">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="bbb55-133">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="bbb55-134">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bbb55-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




