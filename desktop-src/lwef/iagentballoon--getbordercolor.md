---
title: Иажентбаллун Жетбордерколор
description: Иажентбаллун Жетбордерколор
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777582"
---
# <a name="iagentballoongetbordercolor"></a><span data-ttu-id="5242e-103">Иажентбаллун:: Жетбордерколор</span><span class="sxs-lookup"><span data-stu-id="5242e-103">IAgentBalloon::GetBorderColor</span></span>

<span data-ttu-id="5242e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5242e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

<span data-ttu-id="5242e-105">Извлекает значение цвета границы, отображаемого для всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="5242e-105">Retrieves the value for the border color displayed for a word balloon.</span></span>

-   <span data-ttu-id="5242e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5242e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5242e-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*плбордерколор*</span><span class="sxs-lookup"><span data-stu-id="5242e-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span></span>
</dt> <dd>

<span data-ttu-id="5242e-108">Адрес переменной, получающей параметр цвета для границы всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="5242e-108">The address of a variable that receives the color setting for the balloon border.</span></span>

</dd> </dl>

<span data-ttu-id="5242e-109">Цвет границы для всплывающего слова символа определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5242e-109">The border color for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="5242e-110">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="5242e-110">It cannot be changed by an application.</span></span> <span data-ttu-id="5242e-111">Однако пользователь может изменить цвет границы для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5242e-111">However, the user can change the border color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="5242e-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="5242e-112">See Also</span></span>

<span data-ttu-id="5242e-113">[**Иажентбаллун:: жетбаккколор**](iagentballoon--getbackcolor.md), [ **иажентбаллун:: "ForeColor"**](iagentballoon--getforecolor.md)</span><span class="sxs-lookup"><span data-stu-id="5242e-113">[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)</span></span>


 

 




