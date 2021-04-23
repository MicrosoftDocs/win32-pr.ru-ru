---
description: Чтобы получить уровень достоверности для каждого результата распознавания, можно получить либо свойство достоверности объекта Рекогнитионалтернате, либо свойство достоверности объекта жеста.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Свойство достоверности [о распознавании]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896685"
---
# <a name="confidence-property-about-recognition"></a><span data-ttu-id="bf628-103">Свойство достоверности \[ о распознавании\]</span><span class="sxs-lookup"><span data-stu-id="bf628-103">Confidence Property \[About Recognition\]</span></span>

<span data-ttu-id="bf628-104">Чтобы получить уровень достоверности для каждого результата распознавания, можно получить либо свойство [**достоверности**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) объекта [**рекогнитионалтернате**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) , либо свойство [**достоверности**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) объекта [**жеста**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .</span><span class="sxs-lookup"><span data-stu-id="bf628-104">To obtain a level of confidence for each recognition result, you can get either the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) property of the [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object or the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) property of the [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object.</span></span> <span data-ttu-id="bf628-105">Уровень достоверности — это число, указывающее степень достоверности для каждого альтернативного результата распознавания, который распознаватель возвращает для соответствующего сегмента распознавания.</span><span class="sxs-lookup"><span data-stu-id="bf628-105">The confidence level is a number that indicates the degree of confidence for each alternate recognition result that the recognizer returns for a corresponding recognition segment.</span></span>

<span data-ttu-id="bf628-106">Достоверность возвращается как низкая, средняя или высокая.</span><span class="sxs-lookup"><span data-stu-id="bf628-106">Confidence is returned as low, average, or high.</span></span> <span data-ttu-id="bf628-107">Приложение использует эти результаты для:</span><span class="sxs-lookup"><span data-stu-id="bf628-107">The application uses these results to:</span></span>

-   <span data-ttu-id="bf628-108">Укажите пользователю, что существует несколько возможностей.</span><span class="sxs-lookup"><span data-stu-id="bf628-108">Indicate to the user that multiple possibilities exist.</span></span>
-   <span data-ttu-id="bf628-109">Ранжирование вариантов по уровню достоверности.</span><span class="sxs-lookup"><span data-stu-id="bf628-109">Rank the alternates by confidence level.</span></span>

## <a name="what-affects-confidence"></a><span data-ttu-id="bf628-110">Что влияет на достоверность</span><span class="sxs-lookup"><span data-stu-id="bf628-110">What Affects Confidence</span></span>

<span data-ttu-id="bf628-111">Вот некоторые вещи, которые затрудняют распознавание рукописного текста и могут повлиять на достоверность:</span><span class="sxs-lookup"><span data-stu-id="bf628-111">Some of the things that make handwriting recognition difficult and affect confidence include:</span></span>

-   <span data-ttu-id="bf628-112">Трудности при определении сегментации слов</span><span class="sxs-lookup"><span data-stu-id="bf628-112">Difficulty determining word segmentation</span></span>

![изображение, показывающее, что запись слишком близка](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   <span data-ttu-id="bf628-114">Проблемы с вариантами</span><span class="sxs-lookup"><span data-stu-id="bf628-114">Case difficulties</span></span>

![изображение проблем с рукописными версиями слова "Case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   <span data-ttu-id="bf628-116">Нераспространенные стили письма</span><span class="sxs-lookup"><span data-stu-id="bf628-116">Uncommon writing styles</span></span>
-   <span data-ttu-id="bf628-117">Изолированные знаки препинания</span><span class="sxs-lookup"><span data-stu-id="bf628-117">Isolated punctuation</span></span>

![изображение, содержащее кавычки, которые находятся слишком далеко от текста](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   <span data-ttu-id="bf628-119">Символы с диакритическими знаками в распознавателях английского языка</span><span class="sxs-lookup"><span data-stu-id="bf628-119">Accented characters in English recognizers</span></span>

> [!Note]  
> <span data-ttu-id="bf628-120">Оценка достоверности доступна только для США английского и всех распознавателей жестов в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="bf628-120">Confidence evaluation is available only for United States English and all gesture recognizers in this release.</span></span> <span data-ttu-id="bf628-121">Методы, которые предоставляют свойство достоверности для любого другого распознавателя, возвращают **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="bf628-121">Methods that provide the confidence property for any other recognizer will return **E\_NOTIMPL**.</span></span>

 

 

 



