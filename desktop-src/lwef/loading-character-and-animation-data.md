---
title: Загрузка данных символов и анимации
description: Загрузка данных символов и анимации
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700645"
---
# <a name="loading-character-and-animation-data"></a><span data-ttu-id="ad511-103">Загрузка данных символов и анимации</span><span class="sxs-lookup"><span data-stu-id="ad511-103">Loading Character and Animation Data</span></span>

<span data-ttu-id="ad511-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ad511-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="ad511-105">После получения указателя на интерфейс [**иажентекс**](iagentex.md) можно использовать метод [**Load**](load-method.md) для загрузки символа и получения его интерфейса [**иажентчарактерекс**](iagentcharacterex.md) .</span><span class="sxs-lookup"><span data-stu-id="ad511-105">After you have a pointer to the [**IAgentEx**](iagentex.md) interface, you can use the [**Load**](load-method.md) method to load a character and retrieve its [**IAgentCharacterEx**](iagentcharacterex.md) interface.</span></span> <span data-ttu-id="ad511-106">Существует три различных варианта пути загрузки символа.</span><span class="sxs-lookup"><span data-stu-id="ad511-106">There are three different possibilities for the Load path of a character.</span></span> <span data-ttu-id="ad511-107">Первый из них совместим с Microsoft Agent 1,5, где указанный путь представляет собой полный путь и имя файла символов.</span><span class="sxs-lookup"><span data-stu-id="ad511-107">The first is compatible with Microsoft Agent 1.5 where the specified path is the full path and filename of a character file.</span></span> <span data-ttu-id="ad511-108">Вторая возможность — указать только имя файла, в этом случае агент ищет его в каталоге chars.</span><span class="sxs-lookup"><span data-stu-id="ad511-108">The second possibility is to specify the filename only, in which case, Agent looks in its Chars directory.</span></span> <span data-ttu-id="ad511-109">Последняя возможность — предоставить пустой параметр Variant, который вызывает загрузку символа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad511-109">The last possibility is to supply an empty Variant parameter that causes the default character to be loaded.</span></span>


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



<span data-ttu-id="ad511-110">Этот интерфейс можно использовать для доступа к методам символа:</span><span class="sxs-lookup"><span data-stu-id="ad511-110">You can use this interface to access the character's methods:</span></span>


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



<span data-ttu-id="ad511-111">Если службы агента Майкрософт больше не нужны, например при завершении работы клиентского приложения, освободите его интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ad511-111">When you no longer need Microsoft Agent services, such as when your client application shuts down, release its interfaces.</span></span> <span data-ttu-id="ad511-112">Обратите внимание, что освобождение символьного интерфейса не приводит к выгрузке символа.</span><span class="sxs-lookup"><span data-stu-id="ad511-112">Note that releasing the character interface does not unload the character.</span></span> <span data-ttu-id="ad511-113">Вызовите метод [**unload**](unload-method.md) , чтобы сделать это перед освобождением интерфейса [**иажентекс**](iagentex.md) :</span><span class="sxs-lookup"><span data-stu-id="ad511-113">Call the [**Unload**](unload-method.md) method to do this before releasing the [**IAgentEx**](iagentex.md) interface:</span></span>


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




