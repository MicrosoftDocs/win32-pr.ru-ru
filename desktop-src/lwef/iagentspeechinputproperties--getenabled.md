---
title: Иажентспичинпутпропертиес
description: Иажентспичинпутпропертиес
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772542"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a><span data-ttu-id="252af-103">Иажентспичинпутпропертиес:: enable</span><span class="sxs-lookup"><span data-stu-id="252af-103">IAgentSpeechInputProperties::GetEnabled</span></span>

<span data-ttu-id="252af-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="252af-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

<span data-ttu-id="252af-105">Извлекает значение, указывающее, включен ли установленный модуль распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="252af-105">Retrieves a value indicating whether the installed speech recognition engine is enabled.</span></span>

-   <span data-ttu-id="252af-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="252af-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="252af-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*</span><span class="sxs-lookup"><span data-stu-id="252af-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="252af-108">Адрес переменной, принимающей **значение true** , если в настоящий момент включен модуль распознавания речи, и **значение false** , если оно отключено.</span><span class="sxs-lookup"><span data-stu-id="252af-108">Address of a variable that receives **True** if the speech engine is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

 

 




