---
description: Когда приложение работает с целыми словами, допустимые позиции для курсора помечаются значением элемента Фвордстоп \_ структуры Script логаттр. Это значение извлекается путем вызова Скриптбреак.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Использование точек останова Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272948"
---
# <a name="using-word-break-points"></a><span data-ttu-id="d7276-104">Использование точек останова Word</span><span class="sxs-lookup"><span data-stu-id="d7276-104">Using Word Break Points</span></span>

<span data-ttu-id="d7276-105">Когда приложение работает с целыми словами, допустимые позиции для курсора помечаются значением элемента **фвордстоп** структуры [**script \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="d7276-105">When the application is dealing with whole words, valid positions for the caret are marked by the value of the **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="d7276-106">Это значение извлекается путем вызова [**скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="d7276-106">This value is retrieved by making a call to [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

<span data-ttu-id="d7276-107">Допустимые позиции для разбиения строк между словами помечаются значением **фсофтбреак** , полученным с помощью [**скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="d7276-107">Valid positions for breaking lines between words are marked by the **fSoftBreak** value retrieved by [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7276-108">См. также</span><span class="sxs-lookup"><span data-stu-id="d7276-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7276-109">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="d7276-109">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



