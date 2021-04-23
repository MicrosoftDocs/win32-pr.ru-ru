---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710149"
---
# <a name="iagentballoongetforecolor"></a><span data-ttu-id="348f8-103">Иажентбаллун::/ForeColor</span><span class="sxs-lookup"><span data-stu-id="348f8-103">IAgentBalloon::GetForeColor</span></span>

<span data-ttu-id="348f8-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="348f8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

<span data-ttu-id="348f8-105">Извлекает значение цвета переднего плана, отображаемого в окне всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="348f8-105">Retrieves the value for the foreground color displayed in a word balloon.</span></span>

-   <span data-ttu-id="348f8-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="348f8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="348f8-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*плфгколор*</span><span class="sxs-lookup"><span data-stu-id="348f8-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span></span>
</dt> <dd>

<span data-ttu-id="348f8-108">Адрес переменной, получающей параметр цвета для переднего плана.</span><span class="sxs-lookup"><span data-stu-id="348f8-108">The address of a variable that receives the color setting for the balloon foreground.</span></span>

</dd> </dl>

<span data-ttu-id="348f8-109">Цвет переднего плана, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="348f8-109">The foreground color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="348f8-110">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="348f8-110">It cannot be changed by an application.</span></span> <span data-ttu-id="348f8-111">Однако пользователь может переопределить цвет переднего плана для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="348f8-111">However, the user can override the foreground color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="348f8-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="348f8-112">See Also</span></span>

[<span data-ttu-id="348f8-113">**Иажентбаллун:: Жетбаккколор**</span><span class="sxs-lookup"><span data-stu-id="348f8-113">**IAgentBalloon::GetBackColor**</span></span>](iagentballoon--getbackcolor.md)


 

 




