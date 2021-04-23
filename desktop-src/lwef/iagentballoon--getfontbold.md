---
title: Иажентбаллун Жетфонтболд
description: Иажентбаллун Жетфонтболд
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258587"
---
# <a name="iagentballoongetfontbold"></a><span data-ttu-id="90a0a-103">Иажентбаллун:: Жетфонтболд</span><span class="sxs-lookup"><span data-stu-id="90a0a-103">IAgentBalloon::GetFontBold</span></span>

<span data-ttu-id="90a0a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="90a0a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

<span data-ttu-id="90a0a-105">Указывает, является ли шрифт, используемый в выноске слова, полужирным.</span><span class="sxs-lookup"><span data-stu-id="90a0a-105">Indicates whether the font used in a word balloon is bold.</span></span>

-   <span data-ttu-id="90a0a-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="90a0a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="90a0a-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*пбфонтболд*</span><span class="sxs-lookup"><span data-stu-id="90a0a-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span></span>
</dt> <dd>

<span data-ttu-id="90a0a-108">Адрес значения, которое принимает значение **true** , если шрифт имеет полужирное начертание, и **значение false** , если он не является полужирным.</span><span class="sxs-lookup"><span data-stu-id="90a0a-108">The address of a value that receives **True** if the font is bold and **False** if not bold.</span></span>

</dd> </dl>

<span data-ttu-id="90a0a-109">Стиль шрифта, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="90a0a-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="90a0a-110">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="90a0a-110">It cannot be changed by an application.</span></span> <span data-ttu-id="90a0a-111">Однако пользователь может переопределить параметры шрифта для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="90a0a-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




