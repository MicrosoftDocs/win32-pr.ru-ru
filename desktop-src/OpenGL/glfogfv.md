---
title: Функция glFogfv (Gl.h)
description: Функция Глфогфв задает параметры тумана. | Функция Глфогфв (GL. h)
ms.assetid: a2243ff4-4f3a-4b8c-b4fb-ce2cd74815e4
keywords:
- Функция Глфогфв OpenGL
topic_type:
- apiref
api_name:
- glFogfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407dd9b9c984a744e903a2c269d21028d32977a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273656"
---
# <a name="glfogfv-function"></a><span data-ttu-id="66f74-105">Функция Глфогфв</span><span class="sxs-lookup"><span data-stu-id="66f74-105">glFogfv function</span></span>

<span data-ttu-id="66f74-106">Функция **глфогфв** задает параметры тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f74-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66f74-107">Syntax</span></span>


```C++
void WINAPI glFogfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="66f74-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="66f74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f74-109">*pname*</span><span class="sxs-lookup"><span data-stu-id="66f74-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="66f74-110">Задает параметр тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="66f74-111">Принимает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="66f74-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="66f74-112">Значение</span><span class="sxs-lookup"><span data-stu-id="66f74-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="66f74-113">Значение</span><span class="sxs-lookup"><span data-stu-id="66f74-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="66f74-114"><dt>**\_режим тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="66f74-115">Параметр *params* — это значение с плавающей запятой, которое указывает уравнение, используемое для вычисления коэффициента смешения тумана, *f*.</span><span class="sxs-lookup"><span data-stu-id="66f74-115">The *params* parameter is a floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="66f74-116">Допустимы три символьных константы: GL \_ , GL \_ и GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="66f74-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="66f74-117">Уравнения, соответствующие этим символьным константам, определены в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="66f74-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="66f74-118">По умолчанию для тумана используется режим "GL \_ exp".</span><span class="sxs-lookup"><span data-stu-id="66f74-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                           |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="66f74-119"><dt>**\_плотность тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="66f74-120">Параметр *params* — это значение с плавающей запятой, определяющее *плотность*, плотность тумана, используемую в обоих экспоненциальных уравнениях.</span><span class="sxs-lookup"><span data-stu-id="66f74-120">The *params* parameter is a floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="66f74-121">Принимаются только неотрицательные плотности.</span><span class="sxs-lookup"><span data-stu-id="66f74-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="66f74-122">Плотность тумана по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="66f74-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                              |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="66f74-123"><dt>**Начало работы с \_ туманом GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="66f74-124">Параметр *params* — это значение с плавающей запятой, которое указывает *Start*, ближайшее расстояние, используемое в уравнении линейного тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-124">The *params* parameter is a floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="66f74-125">Ближайшее расстояние по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="66f74-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="66f74-126"><dt>**Окончание GL в главной \_ \_ части**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="66f74-127">Параметр *params* — это значение с плавающей запятой, которое указывает *конец*, расстояние, используемое в уравнении линейного тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-127">The *params* parameter is a floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="66f74-128">По умолчанию расстояние равно 1,0.</span><span class="sxs-lookup"><span data-stu-id="66f74-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="66f74-129"><dt>**\_индекс тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="66f74-130">Параметр *params* — это значение с плавающей запятой, которое указывает *i*<sub>f</sub> , цветовой индекс тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-130">The *params* parameter is a floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="66f74-131">Индекс тумана по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="66f74-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="66f74-132"><dt>**\_Цвет тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="66f74-133">Параметр *params* содержит четыре значения с плавающей запятой, определяющие *C*<sub>f</sub> , цвет тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-133">The *params* parameter contains four floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="66f74-134">Целочисленные значения сопоставляются линейно, так что наиболее положительное значение, представленное в результате, сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="66f74-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="66f74-135">Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="66f74-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="66f74-136">После преобразования все компоненты цвета записываются в диапазон \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="66f74-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="66f74-137">Цвет тумана по умолчанию — (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="66f74-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="66f74-138">*params*</span><span class="sxs-lookup"><span data-stu-id="66f74-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="66f74-139">Указывает значение или значения, которые будут назначены *pname*.</span><span class="sxs-lookup"><span data-stu-id="66f74-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="66f74-140">\_ \_ Для цвета в главной тумане требуется массив из четырех значений.</span><span class="sxs-lookup"><span data-stu-id="66f74-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="66f74-141">Все остальные параметры принимают массив, содержащий только одно значение.</span><span class="sxs-lookup"><span data-stu-id="66f74-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f74-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66f74-142">Return value</span></span>

<span data-ttu-id="66f74-143">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="66f74-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66f74-144">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="66f74-144">Error codes</span></span>

<span data-ttu-id="66f74-145">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="66f74-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="66f74-146">Имя</span><span class="sxs-lookup"><span data-stu-id="66f74-146">Name</span></span>                                                                                                  | <span data-ttu-id="66f74-147">Значение</span><span class="sxs-lookup"><span data-stu-id="66f74-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66f74-148"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="66f74-149">*pname* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="66f74-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="66f74-150"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="66f74-151">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="66f74-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="66f74-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66f74-152">Remarks</span></span>

<span data-ttu-id="66f74-153">Вы включаете и отключаете туман с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md), используя аргумент GL в виде \_ тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="66f74-154">При включении туман влияет на растровую геометрию, точечные рисунки и блоки пикселей, но не на операции очистки буфера.</span><span class="sxs-lookup"><span data-stu-id="66f74-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="66f74-155">Функция **глфогфв** присваивает значение или значения в *params* параметру тумана, заданному аргументом *pname*.</span><span class="sxs-lookup"><span data-stu-id="66f74-155">The **glFogfv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="66f74-156">Туман смешивает цвет тумана с каждым растровым цветом фрагмента пикселя с помощью коэффициента смешения *f*.</span><span class="sxs-lookup"><span data-stu-id="66f74-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="66f74-157">Коэффициент *f* может быть вычислен одним из трех способов в зависимости от режима тумана.</span><span class="sxs-lookup"><span data-stu-id="66f74-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="66f74-158">Пусть *z* — это расстояние в координатах глаз от начала до фогжед фрагмента.</span><span class="sxs-lookup"><span data-stu-id="66f74-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="66f74-159">Уравнение \_ линейного тумана GL:</span><span class="sxs-lookup"><span data-stu-id="66f74-159">The equation for GL\_LINEAR fog is:</span></span>

![Уравнение, показывающее значение GL_LINEAR тумана.](images/fog01.png)

<span data-ttu-id="66f74-161">Уравнение для наглавной \_ тумана GL имеет следующее:</span><span class="sxs-lookup"><span data-stu-id="66f74-161">The equation for GL\_EXP fog is:</span></span>

![Уравнение, показывающее значение коэффициента смешения в GL_EXP режиме тумана.](images/fog02.png)

<span data-ttu-id="66f74-163">Уравнение для \_ EXP2 тумана GL имеет следующее значение:</span><span class="sxs-lookup"><span data-stu-id="66f74-163">The equation for GL\_EXP2 fog is:</span></span>

![Уравнение, показывающее значение коэффициента смешения в GL_EXP2 режиме тумана.](images/fog03.png)

<span data-ttu-id="66f74-165">Независимо от режима тумана, *f* замещается в диапазон \[ 0, 1 \] после его расчета.</span><span class="sxs-lookup"><span data-stu-id="66f74-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="66f74-166">Затем, если OpenGL находится в режиме цвета RGBA, цвет кода *C*<sub>r</sub> заменяется на</span><span class="sxs-lookup"><span data-stu-id="66f74-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Уравнение, показывающее цвет фрагмента фогжед в виде функции коэффициента смешения и цвета тумана.](images/fog04.png)

<span data-ttu-id="66f74-168">В режиме индексирования Color индекс фрагмента, который *я* заменил <sub>r</sub> , заменяется на</span><span class="sxs-lookup"><span data-stu-id="66f74-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Уравнение, показывающее цветовой индекс фрагмента фогжед в качестве функции коэффициента смешения и индексированного цвета.](images/fog05.png)

<span data-ttu-id="66f74-170">Следующие функции извлекают сведения, относящиеся к функциям **глфог** :</span><span class="sxs-lookup"><span data-stu-id="66f74-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="66f74-171">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ Color для тумана \_</span><span class="sxs-lookup"><span data-stu-id="66f74-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="66f74-172">**глжет** с аргументом \_ index тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="66f74-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="66f74-173">**глжет** с аргументом \_ плотность ТУМАНа в ГК \_</span><span class="sxs-lookup"><span data-stu-id="66f74-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="66f74-174">**глжет** с аргументом \_ Start тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="66f74-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="66f74-175">**глжет** с аргументом \_ конец GL в тумане \_</span><span class="sxs-lookup"><span data-stu-id="66f74-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="66f74-176">**глжет** с аргументом в режиме GL в \_ тумане \_</span><span class="sxs-lookup"><span data-stu-id="66f74-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="66f74-177">[**глисенаблед**](glisenabled.md) с аргументом GL в виде \_ тумана</span><span class="sxs-lookup"><span data-stu-id="66f74-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="66f74-178">Требования</span><span class="sxs-lookup"><span data-stu-id="66f74-178">Requirements</span></span>



| <span data-ttu-id="66f74-179">Требование</span><span class="sxs-lookup"><span data-stu-id="66f74-179">Requirement</span></span> | <span data-ttu-id="66f74-180">Значение</span><span class="sxs-lookup"><span data-stu-id="66f74-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66f74-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66f74-181">Minimum supported client</span></span><br/> | <span data-ttu-id="66f74-182">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66f74-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="66f74-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66f74-183">Minimum supported server</span></span><br/> | <span data-ttu-id="66f74-184">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66f74-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66f74-185">Заголовок</span><span class="sxs-lookup"><span data-stu-id="66f74-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="66f74-186"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="66f74-187">Библиотека</span><span class="sxs-lookup"><span data-stu-id="66f74-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="66f74-188"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="66f74-189">DLL</span><span class="sxs-lookup"><span data-stu-id="66f74-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66f74-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66f74-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f74-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66f74-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f74-192">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="66f74-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="66f74-193">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="66f74-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="66f74-194">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="66f74-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="66f74-195">**гленд**</span><span class="sxs-lookup"><span data-stu-id="66f74-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="66f74-196">**глжет**</span><span class="sxs-lookup"><span data-stu-id="66f74-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="66f74-197">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="66f74-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





