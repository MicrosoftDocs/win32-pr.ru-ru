---
title: Иажентнотифисинк Активатеинпутстате
description: Иажентнотифисинк Активатеинпутстате
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258759"
---
# <a name="iagentnotifysinkactivateinputstate"></a><span data-ttu-id="0ed8b-103">Иажентнотифисинк:: Активатеинпутстате</span><span class="sxs-lookup"><span data-stu-id="0ed8b-103">IAgentNotifySink::ActivateInputState</span></span>

<span data-ttu-id="0ed8b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ed8b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

<span data-ttu-id="0ed8b-105">Уведомляет клиентское приложение о том, что введенное значение активного состояния ввода символа изменилось.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-105">Notifies a client application that a character's input active state changed.</span></span>

-   <span data-ttu-id="0ed8b-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="0ed8b-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="0ed8b-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="0ed8b-108">Идентификатор символа, состояние активации которого изменилось.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-108">Identifier of the character whose input activation state changed.</span></span>

</dd> <dt>

<span data-ttu-id="0ed8b-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*бактиватед*</span><span class="sxs-lookup"><span data-stu-id="0ed8b-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span></span>
</dt> <dd>

<span data-ttu-id="0ed8b-110">Входной флаг активности.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-110">Input active flag.</span></span> <span data-ttu-id="0ed8b-111">Это логическое значение равно **true** , если символ, на который ссылается *двчарид* , стал активным входным. и **false** , если символ потерял активное состояние входа.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-111">This Boolean value is **True** if the character referred to by *dwCharID* became input active; and **False** if the character lost its input active state.</span></span>

</dd> </dl>

 

 




