---
title: Иажентнотифисинк Баллунвисиблестате
description: Иажентнотифисинк Баллунвисиблестате
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700612"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a><span data-ttu-id="733a5-103">Иажентнотифисинк:: Баллунвисиблестате</span><span class="sxs-lookup"><span data-stu-id="733a5-103">IAgentNotifySink::BalloonVisibleState</span></span>

<span data-ttu-id="733a5-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="733a5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

<span data-ttu-id="733a5-105">Уведомляет клиентское приложение, когда изменяется состояние видимости всплывающего слова символа.</span><span class="sxs-lookup"><span data-stu-id="733a5-105">Notifies a client application when the visibility state of the character's word balloon changes.</span></span>

-   <span data-ttu-id="733a5-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="733a5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="733a5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="733a5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="733a5-108">Идентификатор символа, чье состояние видимости всплывающей подсказки слова изменилось.</span><span class="sxs-lookup"><span data-stu-id="733a5-108">Identifier of the character whose word balloon's visibility state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="733a5-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*</span><span class="sxs-lookup"><span data-stu-id="733a5-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="733a5-110">Флаг видимости.</span><span class="sxs-lookup"><span data-stu-id="733a5-110">Visibility flag.</span></span> <span data-ttu-id="733a5-111">Это логическое значение имеет **значение true** , когда отображается всплывающее сообщение слова "символ". и **false** , если он скрыт.</span><span class="sxs-lookup"><span data-stu-id="733a5-111">This Boolean value is **True** when character's word balloon becomes visible; and **False** when it becomes hidden.</span></span>

</dd> </dl>

<span data-ttu-id="733a5-112">Это событие отправляется всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="733a5-112">This event is sent to all clients of the character.</span></span>

 

 




