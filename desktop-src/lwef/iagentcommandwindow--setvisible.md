---
title: Иаженткоммандвиндов Сетвисибле
description: Иаженткоммандвиндов Сетвисибле
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068170"
---
# <a name="iagentcommandwindowsetvisible"></a><span data-ttu-id="e01ec-103">Иаженткоммандвиндов:: Сетвисибле</span><span class="sxs-lookup"><span data-stu-id="e01ec-103">IAgentCommandWindow::SetVisible</span></span>

<span data-ttu-id="e01ec-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e01ec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

<span data-ttu-id="e01ec-105">Установите свойство [**Visible**](visible-property.md) для окна "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="e01ec-105">Set the [**Visible**](visible-property.md) property for the Voice Commands Window.</span></span>

-   <span data-ttu-id="e01ec-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e01ec-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e01ec-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*</span><span class="sxs-lookup"><span data-stu-id="e01ec-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="e01ec-108">Параметр [**видимого**](visible-property.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="e01ec-108">[**Visible**](visible-property.md) property setting.</span></span> <span data-ttu-id="e01ec-109">Значение **true** отображает окно "Voice Commands"; **Значение false** скрывает его.</span><span class="sxs-lookup"><span data-stu-id="e01ec-109">A value of **True** displays the Voice Commands Window; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="e01ec-110">Пользователь может переопределить это свойство.</span><span class="sxs-lookup"><span data-stu-id="e01ec-110">The user can override this property.</span></span>

## <a name="see-also"></a><span data-ttu-id="e01ec-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="e01ec-111">See Also</span></span>

[<span data-ttu-id="e01ec-112">**Иаженткоммандвиндов:: Visible**</span><span class="sxs-lookup"><span data-stu-id="e01ec-112">**IAgentCommandWindow::GetVisible**</span></span>](iagentcommandwindow--getvisible.md)


 

 




