---
title: Иажентчарактер Хасосерклиентс
description: Иажентчарактер Хасосерклиентс
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532501"
---
# <a name="iagentcharacterhasotherclients"></a><span data-ttu-id="253a4-103">Иажентчарактер:: Хасосерклиентс</span><span class="sxs-lookup"><span data-stu-id="253a4-103">IAgentCharacter::HasOtherClients</span></span>

<span data-ttu-id="253a4-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="253a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

<span data-ttu-id="253a4-105">Возвращает значение, указывающее, есть ли у символа другие клиенты.</span><span class="sxs-lookup"><span data-stu-id="253a4-105">Retrieves whether a character has other clients.</span></span>

-   <span data-ttu-id="253a4-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="253a4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="253a4-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*плнумосерклиентс*</span><span class="sxs-lookup"><span data-stu-id="253a4-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span></span>
</dt> <dd>

<span data-ttu-id="253a4-108">Адрес переменной, которая получает число других подключенных клиентов для символа (общее число клиентов за вычетом клиента).</span><span class="sxs-lookup"><span data-stu-id="253a4-108">Address of a variable that receives the number of other connected clients for the character (total number of clients minus your client).</span></span>

</dd> </dl>

 

 




