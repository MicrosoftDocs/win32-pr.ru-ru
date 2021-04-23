---
title: Иажентбаллун Сетфонтсизе
description: Иажентбаллун Сетфонтсизе
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332248"
---
# <a name="iagentballoonsetfontsize"></a><span data-ttu-id="d0d92-103">Иажентбаллун:: Сетфонтсизе</span><span class="sxs-lookup"><span data-stu-id="d0d92-103">IAgentBalloon::SetFontSize</span></span>

<span data-ttu-id="d0d92-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0d92-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

<span data-ttu-id="d0d92-105">Задает размер шрифта, отображаемого в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="d0d92-105">Sets the size of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="d0d92-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d0d92-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d0d92-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*лфонтсизе*</span><span class="sxs-lookup"><span data-stu-id="d0d92-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="d0d92-108">Размер шрифта.</span><span class="sxs-lookup"><span data-stu-id="d0d92-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="d0d92-109">Размер шрифта по умолчанию, используемый в подсказке для символа, определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d0d92-109">The default font size used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="d0d92-110">Его можно изменить с помощью **иажентбаллун:: сетфонтсизе**.</span><span class="sxs-lookup"><span data-stu-id="d0d92-110">You can change it with **IAgentBalloon::SetFontSize**.</span></span> <span data-ttu-id="d0d92-111">Однако пользователь может переопределить параметр размера шрифта для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d0d92-111">However, the user can override the font size setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0d92-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="d0d92-112">See Also</span></span>

[<span data-ttu-id="d0d92-113">**Иажентбаллун:: FontSize**</span><span class="sxs-lookup"><span data-stu-id="d0d92-113">**IAgentBalloon::GetFontSize**</span></span>](iagentballoon--getfontsize.md)


 

 




