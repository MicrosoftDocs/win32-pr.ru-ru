---
title: Иажентчарактер Жетттспитч
description: Иажентчарактер Жетттспитч
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691388"
---
# <a name="iagentcharactergetttspitch"></a><span data-ttu-id="c5922-103">Иажентчарактер:: Жетттспитч</span><span class="sxs-lookup"><span data-stu-id="c5922-103">IAgentCharacter::GetTTSPitch</span></span>

<span data-ttu-id="c5922-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5922-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

<span data-ttu-id="c5922-105">Извлекает значение параметра "выходные данные" TTS для символа.</span><span class="sxs-lookup"><span data-stu-id="c5922-105">Retrieves the character's TTS output pitch setting.</span></span>

-   <span data-ttu-id="c5922-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c5922-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c5922-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*пдвпитч*</span><span class="sxs-lookup"><span data-stu-id="c5922-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span></span>
</dt> <dd>

<span data-ttu-id="c5922-108">Адрес переменной, которая получает текущий параметр TTS для текущего символа в герцах.</span><span class="sxs-lookup"><span data-stu-id="c5922-108">Address of a variable that receives the character's current TTS pitch setting in Hertz.</span></span>

</dd> </dl>

<span data-ttu-id="c5922-109">Несмотря на то, что приложение не может записать это значение, в выходной текст можно включить Теги кувшина, которые будут временно увеличивать шаг для конкретного utterance.</span><span class="sxs-lookup"><span data-stu-id="c5922-109">Although your application cannot write this value, you can include pitch tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="c5922-110">Этот метод применяется только к символам, настроенным для вывода TTS.</span><span class="sxs-lookup"><span data-stu-id="c5922-110">This method applies only to characters configured for TTS output.</span></span> <span data-ttu-id="c5922-111">Если подсистема синтеза речи (TTS) не включена (или не установлена) или символ не поддерживает вывод TTS, этот метод возвращает ноль (0).</span><span class="sxs-lookup"><span data-stu-id="c5922-111">If the speech synthesis (TTS) engine is not enabled (or installed) or the character does not support TTS output, this method returns zero (0).</span></span>

 

 




