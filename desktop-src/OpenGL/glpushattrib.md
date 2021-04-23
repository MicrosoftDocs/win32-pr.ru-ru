---
title: Функция Глпушаттриб (GL. h)
description: Помещает стек атрибутов.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- Функция Глпушаттриб OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071307"
---
# <a name="glpushattrib-function"></a><span data-ttu-id="5ddb8-104">Функция Глпушаттриб</span><span class="sxs-lookup"><span data-stu-id="5ddb8-104">glPushAttrib function</span></span>

<span data-ttu-id="5ddb8-105">Помещает стек атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-105">Pushes the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ddb8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ddb8-106">Syntax</span></span>


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="5ddb8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ddb8-108">*виде*</span><span class="sxs-lookup"><span data-stu-id="5ddb8-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddb8-109">Маска, указывающая, какие атрибуты следует сохранить.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-109">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="5ddb8-110">Константы символьной маски и связанные с ними состояния OpenGL имеют следующие значения (список абзацев с отступом, какие атрибуты сохраняются):</span><span class="sxs-lookup"><span data-stu-id="5ddb8-110">The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):</span></span>

<dl> <dt>

<span data-ttu-id="5ddb8-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_бит накопленного \_ буфера GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL\_ACCUM\_BUFFER\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="5ddb8-112">Очистить значение буфера накопления</span><span class="sxs-lookup"><span data-stu-id="5ddb8-112">Accumulation buffer clear value</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_ \_ бит буфера цвета \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL\_COLOR\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-114">\_ \_ Бит включения тестового альфа-канала GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-114">GL\_ALPHA\_TEST enable bit</span></span>

<span data-ttu-id="5ddb8-115">Функция тестирования Alpha и ссылочное значение</span><span class="sxs-lookup"><span data-stu-id="5ddb8-115">Alpha test function and reference value</span></span>

<span data-ttu-id="5ddb8-116">\_Бит включения для Blend в ГК</span><span class="sxs-lookup"><span data-stu-id="5ddb8-116">GL\_BLEND enable bit</span></span>

<span data-ttu-id="5ddb8-117">Наложение исходных и целевых функций</span><span class="sxs-lookup"><span data-stu-id="5ddb8-117">Blending source and destination functions</span></span>

<span data-ttu-id="5ddb8-118">\_Бит включения СГЛАЖИВАНИЯ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-118">GL\_DITHER enable bit</span></span>

<span data-ttu-id="5ddb8-119">\_ \_ Параметр буфера рисования GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-119">GL\_DRAW\_BUFFER setting</span></span>

<span data-ttu-id="5ddb8-120">\_Бит включения логики операций ГК \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-120">GL\_LOGIC\_OP enable bit</span></span>

<span data-ttu-id="5ddb8-121">Логическая функция Op</span><span class="sxs-lookup"><span data-stu-id="5ddb8-121">Logic op function</span></span>

<span data-ttu-id="5ddb8-122">Четкие значения в цветном режиме и в режиме индекса</span><span class="sxs-lookup"><span data-stu-id="5ddb8-122">Color-mode and index-mode clear values</span></span>

<span data-ttu-id="5ddb8-123">Цветовой режим и вритемаскс в режиме индекса</span><span class="sxs-lookup"><span data-stu-id="5ddb8-123">Color-mode and index-mode writemasks</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>\_текущий \_ бит GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL\_CURRENT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-125">Текущий цвет RGBA</span><span class="sxs-lookup"><span data-stu-id="5ddb8-125">Current RGBA color</span></span>

<span data-ttu-id="5ddb8-126">Текущий индекс цвета</span><span class="sxs-lookup"><span data-stu-id="5ddb8-126">Current color index</span></span>

<span data-ttu-id="5ddb8-127">Текущий вектор нормали</span><span class="sxs-lookup"><span data-stu-id="5ddb8-127">Current normal vector</span></span>

