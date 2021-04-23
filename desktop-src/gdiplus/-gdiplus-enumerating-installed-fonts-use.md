---
description: Класс Инсталледфонтколлектион наследует от абстрактного базового класса Фонтколлектион.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Перечисление установленных шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f41242522c2575ffb08e53f7100380ac9a849d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264065"
---
# <a name="enumerating-installed-fonts"></a><span data-ttu-id="ebb18-103">Перечисление установленных шрифтов</span><span class="sxs-lookup"><span data-stu-id="ebb18-103">Enumerating Installed Fonts</span></span>

<span data-ttu-id="ebb18-104">Класс [**инсталледфонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) наследует от абстрактного базового класса [**фонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="ebb18-104">The [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="ebb18-105">Для перечисления шрифтов, установленных на компьютере, можно использовать объект **инсталледфонтколлектион** .</span><span class="sxs-lookup"><span data-stu-id="ebb18-105">You can use an **InstalledFontCollection** object to enumerate the fonts installed on the computer.</span></span> <span data-ttu-id="ebb18-106">Метод [**фонтколлектион::**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) IsArray объекта **инсталледфонтколлектион** возвращает массив объектов [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="ebb18-106">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of an **InstalledFontCollection** object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="ebb18-107">Перед вызовом **фонтколлектион::-семейства** необходимо выделить буфер, достаточно большой для хранения этого массива.</span><span class="sxs-lookup"><span data-stu-id="ebb18-107">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="ebb18-108">Чтобы определить размер требуемого буфера, вызовите метод [**фонтколлектион:: жетфамиликаунт**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) и умножьте возвращаемое значение на **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="ebb18-108">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="ebb18-109">В следующем примере перечисляются имена всех семейств шрифтов, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="ebb18-109">The following example lists the names of all the font families installed on the computer.</span></span> <span data-ttu-id="ebb18-110">Код извлекает имена семейств шрифтов, вызывая метод [**FontFamily:: жетфамилинаме**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) каждого объекта [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) в массиве, возвращенном [**фонтколлектион::**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)IsArray.</span><span class="sxs-lookup"><span data-stu-id="ebb18-110">The code retrieves the font family names by calling the [**FontFamily::GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) method of each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the array returned by [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span></span> <span data-ttu-id="ebb18-111">По мере извлечения имен семейств они объединяются для формирования списка с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="ebb18-111">As the family names are retrieved, they are concatenated to form a comma-separated list.</span></span> <span data-ttu-id="ebb18-112">Затем метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) рисует список с разделителями-запятыми в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="ebb18-112">Then the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class draws the comma-separated list in a rectangle.</span></span>


```
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 8, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 500.0f, 500.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

INT          count = 0;
INT          found = 0;
WCHAR        familyName[LF_FACESIZE];  // enough space for one family name
WCHAR*       familyList = NULL;
FontFamily*  pFontFamily = NULL;

InstalledFontCollection installedFontCollection;

// How many font families are installed?
count = installedFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
installedFontCollection.GetFamilies(count, pFontFamily, &found);

// The loop below creates a large string that is a comma-separated
// list of all font family names.
// Allocate a buffer large enough to hold that string.
familyList = new WCHAR[count*(sizeof(familyName)+ 3)];
StringCchCopy(familyList, 1, L"");

for(INT j = 0; j < count; ++j)
{
   pFontFamily[j].GetFamilyName(familyName);  
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), familyName);
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), L",  ");
}

// Draw the large string (list of all families) in a rectangle.
graphics.DrawString(
   familyList, -1, &font, rectF, NULL, &solidBrush);

delete [] pFontFamily;
delete [] familyList;
            
```



<span data-ttu-id="ebb18-113">На следующем рисунке показаны возможные выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="ebb18-113">The following illustration shows a possible output of the preceding code.</span></span> <span data-ttu-id="ebb18-114">При выполнении кода выходные данные могут отличаться в зависимости от установленных на компьютере шрифтов.</span><span class="sxs-lookup"><span data-stu-id="ebb18-114">If you run the code, the output might be different, depending on the fonts installed on your computer.</span></span>

![снимок экрана окна, содержащего список установленных семейств шрифтов с разделителями-запятыми](images/fontstext6.png)

 

 



