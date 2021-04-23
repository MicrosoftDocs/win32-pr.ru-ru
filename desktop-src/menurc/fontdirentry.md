---
title: Структура ФОНТДИРЕНТРИ
description: Содержит сведения об отдельном шрифте в группе ресурсов шрифтов. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Меню структуры ФОНТДИРЕНТРИ и другие ресурсы
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489663"
---
# <a name="fontdirentry-structure"></a><span data-ttu-id="76013-105">Структура ФОНТДИРЕНТРИ</span><span class="sxs-lookup"><span data-stu-id="76013-105">FONTDIRENTRY structure</span></span>

<span data-ttu-id="76013-106">Содержит сведения об отдельном шрифте в группе ресурсов шрифтов.</span><span class="sxs-lookup"><span data-stu-id="76013-106">Contains information about an individual font in a font resource group.</span></span> <span data-ttu-id="76013-107">Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="76013-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="76013-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76013-108">Syntax</span></span>


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a><span data-ttu-id="76013-109">Члены</span><span class="sxs-lookup"><span data-stu-id="76013-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="76013-110">**дфверсион**</span><span class="sxs-lookup"><span data-stu-id="76013-110">**dfVersion**</span></span>
</dt> <dd>

<span data-ttu-id="76013-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-112">Определяемый пользователем номер версии для данных ресурсов, которые средства могут использовать для чтения и записи файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76013-112">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span>

</dd> <dt>

<span data-ttu-id="76013-113">**дфсизе**</span><span class="sxs-lookup"><span data-stu-id="76013-113">**dfSize**</span></span>
</dt> <dd>

<span data-ttu-id="76013-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="76013-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-115">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="76013-115">The size of the file, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="76013-116">**Дфкопиригхт \[ 60\]**</span><span class="sxs-lookup"><span data-stu-id="76013-116">**dfCopyright\[60\]**</span></span>
</dt> <dd>

<span data-ttu-id="76013-117">Тип: **char**</span><span class="sxs-lookup"><span data-stu-id="76013-117">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="76013-118">Информация об авторских правах поставщика шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-118">The font supplier's copyright information.</span></span>

</dd> <dt>

<span data-ttu-id="76013-119">**дфтипе**</span><span class="sxs-lookup"><span data-stu-id="76013-119">**dfType**</span></span>
</dt> <dd>

<span data-ttu-id="76013-120">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-120">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-121">Тип файла шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-121">The type of font file.</span></span>

</dd> <dt>

<span data-ttu-id="76013-122">**дфпоинтс**</span><span class="sxs-lookup"><span data-stu-id="76013-122">**dfPoints**</span></span>
</dt> <dd>

<span data-ttu-id="76013-123">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-123">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-124">Размер точки, с которой этот набор символов выглядит лучше.</span><span class="sxs-lookup"><span data-stu-id="76013-124">The point size at which this character set looks best.</span></span>

</dd> <dt>

<span data-ttu-id="76013-125">**дфвертрес**</span><span class="sxs-lookup"><span data-stu-id="76013-125">**dfVertRes**</span></span>
</dt> <dd>

<span data-ttu-id="76013-126">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-127">Вертикальное разрешение (в точках на дюйм), для которого была выполнена цифра кодировки.</span><span class="sxs-lookup"><span data-stu-id="76013-127">The vertical resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="76013-128">**дфхоризрес**</span><span class="sxs-lookup"><span data-stu-id="76013-128">**dfHorizRes**</span></span>
</dt> <dd>

<span data-ttu-id="76013-129">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-129">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-130">Горизонтальное разрешение (в точках на дюйм), в котором эта кодировка была цифрой.</span><span class="sxs-lookup"><span data-stu-id="76013-130">The horizontal resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="76013-131">**дфасцент**</span><span class="sxs-lookup"><span data-stu-id="76013-131">**dfAscent**</span></span>
</dt> <dd>

<span data-ttu-id="76013-132">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-132">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-133">Расстояние от верха ячейки определения символа до базовой линии типографского шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-133">The distance from the top of a character definition cell to the baseline of the typographical font.</span></span>

</dd> <dt>

