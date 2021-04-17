---
title: Иажентбаллун Жетфонтиталик
description: Иажентбаллун Жетфонтиталик
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710085"
---
# <a name="iagentballoongetfontitalic"></a><span data-ttu-id="1b783-103">Иажентбаллун:: Жетфонтиталик</span><span class="sxs-lookup"><span data-stu-id="1b783-103">IAgentBalloon::GetFontItalic</span></span>

<span data-ttu-id="1b783-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1b783-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

<span data-ttu-id="1b783-105">Указывает, является ли шрифт, используемый в выноске слова, курсивом.</span><span class="sxs-lookup"><span data-stu-id="1b783-105">Indicates whether the font used in a word balloon is italic.</span></span>

-   <span data-ttu-id="1b783-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1b783-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1b783-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*пбфонтиталик*</span><span class="sxs-lookup"><span data-stu-id="1b783-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span></span>
</dt> <dd>

<span data-ttu-id="1b783-108">Адрес значения, которое принимает значение **true** , если шрифт является курсивом, и **значение false** , если он не является курсивом.</span><span class="sxs-lookup"><span data-stu-id="1b783-108">The address of a value that receives **True** if the font is italic and **False** if not italic.</span></span>

</dd> </dl>

<span data-ttu-id="1b783-109">Стиль шрифта, используемый в подсказке к слову, определяется в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1b783-109">The font style used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1b783-110">Оно не может быть изменено приложением.</span><span class="sxs-lookup"><span data-stu-id="1b783-110">It cannot be changed by an application.</span></span> <span data-ttu-id="1b783-111">Однако пользователь может переопределить параметры шрифта для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1b783-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