<span data-ttu-id="5ddb8-128">Текущие координаты текстуры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-128">Current texture coordinates</span></span>

<span data-ttu-id="5ddb8-129">Текущая разметка для текущей растровой \_ \_ \_ координаты ГК \_ допустимый флаг</span><span class="sxs-lookup"><span data-stu-id="5ddb8-129">Current raster position GL\_CURRENT\_RASTER\_POSITION\_VALID flag</span></span>

<span data-ttu-id="5ddb8-130">Цвет RGBA, связанный с текущей позицией в виде растрового изображения</span><span class="sxs-lookup"><span data-stu-id="5ddb8-130">RGBA color associated with current raster position</span></span>

<span data-ttu-id="5ddb8-131">Цветовой индекс, связанный с текущей позицией в виде растрового изображения</span><span class="sxs-lookup"><span data-stu-id="5ddb8-131">Color index associated with current raster position</span></span>

<span data-ttu-id="5ddb8-132">Координаты текстуры, связанные с текущей позицией в виде растрового изображения</span><span class="sxs-lookup"><span data-stu-id="5ddb8-132">Texture coordinates associated with current raster position</span></span>

<span data-ttu-id="5ddb8-133">\_Флаг флага пограничных колонтитулов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-133">GL\_EDGE\_FLAG flag</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_ \_ бит буфера глубины \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL\_DEPTH\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-135">\_ \_ Бит включения теста глубины в ГК</span><span class="sxs-lookup"><span data-stu-id="5ddb8-135">GL\_DEPTH\_TEST enable bit</span></span>

<span data-ttu-id="5ddb8-136">Функция тестирования буфера глубины</span><span class="sxs-lookup"><span data-stu-id="5ddb8-136">Depth buffer test function</span></span>

<span data-ttu-id="5ddb8-137">Очистить значение буфера глубины</span><span class="sxs-lookup"><span data-stu-id="5ddb8-137">Depth buffer clear value</span></span>

<span data-ttu-id="5ddb8-138">\_ \_ Бит включения ВРИТЕМАСК глубины GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-138">GL\_DEPTH\_WRITEMASK enable bit</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_бит включения \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL\_ENABLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-140">\_Флаг теста альфа-канала GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-140">GL\_ALPHA\_TEST flag</span></span>

<span data-ttu-id="5ddb8-141">\_Флаг автоматической \_ обычной настройки GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-141">GL\_AUTO\_NORMAL flag</span></span>

<span data-ttu-id="5ddb8-142">Флаг "Blend" в ГК \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-142">GL\_BLEND flag</span></span>

<span data-ttu-id="5ddb8-143">Включение BITS для определяемых пользователем обтравочных плоскостей</span><span class="sxs-lookup"><span data-stu-id="5ddb8-143">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="5ddb8-144">\_цветовой \_ материал GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-144">GL\_COLOR\_MATERIAL</span></span>

<span data-ttu-id="5ddb8-145">\_Флаг лица для отбора GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-145">GL\_CULL\_FACE flag</span></span>

<span data-ttu-id="5ddb8-146">\_ \_ Флаг теста глубины GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-146">GL\_DEPTH\_TEST flag</span></span>

<span data-ttu-id="5ddb8-147">\_Флаг СГЛАЖИВАНИЯ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-147">GL\_DITHER flag</span></span>

<span data-ttu-id="5ddb8-148">\_Флаг параметра тумана GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-148">GL\_FOG flag</span></span>

<span data-ttu-id="5ddb8-149">\_Некоторая легкая *я* , где 0 <= *i* < \_ Максимальное \_ освещение</span><span class="sxs-lookup"><span data-stu-id="5ddb8-149">GL\_LIGHT *i* where 0 <= *i* < GL\_MAX\_LIGHTS</span></span>

<span data-ttu-id="5ddb8-150">\_Флаг освещения GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-150">GL\_LIGHTING flag</span></span>

