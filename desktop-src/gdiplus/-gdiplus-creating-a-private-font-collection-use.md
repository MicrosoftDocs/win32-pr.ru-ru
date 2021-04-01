---
description: Класс Приватефонтколлектион наследует от абстрактного базового класса Фонтколлектион. Вы можете использовать объект Приватефонтколлектион для поддержки набора шрифтов, предназначенных специально для вашего приложения.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Создание частной коллекции шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264070"
---
# <a name="creating-a-private-font-collection"></a>Создание частной коллекции шрифтов

Класс [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) наследует от абстрактного базового класса [**фонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) . Вы можете использовать объект **приватефонтколлектион** для поддержки набора шрифтов, предназначенных специально для вашего приложения.

Частная коллекция шрифтов может включать установленные системные шрифты, а также шрифты, которые не были установлены на компьютере. Чтобы добавить файл шрифта в коллекцию частных шрифтов, вызовите метод [**приватефонтколлектион:: аддфонтфиле**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .

> [!Note]  
> При использовании интерфейса GDI+ API не следует разрешать приложению скачивать произвольные шрифты из ненадежных источников. Операционная система требует повышенных привилегий, чтобы гарантировать, что все установленные шрифты являются доверенными.

 

Метод [**фонтколлектион::**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) IsArray объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) возвращает массив объектов [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Перед вызовом **фонтколлектион::-семейства** необходимо выделить буфер, достаточно большой для хранения этого массива. Чтобы определить размер требуемого буфера, вызовите метод [**фонтколлектион:: жетфамиликаунт**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) и умножьте возвращаемое значение на **sizeof**(**FontFamily**).

Количество семейств шрифтов в частной коллекции шрифтов не обязательно совпадает с количеством файлов шрифтов, добавленных в коллекцию. Например, предположим, что в коллекцию добавляются файлы Ариалбд. ТФФ, Times. ТФФ и Тимесбд. ТФФ. В коллекции будут содержаться три файла, но только два семейства, так как Times. ТФФ и Тимесбд. ТФФ принадлежат одному семейству.

В следующем примере в объект [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) добавляются следующие три файла шрифтов:

-   C: \\ WinNT \\ Шрифты \\ Arial. ТФФ (Arial, Regular)
-   C: \\ WinNT \\ Шрифты \\ каурби. ТФФ (Courier New, жирный курсив)
-   C: \\ WinNT \\ Шрифты \\ тимесбд. ТФФ (Times Нью-Roman, Bold)

Код вызывает метод [**фонтколлектион:: жетфамиликаунт**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) , чтобы определить количество семейств в закрытой коллекции, а затем вызывает [**фонтколлектион::**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) IsArray для получения массива объектов [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .

Для каждого объекта [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) в коллекции код вызывает метод [**FontFamily:: исстилеаваилабле**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) , чтобы определить, доступны ли различные стили (обычный, полужирный, курсив, полужирный курсив, подчеркивание и зачеркивание). Аргументы, передаваемые методу **FontFamily:: исстилеаваилабле** , являются членами перечисления [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , который объявлен в гдиплусенумс. h.

Если имеется определенное сочетание семейства или стиля, объект [**шрифта**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) создается с использованием этого семейства и стиля. Первый аргумент, передаваемый конструктору **Font** , — это имя семейства шрифтов (а не объект [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) , как в случае с другими вариантами конструктора **шрифтов** ), а последний аргумент — это адрес объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) . После создания объекта **Font** его адрес передается методу [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) для вывода имени семейства вместе с именем стиля.


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



На следующем рисунке показаны выходные данные предыдущего кода.

![снимок экрана: окно со списком из девяти названий шрифтов, каждое из которых демонстрирует именованный шрифт](images/fontstext7.png)

Arial. ТФФ (который был добавлен в коллекцию частных шрифтов в предыдущем примере кода) — это файл шрифта для обычного стиля Arial. Однако обратите внимание, что в выходных данных программы отображается несколько доступных стилей, кроме Regular для семейства шрифтов Arial. Это связано с тем, что Windows GDI+ может имитировать стили полужирного, курсивного начертания и полужирного шрифта из обычного стиля. GDI+ также может создавать подчеркивания и стрикеаутс из обычного стиля.

Аналогичным образом GDI+ может имитировать полужирный курсив в стиле полужирного начертания или курсива. Выходные данные программы показывают, что стиль полужирного начертания доступен для семейства Times, несмотря на то, что Тимесбд. ТФФ (Times New Roman, Bold) является единственным файлом в коллекции.

В этой таблице указаны несистемные шрифты, поддерживаемые GDI+.



|                     | GDI | GDI+ в Windows 7 | GDI+ в Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . FON                | да | Нет                | Нет                | Нет          |
| . фнт                | да | Нет                | Нет                | Нет          |
| . TTF                | да | да               | да               | да         |
| . ОТФ с TrueType  | да | да               | да               | да         |
| . ОТФ с Adobe CFF | да | Нет                | да               | да         |
| Тип Adobe 1        | да | Нет                | Нет                | Нет          |



 

 

 



