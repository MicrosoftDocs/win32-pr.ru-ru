---
title: Иажентбаллун Жетфонтнаме
description: Иажентбаллун Жетфонтнаме
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411360"
---
# <a name="iagentballoongetfontname"></a><span data-ttu-id="a1f73-103">Иажентбаллун:: Жетфонтнаме</span><span class="sxs-lookup"><span data-stu-id="a1f73-103">IAgentBalloon::GetFontName</span></span>

<span data-ttu-id="a1f73-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1f73-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

<span data-ttu-id="a1f73-105">Извлекает значение шрифта, отображаемого в тексте всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="a1f73-105">Retrieves the value for the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="a1f73-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a1f73-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a1f73-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*пбсзфонтнаме*</span><span class="sxs-lookup"><span data-stu-id="a1f73-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="a1f73-108">Адрес объекта BSTR, который получает имя шрифта, отображаемое в тексте всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="a1f73-108">The address of a BSTR that receives the font name displayed in a word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="a1f73-109">Шрифт по умолчанию, используемый в подсказке для символьного слова, определен в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a1f73-109">The default font used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a1f73-110">Его можно изменить с помощью [**иажентбаллун:: сетфонтнаме**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span><span class="sxs-lookup"><span data-stu-id="a1f73-110">You can change it with [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span></span> <span data-ttu-id="a1f73-111">Пользователь может переопределить параметр шрифта для всех символов с помощью страницы свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a1f73-111">The user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

 

 