<span data-ttu-id="5ddb8-151">\_ \_ Флаг СГЛАЖИВАНИЯ линии GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-151">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="5ddb8-152">\_ \_ Флаг СТИППЛЕ строки GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-152">GL\_LINE\_STIPPLE flag</span></span>

<span data-ttu-id="5ddb8-153">\_ \_ Флаг логики логического цвета GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-153">GL\_COLOR\_LOGIC\_OP flag</span></span>

<span data-ttu-id="5ddb8-154">\_ \_ Флаг Op логики индекса GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-154">GL\_INDEX\_LOGIC\_OP flag</span></span>

<span data-ttu-id="5ddb8-155">GL \_ «Карта1» \_ x, где x — это тип Map</span><span class="sxs-lookup"><span data-stu-id="5ddb8-155">GL\_MAP1\_x where x is a map type</span></span>

<span data-ttu-id="5ddb8-156">GL \_ MAP2 \_ x, где x — это тип Map</span><span class="sxs-lookup"><span data-stu-id="5ddb8-156">GL\_MAP2\_x where x is a map type</span></span>

<span data-ttu-id="5ddb8-157">\_Флаг нормализации GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-157">GL\_NORMALIZE flag</span></span>

<span data-ttu-id="5ddb8-158">\_ \_ Флаг СГЛАЖИВАНИЯ точки GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-158">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="5ddb8-159">\_ \_ Флаг смещения строки для МНОГОУГОЛЬНИКов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-159">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="5ddb8-160">\_ \_ Флаг заполнения смещения для МНОГОУГОЛЬНИКов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-160">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="5ddb8-161">\_ \_ Флаг точки смещения для МНОГОУГОЛЬНИКов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-161">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="5ddb8-162">\_ \_ Флаг гладкого МНОГОУГОЛЬНИКа GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-162">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="5ddb8-163">\_Флаг стиппле для многоугольника GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-163">GL\_POLYGON\_STIPPLE flag</span></span>

<span data-ttu-id="5ddb8-164">\_Флаг теста "прямоугольная вырезание" \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-164">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="5ddb8-165">\_Флаг теста трафарета GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-165">GL\_STENCIL\_TEST flag</span></span>

<span data-ttu-id="5ddb8-166">\_ \_ Флаг одномерного текстуры GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-166">GL\_TEXTURE\_1D flag</span></span>

<span data-ttu-id="5ddb8-167">\_ \_ Флаг 2D текстуры GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-167">GL\_TEXTURE\_2D flag</span></span>

<span data-ttu-id="5ddb8-168">Помечает \_ заливку текстур главной книги ( \_ Gen \_ x), где x — S, T, R или Q</span><span class="sxs-lookup"><span data-stu-id="5ddb8-168">Flags GL\_TEXTURE\_GEN\_x where x is S, T, R, or Q</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>\_бит оценки \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL\_EVAL\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-170">GL \_ «Карта1» \_ x включает биты, где x — это тип Map</span><span class="sxs-lookup"><span data-stu-id="5ddb8-170">GL\_MAP1\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="5ddb8-171">GL \_ MAP2 \_ x включает биты, где x — это тип Map</span><span class="sxs-lookup"><span data-stu-id="5ddb8-171">GL\_MAP2\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="5ddb8-172">1-мерная конечные точки и подразделения сетки</span><span class="sxs-lookup"><span data-stu-id="5ddb8-172">1-D grid endpoints and divisions</span></span>

<span data-ttu-id="5ddb8-173">2-мерная конечные точки и подразделения сетки</span><span class="sxs-lookup"><span data-stu-id="5ddb8-173">2-D grid endpoints and divisions</span></span>

<span data-ttu-id="5ddb8-174">\_Бит автоматического \_ обычного включения GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-174">GL\_AUTO\_NORMAL enable bit</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>бит в главной системе \_ тумана \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL\_FOG\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-176">Флаг включения в GL для \_ тумана</span><span class="sxs-lookup"><span data-stu-id="5ddb8-176">GL\_FOG enable flag</span></span>

