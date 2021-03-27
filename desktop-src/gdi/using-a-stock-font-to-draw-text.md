---
description: Система предоставляет шесть стандартных шрифтов.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Использование шрифта акции для рисования текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999277"
---
# <a name="using-a-stock-font-to-draw-text"></a><span data-ttu-id="d09e2-103">Использование шрифта акции для рисования текста</span><span class="sxs-lookup"><span data-stu-id="d09e2-103">Using a Stock Font to Draw Text</span></span>

<span data-ttu-id="d09e2-104">Система предоставляет шесть стандартных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="d09e2-104">The system provides six stock fonts.</span></span> <span data-ttu-id="d09e2-105">Стандартный шрифт — это логический шрифт, который приложение может получить, вызвав функцию [жетстоккобжект](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) и указав требуемый шрифт.</span><span class="sxs-lookup"><span data-stu-id="d09e2-105">A stock font is a logical font that an application can obtain by calling the [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function and specifying the requested font.</span></span> <span data-ttu-id="d09e2-106">Следующий список содержит значения, которые можно указать для получения шрифта акции.</span><span class="sxs-lookup"><span data-stu-id="d09e2-106">The following list contains the values that you can specify to obtain a stock font.</span></span>



| <span data-ttu-id="d09e2-107">Значение</span><span class="sxs-lookup"><span data-stu-id="d09e2-107">Value</span></span>                 | <span data-ttu-id="d09e2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d09e2-108">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09e2-109">\_фиксированный \_ Шрифт ANSI</span><span class="sxs-lookup"><span data-stu-id="d09e2-109">ANSI\_FIXED\_FONT</span></span>     | <span data-ttu-id="d09e2-110">Задает шрифт с пробелом, основанный на кодировке Windows.</span><span class="sxs-lookup"><span data-stu-id="d09e2-110">Specifies a monospace font based on the Windows character set.</span></span> <span data-ttu-id="d09e2-111">Обычно используется шрифт Courier.</span><span class="sxs-lookup"><span data-stu-id="d09e2-111">A Courier font is typically used.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="d09e2-112">\_Шрифт ANSI var \_</span><span class="sxs-lookup"><span data-stu-id="d09e2-112">ANSI\_VAR\_FONT</span></span>       | <span data-ttu-id="d09e2-113">Задает пропорциональный шрифт, основанный на кодировке Windows.</span><span class="sxs-lookup"><span data-stu-id="d09e2-113">Specifies a proportional font based on the Windows character set.</span></span> <span data-ttu-id="d09e2-114">Обычно используется MS Sans Serif.</span><span class="sxs-lookup"><span data-stu-id="d09e2-114">MS Sans Serif is typically used.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="d09e2-115">\_Шрифт устройства по умолчанию \_</span><span class="sxs-lookup"><span data-stu-id="d09e2-115">DEVICE\_DEFAULT\_FONT</span></span> | <span data-ttu-id="d09e2-116">Указывает предпочтительный шрифт для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="d09e2-116">Specifies the preferred font for the specified device.</span></span> <span data-ttu-id="d09e2-117">Обычно это системный шрифт для устройств вывода. Однако для некоторых матричных принтеров это шрифт, находящийся на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d09e2-117">This is typically the System font for display devices; however, for some dot-matrix printers this is a font that is resident on the device.</span></span> <span data-ttu-id="d09e2-118">(Печать с этим шрифтом обычно выполняется быстрее, чем печать с помощью скачанного растрового шрифта).</span><span class="sxs-lookup"><span data-stu-id="d09e2-118">(Printing with this font is usually faster than printing with a downloaded, bitmap font).</span></span>    |
| <span data-ttu-id="d09e2-119">\_нефиксированный \_ Шрифт OEM</span><span class="sxs-lookup"><span data-stu-id="d09e2-119">OEM\_FIXED\_FONT</span></span>      | <span data-ttu-id="d09e2-120">Задает шрифт с пробелом, основанный на наборе символов OEM.</span><span class="sxs-lookup"><span data-stu-id="d09e2-120">Specifies a monospace font based on an OEM character set.</span></span> <span data-ttu-id="d09e2-121">Для компьютеров IBM и совместимых шрифтов OEM-версия основывается на кодировке IBM PC.</span><span class="sxs-lookup"><span data-stu-id="d09e2-121">For IBM computers and compatibles, the OEM font is based on the IBM PC character set.</span></span>                                                                                                                                                 |
| <span data-ttu-id="d09e2-122">СИСТЕМНЫЙ \_ Шрифт</span><span class="sxs-lookup"><span data-stu-id="d09e2-122">SYSTEM\_FONT</span></span>          | <span data-ttu-id="d09e2-123">Указывает системный шрифт.</span><span class="sxs-lookup"><span data-stu-id="d09e2-123">Specifies the System font.</span></span> <span data-ttu-id="d09e2-124">Это пропорциональный шрифт, основанный на кодировке Windows, и используется операционной системой для вывода заголовков окон, имен меню и текста в диалоговых окнах.</span><span class="sxs-lookup"><span data-stu-id="d09e2-124">This is a proportional font based on the Windows character set, and is used by the operating system to display window titles, menu names, and text in dialog boxes.</span></span> <span data-ttu-id="d09e2-125">Системный шрифт всегда доступен.</span><span class="sxs-lookup"><span data-stu-id="d09e2-125">The System font is always available.</span></span> <span data-ttu-id="d09e2-126">Другие шрифты доступны, только если они установлены.</span><span class="sxs-lookup"><span data-stu-id="d09e2-126">Other fonts are available only if they have been installed.</span></span> |
| <span data-ttu-id="d09e2-127">\_фиксированный системный \_ Шрифт</span><span class="sxs-lookup"><span data-stu-id="d09e2-127">SYSTEM\_FIXED\_FONT</span></span>   | <span data-ttu-id="d09e2-128">Задает в ранних версиях Windows шрифт в виде пробела, совместимый с системным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="d09e2-128">Specifies a monospace font compatible with the System font in early versions of Windows.</span></span>                                                                                                                                                                                                        |



 

<span data-ttu-id="d09e2-129">Дополнительные сведения о шрифтах см. в разделе [о шрифтах](about-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="d09e2-129">For more information on fonts, see [About Fonts](about-fonts.md).</span></span>

<span data-ttu-id="d09e2-130">В следующем примере показано получение маркера для шрифта переменной акции, его выбор в контексте устройства, а затем запись строки с использованием этого шрифта:</span><span class="sxs-lookup"><span data-stu-id="d09e2-130">The following example retrieves a handle to the variable stock font, selects it into a device context, and then writes a string using that font:</span></span>


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



<span data-ttu-id="d09e2-131">Если другие стандартные шрифты недоступны, [жетстоккобжект](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) возвращает маркер системного ШРИФТА (системный \_ Шрифт).</span><span class="sxs-lookup"><span data-stu-id="d09e2-131">If other stock fonts are not available, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) returns a handle to the System font (SYSTEM\_FONT).</span></span> <span data-ttu-id="d09e2-132">Стандартные шрифты следует использовать только в том случае, если в качестве режима сопоставления для контекста устройства приложения используется \_ текст mm.</span><span class="sxs-lookup"><span data-stu-id="d09e2-132">You should use stock fonts only if the mapping mode for your application's device context is MM\_TEXT.</span></span>

 

 



