---
title: Иаженткоммандсекс Сетфонтсизе
description: Иаженткоммандсекс Сетфонтсизе
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487592"
---
# <a name="iagentcommandsexsetfontsize"></a><span data-ttu-id="c6f9d-103">Иаженткоммандсекс:: Сетфонтсизе</span><span class="sxs-lookup"><span data-stu-id="c6f9d-103">IAgentCommandsEx::SetFontSize</span></span>

<span data-ttu-id="c6f9d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6f9d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

<span data-ttu-id="c6f9d-105">Задает размер шрифта, отображаемого во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="c6f9d-105">Sets the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="c6f9d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c6f9d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c6f9d-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*лфонтсизе*</span><span class="sxs-lookup"><span data-stu-id="c6f9d-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="c6f9d-108">Размер шрифта.</span><span class="sxs-lookup"><span data-stu-id="c6f9d-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="c6f9d-109">Это свойство определяет размер шрифта, используемого для отображения текста во всплывающем меню символа, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="c6f9d-109">This property determines the point size of the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="c6f9d-110">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра идентификатор языка символа — или, если это не задано — пользовательский параметр языка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6f9d-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language setting.</span></span> <span data-ttu-id="c6f9d-111">Если вход не активен, текст [**заголовка**](caption-property.md) [**команды**](/windows/desktop/lwef/the-command-object) клиентского приложения отображается в кегле, указанном для клиента input-Active.</span><span class="sxs-lookup"><span data-stu-id="c6f9d-111">If not input-active, your client application's [**Command**](/windows/desktop/lwef/the-command-object) [**Caption**](caption-property.md) text appears in the point size specified for the input-active client.</span></span>

<span data-ttu-id="c6f9d-112">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="c6f9d-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6f9d-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="c6f9d-113">See Also</span></span>

<span data-ttu-id="c6f9d-114">[**Иаженткоммандсекс:: FontSize**](iagentcommandsex--getfontsize.md), [**Иаженткоммандсекс:: жетфонтнаме**](iagentcommandsex--getfontname.md), [**иаженткоммандсекс:: сетфонтнаме**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="c6f9d-114">[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 