<span data-ttu-id="5ddb8-177">Цвет тумана</span><span class="sxs-lookup"><span data-stu-id="5ddb8-177">Fog color</span></span>

<span data-ttu-id="5ddb8-178">Плотность тумана</span><span class="sxs-lookup"><span data-stu-id="5ddb8-178">Fog density</span></span>

<span data-ttu-id="5ddb8-179">Начало линейного тумана</span><span class="sxs-lookup"><span data-stu-id="5ddb8-179">Linear fog start</span></span>

<span data-ttu-id="5ddb8-180">Конец линейной тумана</span><span class="sxs-lookup"><span data-stu-id="5ddb8-180">Linear fog end</span></span>

<span data-ttu-id="5ddb8-181">Индекс тумана</span><span class="sxs-lookup"><span data-stu-id="5ddb8-181">Fog index</span></span>

<span data-ttu-id="5ddb8-182">\_Значение режима тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-182">GL\_FOG\_MODE value</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>бит указания GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL\_HINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-184">\_ \_ Настройка подсказок по корректировке главной точки \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-184">GL\_PERSPECTIVE\_CORRECTION\_HINT setting</span></span>

<span data-ttu-id="5ddb8-185">\_ \_ Параметр гладкой подсказки для точки \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-185">GL\_POINT\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="5ddb8-186">\_ \_ Параметр СГЛАЖИВАНИЯ строки \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-186">GL\_LINE\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="5ddb8-187">\_ \_ Параметр гладкой подсказки для МНОГОУГОЛЬНИКов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-187">GL\_POLYGON\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="5ddb8-188">\_Параметр подсказки для параметра GL в ГК \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-188">GL\_FOG\_HINT setting</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_бит освещения \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL\_LIGHTING\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-190">\_ \_ Бит включения цветового материала GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-190">GL\_COLOR\_MATERIAL enable bit</span></span>

<span data-ttu-id="5ddb8-191">\_Значение цвета для цветового \_ материала GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-191">GL\_COLOR\_MATERIAL\_FACE value</span></span>

<span data-ttu-id="5ddb8-192">Параметры цветового материала, которые отслеживают текущий цвет</span><span class="sxs-lookup"><span data-stu-id="5ddb8-192">Color material parameters that are tracking the current color</span></span>

<span data-ttu-id="5ddb8-193">Цвет окружающей сцены</span><span class="sxs-lookup"><span data-stu-id="5ddb8-193">Ambient scene color</span></span>

<span data-ttu-id="5ddb8-194">\_ \_ \_ \_ Значение локального средства просмотра модели освещения GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-194">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER value</span></span>

<span data-ttu-id="5ddb8-195">\_ \_ Двусторонняя модель GL — \_ два \_ параметра</span><span class="sxs-lookup"><span data-stu-id="5ddb8-195">GL\_LIGHT\_MODEL\_TWO\_SIDE setting</span></span>

<span data-ttu-id="5ddb8-196">\_Бит включения освещения GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-196">GL\_LIGHTING enable bit</span></span>

<span data-ttu-id="5ddb8-197">Включить бит для каждого освещения</span><span class="sxs-lookup"><span data-stu-id="5ddb8-197">Enable bit for each light</span></span>

<span data-ttu-id="5ddb8-198">Интенсивность внешнего, рассеянного и отраженного света для каждого освещения</span><span class="sxs-lookup"><span data-stu-id="5ddb8-198">Ambient, diffuse, and specular intensity for each light</span></span>

<span data-ttu-id="5ddb8-199">Направление, расположение, показатель степени и угол отсечения для каждого освещения</span><span class="sxs-lookup"><span data-stu-id="5ddb8-199">Direction, position, exponent, and cutoff angle for each light</span></span>

