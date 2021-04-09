---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889111"
---
# <a name="iagentballoongetvisible"></a><span data-ttu-id="c70f8-103">Иажентбаллун:: Visible</span><span class="sxs-lookup"><span data-stu-id="c70f8-103">IAgentBalloon::GetVisible</span></span>

<span data-ttu-id="c70f8-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c70f8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

<span data-ttu-id="c70f8-105">Определяет, отображается ли всплывающая подсказка слова как видимая или скрытая.</span><span class="sxs-lookup"><span data-stu-id="c70f8-105">Determines whether the word balloon is visible or hidden.</span></span>

-   <span data-ttu-id="c70f8-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c70f8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c70f8-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*</span><span class="sxs-lookup"><span data-stu-id="c70f8-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="c70f8-108">Адрес переменной, принимающей **значение true** , если всплывающая подсказка слова видима, и **значение false** , если оно скрыто.</span><span class="sxs-lookup"><span data-stu-id="c70f8-108">Address of a variable that receives **True** if the word balloon is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c70f8-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="c70f8-109">See Also</span></span>

[<span data-ttu-id="c70f8-110">**Иажентбаллун:: Сетвисибле**</span><span class="sxs-lookup"><span data-stu-id="c70f8-110">**IAgentBalloon::SetVisible**</span></span>](iagentballoon--setvisible.md)


 

 




