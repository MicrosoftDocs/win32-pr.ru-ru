---
title: Функция Глполигоноффсет (GL. h)
description: Функция Глполигоноффсет задает масштаб и единицы, используемые OpenGL для вычисления значений глубины.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- Функция Глполигоноффсет OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415688"
---
# <a name="glpolygonoffset-function"></a><span data-ttu-id="d2970-104">Функция Глполигоноффсет</span><span class="sxs-lookup"><span data-stu-id="d2970-104">glPolygonOffset function</span></span>

<span data-ttu-id="d2970-105">Функция **глполигоноффсет** задает масштаб и единицы, используемые OpenGL для вычисления значений глубины.</span><span class="sxs-lookup"><span data-stu-id="d2970-105">The **glPolygonOffset** function sets the scale and units OpenGL uses to calculate depth values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2970-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2970-106">Syntax</span></span>


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a><span data-ttu-id="d2970-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2970-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2970-108">*многофакторной*</span><span class="sxs-lookup"><span data-stu-id="d2970-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="d2970-109">Задает коэффициент масштабирования, используемый для создания смещения глубины переменной для каждого многоугольника.</span><span class="sxs-lookup"><span data-stu-id="d2970-109">Specifies a scale factor that is used to create a variable depth offset for each polygon.</span></span> <span data-ttu-id="d2970-110">Начальное значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d2970-110">The initial value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2970-111">*Комплект*</span><span class="sxs-lookup"><span data-stu-id="d2970-111">*units*</span></span> 
</dt> <dd>

<span data-ttu-id="d2970-112">Задает значение, умноженное на значение, зависящее от реализации, для создания смещения глубины константы.</span><span class="sxs-lookup"><span data-stu-id="d2970-112">Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset.</span></span> <span data-ttu-id="d2970-113">Начальное значение равно 0.</span><span class="sxs-lookup"><span data-stu-id="d2970-113">The initial value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2970-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2970-114">Return value</span></span>

<span data-ttu-id="d2970-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d2970-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d2970-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d2970-116">Error codes</span></span>

<span data-ttu-id="d2970-117">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="d2970-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d2970-118">Имя</span><span class="sxs-lookup"><span data-stu-id="d2970-118">Name</span></span>                                                                                                  | <span data-ttu-id="d2970-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d2970-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2970-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d2970-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d2970-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d2970-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d2970-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2970-122">Remarks</span></span>

<span data-ttu-id="d2970-123">Если \_ включено смещение многоугольников GL \_ , то значение глубины каждого фрагмента будет смещено после интерполяции из значений глубины соответствующих вершин.</span><span class="sxs-lookup"><span data-stu-id="d2970-123">When GL\_POLYGON\_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices.</span></span> <span data-ttu-id="d2970-124">Значение смещения равно *множителю* \* ? z + r \* , где? z — это измерение изменения глубины относительно области экрана многоугольника, а r — наименьшее значение, которое гарантированно создает разрешаемое смещение для данной реализации.</span><span class="sxs-lookup"><span data-stu-id="d2970-124">The value of the offset is *factor* \* ?z + r \**units*, where ?z is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation.</span></span> <span data-ttu-id="d2970-125">Смещение добавляется перед выполнением теста глубины и перед записью значения в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="d2970-125">The offset is added before the depth test is performed and before the value is written into the depth buffer.</span></span>

<span data-ttu-id="d2970-126">Функция **глполигоноффсет** полезна для визуализации изображений в скрытом тексте, для применения декалс к поверхностям и для отрисовки сплошных с выделенными краями.</span><span class="sxs-lookup"><span data-stu-id="d2970-126">The **glPolygonOffset** function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.</span></span>

<span data-ttu-id="d2970-127">Функция **глполигоноффсет** не влияет на координаты глубины, помещенные в буфер обратной связи.</span><span class="sxs-lookup"><span data-stu-id="d2970-127">The **glPolygonOffset** function has no effect on depth coordinates placed in the feedback buffer.</span></span> <span data-ttu-id="d2970-128">Он также не влияет на выбор.</span><span class="sxs-lookup"><span data-stu-id="d2970-128">It also has no effect on selection.</span></span>

<span data-ttu-id="d2970-129">Следующие функции извлекают сведения, относящиеся к **глполигоноффсет**:</span><span class="sxs-lookup"><span data-stu-id="d2970-129">The following functions retrieve information related to **glPolygonOffset**:</span></span>

-   <span data-ttu-id="d2970-130">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ \_ коэффициент смещения" в ГК</span><span class="sxs-lookup"><span data-stu-id="d2970-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_FACTOR</span></span>
-   <span data-ttu-id="d2970-131">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ \_ единицы смещения" в GL</span><span class="sxs-lookup"><span data-stu-id="d2970-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_UNITS</span></span>
-   <span data-ttu-id="d2970-132">[**глисенаблед**](glisenabled.md) с аргументом GL, \_ \_ смещение смещения многоугольника \_</span><span class="sxs-lookup"><span data-stu-id="d2970-132">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_FILL</span></span>
-   <span data-ttu-id="d2970-133">[**глисенаблед**](glisenabled.md) с аргументом \_ \_ СМЕЩ. смещение \_ строки</span><span class="sxs-lookup"><span data-stu-id="d2970-133">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_LINE</span></span>
-   <span data-ttu-id="d2970-134">[**глисенаблед**](glisenabled.md) с аргументом в качестве \_ \_ точки смещения для многоугольника GL \_</span><span class="sxs-lookup"><span data-stu-id="d2970-134">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_POINT</span></span>

> [!Note]  
> <span data-ttu-id="d2970-135">Функция **глполигоноффсет** доступна только в OpenGl версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d2970-135">The **glPolygonOffset** function is only available in OpenGl version 1.1 or greater.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2970-136">Требования</span><span class="sxs-lookup"><span data-stu-id="d2970-136">Requirements</span></span>



| <span data-ttu-id="d2970-137">Требование</span><span class="sxs-lookup"><span data-stu-id="d2970-137">Requirement</span></span> | <span data-ttu-id="d2970-138">Значение</span><span class="sxs-lookup"><span data-stu-id="d2970-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2970-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2970-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d2970-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2970-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d2970-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2970-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d2970-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2970-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2970-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d2970-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2970-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2970-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d2970-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2970-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2970-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2970-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2970-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d2970-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2970-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2970-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2970-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2970-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2970-150">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="d2970-150">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="d2970-151">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="d2970-151">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="d2970-152">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="d2970-152">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="d2970-153">**глжет**</span><span class="sxs-lookup"><span data-stu-id="d2970-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d2970-154">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="d2970-154">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="d2970-155">**гллиневидс**</span><span class="sxs-lookup"><span data-stu-id="d2970-155">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="d2970-156">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="d2970-156">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="d2970-157">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="d2970-157">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





