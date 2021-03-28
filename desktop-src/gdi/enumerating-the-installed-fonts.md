---
description: В некоторых случаях приложение должно иметь возможность перечислить доступные шрифты и выбрать один из них, наиболее подходящий для конкретной операции.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Перечисление установленных шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263682"
---
# <a name="enumerating-the-installed-fonts"></a><span data-ttu-id="a604d-103">Перечисление установленных шрифтов</span><span class="sxs-lookup"><span data-stu-id="a604d-103">Enumerating the Installed Fonts</span></span>

<span data-ttu-id="a604d-104">В некоторых случаях приложение должно иметь возможность перечислить доступные шрифты и выбрать один из них, наиболее подходящий для конкретной операции.</span><span class="sxs-lookup"><span data-stu-id="a604d-104">In some instances, an application must be able to enumerate the available fonts and select the one most appropriate for a particular operation.</span></span> <span data-ttu-id="a604d-105">Приложение может перечислить доступные шрифты, вызвав функцию [енумфонтс](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) или [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) .</span><span class="sxs-lookup"><span data-stu-id="a604d-105">An application can enumerate the available fonts by calling the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) or [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function.</span></span> <span data-ttu-id="a604d-106">Эти функции отправляют сведения о доступных шрифтах в функцию обратного вызова, которую предоставляет приложение.</span><span class="sxs-lookup"><span data-stu-id="a604d-106">These functions send information about the available fonts to a callback function that the application supplies.</span></span> <span data-ttu-id="a604d-107">Функция обратного вызова получает сведения в структурах [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) и [невтекстметрик](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="a604d-107">The callback function receives information in [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) and [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structures.</span></span> <span data-ttu-id="a604d-108">(Структура [**невтекстметрик**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) содержит сведения о шрифте TrueType.</span><span class="sxs-lookup"><span data-stu-id="a604d-108">(The [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure contains information about a TrueType font.</span></span> <span data-ttu-id="a604d-109">Когда функция ответного вызова получает сведения о шрифте, отличном от TrueType, сведения содержатся в структуре [текстметрик](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .) С помощью этих сведений приложение может ограничить выбор пользователей только доступными шрифтами.</span><span class="sxs-lookup"><span data-stu-id="a604d-109">When the callback function receives information about a non-TrueType font, the information is contained in a [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.) By using this information, an application can limit the user's choices to only those fonts that are available.</span></span>

<span data-ttu-id="a604d-110">Функция [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) похожа на функцию [**енумфонтс**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) , но включает некоторые дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="a604d-110">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function is similar to the [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) function but includes some extra functionality.</span></span> <span data-ttu-id="a604d-111">**EnumFontFamilies** позволяет приложению использовать стили, доступные в шрифтах TrueType.</span><span class="sxs-lookup"><span data-stu-id="a604d-111">**EnumFontFamilies** allows an application to take advantage of styles available with TrueType fonts.</span></span> <span data-ttu-id="a604d-112">Новые и обновленные приложения должны использовать **EnumFontFamilies** вместо **енумфонтс**.</span><span class="sxs-lookup"><span data-stu-id="a604d-112">New and upgraded applications should use **EnumFontFamilies** instead of **EnumFonts**.</span></span>

<span data-ttu-id="a604d-113">Шрифты TrueType организованы по имени гарнитуры (например, Courier New) и именам стилей (например, курсив, полужирный шрифт и жирный шрифт).</span><span class="sxs-lookup"><span data-stu-id="a604d-113">TrueType fonts are organized around a typeface name (for example, Courier New) and style names (for example, italic, bold, and extra-bold).</span></span> <span data-ttu-id="a604d-114">Функция [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) перечисляет все стили, связанные с указанным именем семейства, а не просто атрибуты Bold и Italic.</span><span class="sxs-lookup"><span data-stu-id="a604d-114">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function enumerates all the styles associated with a specified family name, not simply the bold and italic attributes.</span></span> <span data-ttu-id="a604d-115">Например, если система включает шрифт TrueType с названием Courier New, то **EnumFontFamilies** переводит его в список новых шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a604d-115">For example, when the system includes a TrueType font called Courier New Extra-Bold, **EnumFontFamilies** lists it with the other Courier New fonts.</span></span> <span data-ttu-id="a604d-116">Возможности **EnumFontFamilies** полезны для шрифтов с множеством или необычными стилями и для шрифтов, пересекающих международные границы.</span><span class="sxs-lookup"><span data-stu-id="a604d-116">The capabilities of **EnumFontFamilies** are helpful for fonts with many or unusual styles and for fonts that cross international borders.</span></span>

<span data-ttu-id="a604d-117">Если приложение не предоставляет имя гарнитуры, функции [енумфонтс](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) и [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) предоставляют сведения о одном шрифте в каждом доступном семействе.</span><span class="sxs-lookup"><span data-stu-id="a604d-117">If an application does not supply a typeface name, the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions supply information about one font in each available family.</span></span> <span data-ttu-id="a604d-118">Чтобы перечислить все шрифты в контексте устройства, в приложении можно указать **значение NULL** для имени гарнитуры, скомпилировать список доступных гарнитур, а затем перечислить каждый шрифт в каждой гарнитуре.</span><span class="sxs-lookup"><span data-stu-id="a604d-118">To enumerate all the fonts in a device context, the application can specify **NULL** for the typeface name, compile a list of the available typefaces, and then enumerate each font in each typeface.</span></span>

<span data-ttu-id="a604d-119">В следующем примере функция [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) используется для получения количества доступных растровых, векторных и шрифтовых семейств шрифтов TrueType.</span><span class="sxs-lookup"><span data-stu-id="a604d-119">The following example uses the [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function to retrieve the number of available raster, vector, and TrueType font families.</span></span>


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



<span data-ttu-id="a604d-120">В этом примере используются две маски, РАСТРОВые \_ фонттипе и TRUETYPE \_ фонттипе, чтобы определить тип перечисляемого шрифта.</span><span class="sxs-lookup"><span data-stu-id="a604d-120">This example uses two masks, RASTER\_FONTTYPE and TRUETYPE\_FONTTYPE, to determine the type of font being enumerated.</span></span> <span data-ttu-id="a604d-121">Если задан РАСТРОВый \_ бит фонттипе, то шрифт является растровым шрифтом.</span><span class="sxs-lookup"><span data-stu-id="a604d-121">If the RASTER\_FONTTYPE bit is set, the font is a raster font.</span></span> <span data-ttu-id="a604d-122">Если \_ установлен бит TrueType фонттипе, шрифт будет шрифтом TrueType.</span><span class="sxs-lookup"><span data-stu-id="a604d-122">If the TRUETYPE\_FONTTYPE bit is set, the font is a TrueType font.</span></span> <span data-ttu-id="a604d-123">Если ни один из битов не задан, то шрифт является векторным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="a604d-123">If neither bit is set, the font is a vector font.</span></span> <span data-ttu-id="a604d-124">Третья маска, фонттипе устройства \_ , задается, когда устройство (например, лазерный принтер) поддерживает загрузку шрифтов TrueType; оно равно нулю, если устройство является видеоадаптером, точечным принтером или другим растровым устройством.</span><span class="sxs-lookup"><span data-stu-id="a604d-124">A third mask, DEVICE\_FONTTYPE, is set when a device (for example, a laser printer) supports downloading TrueType fonts; it is zero if the device is a display adapter, dot-matrix printer, or other raster device.</span></span> <span data-ttu-id="a604d-125">Приложение также может использовать \_ маску фонттипеа устройства для различения предоставляемых GDI растровых шрифтов от шрифтов, предоставляемых устройством.</span><span class="sxs-lookup"><span data-stu-id="a604d-125">An application can also use the DEVICE\_FONTTYPE mask to distinguish GDI-supplied raster fonts from device-supplied fonts.</span></span> <span data-ttu-id="a604d-126">Система может имитировать атрибуты полужирного начертания, курсива, подчеркивания и зачеркивания для растровых шрифтов, предоставляемых GDI, но не для шрифтов, предоставляемых устройствами.</span><span class="sxs-lookup"><span data-stu-id="a604d-126">The system can simulate bold, italic, underline, and strikeout attributes for GDI-supplied raster fonts, but not for device-supplied fonts.</span></span>

<span data-ttu-id="a604d-127">Приложение также может проверить биты 1 и 2 в элементе **тмпитчандфамили** структуры [невтекстметрик](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) , чтобы определить шрифт TrueType.</span><span class="sxs-lookup"><span data-stu-id="a604d-127">An application can also check bits 1 and 2 in the **tmPitchAndFamily** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure to identify a TrueType font.</span></span> <span data-ttu-id="a604d-128">Если бит 1 равен 0, а бит 2 — 1, то шрифт является шрифтом TrueType.</span><span class="sxs-lookup"><span data-stu-id="a604d-128">If bit 1 is 0 and bit 2 is 1, the font is a TrueType font.</span></span>

<span data-ttu-id="a604d-129">Векторные шрифты классифицируются как OEM \_ CharSet, а не ANSI \_ CharSet.</span><span class="sxs-lookup"><span data-stu-id="a604d-129">Vector fonts are categorized as OEM\_CHARSET instead of ANSI\_CHARSET.</span></span> <span data-ttu-id="a604d-130">Некоторые приложения определяют векторные шрифты с помощью этих сведений, проверяя элемент **тмчарсет** структуры [**невтекстметрик**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="a604d-130">Some applications identify vector fonts by using this information, checking the **tmCharSet** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span> <span data-ttu-id="a604d-131">Такая классификация обычно запрещает средству сопоставления шрифтов выбирать векторные шрифты, если они не были специально запрошены.</span><span class="sxs-lookup"><span data-stu-id="a604d-131">This categorization usually prevents the font mapper from choosing vector fonts unless they are specifically requested.</span></span> <span data-ttu-id="a604d-132">(Большинство приложений больше не используют векторные шрифты, поскольку их штрихи представляют собой одиночные линии, и они занимают больше времени, чем шрифты TrueType, которые предлагают многие из тех же функций масштабирования и вращения, которые требовали векторных шрифтов.)</span><span class="sxs-lookup"><span data-stu-id="a604d-132">(Most applications no longer use vector fonts because their strokes are single lines and they take longer to draw than TrueType fonts, which offer many of the same scaling and rotation features that required vector fonts.)</span></span>

 

 
