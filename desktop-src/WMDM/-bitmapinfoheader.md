---
title: Структура _BITMAPINFOHEADER
description: '\_Структура битмапинфохеадер определяет формат видеокадра.'
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699043"
---
# <a name="_bitmapinfoheader-structure"></a><span data-ttu-id="9f4fe-104">\_Структура БИТМАПИНФОХЕАДЕР</span><span class="sxs-lookup"><span data-stu-id="9f4fe-104">\_BITMAPINFOHEADER structure</span></span>

<span data-ttu-id="9f4fe-105">Структура **\_ битмапинфохеадер** определяет формат видеокадра.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-105">The **\_BITMAPINFOHEADER** structure defines the format of a video frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4fe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f4fe-106">Syntax</span></span>


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="9f4fe-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9f4fe-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f4fe-108">**бисизе**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-108">**biSize**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-109">Указывает число байтов, необходимых для структуры.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-109">Specifies the number of bytes required by the structure.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-110">**бивидс**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-110">**biWidth**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-111">Задает ширину точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-111">Specifies the width of the bitmap, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-112">**бихеигхт**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-112">**biHeight**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-113">Задает высоту точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-113">Specifies the height of the bitmap, in pixels.</span></span> <span data-ttu-id="9f4fe-114">Если **бихеигхт** является положительным, то точечный рисунок имеет значение DIB, а его источник — в левом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-114">If **biHeight** is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner.</span></span> <span data-ttu-id="9f4fe-115">Если **бихеигхт** является отрицательным, точечный рисунок является верхним (DIB) и его источником является левый верхний угол.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-115">If **biHeight** is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.</span></span> <span data-ttu-id="9f4fe-116">Если **бихеигхт** имеет отрицательное значение, указывая, что значение DIB сверху вниз, **бикомпрессион** должно быть либо BI \_ RGB, либо BI \_ битовых полей.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-116">If **biHeight** is negative, indicating a top-down DIB, **biCompression** must be either BI\_RGB or BI\_BITFIELDS.</span></span> <span data-ttu-id="9f4fe-117">Не удается сжать файлы DIB, расположенные сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-117">Top-down DIBs cannot be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-118">**бипланес**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-118">**biPlanes**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-119">Указывает количество плоскостей для целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-119">Specifies the number of planes for the target device.</span></span> <span data-ttu-id="9f4fe-120">Это значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-120">This value must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-121">**бибиткаунт**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-121">**biBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-122">Указывает число битов на пиксель.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-122">Specifies the number of bits per pixel.</span></span> <span data-ttu-id="9f4fe-123">Элемент **бибиткаунт** структуры **битмапинфохеадер** определяет количество битов, определяющих каждый пиксель, и максимальное число цветов в точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-123">The **biBitCount** member of the **BITMAPINFOHEADER** structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap.</span></span> <span data-ttu-id="9f4fe-124">Этот элемент должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-124">This member must be one of the following values.</span></span>



