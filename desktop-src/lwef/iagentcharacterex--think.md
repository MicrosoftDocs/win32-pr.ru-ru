---
title: Иажентчарактерекс думать
description: Иажентчарактерекс думать
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069908"
---
# <a name="iagentcharacterexthink"></a><span data-ttu-id="d0ee8-103">Иажентчарактерекс:: подумать</span><span class="sxs-lookup"><span data-stu-id="d0ee8-103">IAgentCharacterEx::Think</span></span>

<span data-ttu-id="d0ee8-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0ee8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="d0ee8-105">Отображает подсказку относительного слова символа с указанным текстом.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-105">Displays the character's thought word balloon with the specified text.</span></span>

-   <span data-ttu-id="d0ee8-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d0ee8-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*бсзтекст*</span><span class="sxs-lookup"><span data-stu-id="d0ee8-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="d0ee8-108">Текст, отображаемый в фигурных выносках символа.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-108">The text to appear in the character's thought balloon.</span></span>

</dd> <dt>

<span data-ttu-id="d0ee8-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="d0ee8-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="d0ee8-110">Адрес переменной, которая получает идентификатор запроса на **обдумывание** .</span><span class="sxs-lookup"><span data-stu-id="d0ee8-110">Address of a variable that receives the **Think** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="d0ee8-111">Как и метод [**иажентчарактер:: говорите**](iagentcharacter--speak.md) , метод **обработки** является запросом в очереди, который отображает текст в выноске, за исключением того, что мысли отображаются в специальной фигурной подсказке.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-111">Like the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method, the **Think** method is a queued request that displays text in a word balloon, except that thoughts display in a special thought balloon.</span></span> <span data-ttu-id="d0ee8-112">Всплывающее подсказка поддерживает только тег элемента управления речью в закладке (**\\ МРК**) и игнорирует все другие теги элементов управления речевыми функциями.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-112">The thought balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="d0ee8-113">В отличие от **иажентчарактер:: говорите**, метод **обработки** не изменяет состояние анимации символа.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-113">Unlike **IAgentCharacter::Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="d0ee8-114">Параметры [**иажентбаллун**](/windows/desktop/lwef/iagentballoon) также применяются к стилю оформления всплывающего элемента.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-114">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) settings also apply to the appearance style of the thought balloon.</span></span> <span data-ttu-id="d0ee8-115">Например, свойство [**включения**](enabled-property.md) всплывающего окна должно также иметь **значение true** для отображаемого текста.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-115">For example, the balloon's [**Enabled**](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="d0ee8-116">Автоматическое разбиение слов в подсказке для Microsoft Agent разбивает слова на пробелы (например, пробелы и знаки табуляции).</span><span class="sxs-lookup"><span data-stu-id="d0ee8-116">Microsoft Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="d0ee8-117">Однако он может нарушить работу слова, чтобы вместить всплывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-117">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="d0ee8-118">В таких языках, как японский, китайский и тайский, если пробелы не используются для разбиения слов на слова, вставьте символ нулевой ширины (0x200B) в Юникоде между символами, чтобы определить логические разрывы слов.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-118">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="d0ee8-119">Задайте идентификатор языка символа (с помощью [**иажентчарактерекс:: сетлангуажеид**](iagentcharacterex--setlanguageid.md) перед использованием метода [**Иажентчарактер:: говорите**](iagentcharacter--speak.md) , чтобы обеспечить отображение текста в выноске слова.</span><span class="sxs-lookup"><span data-stu-id="d0ee8-119">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d0ee8-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="d0ee8-120">See Also</span></span>

<span data-ttu-id="d0ee8-121">[**Иажентбаллун:: enable**](iagentballoon--getenabled.md), [**Иажентбаллунекс:: SetStyle**](iagentballoonex--setstyle.md), [**иажентчарактер:: говорите**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="d0ee8-121">[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)</span></span>


 

 