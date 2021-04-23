---
title: Использование функции PlaySound для цикла звуков
description: Использование функции PlaySound для цикла звуков
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- волна Audio, функция PlaySound
- звуковая волна, циклический перебор звуков
- волна Audio, параметр Фдвсаунд
- Функция PlaySound, циклическое воспроизведение звуков
- Функция PlaySound, параметр Фдвсаунд
- Циклическая волна-звук
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412789"
---
# <a name="using-playsound-to-loop-sounds"></a><span data-ttu-id="2b21e-109">Использование функции PlaySound для цикла звуков</span><span class="sxs-lookup"><span data-stu-id="2b21e-109">Using PlaySound to Loop Sounds</span></span>

<span data-ttu-id="2b21e-110">Если \_ для параметра фдвсаунд функции PlaySound заданы флаги «цикл snd» и «snd \_ Async», звук будет продолжать воспроизводиться повторно, как показано в следующем примере:  [](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b21e-110">If you specify the SND\_LOOP and SND\_ASYNC flags for the *fdwSound* parameter of the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function, the sound will continue to play repeatedly as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



<span data-ttu-id="2b21e-111">Если требуется циклически прокручивать звук, необходимо воспроизвести его асинхронно; нельзя использовать \_ флаг синхронизации snd с \_ флагом цикла snd.</span><span class="sxs-lookup"><span data-stu-id="2b21e-111">If you want to loop a sound, you must play it asynchronously; you cannot use the SND\_SYNC flag with the SND\_LOOP flag.</span></span> <span data-ttu-id="2b21e-112">Циклический звук будет воспроизводиться до тех пор, пока не будет вызвана **PlaySound** для воспроизведения другого звука.</span><span class="sxs-lookup"><span data-stu-id="2b21e-112">A looped sound will continue to play until you call **PlaySound** to play another sound.</span></span> <span data-ttu-id="2b21e-113">Чтобы предотвратить воспроизведение звука (циклический или асинхронный) без воспроизведения другого звука, используйте следующую инструкцию:</span><span class="sxs-lookup"><span data-stu-id="2b21e-113">To stop playing a sound (looped or asynchronous) without playing another sound, use the following statement:</span></span>


```C++
PlaySound(NULL, NULL, 0); 
```



 

 