---
title: Использование структур в WCS 1.0
description: Большая часть структур, используемых WCS 1,0, очень проста и требует небольшое объяснение. Они описаны в разделе "Справочник по WCS 1,0", озаглавленном "структуры".
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Цветовая система Windows (WCS), структуры
- WCS (цветовая система Windows), структуры
- Управление цветом изображений, структуры
- Управление цветом, структуры
- цвета, структуры
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720069"
---
# <a name="using-structures-in-wcs-10"></a><span data-ttu-id="f5b11-109">Использование структур в WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="f5b11-109">Using Structures in WCS 1.0</span></span>

<span data-ttu-id="f5b11-110">Большая часть структур, используемых WCS 1,0, очень проста и требует небольшое объяснение.</span><span class="sxs-lookup"><span data-stu-id="f5b11-110">Most of the structures used by WCS 1.0 are very straightforward and require little explanation.</span></span> <span data-ttu-id="f5b11-111">Они описаны в разделе "Справочник по WCS 1,0", озаглавленном " [структуры](structures.md)".</span><span class="sxs-lookup"><span data-stu-id="f5b11-111">They are documented in the WCS 1.0 Reference section entitled [Structures](structures.md).</span></span>

<span data-ttu-id="f5b11-112">Исключения представляют собой структуру [**колорматчсетупв**](/windows/win32/api/icm/ns-icm-colormatchsetupw) , используемую функцией [**сетупколорматчингв**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) , и следующие структуры Windows, определенные в вингди. h:</span><span class="sxs-lookup"><span data-stu-id="f5b11-112">Exceptions are the [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure used by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function, and the following Windows structures defined in Wingdi.h:</span></span>

-   [<span data-ttu-id="f5b11-113">BITMAPV5HEADER</span><span class="sxs-lookup"><span data-stu-id="f5b11-113">BITMAPV5HEADER</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="f5b11-114">**логколорспаце**</span><span class="sxs-lookup"><span data-stu-id="f5b11-114">**LOGCOLORSPACE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [<span data-ttu-id="f5b11-115">**Циексиз**</span><span class="sxs-lookup"><span data-stu-id="f5b11-115">**CIEXYZ**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [<span data-ttu-id="f5b11-116">**Циексизтрипле**</span><span class="sxs-lookup"><span data-stu-id="f5b11-116">**CIEXYZTRIPLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

<span data-ttu-id="f5b11-117">В следующих разделах рассматривается более большая длина:</span><span class="sxs-lookup"><span data-stu-id="f5b11-117">The following topics are discussed at greater length:</span></span>

-   [<span data-ttu-id="f5b11-118">Структуры заголовка битовой карты Windows</span><span class="sxs-lookup"><span data-stu-id="f5b11-118">Windows Bitmap Header Structures</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="f5b11-119">Различия между заголовками v4 и V5</span><span class="sxs-lookup"><span data-stu-id="f5b11-119">Differences Between V4 and V5 Headers</span></span>](#differences-between-v4-and-v5-headers)
-   [<span data-ttu-id="f5b11-120">Bitmap.exe: служебная программа Command-Line для преобразования заголовков битовых карт</span><span class="sxs-lookup"><span data-stu-id="f5b11-120">Bitmap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a><span data-ttu-id="f5b11-121">Структуры заголовка битовой карты Windows</span><span class="sxs-lookup"><span data-stu-id="f5b11-121">Windows Bitmap Header Structures</span></span>

<span data-ttu-id="f5b11-122">WCS 1,0 позволяет связывать или внедрять цветовые профили ICC в DIB-аппаратные рисунки.</span><span class="sxs-lookup"><span data-stu-id="f5b11-122">WCS 1.0 allows ICC color profiles to be linked or embedded in device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="f5b11-123">Это позволяет точнее использовать цвета DIB, чем возможно с помощью WCS в Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f5b11-123">This allows DIB colors to be characterized more accurately than was possible using WCS in Windows 95.</span></span> <span data-ttu-id="f5b11-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , Новая структура заголовка точечного рисунка, определена в вингди. h в выпуске Windows 98.</span><span class="sxs-lookup"><span data-stu-id="f5b11-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , the new bitmap header structure, is defined in Wingdi.h in the release of Windows 98.</span></span> <span data-ttu-id="f5b11-125">В целях разработки он также включается в файл ICM. h со ссылкой этого программиста.</span><span class="sxs-lookup"><span data-stu-id="f5b11-125">For development purposes, it is also included in the file Icm.h with this Programmer's Reference.</span></span> <span data-ttu-id="f5b11-126">Структура **BITMAPV5HEADER** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f5b11-126">The **BITMAPV5HEADER** structure is as follows:</span></span>


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



<span data-ttu-id="f5b11-127">Элементу **bV5CSType** может быть присвоено значение \_ встроенный профиль или профиль, \_ чтобы указать, является ли профиль внедренным или связанным с ним.</span><span class="sxs-lookup"><span data-stu-id="f5b11-127">The member **bV5CSType** can have the values PROFILE\_EMBEDDED or PROFILE\_LINKED to specify whether a profile is embedded or linked with the DIB.</span></span> <span data-ttu-id="f5b11-128">Элемент **bV5ProfileData** — смещение в байтах от начала структуры **BITMAPV5HEADER** до начала данных профиля.</span><span class="sxs-lookup"><span data-stu-id="f5b11-128">The member **bV5ProfileData** is the offset in bytes from the beginning of the **BITMAPV5HEADER** structure to the start of the profile data.</span></span> <span data-ttu-id="f5b11-129">Если профиль внедрен, данные профилирования являются реальным профилем, и если он связан, данные профиля являются именем файла профиля, заканчивающимся нулем.</span><span class="sxs-lookup"><span data-stu-id="f5b11-129">If the profile is embedded, profile data is the actual profile, and if it is linked, the profile data is the null-terminated file name of the profile.</span></span> <span data-ttu-id="f5b11-130">Это не может быть строка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="f5b11-130">This cannot be a Unicode string.</span></span> <span data-ttu-id="f5b11-131">Он должен состоять исключительно из символов из набора символов Windows (кодовая страница 1252).</span><span class="sxs-lookup"><span data-stu-id="f5b11-131">It must be composed exclusively of characters from the Windows character set (code page 1252).</span></span>

<span data-ttu-id="f5b11-132">Когда DIB загружается в память, данные профиля (если они есть) должны следовать за таблицей цветов, а **bV5ProfileData** должно предоставлять смещение данных профиля от начала структуры **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="f5b11-132">When a DIB is loaded into memory, the profile data (if present) should follow the color table, and **bV5ProfileData** should give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span> <span data-ttu-id="f5b11-133">Теперь значение этого элемента будет другим, так как биты битовой карты не следуют за таблицей цветов в памяти.</span><span class="sxs-lookup"><span data-stu-id="f5b11-133">The value of this member will be different now, as the bitmap bits do not follow the color table in memory.</span></span> <span data-ttu-id="f5b11-134">Приложения должны изменить элемент **bV5ProfileData** после загрузки DIB в память.</span><span class="sxs-lookup"><span data-stu-id="f5b11-134">Applications should modify the **bV5ProfileData** member after loading the DIB into memory.</span></span>

<span data-ttu-id="f5b11-135">Для упакованных DIB данные профиля должны соответствовать битовым изображениям, аналогичным формату файла.</span><span class="sxs-lookup"><span data-stu-id="f5b11-135">For packed DIBs, the profile data should follow the bitmap bits similar to the file format.</span></span> <span data-ttu-id="f5b11-136">Элемент **bV5ProfileData** должен по-прежнему предоставлять смещение данных профиля от начала структуры **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="f5b11-136">The **bV5ProfileData** member should still give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span>

<span data-ttu-id="f5b11-137">Приложения должны получать доступ к данным профиля, только если **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** является \_ встроенным или связанным с профилями \_ .</span><span class="sxs-lookup"><span data-stu-id="f5b11-137">Applications should access the profile data only when **bV5Size** == **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** is PROFILE\_EMBEDDED or PROFILE\_LINKED.</span></span>

<span data-ttu-id="f5b11-138">Если профиль связан, путь к профилю может быть любым полным именем (включая сетевой путь), который можно открыть с помощью функции Win32 **CreateFile** .</span><span class="sxs-lookup"><span data-stu-id="f5b11-138">If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the Win32 **CreateFile** function.</span></span>

## <a name="differences-between-v4-and-v5-headers"></a><span data-ttu-id="f5b11-139">Различия между заголовками v4 и V5</span><span class="sxs-lookup"><span data-stu-id="f5b11-139">Differences Between V4 and V5 Headers</span></span>

<span data-ttu-id="f5b11-140">При работе с новой структурой точечных рисунков полезно понимать различия в настройке структур **BITMAPV4HEADER** и **BITMAPV5HEADER** :</span><span class="sxs-lookup"><span data-stu-id="f5b11-140">In working with the new bitmap structure, it is useful to recognize differences in how **BITMAPV4HEADER** and **BITMAPV5HEADER** structures are set up:</span></span>



| <span data-ttu-id="f5b11-141">Заголовок v4</span><span class="sxs-lookup"><span data-stu-id="f5b11-141">V4 Header</span></span>     | <span data-ttu-id="f5b11-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f5b11-142">Meaning</span></span>                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b11-143">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-143">**bV4CSType**</span></span> | <span data-ttu-id="f5b11-144">\_откалиброванный \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="f5b11-144">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="f5b11-145">Это значение подразумевает, что конечные точки и гаммы заданы в соответствующих полях.</span><span class="sxs-lookup"><span data-stu-id="f5b11-145">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="f5b11-146">Фиктивные значения вызывают проблемы.</span><span class="sxs-lookup"><span data-stu-id="f5b11-146">Bogus values cause trouble.</span></span> |
| <span data-ttu-id="f5b11-147">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-147">**bV4CSType**</span></span> | <span data-ttu-id="f5b11-148">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="f5b11-148">LCS\_sRGB.</span></span> <span data-ttu-id="f5b11-149">Это значение означает, что точечный рисунок находится в цветовом пространстве sRGB (гамма и конечные точки игнорируются).</span><span class="sxs-lookup"><span data-stu-id="f5b11-149">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                 |
| <span data-ttu-id="f5b11-150">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-150">**bV4CSType**</span></span> | <span data-ttu-id="f5b11-151">\_ \_ цветовое пространство Windows LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="f5b11-151">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="f5b11-152">Это значение означает, что точечный рисунок находится в цветовом пространстве Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5b11-152">This value implies that the bitmap is in Windows default color space.</span></span>                                    |



 



| <span data-ttu-id="f5b11-153">Заголовок V5</span><span class="sxs-lookup"><span data-stu-id="f5b11-153">V5 Header</span></span>     | <span data-ttu-id="f5b11-154">Значение</span><span class="sxs-lookup"><span data-stu-id="f5b11-154">Meaning</span></span>                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b11-155">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-155">**bV5CSType**</span></span> | <span data-ttu-id="f5b11-156">\_откалиброванный \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="f5b11-156">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="f5b11-157">Это значение подразумевает, что конечные точки и гаммы заданы в соответствующих полях.</span><span class="sxs-lookup"><span data-stu-id="f5b11-157">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="f5b11-158">Фиктивные значения вызывают проблемы.</span><span class="sxs-lookup"><span data-stu-id="f5b11-158">Bogus values cause trouble.</span></span>                         |
| <span data-ttu-id="f5b11-159">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-159">**bV5CSType**</span></span> | <span data-ttu-id="f5b11-160">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="f5b11-160">LCS\_sRGB.</span></span> <span data-ttu-id="f5b11-161">Это значение означает, что точечный рисунок находится в цветовом пространстве sRGB (гамма и конечные точки игнорируются).</span><span class="sxs-lookup"><span data-stu-id="f5b11-161">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                                         |
| <span data-ttu-id="f5b11-162">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-162">**bV5CSType**</span></span> | <span data-ttu-id="f5b11-163">\_внедренный профиль.</span><span class="sxs-lookup"><span data-stu-id="f5b11-163">PROFILE\_EMBEDDED.</span></span> <span data-ttu-id="f5b11-164">Это значение подразумевает, что **bV5ProfileData** указывает на буфер памяти, который содержит используемый профиль (гамма и конечные точки игнорируются).</span><span class="sxs-lookup"><span data-stu-id="f5b11-164">This value implies that **bV5ProfileData** points to a memory buffer that contains the profile to use (gammas and endpoints are ignored).</span></span> |
| <span data-ttu-id="f5b11-165">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-165">**bV5CSType**</span></span> | <span data-ttu-id="f5b11-166">\_связанный профиль.</span><span class="sxs-lookup"><span data-stu-id="f5b11-166">PROFILE\_LINKED.</span></span> <span data-ttu-id="f5b11-167">Это значение подразумевает, что **bV5ProfileData** указывает на имя файла профиля для использования (гамма и конечные точки игнорируются).</span><span class="sxs-lookup"><span data-stu-id="f5b11-167">This value implies that **bV5ProfileData** points to the file name of the profile to use (gammas and endpoints are ignored).</span></span>                |
| <span data-ttu-id="f5b11-168">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="f5b11-168">**bV5CSType**</span></span> | <span data-ttu-id="f5b11-169">\_ \_ цветовое пространство Windows LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="f5b11-169">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="f5b11-170">Это значение означает, что точечный рисунок находится в цветовом пространстве Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5b11-170">This value implies that the bitmap is in Windows default color space.</span></span>                                                            |



 

<span data-ttu-id="f5b11-171">Чтобы преобразовать старые точечные рисунки в новую структуру **BITMAPV5HEADER** , файл программы преобразования командной строки с именем Bitmap.exe включен в Справочник программиста по WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="f5b11-171">In order to convert older bitmaps to and from the new **BITMAPV5HEADER** structure, a command-line conversion utility file named Bitmap.exe is included in the WCS 1.0 Programmer's Reference.</span></span>

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a><span data-ttu-id="f5b11-172">BitMap.exe: служебная программа Command-Line для преобразования заголовков битовых карт</span><span class="sxs-lookup"><span data-stu-id="f5b11-172">BitMap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>

<span data-ttu-id="f5b11-173">Bitmap.exe — это программа командной строки, расположенная в \\ папке bin в указанной папке установки.</span><span class="sxs-lookup"><span data-stu-id="f5b11-173">Bitmap.exe is a command-line utility located in the \\Bin folder under the installation folder that you specified.</span></span> <span data-ttu-id="f5b11-174">Он изменяет заголовки точечных рисунков Windows, позволяя преобразовывать существующие растровые изображения из структур заголовков **битмапинфохеадер** и **BITMAPV4HEADER** в более новую структуру **BITMAPV5HEADER** и обратно.</span><span class="sxs-lookup"><span data-stu-id="f5b11-174">It modifies the headers of Windows bitmaps, allowing you to convert existing bitmaps from **BITMAPINFOHEADER** and **BITMAPV4HEADER** header structures to the newer **BITMAPV5HEADER** structure and back again.</span></span> <span data-ttu-id="f5b11-175">Синтаксис командной строки выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f5b11-175">The command-line syntax is as follows:</span></span>


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



<span data-ttu-id="f5b11-176">Параметры командной строки имеют следующие последствия.</span><span class="sxs-lookup"><span data-stu-id="f5b11-176">The command-line switches have the following effects.</span></span>



| <span data-ttu-id="f5b11-177">Коммутатор</span><span class="sxs-lookup"><span data-stu-id="f5b11-177">Switch</span></span> | <span data-ttu-id="f5b11-178">Значение</span><span class="sxs-lookup"><span data-stu-id="f5b11-178">Meaning</span></span>                                                                  |
|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="f5b11-179">/d</span><span class="sxs-lookup"><span data-stu-id="f5b11-179">/d</span></span>     | <span data-ttu-id="f5b11-180">Значения по умолчанию автоматически вносятся в преобразованные заголовки.</span><span class="sxs-lookup"><span data-stu-id="f5b11-180">Default values are automatically entered in the converted headers.</span></span>       |
| <span data-ttu-id="f5b11-181">/1</span><span class="sxs-lookup"><span data-stu-id="f5b11-181">/1</span></span>     | <span data-ttu-id="f5b11-182">Преобразует указанные растровые изображения в **битмапинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="f5b11-182">Convert the specified bitmaps to **BITMAPINFOHEADER**</span></span>                    |
| <span data-ttu-id="f5b11-183">/4</span><span class="sxs-lookup"><span data-stu-id="f5b11-183">/4</span></span>     | <span data-ttu-id="f5b11-184">Преобразует указанные растровые изображения в **BITMAPV4HEADER**</span><span class="sxs-lookup"><span data-stu-id="f5b11-184">Convert the specified bitmaps to **BITMAPV4HEADER**</span></span>                      |
| <span data-ttu-id="f5b11-185">/5</span><span class="sxs-lookup"><span data-stu-id="f5b11-185">/5</span></span>     | <span data-ttu-id="f5b11-186">Преобразует указанные растровые изображения в **BITMAPV5HEADER**</span><span class="sxs-lookup"><span data-stu-id="f5b11-186">Convert the specified bitmaps to **BITMAPV5HEADER**</span></span>                      |
| <span data-ttu-id="f5b11-187">/f</span><span class="sxs-lookup"><span data-stu-id="f5b11-187">/f</span></span>     | <span data-ttu-id="f5b11-188">Принудительное преобразование, даже если точечный рисунок уже имеет правый заголовок</span><span class="sxs-lookup"><span data-stu-id="f5b11-188">Forces conversion, even if the bitmap already has the right header</span></span>       |
| <span data-ttu-id="f5b11-189">/s</span><span class="sxs-lookup"><span data-stu-id="f5b11-189">/s</span></span>     | <span data-ttu-id="f5b11-190">Преобразует точечные рисунки в указанной папке и всех подкаталогах в ней</span><span class="sxs-lookup"><span data-stu-id="f5b11-190">Converts bitmaps in the specified folder and all subdirectories under it</span></span> |



 

 

 