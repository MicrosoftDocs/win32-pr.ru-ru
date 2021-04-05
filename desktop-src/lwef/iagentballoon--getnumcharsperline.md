---
title: Иажентбаллун Жетнумчарсперлине
description: Иажентбаллун Жетнумчарсперлине
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068560"
---
# <a name="iagentballoongetnumcharsperline"></a><span data-ttu-id="bf52a-103">Иажентбаллун:: Жетнумчарсперлине</span><span class="sxs-lookup"><span data-stu-id="bf52a-103">IAgentBalloon::GetNumCharsPerLine</span></span>

<span data-ttu-id="bf52a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bf52a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

<span data-ttu-id="bf52a-105">Возвращает значение для среднего количества символов в строке, отображаемых в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="bf52a-105">Retrieves the value for the average number of characters per line displayed in a word balloon.</span></span>

-   <span data-ttu-id="bf52a-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bf52a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bf52a-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*пбчарсперлине*</span><span class="sxs-lookup"><span data-stu-id="bf52a-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="bf52a-108">Адрес переменной, которая получает количество символов в строке.</span><span class="sxs-lookup"><span data-stu-id="bf52a-108">The address of a variable that receives the number of characters per line.</span></span>

</dd> </dl>

<span data-ttu-id="bf52a-109">Сервер Microsoft Agent автоматически прокручивает строки, отображаемые для речевого вывода, в окне всплывающей программы.</span><span class="sxs-lookup"><span data-stu-id="bf52a-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="bf52a-110">Среднее число символов в строке для всплывающего слова символа определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="bf52a-110">The average number of characters per line for a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="bf52a-111">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="bf52a-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf52a-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="bf52a-112">See Also</span></span>

[<span data-ttu-id="bf52a-113">**Иажентбаллун:: Жетнумлинес**</span><span class="sxs-lookup"><span data-stu-id="bf52a-113">**IAgentBalloon::GetNumLines**</span></span>](iagentballoon--getnumlines.md)


 

 




