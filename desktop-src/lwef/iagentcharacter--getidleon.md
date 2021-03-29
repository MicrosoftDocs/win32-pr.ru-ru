---
title: Иажентчарактер Жетидлеон
description: Иажентчарактер Жетидлеон
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780129"
---
# <a name="iagentcharactergetidleon"></a><span data-ttu-id="69656-103">Иажентчарактер:: Жетидлеон</span><span class="sxs-lookup"><span data-stu-id="69656-103">IAgentCharacter::GetIdleOn</span></span>

<span data-ttu-id="69656-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="69656-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

<span data-ttu-id="69656-105">Указывает состояние обработки автоматического простоя для символа.</span><span class="sxs-lookup"><span data-stu-id="69656-105">Indicates the automatic idle processing state for a character.</span></span>

-   <span data-ttu-id="69656-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="69656-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="69656-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*пбон*</span><span class="sxs-lookup"><span data-stu-id="69656-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="69656-108">Адрес переменной, которая получает **значение true** , если сервер Microsoft Agent автоматически воспроизводит анимацию состояния **состояние простоя** для символа и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="69656-108">Address of a variable that receives **True** if the Microsoft Agent server automatically plays **Idling** state animations for a character and **False** if not.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="69656-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="69656-109">See Also</span></span>

[<span data-ttu-id="69656-110">**Иажентчарактер:: Сетидлеон**</span><span class="sxs-lookup"><span data-stu-id="69656-110">**IAgentCharacter::SetIdleOn**</span></span>](iagentcharacter--setidleon.md)


 

 