<span data-ttu-id="76013-134">**дфинтерналлеадинг**</span><span class="sxs-lookup"><span data-stu-id="76013-134">**dfInternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="76013-135">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-135">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-136">Объем ведущих элементов в границах, заданных элементом **дфпиксхеигхт** .</span><span class="sxs-lookup"><span data-stu-id="76013-136">The amount of leading inside the bounds set by the **dfPixHeight** member.</span></span> <span data-ttu-id="76013-137">В этой области могут встречаться диакритические знаки и другие диакритические символы.</span><span class="sxs-lookup"><span data-stu-id="76013-137">Accent marks and other diacritical characters can occur in this area.</span></span>

</dd> <dt>

<span data-ttu-id="76013-138">**дфекстерналлеадинг**</span><span class="sxs-lookup"><span data-stu-id="76013-138">**dfExternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="76013-139">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-140">Количество дополнительных ведущих, которые приложение добавляет между строками.</span><span class="sxs-lookup"><span data-stu-id="76013-140">The amount of extra leading that the application adds between rows.</span></span>

</dd> <dt>

<span data-ttu-id="76013-141">**дфиталик**</span><span class="sxs-lookup"><span data-stu-id="76013-141">**dfItalic**</span></span>
</dt> <dd>

<span data-ttu-id="76013-142">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-142">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-143">Курсив, если не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="76013-143">An italic font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="76013-144">**дфундерлине**</span><span class="sxs-lookup"><span data-stu-id="76013-144">**dfUnderline**</span></span>
</dt> <dd>

<span data-ttu-id="76013-145">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-146">Подчеркнутый шрифт, если не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="76013-146">An underlined font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="76013-147">**дфстрикеаут**</span><span class="sxs-lookup"><span data-stu-id="76013-147">**dfStrikeOut**</span></span>
</dt> <dd>

<span data-ttu-id="76013-148">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-148">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-149">Зачеркивание шрифта, если он не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="76013-149">A strikeout font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="76013-150">**дфвеигхт**</span><span class="sxs-lookup"><span data-stu-id="76013-150">**dfWeight**</span></span>
</dt> <dd>

<span data-ttu-id="76013-151">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-151">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-152">Вес шрифта в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="76013-152">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="76013-153">Например, 400 — это латинский, а 700 — полужирный.</span><span class="sxs-lookup"><span data-stu-id="76013-153">For example, 400 is roman and 700 is bold.</span></span> <span data-ttu-id="76013-154">Если это значение равно нулю, используется вес по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76013-154">If this value is zero, a default weight is used.</span></span> <span data-ttu-id="76013-155">Дополнительные заданные значения см. в описании структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="76013-155">For additional defined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="76013-156">**дфчарсет**</span><span class="sxs-lookup"><span data-stu-id="76013-156">**dfCharSet**</span></span>
</dt> <dd>

<span data-ttu-id="76013-157">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-157">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-158">Кодировка шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-158">The character set of the font.</span></span> <span data-ttu-id="76013-159">Предварительно определенные значения см. в описании структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="76013-159">For predefined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="76013-160">**дфпиксвидс**</span><span class="sxs-lookup"><span data-stu-id="76013-160">**dfPixWidth**</span></span>
</dt> <dd>

<span data-ttu-id="76013-161">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-161">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-162">Ширина сетки, в которой была выполнена цифра векторного шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-162">The width of the grid on which a vector font was digitized.</span></span> <span data-ttu-id="76013-163">Для растровых шрифтов, если элемент не равен нулю, он представляет ширину для всех символов в битовой карте.</span><span class="sxs-lookup"><span data-stu-id="76013-163">For raster fonts, if the member is not equal to zero, it represents the width for all the characters in the bitmap.</span></span> <span data-ttu-id="76013-164">Если элемент равен нулю, то шрифт имеет символы переменной ширины.</span><span class="sxs-lookup"><span data-stu-id="76013-164">If the member is equal to zero, the font has variable-width characters.</span></span>

</dd> <dt>

<span data-ttu-id="76013-165">**дфпиксхеигхт**</span><span class="sxs-lookup"><span data-stu-id="76013-165">**dfPixHeight**</span></span>
</dt> <dd>

