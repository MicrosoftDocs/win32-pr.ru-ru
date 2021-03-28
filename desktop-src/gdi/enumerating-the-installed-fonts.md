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
# <a name="enumerating-the-installed-fonts"></a>Перечисление установленных шрифтов

В некоторых случаях приложение должно иметь возможность перечислить доступные шрифты и выбрать один из них, наиболее подходящий для конкретной операции. Приложение может перечислить доступные шрифты, вызвав функцию [енумфонтс](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) или [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) . Эти функции отправляют сведения о доступных шрифтах в функцию обратного вызова, которую предоставляет приложение. Функция обратного вызова получает сведения в структурах [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) и [невтекстметрик](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . (Структура [**невтекстметрик**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) содержит сведения о шрифте TrueType. Когда функция ответного вызова получает сведения о шрифте, отличном от TrueType, сведения содержатся в структуре [текстметрик](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .) С помощью этих сведений приложение может ограничить выбор пользователей только доступными шрифтами.

Функция [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) похожа на функцию [**енумфонтс**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) , но включает некоторые дополнительные функции. **EnumFontFamilies** позволяет приложению использовать стили, доступные в шрифтах TrueType. Новые и обновленные приложения должны использовать **EnumFontFamilies** вместо **енумфонтс**.

Шрифты TrueType организованы по имени гарнитуры (например, Courier New) и именам стилей (например, курсив, полужирный шрифт и жирный шрифт). Функция [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) перечисляет все стили, связанные с указанным именем семейства, а не просто атрибуты Bold и Italic. Например, если система включает шрифт TrueType с названием Courier New, то **EnumFontFamilies** переводит его в список новых шрифтов. Возможности **EnumFontFamilies** полезны для шрифтов с множеством или необычными стилями и для шрифтов, пересекающих международные границы.

Если приложение не предоставляет имя гарнитуры, функции [енумфонтс](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) и [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) предоставляют сведения о одном шрифте в каждом доступном семействе. Чтобы перечислить все шрифты в контексте устройства, в приложении можно указать **значение NULL** для имени гарнитуры, скомпилировать список доступных гарнитур, а затем перечислить каждый шрифт в каждой гарнитуре.

В следующем примере функция [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) используется для получения количества доступных растровых, векторных и шрифтовых семейств шрифтов TrueType.


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



В этом примере используются две маски, РАСТРОВые \_ фонттипе и TRUETYPE \_ фонттипе, чтобы определить тип перечисляемого шрифта. Если задан РАСТРОВый \_ бит фонттипе, то шрифт является растровым шрифтом. Если \_ установлен бит TrueType фонттипе, шрифт будет шрифтом TrueType. Если ни один из битов не задан, то шрифт является векторным шрифтом. Третья маска, фонттипе устройства \_ , задается, когда устройство (например, лазерный принтер) поддерживает загрузку шрифтов TrueType; оно равно нулю, если устройство является видеоадаптером, точечным принтером или другим растровым устройством. Приложение также может использовать \_ маску фонттипеа устройства для различения предоставляемых GDI растровых шрифтов от шрифтов, предоставляемых устройством. Система может имитировать атрибуты полужирного начертания, курсива, подчеркивания и зачеркивания для растровых шрифтов, предоставляемых GDI, но не для шрифтов, предоставляемых устройствами.

Приложение также может проверить биты 1 и 2 в элементе **тмпитчандфамили** структуры [невтекстметрик](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) , чтобы определить шрифт TrueType. Если бит 1 равен 0, а бит 2 — 1, то шрифт является шрифтом TrueType.

Векторные шрифты классифицируются как OEM \_ CharSet, а не ANSI \_ CharSet. Некоторые приложения определяют векторные шрифты с помощью этих сведений, проверяя элемент **тмчарсет** структуры [**невтекстметрик**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . Такая классификация обычно запрещает средству сопоставления шрифтов выбирать векторные шрифты, если они не были специально запрошены. (Большинство приложений больше не используют векторные шрифты, поскольку их штрихи представляют собой одиночные линии, и они занимают больше времени, чем шрифты TrueType, которые предлагают многие из тех же функций масштабирования и вращения, которые требовали векторных шрифтов.)

 

 