| <span data-ttu-id="9f4fe-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9f4fe-125">Value</span></span> | <span data-ttu-id="9f4fe-126">Описание</span><span class="sxs-lookup"><span data-stu-id="9f4fe-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4fe-127">1</span><span class="sxs-lookup"><span data-stu-id="9f4fe-127">1</span></span>     | <span data-ttu-id="9f4fe-128">Точечный рисунок является монохромным, а элемент Бмиколорс содержит две записи.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-128">The bitmap is monochrome, and the bmiColors member contains two entries.</span></span> <span data-ttu-id="9f4fe-129">Каждый бит в массиве Bitmap представляет пиксель.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-129">Each bit in the bitmap array represents a pixel.</span></span> <span data-ttu-id="9f4fe-130">Если бит снят, пиксель отображается с цветом первой записи в таблице Бмиколорс; Если бит установлен, пиксел имеет цвет второй записи в таблице.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-130">If the bit is clear, the pixel is displayed with the color of the first entry in the bmiColors table; if the bit is set, the pixel has the color of the second entry in the table.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9f4fe-131">2</span><span class="sxs-lookup"><span data-stu-id="9f4fe-131">2</span></span>     | <span data-ttu-id="9f4fe-132">Точечный рисунок имеет четыре возможных значения цвета.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-132">The bitmap has four possible color values.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9f4fe-133">4</span><span class="sxs-lookup"><span data-stu-id="9f4fe-133">4</span></span>     | <span data-ttu-id="9f4fe-134">Точечный рисунок имеет не более 16 цветов, а элемент Бмиколорс содержит до 16 записей.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-134">The bitmap has a maximum of 16 colors, and the bmiColors member contains up to 16 entries.</span></span> <span data-ttu-id="9f4fe-135">Каждый пиксель точечного рисунка представлен 4-битным индексом в таблице цветов.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-135">Each pixel in the bitmap is represented by a 4-bit index into the color table.</span></span> <span data-ttu-id="9f4fe-136">Например, если первый байт в битовой карте — 0x1F, то байт представляет два пикселя.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-136">For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels.</span></span> <span data-ttu-id="9f4fe-137">Первый пиксель содержит цвет во второй записи таблицы, а второй пиксель содержит цвет в записи шестнадцатой таблицы.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-137">The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="9f4fe-138">8</span><span class="sxs-lookup"><span data-stu-id="9f4fe-138">8</span></span>     | <span data-ttu-id="9f4fe-139">Точечный рисунок имеет максимум 256 цветов, а элемент Бмиколорс содержит до 256 записей.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-139">The bitmap has a maximum of 256 colors, and the bmiColors member contains up to 256 entries.</span></span> <span data-ttu-id="9f4fe-140">В этом случае каждый байт в массиве представляет один пиксель.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-140">In this case, each byte in the array represents a single pixel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9f4fe-141">16</span><span class="sxs-lookup"><span data-stu-id="9f4fe-141">16</span></span>    | <span data-ttu-id="9f4fe-142">Размер точечного рисунка не должен превышать 2 ^ 16 цветов.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-142">The bitmap has a maximum of 2^16 colors.</span></span> <span data-ttu-id="9f4fe-143">Если элемент Бикомпрессион в БИТМАПИНФОХЕАДЕР является BI \_ RGB, то элемент бмиколорс имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-143">If the biCompression member of the BITMAPINFOHEADER is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="9f4fe-144">Каждое слово в массиве Bitmap представляет один пиксель.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-144">Each WORD in the bitmap array represents a single pixel.</span></span> <span data-ttu-id="9f4fe-145">Относительные интенситиес красного, зеленого и синего цветов представлены 5 битами для каждого компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-145">The relative intensities of red, green, and blue are represented with 5 bits for each color component.</span></span> <span data-ttu-id="9f4fe-146">Значение синего находится в наименее значащих 5 бит, за которым следуют 5 бит для зеленого и Красного.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-146">The value for blue is in the least significant 5 bits, followed by 5 bits each for green and red.</span></span> <span data-ttu-id="9f4fe-147">Наиболее значимый бит не используется.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-147">The most significant bit is not used.</span></span> <span data-ttu-id="9f4fe-148">Таблица цветов Бмиколорс используется для оптимизации цветов, используемых на устройствах на основе палитры, и должна содержать количество записей, заданных элементом Биклрусед.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-148">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span> |
| <span data-ttu-id="9f4fe-149">24</span><span class="sxs-lookup"><span data-stu-id="9f4fe-149">24</span></span>    | <span data-ttu-id="9f4fe-150">Битовая карта имеет не более 2 ^ 24 цветов, а элемент Бмиколорс имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-150">The bitmap has a maximum of 2^24 colors, and the bmiColors member is **NULL**.</span></span> <span data-ttu-id="9f4fe-151">Каждый 3-байтовый Triplet в массиве Bitmap представляет относительные интенситиес синего, зеленого и красного, соответственно, для пикселя.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-151">Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="9f4fe-152">Таблица цветов Бмиколорс используется для оптимизации цветов, используемых на устройствах на основе палитры, и должна содержать количество записей, заданных элементом Биклрусед.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-152">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="9f4fe-153">32</span><span class="sxs-lookup"><span data-stu-id="9f4fe-153">32</span></span>    | <span data-ttu-id="9f4fe-154">Размер точечного рисунка не должен превышать 2 ^ 32 цвета.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-154">The bitmap has a maximum of 2^32 colors.</span></span> <span data-ttu-id="9f4fe-155">Если элемент Бикомпрессион является BI \_ RGB, то элемент бмиколорс имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-155">If the biCompression member is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="9f4fe-156">Каждый DWORD в массиве Bitmap представляет относительные интенситиесы синего, зеленого и красного, соответственно, для пикселя.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-156">Each DWORD in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="9f4fe-157">Старший байт в каждом DWORD не используется.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-157">The high byte in each DWORD is not used.</span></span> <span data-ttu-id="9f4fe-158">Таблица цветов Бмиколорс используется для оптимизации цветов, используемых на устройствах на основе палитры, и должна содержать количество записей, заданных элементом Биклрусед.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-158">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="9f4fe-159">**бикомпрессион**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-159">**biCompression**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-160">Указывает тип сжатия для сжатого нижнего точечного рисунка (файлы DIB, расположенные сверху вниз, не могут быть сжаты).</span><span class="sxs-lookup"><span data-stu-id="9f4fe-160">Specifies the type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed).</span></span> <span data-ttu-id="9f4fe-161">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-161">This member can be the one of the following values.</span></span>



