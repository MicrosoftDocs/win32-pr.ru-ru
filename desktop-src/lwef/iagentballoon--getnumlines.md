---
title: Иажентбаллун Жетнумлинес
description: Иажентбаллун Жетнумлинес
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411357"
---
# <a name="iagentballoongetnumlines"></a><span data-ttu-id="d8428-103">Иажентбаллун:: Жетнумлинес</span><span class="sxs-lookup"><span data-stu-id="d8428-103">IAgentBalloon::GetNumLines</span></span>

<span data-ttu-id="d8428-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8428-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

<span data-ttu-id="d8428-105">Получает значение числа строк, отображаемых в выноске.</span><span class="sxs-lookup"><span data-stu-id="d8428-105">Retrieves the value of the number of lines displayed in a word balloon.</span></span>

-   <span data-ttu-id="d8428-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d8428-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d8428-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*пклинес*</span><span class="sxs-lookup"><span data-stu-id="d8428-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span></span>
</dt> <dd>

<span data-ttu-id="d8428-108">Адрес переменной, которая получает количество отображаемых строк.</span><span class="sxs-lookup"><span data-stu-id="d8428-108">The address of a variable that receives the number of lines displayed.</span></span>

</dd> </dl>

<span data-ttu-id="d8428-109">Сервер Microsoft Agent автоматически прокручивает строки, отображаемые для речевого вывода, в окне всплывающей программы.</span><span class="sxs-lookup"><span data-stu-id="d8428-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="d8428-110">Число строк для текстового всплывающего слова определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d8428-110">The number of lines for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="d8428-111">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="d8428-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8428-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="d8428-112">See Also</span></span>

[<span data-ttu-id="d8428-113">**Иажентбаллун:: Жетнумчарсперлине**</span><span class="sxs-lookup"><span data-stu-id="d8428-113">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




