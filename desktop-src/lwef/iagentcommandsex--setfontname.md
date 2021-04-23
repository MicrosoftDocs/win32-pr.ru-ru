---
title: Иаженткоммандсекс Сетфонтнаме
description: Иаженткоммандсекс Сетфонтнаме
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773694"
---
# <a name="iagentcommandsexsetfontname"></a><span data-ttu-id="864af-103">Иаженткоммандсекс:: Сетфонтнаме</span><span class="sxs-lookup"><span data-stu-id="864af-103">IAgentCommandsEx::SetFontName</span></span>

<span data-ttu-id="864af-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="864af-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

<span data-ttu-id="864af-105">Задает шрифт, отображаемый во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="864af-105">Sets the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="864af-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="864af-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="864af-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*бсзфонтнаме*</span><span class="sxs-lookup"><span data-stu-id="864af-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="864af-108">Значение типа BSTR, которое задает шрифт, отображаемый во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="864af-108">A BSTR that sets the font displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="864af-109">Это свойство определяет шрифт, используемый для отображения текста во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="864af-109">This property determines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="864af-110">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа — или, если это не задано — параметр идентификатор языка пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="864af-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language ID setting.</span></span>

<span data-ttu-id="864af-111">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="864af-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="864af-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="864af-112">See Also</span></span>

<span data-ttu-id="864af-113">[**Иаженткоммандсекс:: жетфонтнаме**](iagentcommandsex--getfontname.md), [**Иаженткоммандсекс:: FontSize**](iagentcommandsex--getfontsize.md), [**иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="864af-113">[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




