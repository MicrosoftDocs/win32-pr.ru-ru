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
# <a name="loading-character-and-animation-data"></a>Загрузка данных символов и анимации

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

После получения указателя на интерфейс [**иажентекс**](iagentex.md) можно использовать метод [**Load**](load-method.md) для загрузки символа и получения его интерфейса [**иажентчарактерекс**](iagentcharacterex.md) . Существует три различных варианта пути загрузки символа. Первый из них совместим с Microsoft Agent 1,5, где указанный путь представляет собой полный путь и имя файла символов. Вторая возможность — указать только имя файла, в этом случае агент ищет его в каталоге chars. Последняя возможность — предоставить пустой параметр Variant, который вызывает загрузку символа по умолчанию.


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



Этот интерфейс можно использовать для доступа к методам символа:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Если службы агента Майкрософт больше не нужны, например при завершении работы клиентского приложения, освободите его интерфейсы. Обратите внимание, что освобождение символьного интерфейса не приводит к выгрузке символа. Вызовите метод [**unload**](unload-method.md) , чтобы сделать это перед освобождением интерфейса [**иажентекс**](iagentex.md) :


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



 

 