<span data-ttu-id="5ddb8-200">Постоянные, линейные и квадратичные факторы ослабления для каждого освещения</span><span class="sxs-lookup"><span data-stu-id="5ddb8-200">Constant, linear, and quadratic attenuation factors for each light</span></span>

<span data-ttu-id="5ddb8-201">Цвет внешнего, рассеянного, отраженного и эмиссионныйного цвета для каждого материала</span><span class="sxs-lookup"><span data-stu-id="5ddb8-201">Ambient, diffuse, specular, and emissive color for each material</span></span>

<span data-ttu-id="5ddb8-202">Внешние, диффузные и отраженные цветовые индексы для каждого материала</span><span class="sxs-lookup"><span data-stu-id="5ddb8-202">Ambient, diffuse, and specular color indexes for each material</span></span>

<span data-ttu-id="5ddb8-203">Показатель степени отражения для каждого материала \_ , \_ параметр модели ОТТЕНКов GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-203">Specular exponent for each material GL\_SHADE\_MODEL setting</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_бит строки \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL\_LINE\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="5ddb8-205">\_ \_ Флаг СГЛАЖИВАНИЯ линии GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-205">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="5ddb8-206">\_ \_ Бит включения СТИППЛЕ строки GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-206">GL\_LINE\_STIPPLE enable bit</span></span>

<span data-ttu-id="5ddb8-207">Шаблон стиппле строки и счетчик повторов</span><span class="sxs-lookup"><span data-stu-id="5ddb8-207">Line stipple pattern and repeat counter</span></span>

<span data-ttu-id="5ddb8-208">Толщина линии</span><span class="sxs-lookup"><span data-stu-id="5ddb8-208">Line width</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_бит списка \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL\_LIST\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-210">\_ \_ Базовый параметр списка GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-210">GL\_LIST\_BASE setting</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_ \_ бит режима "пиксель" в GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL\_PIXEL\_MODE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-212">\_Параметры Красного \_ смещения и \_ красной \_ шкалы GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-212">GL\_RED\_BIAS and GL\_RED\_SCALE settings</span></span>

<span data-ttu-id="5ddb8-213">\_Значения зеленого \_ смещения и зеленого \_ \_ масштаба GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-213">GL\_GREEN\_BIAS and GL\_GREEN\_SCALE values</span></span>

<span data-ttu-id="5ddb8-214">\_Синий \_ сдвиг и \_ синяя \_ шкала GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-214">GL\_BLUE\_BIAS and GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="5ddb8-215">Смещение альфа-канала GL в ГК \_ \_ и \_ масштаб альфа-канала GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-215">GL\_ALPHA\_BIAS and GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="5ddb8-216">\_Смещение глубины \_ и \_ \_ Шкала глубины GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-216">GL\_DEPTH\_BIAS and GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="5ddb8-217">\_ \_ Значения смещения индекса GL и \_ \_ сдвига индекса GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-217">GL\_INDEX\_OFFSET and GL\_INDEX\_SHIFT values</span></span>

<span data-ttu-id="5ddb8-218">\_Цвет схемы GL \_ и \_ \_ Флаги трафарета схемы GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-218">GL\_MAP\_COLOR and GL\_MAP\_STENCIL flags</span></span>

<span data-ttu-id="5ddb8-219">\_ \_ \_ Коэффициенты по оси X и \_ масштаба GL в ГК</span><span class="sxs-lookup"><span data-stu-id="5ddb8-219">GL\_ZOOM\_X and GL\_ZOOM\_Y factors</span></span>

<span data-ttu-id="5ddb8-220">\_ \_ Параметр буфера чтения GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-220">GL\_READ\_BUFFER setting</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_бит точки \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL\_POINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-222">\_ \_ Флаг СГЛАЖИВАНИЯ точки GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-222">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="5ddb8-223">Размер точки</span><span class="sxs-lookup"><span data-stu-id="5ddb8-223">Point size</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>бит GL для \_ многоугольника \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL\_POLYGON\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-225">\_ \_ Бит включения лица для ОТБОРа GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-225">GL\_CULL\_FACE enable bit</span></span>

