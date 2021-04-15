---
description: Модуль распознавания рукописного ввода (или средство распознавания) — это программное обеспечение, которое обрабатывает рукописный ввод и преобразует рукописный ввод в текст.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Использование контекста для повышения точности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662387"
---
# <a name="using-context-to-improve-accuracy"></a><span data-ttu-id="36100-103">Использование контекста для повышения точности</span><span class="sxs-lookup"><span data-stu-id="36100-103">Using Context to Improve Accuracy</span></span>

<span data-ttu-id="36100-104">Модуль распознавания рукописного ввода (или средство распознавания) — это программное обеспечение, которое обрабатывает рукописный ввод и преобразует рукописный ввод в текст.</span><span class="sxs-lookup"><span data-stu-id="36100-104">A handwriting recognition engine, or recognizer, is software that processes ink and converts that ink into text.</span></span> <span data-ttu-id="36100-105">Контекст релевантен, сведения о приложении, предоставляемые распознавателю для улучшения точности распознавания.</span><span class="sxs-lookup"><span data-stu-id="36100-105">A context is relevant, application-specific information that you provide to a recognizer to improve recognition accuracy.</span></span> <span data-ttu-id="36100-106">Иными словами, контекст представляет собой любую информацию о входных данных, которая помогает распознавателю точно обрабатывать рукописный ввод в поле.</span><span class="sxs-lookup"><span data-stu-id="36100-106">In other words, context is any piece of information about input that aids the recognizer in accurately processing the ink in a field.</span></span>

<span data-ttu-id="36100-107">В этом разделе описаны различные способы использования контекста в приложении для планшетных ПК, в которых особое внимание уделяется предпочтительному программному методу для приложений, не поддерживающих рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="36100-107">This section describes the different ways you can take advantage of context in your Tablet PC application, placing emphasis on the preferred programmatic technique for applications that are not ink enabled.</span></span>

> [!Note]  
> <span data-ttu-id="36100-108">В разделах технологии планшетных ПК пакета средств разработки программного обеспечения (SDK) для Windows Vista есть места, где термин "контекст" используется в отношении объекта [**рекогнизерконтекст**](inkrecognizercontext-class.md) и его свойств [**префикстекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) и [**суффикстекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) .</span><span class="sxs-lookup"><span data-stu-id="36100-108">There are places in the Tablet PC Technology sections of the Windows Vista Software Development Kit (SDK) where the term "context" is used in regard to the [**RecognizerContext**](inkrecognizercontext-class.md) object and its [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) and [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) properties.</span></span> <span data-ttu-id="36100-109">Не путайте эти другие случаи использования "Context" с определением в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="36100-109">Do not confuse these other usages of "context" with the definition in this section.</span></span>

 

 

 



