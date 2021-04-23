---
description: В однонаправленном тексте позиции курсора не имеют неоднозначности, так как ведущий ребр символа находится в том же месте, что и конечный крайний отступ предыдущего символа.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Отображение курсора в двунаправленных строках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651120"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a><span data-ttu-id="ea173-103">Отображение курсора в двунаправленных строках</span><span class="sxs-lookup"><span data-stu-id="ea173-103">Displaying the Caret in Bidirectional Strings</span></span>

<span data-ttu-id="ea173-104">В однонаправленном тексте позиции курсора не имеют неоднозначности, так как ведущий ребр символа находится в том же месте, что и конечный крайний отступ предыдущего символа.</span><span class="sxs-lookup"><span data-stu-id="ea173-104">In unidirectional text, the caret position has no ambiguity because the leading edge of a character is at the same place as the trailing edge of the previous character.</span></span> <span data-ttu-id="ea173-105">Однако в двунаправленном тексте курсор между запусками противоположного направления является неоднозначным.</span><span class="sxs-lookup"><span data-stu-id="ea173-105">However, in bidirectional text, the caret position between runs of opposing direction is ambiguous.</span></span> <span data-ttu-id="ea173-106">Например, в абзаце "хеллосалаам" слева направо последняя буква "Привет" непосредственно предшествует первой букве "Эс Салам".</span><span class="sxs-lookup"><span data-stu-id="ea173-106">For example, in the left-to-right paragraph "hellosalaam", the last letter of "hello" immediately precedes the first letter of "salaam".</span></span> <span data-ttu-id="ea173-107">Наилучшее расположение курсора зависит от того, считается ли он подходящей операцией "o" из "Hello" или перед "s" из "Эс Салам".</span><span class="sxs-lookup"><span data-stu-id="ea173-107">The best position in which to display the caret depends on whether it is considered to follow the "o" of "hello" or to precede the "s" of "salaam".</span></span>

<span data-ttu-id="ea173-108">Uniscribe использует соглашения о позиционировании курсоров, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ea173-108">Uniscribe uses the caret positioning conventions shown in the next table.</span></span>



| <span data-ttu-id="ea173-109">Ситуация</span><span class="sxs-lookup"><span data-stu-id="ea173-109">Situation</span></span>       | <span data-ttu-id="ea173-110">Визуальное размещение курсора</span><span class="sxs-lookup"><span data-stu-id="ea173-110">Visual caret placement</span></span>                       |
|-----------------|----------------------------------------------|
| <span data-ttu-id="ea173-111">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="ea173-111">Typing</span></span>          | <span data-ttu-id="ea173-112">Конечный конец последнего введенного символа.</span><span class="sxs-lookup"><span data-stu-id="ea173-112">Trailing edge of last character typed.</span></span>       |
| <span data-ttu-id="ea173-113">Вставки</span><span class="sxs-lookup"><span data-stu-id="ea173-113">Pasting</span></span>         | <span data-ttu-id="ea173-114">Конечный конец последнего вставленного символа.</span><span class="sxs-lookup"><span data-stu-id="ea173-114">Trailing edge of last character pasted.</span></span>      |
| <span data-ttu-id="ea173-115">Курсор позаботится</span><span class="sxs-lookup"><span data-stu-id="ea173-115">Caret advancing</span></span> | <span data-ttu-id="ea173-116">Конечный крайний конец последнего переданного символа.</span><span class="sxs-lookup"><span data-stu-id="ea173-116">Trailing edge of last character passed over.</span></span> |
| <span data-ttu-id="ea173-117">Снятие курсора с учета</span><span class="sxs-lookup"><span data-stu-id="ea173-117">Caret retiring</span></span>  | <span data-ttu-id="ea173-118">Начальная граница последнего переданного символа.</span><span class="sxs-lookup"><span data-stu-id="ea173-118">Leading edge of last character passed over.</span></span>  |
| <span data-ttu-id="ea173-119">Домашняя страница</span><span class="sxs-lookup"><span data-stu-id="ea173-119">Home</span></span>            | <span data-ttu-id="ea173-120">Передний края строки.</span><span class="sxs-lookup"><span data-stu-id="ea173-120">Leading edge of line.</span></span>                        |
| <span data-ttu-id="ea173-121">Конец</span><span class="sxs-lookup"><span data-stu-id="ea173-121">End</span></span>             | <span data-ttu-id="ea173-122">Конечная граница строки.</span><span class="sxs-lookup"><span data-stu-id="ea173-122">Trailing edge of line.</span></span>                       |



 

<span data-ttu-id="ea173-123">Курсор можно разместите, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ea173-123">The caret can be positioned as shown in the following example:</span></span>


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



<span data-ttu-id="ea173-124">Позиционирование курсора может быть проще, как показано ниже, при условии, что значение *фадванЦинг* ограничено значением **true** или **false**:</span><span class="sxs-lookup"><span data-stu-id="ea173-124">Positioning of the caret can be simpler, as shown below, given an *fAdvancing* value restricted to **TRUE** or **FALSE**:</span></span>


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



<span data-ttu-id="ea173-125">[**Скрипткптокс**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) обрабатывает позиции вне диапазона логически.</span><span class="sxs-lookup"><span data-stu-id="ea173-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) handles out-of-range positions logically.</span></span> <span data-ttu-id="ea173-126">Он возвращает передний конец выполнения для *ичарпос* <0, а завершающую сторону выполнения для *ичарпос* >= length.</span><span class="sxs-lookup"><span data-stu-id="ea173-126">It returns the leading edge of the run for *iCharPos* <0, and the trailing edge of the run for *iCharPos* >= length.</span></span> <span data-ttu-id="ea173-127">Дополнительные сведения см. в разделе [Управление размещением курсора и проверкой попадания](managing-caret-placement-and-hit-testing.md) .</span><span class="sxs-lookup"><span data-stu-id="ea173-127">For more information, see [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea173-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ea173-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea173-129">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="ea173-129">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