<span data-ttu-id="5ddb8-226">\_ \_ Значение режима "отбор лиц" в ГК \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-226">GL\_CULL\_FACE\_MODE value</span></span>

<span data-ttu-id="5ddb8-227">\_Индикатор переднего плана GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-227">GL\_FRONT\_FACE indicator</span></span>

<span data-ttu-id="5ddb8-228">\_Параметр режима многоугольников GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-228">GL\_POLYGON\_MODE setting</span></span>

<span data-ttu-id="5ddb8-229">\_ \_ Флаг гладкого МНОГОУГОЛЬНИКа GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-229">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="5ddb8-230">\_ \_ Бит включения стипплеого МНОГОУГОЛЬНИКа GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-230">GL\_POLYGON\_STIPPLE enable bit</span></span>

<span data-ttu-id="5ddb8-231">\_ \_ Флаг заполнения смещения для МНОГОУГОЛЬНИКов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-231">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="5ddb8-232">\_ \_ Флаг смещения строки для МНОГОУГОЛЬНИКов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-232">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="5ddb8-233">\_ \_ Флаг точки смещения для МНОГОУГОЛЬНИКов GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-233">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="5ddb8-234">\_коэффициент смещения для многоугольников GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-234">GL\_POLYGON\_OFFSET\_FACTOR</span></span>

<span data-ttu-id="5ddb8-235">\_единицы смещения многоугольников GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-235">GL\_POLYGON\_OFFSET\_UNITS</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_ \_ стипплеый БИТОВЫЙ многоугольник GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL\_POLYGON\_STIPPLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-237">Изображение многоугольника стиппле</span><span class="sxs-lookup"><span data-stu-id="5ddb8-237">Polygon stipple image</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>\_бит вырезание GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL\_SCISSOR\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-239">\_Флаг теста "прямоугольная вырезание" \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-239">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="5ddb8-240">Прямоугольная рамка</span><span class="sxs-lookup"><span data-stu-id="5ddb8-240">Scissor box</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_ \_ бит буфера шаблона \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL\_STENCIL\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-242">\_ \_ Бит включения теста для шаблона GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-242">GL\_STENCIL\_TEST enable bit</span></span>

<span data-ttu-id="5ddb8-243">Функция набора элементов и ссылочное значение</span><span class="sxs-lookup"><span data-stu-id="5ddb8-243">Stencil function and reference value</span></span>

<span data-ttu-id="5ddb8-244">Маска значения набора элементов</span><span class="sxs-lookup"><span data-stu-id="5ddb8-244">Stencil value mask</span></span>

<span data-ttu-id="5ddb8-245">Действия с набором элементов: сбой, передача и передача в буфере глубины</span><span class="sxs-lookup"><span data-stu-id="5ddb8-245">Stencil fail, pass, and depth buffer pass actions</span></span>

<span data-ttu-id="5ddb8-246">Очистить значение буфера набора элементов</span><span class="sxs-lookup"><span data-stu-id="5ddb8-246">Stencil buffer clear value</span></span>

<span data-ttu-id="5ddb8-247">Вритемаск буфера элементов</span><span class="sxs-lookup"><span data-stu-id="5ddb8-247">Stencil buffer writemask</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_бит текстуры \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL\_TEXTURE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-249">Включить BITS для четырех координат текстуры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-249">Enable bits for the four texture coordinates</span></span>

<span data-ttu-id="5ddb8-250">Цвет границы для каждого изображения текстуры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-250">Border color for each texture image</span></span>

<span data-ttu-id="5ddb8-251">Функция минификации для каждого изображения текстуры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-251">Minification function for each texture image</span></span>

<span data-ttu-id="5ddb8-252">Функция увеличения для каждого изображения текстуры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-252">Magnification function for each texture image</span></span>

