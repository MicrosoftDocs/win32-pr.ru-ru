---
title: Иажентчарактер Жетекстрадата
description: Иажентчарактер Жетекстрадата
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133054"
---
# <a name="iagentcharactergetextradata"></a><span data-ttu-id="92e7d-103">Иажентчарактер:: Жетекстрадата</span><span class="sxs-lookup"><span data-stu-id="92e7d-103">IAgentCharacter::GetExtraData</span></span>

<span data-ttu-id="92e7d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="92e7d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

<span data-ttu-id="92e7d-105">Извлекает дополнительные данные, хранящиеся как часть символа.</span><span class="sxs-lookup"><span data-stu-id="92e7d-105">Retrieves additional data stored as part of the character.</span></span>

-   <span data-ttu-id="92e7d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="92e7d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="92e7d-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*пбсзекстрадата*</span><span class="sxs-lookup"><span data-stu-id="92e7d-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span></span>
</dt> <dd>

<span data-ttu-id="92e7d-108">Адрес объекта BSTR, который получает значение дополнительных данных для символа.</span><span class="sxs-lookup"><span data-stu-id="92e7d-108">The address of a BSTR that receives the value of the additional data for the character.</span></span> <span data-ttu-id="92e7d-109">Дополнительные данные символов определяются при компиляции с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="92e7d-109">A character's additional data is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="92e7d-110">Разработчик символов может предоставить эту строку, отредактировав. Файл ACD для символа.</span><span class="sxs-lookup"><span data-stu-id="92e7d-110">A character developer can supply this string by editing the .ACD file for a character.</span></span> <span data-ttu-id="92e7d-111">Этот параметр является необязательным и может быть не указан для всех символов, а также не может быть определен или изменен во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="92e7d-111">The setting is optional and may not be supplied for all characters, nor can the data be defined or changed at run time.</span></span> <span data-ttu-id="92e7d-112">Кроме того, значение предоставленных данных определяется разработчиком символов.</span><span class="sxs-lookup"><span data-stu-id="92e7d-112">In addition, the meaning of the data supplied is defined by the character developer.</span></span>

</dd> </dl>

 

 




