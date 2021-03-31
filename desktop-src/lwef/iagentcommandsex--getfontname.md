---
title: Иаженткоммандсекс Жетфонтнаме
description: Иаженткоммандсекс Жетфонтнаме
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411056"
---
# <a name="iagentcommandsexgetfontname"></a><span data-ttu-id="3209b-103">Иаженткоммандсекс:: Жетфонтнаме</span><span class="sxs-lookup"><span data-stu-id="3209b-103">IAgentCommandsEx::GetFontName</span></span>

<span data-ttu-id="3209b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3209b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

<span data-ttu-id="3209b-105">Извлекает значение шрифта, отображаемого во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="3209b-105">Retrieves the value for the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="3209b-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3209b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3209b-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*пбсзфонтнаме*</span><span class="sxs-lookup"><span data-stu-id="3209b-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="3209b-108">Адрес BSTR, который получает имя шрифта, отображаемое во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="3209b-108">The address of a BSTR that receives the font name displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="3209b-109">Возвращаемое имя шрифта соответствует шрифту, используемому для отображения текста во всплывающем меню символа, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="3209b-109">The font name returned corresponds to the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="3209b-110">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа, или если параметр не задан, используется идентификатор языка пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3209b-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language ID setting.</span></span>

<span data-ttu-id="3209b-111">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="3209b-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="3209b-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="3209b-112">See Also</span></span>

<span data-ttu-id="3209b-113">[**Иаженткоммандсекс:: сетфонтнаме**](iagentcommandsex--setfontname.md), [ **иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="3209b-113">[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




