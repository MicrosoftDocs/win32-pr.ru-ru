---
title: Иажентбаллунекс Сетнумлинес
description: Иажентбаллунекс Сетнумлинес
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486952"
---
# <a name="iagentballoonexsetnumlines"></a><span data-ttu-id="71a83-103">Иажентбаллунекс:: Сетнумлинес</span><span class="sxs-lookup"><span data-stu-id="71a83-103">IAgentBalloonEx::SetNumLines</span></span>

<span data-ttu-id="71a83-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71a83-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

<span data-ttu-id="71a83-105">Задает количество строк вывода текста, которые могут отображаться в тексте всплывающего слова символа.</span><span class="sxs-lookup"><span data-stu-id="71a83-105">Sets the number of lines of text output that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="71a83-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="71a83-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="71a83-107">Возвращает значение E \_ INVALIDARG, если параметр равен нулю.</span><span class="sxs-lookup"><span data-stu-id="71a83-107">Returns E\_INVALIDARG if the parameter is zero.</span></span>

<dl> <dt>

<span data-ttu-id="71a83-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*ллинес*</span><span class="sxs-lookup"><span data-stu-id="71a83-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span></span>
</dt> <dd>

<span data-ttu-id="71a83-109">Число строк, отображаемых в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="71a83-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="71a83-110">Минимальное значение — 1, а максимальное — 128.</span><span class="sxs-lookup"><span data-stu-id="71a83-110">The minimum setting is 1 and maximum is 128.</span></span> <span data-ttu-id="71a83-111">Если текст, указанный в методе [**произношения**](speak-method.md) или [**обработки**](think-method.md) , превышает размер текущего всплывающего окна, агент автоматически прокручивает текст в выноске.</span><span class="sxs-lookup"><span data-stu-id="71a83-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="71a83-112">Этот метод завершится ошибкой, если установлен бит стиля всплывающего окна **сизетотекст** .</span><span class="sxs-lookup"><span data-stu-id="71a83-112">This method will fail if the **SizeToText** balloon style bit is set.</span></span>

<span data-ttu-id="71a83-113">Значение по умолчанию основано на параметрах, когда символ компилируется с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="71a83-113">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="71a83-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="71a83-114">See Also</span></span>

<span data-ttu-id="71a83-115">[**Иажентбаллун:: жетнумлинес**](iagentballoon--getnumlines.md), [**Иажентбаллунекс:: Style**](iagentballoonex--getstyle.md), [**иажентбаллунекс:: SetStyle**](iagentballoonex--setstyle.md)</span><span class="sxs-lookup"><span data-stu-id="71a83-115">[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)</span></span>


 

 