<span data-ttu-id="5ddb8-253">Координаты текстуры и режим переноса для каждого изображения текстуры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-253">Texture coordinates and wrap mode for each texture image</span></span>

<span data-ttu-id="5ddb8-254">Цвет и режим для каждой среды текстуры</span><span class="sxs-lookup"><span data-stu-id="5ddb8-254">Color and mode for each texture environment</span></span>

<span data-ttu-id="5ddb8-255">Включить BITS GL \_ \_ , Gen \_ *x*; *x* — S, T, R и Q</span><span class="sxs-lookup"><span data-stu-id="5ddb8-255">Enable bits GL\_TEXTURE\_GEN\_*x*; *x* is S, T, R, and Q</span></span>

<span data-ttu-id="5ddb8-256">\_ \_ Настройка режима Gen текстура GL \_ для S, T, R и Q</span><span class="sxs-lookup"><span data-stu-id="5ddb8-256">GL\_TEXTURE\_GEN\_MODE setting for S, T, R, and Q</span></span>

<span data-ttu-id="5ddb8-257">уравнения Глтексжен плоскости для S, T, R и Q</span><span class="sxs-lookup"><span data-stu-id="5ddb8-257">glTexGen plane equations for S, T, R, and Q</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_бит преобразования \_ GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL\_TRANSFORM\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-259">Коэффициенты шести обтравочных плоскостей</span><span class="sxs-lookup"><span data-stu-id="5ddb8-259">Coefficients of the six clipping planes</span></span>

<span data-ttu-id="5ddb8-260">Включение BITS для определяемых пользователем обтравочных плоскостей</span><span class="sxs-lookup"><span data-stu-id="5ddb8-260">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="5ddb8-261">\_Значение режима матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-261">GL\_MATRIX\_MODE value</span></span>

<span data-ttu-id="5ddb8-262">\_Флаг нормализации GL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-262">GL\_NORMALIZE flag</span></span>

</dd> <dt>

<span data-ttu-id="5ddb8-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_бит окна просмотра GL \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL\_VIEWPORT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="5ddb8-264">Диапазон глубины (почти и далеко)</span><span class="sxs-lookup"><span data-stu-id="5ddb8-264">Depth range (near and far)</span></span>

<span data-ttu-id="5ddb8-265">Источник и экстент окна просмотра</span><span class="sxs-lookup"><span data-stu-id="5ddb8-265">Viewport origin and extent</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ddb8-266">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ddb8-266">Return value</span></span>

<span data-ttu-id="5ddb8-267">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-267">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ddb8-268">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5ddb8-268">Error codes</span></span>

<span data-ttu-id="5ddb8-269">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-269">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5ddb8-270">Имя</span><span class="sxs-lookup"><span data-stu-id="5ddb8-270">Name</span></span>                                                                                                  | <span data-ttu-id="5ddb8-271">Значение</span><span class="sxs-lookup"><span data-stu-id="5ddb8-271">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ddb8-272"><dt>**\_переполнение стека GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ddb8-272"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="5ddb8-273">Функция была вызвана во время заполнения стека атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-273">The function was called while the attribute stack was full.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="5ddb8-274"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5ddb8-274"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5ddb8-275">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5ddb8-275">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5ddb8-276">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ddb8-276">Remarks</span></span>

<span data-ttu-id="5ddb8-277">Функция **глпушаттриб** принимает один аргумент — маску, указывающую, какие группы переменных состояния следует сохранять в стеке атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-277">The **glPushAttrib** function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="5ddb8-278">Символьные константы используются для установки битов в маске.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-278">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="5ddb8-279">Параметр маски обычно создается путем применения логической операции **or** к некоторым из этих констант.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-279">The mask parameter is typically constructed by applying the logical **OR** operation to several of these constants.</span></span> <span data-ttu-id="5ddb8-280">\_ \_ \_ Чтобы сохранить все состояния с накоплением, можно использовать специальную маску GL для всех attrib.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-280">You can use the special mask GL\_ALL\_ATTRIB\_BITS to save all stackable states.</span></span>

