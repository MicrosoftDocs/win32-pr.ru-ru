---
title: Иажентбаллун Сетфонтнаме
description: Иажентбаллун Сетфонтнаме
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068559"
---
# <a name="iagentballoonsetfontname"></a><span data-ttu-id="0d075-103">Иажентбаллун:: Сетфонтнаме</span><span class="sxs-lookup"><span data-stu-id="0d075-103">IAgentBalloon::SetFontName</span></span>

<span data-ttu-id="0d075-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d075-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

<span data-ttu-id="0d075-105">Задает шрифт, отображаемый в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="0d075-105">Sets the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="0d075-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0d075-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d075-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*бсзфонтнаме*</span><span class="sxs-lookup"><span data-stu-id="0d075-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="0d075-108">Значение типа BSTR, которое задает шрифт, отображаемый в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="0d075-108">A BSTR that sets the font displayed in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="0d075-109">Шрифт по умолчанию, используемый в подсказке для символа, определен в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0d075-109">The default font used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0d075-110">Его можно изменить с помощью **иажентбаллун:: сетфонтнаме**.</span><span class="sxs-lookup"><span data-stu-id="0d075-110">You can change it with **IAgentBalloon::SetFontName**.</span></span> <span data-ttu-id="0d075-111">Однако пользователь может переопределить параметр шрифта для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0d075-111">However, the user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d075-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d075-112">See Also</span></span>

[<span data-ttu-id="0d075-113">**Иажентбаллун:: Visible**</span><span class="sxs-lookup"><span data-stu-id="0d075-113">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




