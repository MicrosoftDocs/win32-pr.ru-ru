---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259056"
---
# <a name="iagentballoongetfontsize"></a><span data-ttu-id="15b5c-103">Иажентбаллун:: FontSize</span><span class="sxs-lookup"><span data-stu-id="15b5c-103">IAgentBalloon::GetFontSize</span></span>

<span data-ttu-id="15b5c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15b5c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

<span data-ttu-id="15b5c-105">Извлекает значение размера шрифта, отображаемого в подсказке к слову.</span><span class="sxs-lookup"><span data-stu-id="15b5c-105">Retrieves the value for the size of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="15b5c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="15b5c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="15b5c-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*плфонтсизе*</span><span class="sxs-lookup"><span data-stu-id="15b5c-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="15b5c-108">Адрес значения, получающего размер шрифта.</span><span class="sxs-lookup"><span data-stu-id="15b5c-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="15b5c-109">Размер шрифта по умолчанию, используемый в подсказке для символьного слова, определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="15b5c-109">The default font size used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="15b5c-110">Его можно изменить с помощью [**иажентбаллун:: сетфонтсизе**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span><span class="sxs-lookup"><span data-stu-id="15b5c-110">You can change it with [**IAgentBalloon::SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span></span> <span data-ttu-id="15b5c-111">Однако пользователь может переопределить параметры размера шрифта для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="15b5c-111">However, the user can override the font size settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




