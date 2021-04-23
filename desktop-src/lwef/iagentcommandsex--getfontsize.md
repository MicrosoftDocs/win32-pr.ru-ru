---
title: Иаженткоммандсекс
description: Иаженткоммандсекс
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411055"
---
# <a name="iagentcommandsexgetfontsize"></a><span data-ttu-id="66d8f-103">Иаженткоммандсекс:: FontSize</span><span class="sxs-lookup"><span data-stu-id="66d8f-103">IAgentCommandsEx::GetFontSize</span></span>

<span data-ttu-id="66d8f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="66d8f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

<span data-ttu-id="66d8f-105">Извлекает значение размера шрифта, отображаемого во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="66d8f-105">Retrieves the value for the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="66d8f-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="66d8f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="66d8f-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*плфонтсизе*</span><span class="sxs-lookup"><span data-stu-id="66d8f-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="66d8f-108">Адрес значения, получающего размер шрифта.</span><span class="sxs-lookup"><span data-stu-id="66d8f-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="66d8f-109">Размер кегля возвращаемого шрифта соответствует размеру, определенному для отображения текста во всплывающем меню символа, если клиент является входным.</span><span class="sxs-lookup"><span data-stu-id="66d8f-109">The point size of the font returned corresponds to the size defined to display text in the character's pop-up menu when your client is input-active.</span></span> <span data-ttu-id="66d8f-110">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа, или если параметр не задан, используется пользовательский язык по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66d8f-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language setting.</span></span>

<span data-ttu-id="66d8f-111">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="66d8f-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="66d8f-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="66d8f-112">See Also</span></span>

<span data-ttu-id="66d8f-113">[**Иаженткоммандсекс:: сетфонтсизе**](iagentcommandsex--setfontsize.md), [ **иаженткоммандсекс:: сетфонтнаме**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="66d8f-113">[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 




