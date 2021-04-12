---
title: Иажентбаллунекс Сетнумчарсперлине
description: Иажентбаллунекс Сетнумчарсперлине
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331848"
---
# <a name="iagentballoonexsetnumcharsperline"></a><span data-ttu-id="a4baf-103">Иажентбаллунекс:: Сетнумчарсперлине</span><span class="sxs-lookup"><span data-stu-id="a4baf-103">IAgentBalloonEx::SetNumCharsPerLine</span></span>

<span data-ttu-id="a4baf-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4baf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

<span data-ttu-id="a4baf-105">Задает количество символов в строке, которые могут отображаться в тексте слова символа.</span><span class="sxs-lookup"><span data-stu-id="a4baf-105">Sets the number of characters per line that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="a4baf-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a4baf-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="a4baf-107">Возвращает значение E \_ INVALIDARG, если значение параметра меньше восьми.</span><span class="sxs-lookup"><span data-stu-id="a4baf-107">Returns E\_INVALIDARG if the parameter is less than eight.</span></span>

<dl> <dt>

<span data-ttu-id="a4baf-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*лчарсперлине*</span><span class="sxs-lookup"><span data-stu-id="a4baf-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="a4baf-109">Число строк, отображаемых в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="a4baf-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="a4baf-110">Минимальное значение равно 8, а максимальное — 255.</span><span class="sxs-lookup"><span data-stu-id="a4baf-110">The minimum setting is 8 and the maximum is 255.</span></span> <span data-ttu-id="a4baf-111">Если текст, указанный в методе [**произношения**](speak-method.md) или [**обработки**](think-method.md) , превышает размер текущего всплывающего окна, агент автоматически прокручивает текст в выноске.</span><span class="sxs-lookup"><span data-stu-id="a4baf-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="a4baf-112">Значение по умолчанию основано на параметрах, когда символ компилируется с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a4baf-112">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4baf-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="a4baf-113">See Also</span></span>

[<span data-ttu-id="a4baf-114">**Иажентбаллун:: Жетнумчарсперлине**</span><span class="sxs-lookup"><span data-stu-id="a4baf-114">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




