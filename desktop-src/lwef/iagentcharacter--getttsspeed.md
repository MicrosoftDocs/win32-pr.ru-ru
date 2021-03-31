---
title: Иажентчарактер Жетттсспид
description: Иажентчарактер Жетттсспид
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411451"
---
# <a name="iagentcharactergetttsspeed"></a><span data-ttu-id="de93d-103">Иажентчарактер:: Жетттсспид</span><span class="sxs-lookup"><span data-stu-id="de93d-103">IAgentCharacter::GetTTSSpeed</span></span>

<span data-ttu-id="de93d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de93d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

<span data-ttu-id="de93d-105">Возвращает значение параметра "скорость вывода TTS" для символа.</span><span class="sxs-lookup"><span data-stu-id="de93d-105">Retrieves the character's TTS output speed setting.</span></span>

-   <span data-ttu-id="de93d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="de93d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="de93d-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*пдвспид*</span><span class="sxs-lookup"><span data-stu-id="de93d-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="de93d-108">Адрес переменной, которая получает выходную скорость символа в словах в минуту.</span><span class="sxs-lookup"><span data-stu-id="de93d-108">Address of a variable that receives the output speed of the character in words per minute.</span></span>

</dd> </dl>

<span data-ttu-id="de93d-109">Несмотря на то, что приложение не может записать это значение, в выходной текст можно включить Теги Speed, которые будут временно ускорить вывод для определенного utterance.</span><span class="sxs-lookup"><span data-stu-id="de93d-109">Although your application cannot write this value, you can include speed tags in your output text that will temporarily speed up the output for a particular utterance.</span></span>

<span data-ttu-id="de93d-110">Это свойство возвращает значение текущего параметра скорости вывода речи для символа.</span><span class="sxs-lookup"><span data-stu-id="de93d-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="de93d-111">Для символов, использующих вывод TTS, свойство возвращает фактические выходные данные TTS для символа.</span><span class="sxs-lookup"><span data-stu-id="de93d-111">For characters using TTS output, the property returns the actual TTS output for the character.</span></span> <span data-ttu-id="de93d-112">Если режим TTS не включен или символ не поддерживает вывод TTS, параметр отражает скорость вывода.</span><span class="sxs-lookup"><span data-stu-id="de93d-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

 

 