<span data-ttu-id="76013-166">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-166">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-167">Высота точечного рисунка символа для растровых шрифтов или Высота сетки, в которой была выполнена цифра векторного шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-167">The height of the character bitmap for raster fonts or the height of the grid on which a vector font was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="76013-168">**дфпитчандфамили**</span><span class="sxs-lookup"><span data-stu-id="76013-168">**dfPitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="76013-169">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-169">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-170">Высота и семейство шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-170">The pitch and the family of the font.</span></span> <span data-ttu-id="76013-171">Дополнительные сведения см. в описании структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="76013-171">For additional information, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="76013-172">**дфавгвидс**</span><span class="sxs-lookup"><span data-stu-id="76013-172">**dfAvgWidth**</span></span>
</dt> <dd>

<span data-ttu-id="76013-173">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-173">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-174">Средняя ширина символов в шрифте (обычно определяется как ширина буквы x).</span><span class="sxs-lookup"><span data-stu-id="76013-174">The average width of characters in the font (generally defined as the width of the letter x).</span></span> <span data-ttu-id="76013-175">Это значение не включает в себя выступ, необходимый для полужирного или курсивного начертания.</span><span class="sxs-lookup"><span data-stu-id="76013-175">This value does not include the overhang required for bold or italic characters.</span></span>

</dd> <dt>

<span data-ttu-id="76013-176">**дфмаксвидс**</span><span class="sxs-lookup"><span data-stu-id="76013-176">**dfMaxWidth**</span></span>
</dt> <dd>

<span data-ttu-id="76013-177">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-177">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-178">Ширина самого широкого символа в шрифте.</span><span class="sxs-lookup"><span data-stu-id="76013-178">The width of the widest character in the font.</span></span>

</dd> <dt>

<span data-ttu-id="76013-179">**дффирстчар**</span><span class="sxs-lookup"><span data-stu-id="76013-179">**dfFirstChar**</span></span>
</dt> <dd>

<span data-ttu-id="76013-180">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-180">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-181">Первый код символа, определенный в шрифте.</span><span class="sxs-lookup"><span data-stu-id="76013-181">The first character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="76013-182">**дфластчар**</span><span class="sxs-lookup"><span data-stu-id="76013-182">**dfLastChar**</span></span>
</dt> <dd>

<span data-ttu-id="76013-183">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-183">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-184">Последний код символа, определенный в шрифте.</span><span class="sxs-lookup"><span data-stu-id="76013-184">The last character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="76013-185">**дфдефаултчар**</span><span class="sxs-lookup"><span data-stu-id="76013-185">**dfDefaultChar**</span></span>
</dt> <dd>

<span data-ttu-id="76013-186">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-186">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-187">Символ для замены символов, не наставляемых в шрифте.</span><span class="sxs-lookup"><span data-stu-id="76013-187">The character to substitute for characters not in the font.</span></span>

</dd> <dt>

<span data-ttu-id="76013-188">**дфбреакчар**</span><span class="sxs-lookup"><span data-stu-id="76013-188">**dfBreakChar**</span></span>
</dt> <dd>

<span data-ttu-id="76013-189">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="76013-189">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="76013-190">Символ, который будет использоваться для определения разрывов слов для обоснования текста.</span><span class="sxs-lookup"><span data-stu-id="76013-190">The character that will be used to define word breaks for text justification.</span></span>

</dd> <dt>

<span data-ttu-id="76013-191">**дфвидсбитес**</span><span class="sxs-lookup"><span data-stu-id="76013-191">**dfWidthBytes**</span></span>
</dt> <dd>

<span data-ttu-id="76013-192">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="76013-192">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-193">Число байтов в каждой строке точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="76013-193">The number of bytes in each row of the bitmap.</span></span> <span data-ttu-id="76013-194">Это значение всегда равно, так что строки начинаются с границ слов.</span><span class="sxs-lookup"><span data-stu-id="76013-194">This value is always even so that the rows start on word boundaries.</span></span> <span data-ttu-id="76013-195">Для векторных шрифтов этот член не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="76013-195">For vector fonts, this member has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="76013-196">**дфдевице**</span><span class="sxs-lookup"><span data-stu-id="76013-196">**dfDevice**</span></span>
</dt> <dd>