| <span data-ttu-id="9f4fe-162">Значение</span><span class="sxs-lookup"><span data-stu-id="9f4fe-162">Value</span></span>         | <span data-ttu-id="9f4fe-163">Описание</span><span class="sxs-lookup"><span data-stu-id="9f4fe-163">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4fe-164">RGB для BI \_</span><span class="sxs-lookup"><span data-stu-id="9f4fe-164">BI\_RGB</span></span>       | <span data-ttu-id="9f4fe-165">Несжатый формат.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-165">An uncompressed format.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9f4fe-166">Бизнес-аналитика \_ битовых полей</span><span class="sxs-lookup"><span data-stu-id="9f4fe-166">BI\_BITFIELDS</span></span> | <span data-ttu-id="9f4fe-167">Указывает, что точечный рисунок не сжимается и таблица цветов состоит из трех цветовых масок DWORD, которые задают красный, зеленый и синий компоненты соответственно для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-167">Specifies that the bitmap is not compressed and that the color table consists of three DWORD color masks that specify the red, green, and blue components, respectively, of each pixel.</span></span> <span data-ttu-id="9f4fe-168">Это допустимо при использовании точечных рисунков размером 16 бит и 32 бит/с.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-168">This is valid when used with 16-bpp and 32-bpp bitmaps.</span></span> <span data-ttu-id="9f4fe-169">Это значение допустимо в Microsoft Windows CE версии 2,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-169">This value is valid in Microsoft Windows CE version 2.0 and later.</span></span> |



 

</dd> <dt>

<span data-ttu-id="9f4fe-170">**бисизеимаже**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-170">**biSizeImage**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-171">Задает размер изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-171">Specifies the size of the image, in bytes.</span></span> <span data-ttu-id="9f4fe-172">Это может быть нулевое значение для \_ точечных рисунков RGB BI.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-172">This may be set to zero for BI\_RGB bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-173">**бикспелсперметер**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-173">**biXPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-174">Задает горизонтальное разрешение (в пикселях на счетчик) целевого устройства для точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-174">Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.</span></span> <span data-ttu-id="9f4fe-175">Приложение может использовать это значение для выбора точечного рисунка из группы ресурсов, который наилучшим образом соответствует характеристикам текущего устройства.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-175">An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-176">**бийпелсперметер**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-176">**biYPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-177">Задает вертикальное разрешение (в пикселях на счетчик) целевого устройства для точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-177">Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-178">**биклрусед**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-178">**biClrUsed**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-179">Указывает количество цветовых индексов в таблице цветов, которые фактически используются точечным рисунком.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-179">Specifies the number of color indexes in the color table that are actually used by the bitmap.</span></span> <span data-ttu-id="9f4fe-180">Если это значение равно нулю, точечный рисунок использует максимальное число цветов, соответствующее значению элемента **бибиткаунт** для режима сжатия, заданного параметром **бикомпрессион**.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-180">If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the **biBitCount** member for the compression mode specified by **biCompression**.</span></span>

