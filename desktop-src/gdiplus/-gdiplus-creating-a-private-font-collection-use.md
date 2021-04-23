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
# <a name="creating-a-private-font-collection"></a><span data-ttu-id="bc1f2-104">Создание частной коллекции шрифтов</span><span class="sxs-lookup"><span data-stu-id="bc1f2-104">Creating a Private Font Collection</span></span>

<span data-ttu-id="bc1f2-105">Класс [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) наследует от абстрактного базового класса [**фонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="bc1f2-105">The [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="bc1f2-106">Вы можете использовать объект **приватефонтколлектион** для поддержки набора шрифтов, предназначенных специально для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-106">You can use a **PrivateFontCollection** object to maintain a set of fonts specifically for your application.</span></span>

<span data-ttu-id="bc1f2-107">Частная коллекция шрифтов может включать установленные системные шрифты, а также шрифты, которые не были установлены на компьютере.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-107">A private font collection can include installed system fonts as well as fonts that have not been installed on the computer.</span></span> <span data-ttu-id="bc1f2-108">Чтобы добавить файл шрифта в коллекцию частных шрифтов, вызовите метод [**приватефонтколлектион:: аддфонтфиле**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="bc1f2-108">To add a font file to a private font collection, call the [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span>

> [!Note]  
> <span data-ttu-id="bc1f2-109">При использовании интерфейса GDI+ API не следует разрешать приложению скачивать произвольные шрифты из ненадежных источников.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-109">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="bc1f2-110">Операционная система требует повышенных привилегий, чтобы гарантировать, что все установленные шрифты являются доверенными.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-110">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

 

<span data-ttu-id="bc1f2-111">Метод [**фонтколлектион::**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) IsArray объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) возвращает массив объектов [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="bc1f2-111">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="bc1f2-112">Перед вызовом **фонтколлектион::-семейства** необходимо выделить буфер, достаточно большой для хранения этого массива.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-112">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="bc1f2-113">Чтобы определить размер требуемого буфера, вызовите метод [**фонтколлектион:: жетфамиликаунт**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) и умножьте возвращаемое значение на **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="bc1f2-113">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="bc1f2-114">Количество семейств шрифтов в частной коллекции шрифтов не обязательно совпадает с количеством файлов шрифтов, добавленных в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-114">The number of font families in a private font collection is not necessarily the same as the number of font files that have been added to the collection.</span></span> <span data-ttu-id="bc1f2-115">Например, предположим, что в коллекцию добавляются файлы Ариалбд. ТФФ, Times. ТФФ и Тимесбд. ТФФ.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-115">For example, suppose you add the files ArialBd.tff, Times.tff, and TimesBd.tff to a collection.</span></span> <span data-ttu-id="bc1f2-116">В коллекции будут содержаться три файла, но только два семейства, так как Times. ТФФ и Тимесбд. ТФФ принадлежат одному семейству.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-116">There will be three files but only two families in the collection because Times.tff and TimesBd.tff belong to the same family.</span></span>

<span data-ttu-id="bc1f2-117">В следующем примере в объект [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) добавляются следующие три файла шрифтов:</span><span class="sxs-lookup"><span data-stu-id="bc1f2-117">The following example adds the following three font files to a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object:</span></span>

-   <span data-ttu-id="bc1f2-118">C: \\ WinNT \\ Шрифты \\ Arial. ТФФ (Arial, Regular)</span><span class="sxs-lookup"><span data-stu-id="bc1f2-118">C:\\WINNT\\Fonts\\Arial.tff (Arial, regular)</span></span>
-   <span data-ttu-id="bc1f2-119">C: \\ WinNT \\ Шрифты \\ каурби. ТФФ (Courier New, жирный курсив)</span><span class="sxs-lookup"><span data-stu-id="bc1f2-119">C:\\WINNT\\Fonts\\CourBI.tff (Courier New, bold italic)</span></span>
-   <span data-ttu-id="bc1f2-120">C: \\ WinNT \\ Шрифты \\ тимесбд. ТФФ (Times Нью-Roman, Bold)</span><span class="sxs-lookup"><span data-stu-id="bc1f2-120">C:\\WINNT\\Fonts\\TimesBd.tff (Times New Roman, bold)</span></span>

<span data-ttu-id="bc1f2-121">Код вызывает метод [**фонтколлектион:: жетфамиликаунт**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) , чтобы определить количество семейств в закрытой коллекции, а затем вызывает [**фонтколлектион::**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) IsArray для получения массива объектов [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="bc1f2-121">The code calls the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object to determine the number of families in the private collection, and then calls [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) to retrieve an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span>

<span data-ttu-id="bc1f2-122">Для каждого объекта [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) в коллекции код вызывает метод [**FontFamily:: исстилеаваилабле**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) , чтобы определить, доступны ли различные стили (обычный, полужирный, курсив, полужирный курсив, подчеркивание и зачеркивание).</span><span class="sxs-lookup"><span data-stu-id="bc1f2-122">For each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the collection, the code calls the [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) method to determine whether various styles (regular, bold, italic, bold italic, underline, and strikeout) are available.</span></span> <span data-ttu-id="bc1f2-123">Аргументы, передаваемые методу **FontFamily:: исстилеаваилабле** , являются членами перечисления [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , который объявлен в гдиплусенумс. h.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-123">The arguments passed to the **FontFamily::IsStyleAvailable** method are members of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="bc1f2-124">Если имеется определенное сочетание семейства или стиля, объект [**шрифта**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) создается с использованием этого семейства и стиля.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-124">If a particular family/style combination is available, a [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object is constructed using that family and style.</span></span> <span data-ttu-id="bc1f2-125">Первый аргумент, передаваемый конструктору **Font** , — это имя семейства шрифтов (а не объект [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) , как в случае с другими вариантами конструктора **шрифтов** ), а последний аргумент — это адрес объекта [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="bc1f2-125">The first argument passed to the **Font** constructor is the font family name (not a [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object as is the case for other variations of the **Font** constructor), and the final argument is the address of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span> <span data-ttu-id="bc1f2-126">После создания объекта **Font** его адрес передается методу [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) для вывода имени семейства вместе с именем стиля.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-126">After the **Font** object is constructed, its address is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to display the family name along with the name of the style.</span></span>


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



<span data-ttu-id="bc1f2-127">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-127">The following illustration shows the output of the preceding code.</span></span>

![снимок экрана: окно со списком из девяти названий шрифтов, каждое из которых демонстрирует именованный шрифт](images/fontstext7.png)

<span data-ttu-id="bc1f2-129">Arial. ТФФ (который был добавлен в коллекцию частных шрифтов в предыдущем примере кода) — это файл шрифта для обычного стиля Arial.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-129">Arial.tff (which was added to the private font collection in the preceding code example) is the font file for the Arial regular style.</span></span> <span data-ttu-id="bc1f2-130">Однако обратите внимание, что в выходных данных программы отображается несколько доступных стилей, кроме Regular для семейства шрифтов Arial.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-130">Note, however, that the program output shows several available styles other than regular for the Arial font family.</span></span> <span data-ttu-id="bc1f2-131">Это связано с тем, что Windows GDI+ может имитировать стили полужирного, курсивного начертания и полужирного шрифта из обычного стиля.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-131">That is because Windows GDI+ can simulate the bold, italic, and bold italic styles from the regular style.</span></span> <span data-ttu-id="bc1f2-132">GDI+ также может создавать подчеркивания и стрикеаутс из обычного стиля.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-132">GDI+ can also produce underlines and strikeouts from the regular style.</span></span>

<span data-ttu-id="bc1f2-133">Аналогичным образом GDI+ может имитировать полужирный курсив в стиле полужирного начертания или курсива.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-133">Similarly, GDI+ can simulate the bold italic style from either the bold style or the italic style.</span></span> <span data-ttu-id="bc1f2-134">Выходные данные программы показывают, что стиль полужирного начертания доступен для семейства Times, несмотря на то, что Тимесбд. ТФФ (Times New Roman, Bold) является единственным файлом в коллекции.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-134">The program output shows that the bold italic style is available for the Times family even though TimesBd.tff (Times New Roman, bold) is the only Times file in the collection.</span></span>

<span data-ttu-id="bc1f2-135">В этой таблице указаны несистемные шрифты, поддерживаемые GDI+.</span><span class="sxs-lookup"><span data-stu-id="bc1f2-135">This table specifies the non-system fonts that GDI+ supports.</span></span>



|                     | <span data-ttu-id="bc1f2-136">GDI</span><span class="sxs-lookup"><span data-stu-id="bc1f2-136">GDI</span></span> | <span data-ttu-id="bc1f2-137">GDI+ в Windows 7</span><span class="sxs-lookup"><span data-stu-id="bc1f2-137">GDI+ on Windows 7</span></span> | <span data-ttu-id="bc1f2-138">GDI+ в Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc1f2-138">GDI+ on Windows 8</span></span> | <span data-ttu-id="bc1f2-139">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="bc1f2-139">DirectWrite</span></span> |
|---------------------|-----|-------------------|-------------------|-------------|
| <span data-ttu-id="bc1f2-140">. FON</span><span class="sxs-lookup"><span data-stu-id="bc1f2-140">.FON</span></span>                | <span data-ttu-id="bc1f2-141">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-141">yes</span></span> | <span data-ttu-id="bc1f2-142">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-142">no</span></span>                | <span data-ttu-id="bc1f2-143">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-143">no</span></span>                | <span data-ttu-id="bc1f2-144">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-144">no</span></span>          |
| <span data-ttu-id="bc1f2-145">. фнт</span><span class="sxs-lookup"><span data-stu-id="bc1f2-145">.FNT</span></span>                | <span data-ttu-id="bc1f2-146">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-146">yes</span></span> | <span data-ttu-id="bc1f2-147">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-147">no</span></span>                | <span data-ttu-id="bc1f2-148">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-148">no</span></span>                | <span data-ttu-id="bc1f2-149">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-149">no</span></span>          |
| <span data-ttu-id="bc1f2-150">. TTF</span><span class="sxs-lookup"><span data-stu-id="bc1f2-150">.TTF</span></span>                | <span data-ttu-id="bc1f2-151">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-151">yes</span></span> | <span data-ttu-id="bc1f2-152">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-152">yes</span></span>               | <span data-ttu-id="bc1f2-153">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-153">yes</span></span>               | <span data-ttu-id="bc1f2-154">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-154">yes</span></span>         |
| <span data-ttu-id="bc1f2-155">. ОТФ с TrueType</span><span class="sxs-lookup"><span data-stu-id="bc1f2-155">.OTF with TrueType</span></span>  | <span data-ttu-id="bc1f2-156">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-156">yes</span></span> | <span data-ttu-id="bc1f2-157">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-157">yes</span></span>               | <span data-ttu-id="bc1f2-158">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-158">yes</span></span>               | <span data-ttu-id="bc1f2-159">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-159">yes</span></span>         |
| <span data-ttu-id="bc1f2-160">. ОТФ с Adobe CFF</span><span class="sxs-lookup"><span data-stu-id="bc1f2-160">.OTF with Adobe CFF</span></span> | <span data-ttu-id="bc1f2-161">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-161">yes</span></span> | <span data-ttu-id="bc1f2-162">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-162">no</span></span>                | <span data-ttu-id="bc1f2-163">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-163">yes</span></span>               | <span data-ttu-id="bc1f2-164">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-164">yes</span></span>         |
| <span data-ttu-id="bc1f2-165">Тип Adobe 1</span><span class="sxs-lookup"><span data-stu-id="bc1f2-165">Adobe Type 1</span></span>        | <span data-ttu-id="bc1f2-166">да</span><span class="sxs-lookup"><span data-stu-id="bc1f2-166">yes</span></span> | <span data-ttu-id="bc1f2-167">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-167">no</span></span>                | <span data-ttu-id="bc1f2-168">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-168">no</span></span>                | <span data-ttu-id="bc1f2-169">Нет</span><span class="sxs-lookup"><span data-stu-id="bc1f2-169">no</span></span>          |



 

 

 



