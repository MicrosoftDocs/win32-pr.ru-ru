---
description: Эти значения используются с \_ композицией IME иммжеткомпоситионстринг и WM \_ .
ms.assetid: 14087598-8041-4e02-a168-f5538a437be0
title: Строковые значения композиции IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5b3935329e56f015cdb08a764e1660142a067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897686"
---
# <a name="ime-composition-string-values"></a><span data-ttu-id="134c5-103">Строковые значения композиции IME</span><span class="sxs-lookup"><span data-stu-id="134c5-103">IME Composition String Values</span></span>

<span data-ttu-id="134c5-104">Эти значения используются с [**\_ \_ композицией IME**](wm-ime-composition.md) [**иммжеткомпоситионстринг**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) и WM.</span><span class="sxs-lookup"><span data-stu-id="134c5-104">These values are used with [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) and [**WM\_IME\_COMPOSITION**](wm-ime-composition.md).</span></span>



| <span data-ttu-id="134c5-105">Значение</span><span class="sxs-lookup"><span data-stu-id="134c5-105">Value</span></span>                 | <span data-ttu-id="134c5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="134c5-106">Description</span></span>                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="134c5-107">\_КОМПАТТР GC</span><span class="sxs-lookup"><span data-stu-id="134c5-107">GCS\_COMPATTR</span></span>         | <span data-ttu-id="134c5-108">Извлечение или обновление атрибута строки композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-108">Retrieve or update the attribute of the composition string.</span></span>                                |
| <span data-ttu-id="134c5-109">\_КОМПКЛАУСЕ GC</span><span class="sxs-lookup"><span data-stu-id="134c5-109">GCS\_COMPCLAUSE</span></span>       | <span data-ttu-id="134c5-110">Получение или обновление сведений о предложении строки композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-110">Retrieve or update clause information of the composition string.</span></span>                           |
| <span data-ttu-id="134c5-111">\_КОМПРЕАДАТТР GC</span><span class="sxs-lookup"><span data-stu-id="134c5-111">GCS\_COMPREADATTR</span></span>     | <span data-ttu-id="134c5-112">Извлечение или обновление атрибутов строки чтения текущей композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-112">Retrieve or update the attributes of the reading string of the current composition.</span></span>        |
| <span data-ttu-id="134c5-113">\_КОМПРЕАДКЛАУСЕ GC</span><span class="sxs-lookup"><span data-stu-id="134c5-113">GCS\_COMPREADCLAUSE</span></span>   | <span data-ttu-id="134c5-114">Извлекает или обновляет сведения о предложении строки для чтения строки композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-114">Retrieve or update the clause information of the reading string of the composition string.</span></span> |
| <span data-ttu-id="134c5-115">\_КОМПРЕАДСТР GC</span><span class="sxs-lookup"><span data-stu-id="134c5-115">GCS\_COMPREADSTR</span></span>      | <span data-ttu-id="134c5-116">Извлечение или обновление строки чтения текущей композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-116">Retrieve or update the reading string of the current composition.</span></span>                          |
| <span data-ttu-id="134c5-117">\_КОМПСТР GC</span><span class="sxs-lookup"><span data-stu-id="134c5-117">GCS\_COMPSTR</span></span>          | <span data-ttu-id="134c5-118">Получение или обновление текущей строки композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-118">Retrieve or update the current composition string.</span></span>                                         |
| <span data-ttu-id="134c5-119">\_КУРСОРПОС GC</span><span class="sxs-lookup"><span data-stu-id="134c5-119">GCS\_CURSORPOS</span></span>        | <span data-ttu-id="134c5-120">Получение или обновление позиции курсора в строке композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-120">Retrieve or update the cursor position in composition string.</span></span>                              |
| <span data-ttu-id="134c5-121">\_ДЕЛТАСТАРТ GC</span><span class="sxs-lookup"><span data-stu-id="134c5-121">GCS\_DELTASTART</span></span>       | <span data-ttu-id="134c5-122">Возвращает или обновляет начальную точку любых изменений в строке композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-122">Retrieve or update the starting position of any changes in composition string.</span></span>             |
| <span data-ttu-id="134c5-123">\_РЕСУЛТКЛАУСЕ GC</span><span class="sxs-lookup"><span data-stu-id="134c5-123">GCS\_RESULTCLAUSE</span></span>     | <span data-ttu-id="134c5-124">Получение или обновление сведений о предложении результирующей строки.</span><span class="sxs-lookup"><span data-stu-id="134c5-124">Retrieve or update clause information of the result string.</span></span>                                |
| <span data-ttu-id="134c5-125">\_РЕСУЛТРЕАДКЛАУСЕ GC</span><span class="sxs-lookup"><span data-stu-id="134c5-125">GCS\_RESULTREADCLAUSE</span></span> | <span data-ttu-id="134c5-126">Получение или обновление сведений о предложении строки для чтения.</span><span class="sxs-lookup"><span data-stu-id="134c5-126">Retrieve or update clause information of the reading string.</span></span>                               |
| <span data-ttu-id="134c5-127">\_РЕСУЛТРЕАДСТР GC</span><span class="sxs-lookup"><span data-stu-id="134c5-127">GCS\_RESULTREADSTR</span></span>    | <span data-ttu-id="134c5-128">Извлечение или обновление строки чтения.</span><span class="sxs-lookup"><span data-stu-id="134c5-128">Retrieve or update the reading string.</span></span>                                                     |
| <span data-ttu-id="134c5-129">\_РЕСУЛТСТР GC</span><span class="sxs-lookup"><span data-stu-id="134c5-129">GCS\_RESULTSTR</span></span>        | <span data-ttu-id="134c5-130">Извлечение или обновление строки результата композиции.</span><span class="sxs-lookup"><span data-stu-id="134c5-130">Retrieve or update the string of the composition result.</span></span>                                   |



 

 

 