<span data-ttu-id="5ddb8-281">Функция [**глпопаттриб**](glpopattrib.md) восстанавливает значения переменных состояния, сохраненные с помощью последней команды **глпушаттриб** .</span><span class="sxs-lookup"><span data-stu-id="5ddb8-281">The [**glPopAttrib**](glpopattrib.md) function restores the values of the state variables saved with the last **glPushAttrib** command.</span></span> <span data-ttu-id="5ddb8-282">Несохраненные данные остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-282">Those not saved are left unchanged.</span></span>

<span data-ttu-id="5ddb8-283">При принудительной отправке атрибутов в полный стек или при отключении атрибутов к пустому стеку возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-283">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="5ddb8-284">В любом случае устанавливается флаг ошибки, а в состояние OpenGL другие изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-284">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="5ddb8-285">Изначально стек атрибутов пуст.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-285">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="5ddb8-286">Не все значения для состояния OpenGL можно сохранить в стеке атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-286">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="5ddb8-287">Например, нельзя сохранить пакет пикселей и распаковать состояние, состояние режима рендеринга, а также состояние выбора и обратной связи.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-287">For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.</span></span>

<span data-ttu-id="5ddb8-288">Глубина стека атрибутов зависит от реализации, но должна быть не меньше 16.</span><span class="sxs-lookup"><span data-stu-id="5ddb8-288">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="5ddb8-289">Следующие функции извлекают сведения, относящиеся к **глпушаттриб** и [**глпопаттриб**](glpopattrib.md):</span><span class="sxs-lookup"><span data-stu-id="5ddb8-289">The following functions retrieve information related to **glPushAttrib** and [**glPopAttrib**](glpopattrib.md):</span></span>

<span data-ttu-id="5ddb8-290">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ attrib, \_ глубина стека \_</span><span class="sxs-lookup"><span data-stu-id="5ddb8-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="5ddb8-291">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ Максимальная \_ глубина стека \_ "</span><span class="sxs-lookup"><span data-stu-id="5ddb8-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="5ddb8-292">Требования</span><span class="sxs-lookup"><span data-stu-id="5ddb8-292">Requirements</span></span>



| <span data-ttu-id="5ddb8-293">Требование</span><span class="sxs-lookup"><span data-stu-id="5ddb8-293">Requirement</span></span> | <span data-ttu-id="5ddb8-294">Значение</span><span class="sxs-lookup"><span data-stu-id="5ddb8-294">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddb8-295">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ddb8-295">Minimum supported client</span></span><br/> | <span data-ttu-id="5ddb8-296">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ddb8-296">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5ddb8-297">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ddb8-297">Minimum supported server</span></span><br/> | <span data-ttu-id="5ddb8-298">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ddb8-298">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ddb8-299">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5ddb8-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ddb8-300"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ddb8-300"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5ddb8-301">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ddb8-301">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ddb8-302"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ddb8-302"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5ddb8-303">DLL</span><span class="sxs-lookup"><span data-stu-id="5ddb8-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ddb8-304"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ddb8-304"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ddb8-305">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ddb8-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddb8-306">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-306">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-307">**гленд**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-307">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-308">**глжет**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-308">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-309">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-309">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-310">**глжетеррор**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-310">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-311">**глжетлигхт**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-311">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-312">**глжетмап**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-312">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-313">**глжетматериал**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-313">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-314">**глжетпикселмап**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-314">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-315">**глжетполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-315">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-316">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-316">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-317">**глжеттексенв**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-317">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-318">**глжеттексжен**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-318">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-319">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-319">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-320">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-320">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-321">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-321">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="5ddb8-322">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="5ddb8-322">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





