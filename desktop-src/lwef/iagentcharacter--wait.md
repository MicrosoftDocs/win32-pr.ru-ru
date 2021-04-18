---
title: Иажентчарактер ожидания
description: Иажентчарактер ожидания
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331411"
---
# <a name="iagentcharacterwait"></a><span data-ttu-id="c77b1-103">Иажентчарактер:: wait</span><span class="sxs-lookup"><span data-stu-id="c77b1-103">IAgentCharacter::Wait</span></span>

<span data-ttu-id="c77b1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c77b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="c77b1-105">Содержит очередь анимации символа в указанной анимации (запрос) до завершения другого запроса другого символа.</span><span class="sxs-lookup"><span data-stu-id="c77b1-105">Holds the character's animation queue at the specified animation (request) until another request for another character completes.</span></span>

-   <span data-ttu-id="c77b1-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c77b1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c77b1-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*дврекид*</span><span class="sxs-lookup"><span data-stu-id="c77b1-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c77b1-108">Идентификатор запроса для ожидания.</span><span class="sxs-lookup"><span data-stu-id="c77b1-108">The ID of the request to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="c77b1-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*</span><span class="sxs-lookup"><span data-stu-id="c77b1-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c77b1-110">Адрес переменной, которая получает идентификатор запроса на **Ожидание** .</span><span class="sxs-lookup"><span data-stu-id="c77b1-110">Address of a variable that receives the **Wait** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="c77b1-111">Этот метод следует использовать только в том случае, если поддерживается несколько (одновременных) символов и требуется последовательное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="c77b1-111">Use this method only when you support multiple (simultaneous) characters and want to sequence their interaction.</span></span> <span data-ttu-id="c77b1-112">(Для одного символа каждый запрос анимации воспроизводится последовательно — по завершении предыдущего запроса.) Если у вас есть два символа и требуется, чтобы запрос анимации одного символа дождался до завершения анимации другого символа, присвойте методу **Wait** идентификатор запроса анимации другого символа.</span><span class="sxs-lookup"><span data-stu-id="c77b1-112">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and want one character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation request ID.</span></span>

 

 