<span data-ttu-id="76013-197">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="76013-197">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-198">Смещение в файле до строки, завершающейся нулем, которая указывает имя устройства.</span><span class="sxs-lookup"><span data-stu-id="76013-198">The offset in the file to a null-terminated string that specifies a device name.</span></span> <span data-ttu-id="76013-199">Для универсального шрифта это значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="76013-199">For a generic font, this value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="76013-200">**дффаце**</span><span class="sxs-lookup"><span data-stu-id="76013-200">**dfFace**</span></span>
</dt> <dd>

<span data-ttu-id="76013-201">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="76013-201">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-202">Смещение в файле до строки, завершающейся нулем, которая именует гарнитуру.</span><span class="sxs-lookup"><span data-stu-id="76013-202">The offset in the file to a null-terminated string that names the typeface.</span></span>

</dd> <dt>

<span data-ttu-id="76013-203">**дфресервед**</span><span class="sxs-lookup"><span data-stu-id="76013-203">**dfReserved**</span></span>
</dt> <dd>

<span data-ttu-id="76013-204">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="76013-204">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="76013-205">Этот член зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="76013-205">This member is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="76013-206">**сздевиценаме**</span><span class="sxs-lookup"><span data-stu-id="76013-206">**szDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="76013-207">Тип: **char**</span><span class="sxs-lookup"><span data-stu-id="76013-207">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="76013-208">Имя устройства, если этот файл шрифта предназначен для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="76013-208">The name of the device if this font file is designated for a specific device.</span></span>

</dd> <dt>

<span data-ttu-id="76013-209">**сзфаценаме**</span><span class="sxs-lookup"><span data-stu-id="76013-209">**szFaceName**</span></span>
</dt> <dd>

<span data-ttu-id="76013-210">Тип: **char**</span><span class="sxs-lookup"><span data-stu-id="76013-210">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="76013-211">Имя гарнитуры шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-211">The typeface name of the font.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76013-212">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76013-212">Remarks</span></span>

<span data-ttu-id="76013-213">Существует одна структура **фонтдирентри** для каждого шрифта в RES-файле.</span><span class="sxs-lookup"><span data-stu-id="76013-213">There is one **FONTDIRENTRY** structure for every font in the .res file.</span></span> <span data-ttu-id="76013-214">Приложения, создающие RES-файлы с ресурсами шрифтов, должны также добавить в файл структуру **фонтдирентри** для каждого шрифта.</span><span class="sxs-lookup"><span data-stu-id="76013-214">Applications that generate .res files with font resources must also add to the file a **FONTDIRENTRY** structure for each font.</span></span>

<span data-ttu-id="76013-215">Объявления шрифтов можно комбинировать с другими объявлениями ресурсов в. RC-файл, так как шрифты не должны быть непрерывными в RES-файле.</span><span class="sxs-lookup"><span data-stu-id="76013-215">Font declarations can be mixed with other resource declarations in the .RC file because fonts do not need to be contiguous in the .res file.</span></span>

## <a name="requirements"></a><span data-ttu-id="76013-216">Требования</span><span class="sxs-lookup"><span data-stu-id="76013-216">Requirements</span></span>



| <span data-ttu-id="76013-217">Требование</span><span class="sxs-lookup"><span data-stu-id="76013-217">Requirement</span></span> | <span data-ttu-id="76013-218">Значение</span><span class="sxs-lookup"><span data-stu-id="76013-218">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="76013-219">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76013-219">Minimum supported client</span></span><br/> | <span data-ttu-id="76013-220">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76013-220">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="76013-221">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76013-221">Minimum supported server</span></span><br/> | <span data-ttu-id="76013-222">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76013-222">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="76013-223">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76013-223">See also</span></span>

<dl> <dt>

<span data-ttu-id="76013-224">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="76013-224">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="76013-225">**Аренда**</span><span class="sxs-lookup"><span data-stu-id="76013-225">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="76013-226">**фонтграуфдр**</span><span class="sxs-lookup"><span data-stu-id="76013-226">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="76013-227">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="76013-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="76013-228">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="76013-228">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="76013-229">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="76013-229">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="76013-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="76013-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