</dd> <dt>

<span data-ttu-id="9f4fe-181">**биклримпортант**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-181">**biClrImportant**</span></span>
</dt> <dd>

<span data-ttu-id="9f4fe-182">Указывает количество цветовых индексов, необходимых для отображения точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-182">Specifies the number of color indexes required for displaying the bitmap.</span></span> <span data-ttu-id="9f4fe-183">Если это значение равно нулю, то требуются все цвета.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-183">If this value is zero, all colors are required.</span></span>

<span data-ttu-id="9f4fe-184">Если Биклрусед имеет ненулевое значение, а элемент Бибиткаунт меньше 16, то элемент Биклрусед указывает фактическое число цветов, к которым подсистема графики или драйвер устройства обращается.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-184">If biClrUsed is nonzero and the biBitCount member is less than 16, the biClrUsed member specifies the actual number of colors the graphics engine or device driver accesses.</span></span> <span data-ttu-id="9f4fe-185">Если Бибиткаунт имеет значение 16 или выше, то элемент Биклрусед указывает размер таблицы цветов, используемой для оптимизации производительности системных цветовых палитр.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-185">If biBitCount is 16 or greater, the biClrUsed member specifies the size of the color table used to optimize performance of the system color palettes.</span></span> <span data-ttu-id="9f4fe-186">Если Бибиткаунт равно 16 или 32, то оптимальная цветовая палитра начинается сразу после трех масок DWORD.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-186">If biBitCount equals 16 or 32, the optimal color palette starts immediately following the three DWORD masks.</span></span>

<span data-ttu-id="9f4fe-187">Если точечный рисунок является упакованным точечным рисунком (точечный рисунок, в котором массив точечных рисунков непосредственно следует за \_ структурой битмапинфохеадер и на него ссылается один указатель), то элемент биклрусед должен быть либо нулевым, либо фактическим размером таблицы цветов.</span><span class="sxs-lookup"><span data-stu-id="9f4fe-187">If the bitmap is a packed bitmap (a bitmap in which the bitmap array immediately follows the \_BITMAPINFOHEADER structure and is referenced by a single pointer), the biClrUsed member must be either zero or the actual size of the color table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f4fe-188">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f4fe-188">Remarks</span></span>

<span data-ttu-id="9f4fe-189">Эта структура содержится в структуре **\_ видеоинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="9f4fe-189">This structure is contained within a **\_VIDEOINFOHEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f4fe-190">Требования</span><span class="sxs-lookup"><span data-stu-id="9f4fe-190">Requirements</span></span>



| <span data-ttu-id="9f4fe-191">Требование</span><span class="sxs-lookup"><span data-stu-id="9f4fe-191">Requirement</span></span> | <span data-ttu-id="9f4fe-192">Значение</span><span class="sxs-lookup"><span data-stu-id="9f4fe-192">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4fe-193">Header</span><span class="sxs-lookup"><span data-stu-id="9f4fe-193">Header</span></span><br/> | <dl> <span data-ttu-id="9f4fe-194"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f4fe-194"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f4fe-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f4fe-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f4fe-196">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-196">**Structures**</span></span>](structures.md)
</dt> <dt>

[<span data-ttu-id="9f4fe-197">**\_видеоинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="9f4fe-197">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)
</dt> </dl>

 

 





