---
title: Иажентбаллун Жетбаккколор
description: Иажентбаллун Жетбаккколор
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068172"
---
# <a name="iagentballoongetbackcolor"></a><span data-ttu-id="e2d3a-103">Иажентбаллун:: Жетбаккколор</span><span class="sxs-lookup"><span data-stu-id="e2d3a-103">IAgentBalloon::GetBackColor</span></span>

<span data-ttu-id="e2d3a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e2d3a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

<span data-ttu-id="e2d3a-105">Извлекает значение цвета фона, отображаемого в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="e2d3a-105">Retrieves the value for the background color displayed in a word balloon.</span></span>

-   <span data-ttu-id="e2d3a-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e2d3a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e2d3a-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*плбгколор*</span><span class="sxs-lookup"><span data-stu-id="e2d3a-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span></span>
</dt> <dd>

<span data-ttu-id="e2d3a-108">Адрес переменной, которая получает параметр цвета для фона всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="e2d3a-108">The address of a variable that receives the color setting for the balloon background.</span></span>

</dd> </dl>

<span data-ttu-id="e2d3a-109">Цвет фона, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e2d3a-109">The background color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e2d3a-110">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="e2d3a-110">It cannot be changed by an application.</span></span> <span data-ttu-id="e2d3a-111">Однако пользователь может изменить цвет фона для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e2d3a-111">However, the user can change the background color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2d3a-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="e2d3a-112">See Also</span></span>

[<span data-ttu-id="e2d3a-113">**Иажентбаллун::/ForeColor**</span><span class="sxs-lookup"><span data-stu-id="e2d3a-113">**IAgentBalloon::GetForeColor**</span></span>](iagentballoon--getforecolor.md)


 

 




