---
title: Функция glFogi (Gl.h)
description: Функция Глфоги задает параметры тумана.
ms.assetid: c2ffb41d-3d97-4b72-b16d-cfbffa1179d1
keywords:
- Функция Глфоги OpenGL
topic_type:
- apiref
api_name:
- glFogi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc718a007035204f6e984eea87f1e21ba09ac8f0
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "103913960"
---
# <a name="glfogi-function"></a><span data-ttu-id="9aab2-104">Функция Глфоги</span><span class="sxs-lookup"><span data-stu-id="9aab2-104">glFogi function</span></span>

<span data-ttu-id="9aab2-105">Функция **глфоги** задает параметры тумана.</span><span class="sxs-lookup"><span data-stu-id="9aab2-105">The **glFogi** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aab2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aab2-106">Syntax</span></span>


```C++
void WINAPI glFogi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="9aab2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9aab2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aab2-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="9aab2-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="9aab2-109">Задает однозначный параметр тумана.</span><span class="sxs-lookup"><span data-stu-id="9aab2-109">Specifies a single-valued fog parameter.</span></span>

<span data-ttu-id="9aab2-110">Принимает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9aab2-110">Accepts one of the following values.</span></span>



| <span data-ttu-id="9aab2-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9aab2-111">Value</span></span>                                                                                                                                                             | <span data-ttu-id="9aab2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9aab2-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="9aab2-113"><dt>**\_режим тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-113"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="9aab2-114">Параметр *params* — это одно целое значение, указывающее уравнение, используемое для расчета коэффициента смешения тумана, *f*.</span><span class="sxs-lookup"><span data-stu-id="9aab2-114">The *params* parameter is a single integer value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="9aab2-115">Допустимы три символьных константы: GL \_ , GL \_ и GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="9aab2-115">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="9aab2-116">Уравнения, соответствующие этим символьным константам, определены в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="9aab2-116">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="9aab2-117">По умолчанию для тумана используется режим "GL \_ exp".</span><span class="sxs-lookup"><span data-stu-id="9aab2-117">The default fog mode is GL\_EXP.</span></span><br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="9aab2-118"><dt>**\_плотность тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-118"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="9aab2-119">Параметр *params* — это одно целое значение, указывающее *плотность*, плотность тумана, используемую в обоих экспоненциальных уравнениях.</span><span class="sxs-lookup"><span data-stu-id="9aab2-119">The *params* parameter is a single integer value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="9aab2-120">Принимаются только неотрицательные плотности.</span><span class="sxs-lookup"><span data-stu-id="9aab2-120">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="9aab2-121">Плотность тумана по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="9aab2-121">The default fog density is 1.0.</span></span><br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="9aab2-122"><dt>**Начало работы с \_ туманом GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-122"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="9aab2-123">Параметр *params* — это одно целое значение, указывающее *Start*, близкое расстояние, используемое в уравнении линейного тумана.</span><span class="sxs-lookup"><span data-stu-id="9aab2-123">The *params* parameter is a single integer value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="9aab2-124">Ближайшее расстояние по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="9aab2-124">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="9aab2-125"><dt>**Окончание GL в главной \_ \_ части**</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-125"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="9aab2-126">Параметр *params* — это одно целочисленное значение, указывающее *End*, расстояние, используемое в уравнении линейного тумана.</span><span class="sxs-lookup"><span data-stu-id="9aab2-126">The *params* parameter is a single integer value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="9aab2-127">По умолчанию расстояние равно 1,0.</span><span class="sxs-lookup"><span data-stu-id="9aab2-127">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="9aab2-128"><dt>**\_индекс тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-128"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="9aab2-129">Параметр *params* — это одно целочисленное значение, указывающее *i*<sub>f</sub> , цветовой индекс тумана.</span><span class="sxs-lookup"><span data-stu-id="9aab2-129">The *params* parameter is a single integer value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="9aab2-130">Индекс тумана по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="9aab2-130">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="9aab2-131">*param*</span><span class="sxs-lookup"><span data-stu-id="9aab2-131">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="9aab2-132">Указывает значение, которое будет задано для *pname* .</span><span class="sxs-lookup"><span data-stu-id="9aab2-132">Specifies the value that *pname* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aab2-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9aab2-133">Return value</span></span>

<span data-ttu-id="9aab2-134">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9aab2-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9aab2-135">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9aab2-135">Error codes</span></span>

<span data-ttu-id="9aab2-136">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="9aab2-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9aab2-137">Имя</span><span class="sxs-lookup"><span data-stu-id="9aab2-137">Name</span></span>                                                                                                  | <span data-ttu-id="9aab2-138">Значение</span><span class="sxs-lookup"><span data-stu-id="9aab2-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9aab2-139"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9aab2-140">*pname* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="9aab2-140">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="9aab2-141"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9aab2-142">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9aab2-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9aab2-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9aab2-143">Remarks</span></span>

<span data-ttu-id="9aab2-144">Вы включаете и отключаете туман с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md), используя аргумент GL в виде \_ тумана.</span><span class="sxs-lookup"><span data-stu-id="9aab2-144">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="9aab2-145">При включении туман влияет на растровую геометрию, точечные рисунки и блоки пикселей, но не на операции очистки буфера.</span><span class="sxs-lookup"><span data-stu-id="9aab2-145">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="9aab2-146">Функция **глфоги** присваивает значение или значения в *params* параметру тумана, заданному аргументом *pname*.</span><span class="sxs-lookup"><span data-stu-id="9aab2-146">The **glFogi** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="9aab2-147">Туман смешивает цвет тумана с каждым растровым цветом фрагмента пикселя с помощью коэффициента смешения *f*.</span><span class="sxs-lookup"><span data-stu-id="9aab2-147">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="9aab2-148">Коэффициент *f* может быть вычислен одним из трех способов в зависимости от режима тумана.</span><span class="sxs-lookup"><span data-stu-id="9aab2-148">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="9aab2-149">Пусть *z* — это расстояние в координатах глаз от начала до фогжед фрагмента.</span><span class="sxs-lookup"><span data-stu-id="9aab2-149">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="9aab2-150">Уравнение \_ линейного тумана GL:</span><span class="sxs-lookup"><span data-stu-id="9aab2-150">The equation for GL\_LINEAR fog is:</span></span>

![Уравнение, показывающее значение GL_LINEAR тумана.](images/fog01.png)

<span data-ttu-id="9aab2-152">Уравнение для наглавной \_ тумана GL имеет следующее:</span><span class="sxs-lookup"><span data-stu-id="9aab2-152">The equation for GL\_EXP fog is:</span></span>

![Уравнение, показывающее значение коэффициента смешения в GL_EXP режиме тумана.](images/fog02.png)

<span data-ttu-id="9aab2-154">Уравнение для \_ EXP2 тумана GL имеет следующее значение:</span><span class="sxs-lookup"><span data-stu-id="9aab2-154">The equation for GL\_EXP2 fog is:</span></span>

![Уравнение, показывающее значение коэффициента смешения в GL_EXP2 режиме тумана.](images/fog03.png)

<span data-ttu-id="9aab2-156">Независимо от режима тумана, *f* замещается в диапазон \[ 0, 1 \] после его расчета.</span><span class="sxs-lookup"><span data-stu-id="9aab2-156">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="9aab2-157">Затем, если OpenGL находится в режиме цвета RGBA, цвет кода *C*<sub>r</sub> заменяется на</span><span class="sxs-lookup"><span data-stu-id="9aab2-157">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Уравнение, показывающее цвет фрагмента фогжед в виде функции коэффициента смешения и цвета тумана.](images/fog04.png)

<span data-ttu-id="9aab2-159">В режиме индексирования Color индекс фрагмента, который *я* заменил <sub>r</sub> , заменяется на</span><span class="sxs-lookup"><span data-stu-id="9aab2-159">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Уравнение, показывающее цветовой индекс фрагмента фогжед в качестве функции коэффициента смешения и индексированного цвета.](images/fog05.png)

<span data-ttu-id="9aab2-161">Следующие функции извлекают сведения, относящиеся к функциям **глфог** :</span><span class="sxs-lookup"><span data-stu-id="9aab2-161">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="9aab2-162">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ Color для тумана \_</span><span class="sxs-lookup"><span data-stu-id="9aab2-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="9aab2-163">**глжет** с аргументом \_ index тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="9aab2-163">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="9aab2-164">**глжет** с аргументом \_ плотность ТУМАНа в ГК \_</span><span class="sxs-lookup"><span data-stu-id="9aab2-164">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="9aab2-165">**глжет** с аргументом \_ Start тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="9aab2-165">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="9aab2-166">**глжет** с аргументом \_ конец GL в тумане \_</span><span class="sxs-lookup"><span data-stu-id="9aab2-166">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="9aab2-167">**глжет** с аргументом в режиме GL в \_ тумане \_</span><span class="sxs-lookup"><span data-stu-id="9aab2-167">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="9aab2-168">[**глисенаблед**](glisenabled.md) с аргументом GL в виде \_ тумана</span><span class="sxs-lookup"><span data-stu-id="9aab2-168">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="9aab2-169">Требования</span><span class="sxs-lookup"><span data-stu-id="9aab2-169">Requirements</span></span>



| <span data-ttu-id="9aab2-170">Требование</span><span class="sxs-lookup"><span data-stu-id="9aab2-170">Requirement</span></span> | <span data-ttu-id="9aab2-171">Значение</span><span class="sxs-lookup"><span data-stu-id="9aab2-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aab2-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9aab2-172">Minimum supported client</span></span><br/> | <span data-ttu-id="9aab2-173">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9aab2-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9aab2-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9aab2-174">Minimum supported server</span></span><br/> | <span data-ttu-id="9aab2-175">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9aab2-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9aab2-176">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9aab2-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aab2-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9aab2-178">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9aab2-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="9aab2-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9aab2-180">DLL</span><span class="sxs-lookup"><span data-stu-id="9aab2-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aab2-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aab2-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aab2-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9aab2-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aab2-183">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="9aab2-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9aab2-184">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="9aab2-184">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="9aab2-185">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="9aab2-185">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9aab2-186">**гленд**</span><span class="sxs-lookup"><span data-stu-id="9aab2-186">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9aab2-187">**глжет**</span><span class="sxs-lookup"><span data-stu-id="9aab2-187">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9aab2-188">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="9aab2-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





