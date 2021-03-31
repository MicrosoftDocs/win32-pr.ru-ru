---
title: Функция Глселектбуффер (GL. h)
description: Функция Глселектбуффер устанавливает буфер для значений режима выбора.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- Функция Глселектбуффер OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801180"
---
# <a name="glselectbuffer-function"></a><span data-ttu-id="e9994-104">Функция Глселектбуффер</span><span class="sxs-lookup"><span data-stu-id="e9994-104">glSelectBuffer function</span></span>

<span data-ttu-id="e9994-105">Функция **глселектбуффер** устанавливает буфер для значений режима выбора.</span><span class="sxs-lookup"><span data-stu-id="e9994-105">The **glSelectBuffer** function establishes a buffer for selection mode values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9994-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9994-106">Syntax</span></span>


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="e9994-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9994-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9994-108">*size*</span><span class="sxs-lookup"><span data-stu-id="e9994-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="e9994-109">Размер *буфера*.</span><span class="sxs-lookup"><span data-stu-id="e9994-109">The size of *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="e9994-110">*двойной*</span><span class="sxs-lookup"><span data-stu-id="e9994-110">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="e9994-111">Возвращает данные выбора.</span><span class="sxs-lookup"><span data-stu-id="e9994-111">Returns the selection data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9994-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9994-112">Return value</span></span>

<span data-ttu-id="e9994-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e9994-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9994-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e9994-114">Error codes</span></span>

<span data-ttu-id="e9994-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="e9994-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e9994-116">Имя</span><span class="sxs-lookup"><span data-stu-id="e9994-116">Name</span></span>                                                                                                  | <span data-ttu-id="e9994-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e9994-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9994-118"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e9994-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="e9994-119">*Размер* был отрицательным.</span><span class="sxs-lookup"><span data-stu-id="e9994-119">*size* was negative.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="e9994-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e9994-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e9994-121">Функция была вызвана, пока режим рендеринга был GL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="e9994-121">The function was called while the render mode was GL\_SELECT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="e9994-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e9994-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e9994-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e9994-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9994-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9994-124">Remarks</span></span>

<span data-ttu-id="e9994-125">Функция **глселектбуффер** имеет два параметра: *buffer* является указателем на массив целых чисел без знака, а *size* указывает размер массива.</span><span class="sxs-lookup"><span data-stu-id="e9994-125">The **glSelectBuffer** function has two parameters: *buffer* is a pointer to an array of unsigned integers, and *size* indicates the size of the array.</span></span> <span data-ttu-id="e9994-126">Параметр *buffer* возвращает значения из стека имен (см. [**глинитнамес**](glinitnames.md), [**гллоаднаме**](glloadname.md), [**глпушнаме**](glpushname.md)), если режимом отрисовки является GL \_ SELECT (см. [**глрендермоде**](glrendermode.md)).</span><span class="sxs-lookup"><span data-stu-id="e9994-126">The *buffer* parameter returns values from the name stack (see [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) when the rendering mode is GL\_SELECT (see [**glRenderMode**](glrendermode.md)).</span></span> <span data-ttu-id="e9994-127">Функция **глселектбуффер** должна быть выдана, прежде чем режим выбора будет включен, и она не должна выдаваться, пока для режима отрисовки \_ выбрано значение GL SELECT.</span><span class="sxs-lookup"><span data-stu-id="e9994-127">The **glSelectBuffer** function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL\_SELECT.</span></span>

<span data-ttu-id="e9994-128">Выделение используется программистом для определения примитивов, отображаемых в некоторой области окна.</span><span class="sxs-lookup"><span data-stu-id="e9994-128">Selection is used by a programmer to determine which primitives are drawn into some region of a window.</span></span> <span data-ttu-id="e9994-129">Регион определяется текущими моделвиев и матрицами перспективы.</span><span class="sxs-lookup"><span data-stu-id="e9994-129">The region is defined by the current modelview and perspective matrices.</span></span>

<span data-ttu-id="e9994-130">В режиме выделения фрагменты пикселей не создаются из растрирования.</span><span class="sxs-lookup"><span data-stu-id="e9994-130">In selection mode, no pixel fragments are produced from rasterization.</span></span> <span data-ttu-id="e9994-131">Вместо этого, если примитив пересекает громкость клипа, определяемую фрустум просмотра и определяемыми пользователем отсечениями, этот примитив приводит к попаданию в выделение.</span><span class="sxs-lookup"><span data-stu-id="e9994-131">Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit.</span></span> <span data-ttu-id="e9994-132">(При использовании многоугольников не происходит никаких попаданий, если многоугольник исключается.) При внесении изменений в стек имен или при вызове [**глрендермоде**](glrendermode.md) запись об попадании копируется в *буфер* , если с момента последнего такого события возникли какие-либо обращения (изменение стека имен или вызов **глрендермоде** ).</span><span class="sxs-lookup"><span data-stu-id="e9994-132">(With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when [**glRenderMode**](glrendermode.md) is called, a hit record is copied to *buffer* if any hits have occurred since the last such event (either a name stack change or a **glRenderMode** call).</span></span> <span data-ttu-id="e9994-133">Запись об попадании состоит из числа имен в стеке имен во время события. , за которым следуют минимальные и максимальные значения глубины всех вершин, которые были пройдены с момента предыдущего события; , за которым следует имя стека имен, сначала имя снизу.</span><span class="sxs-lookup"><span data-stu-id="e9994-133">The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.</span></span>

<span data-ttu-id="e9994-134">Возвращенные значения глубины сопоставлены таким, что самое большое целое число без знака соответствует глубине координат окна 1,0, а ноль соответствует глубине координат окна 0,0.</span><span class="sxs-lookup"><span data-stu-id="e9994-134">Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.</span></span>

<span data-ttu-id="e9994-135">При вводе режима выбора внутренний индекс в *буфере* сбрасывается в нуль.</span><span class="sxs-lookup"><span data-stu-id="e9994-135">An internal index into *buffer* is reset to zero whenever selection mode is entered.</span></span> <span data-ttu-id="e9994-136">При каждом копировании записи попадания в *буфер* индекс увеличивается, чтобы он указывал на ячейку, следующую за концом блока намессат, до следующей доступной ячейки.</span><span class="sxs-lookup"><span data-stu-id="e9994-136">Each time a hit record is copied into *buffer*, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell.</span></span> <span data-ttu-id="e9994-137">Значение, если запись о попадании больше, чем количество оставшихся мест в *буфере*, по мере копирования данных, которые можно разместить, и установлен флаг переполнения.</span><span class="sxs-lookup"><span data-stu-id="e9994-137">If the hit record is larger than the number of remaining locations in *buffer*, as much data as can fit is copied, and the overflow flag is set.</span></span> <span data-ttu-id="e9994-138">Если при копировании записи попаданий стек имен пуст, то эта запись состоит из нуля, за которой следуют минимальные и максимальные значения глубины.</span><span class="sxs-lookup"><span data-stu-id="e9994-138">If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.</span></span>

<span data-ttu-id="e9994-139">Режим выбора выходит из-за вызова **глрендермоде** с аргументом, ОТЛИЧНЫМ от GL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="e9994-139">Selection mode is exited by calling **glRenderMode** with an argument other than GL\_SELECT.</span></span> <span data-ttu-id="e9994-140">Всякий раз, когда **глрендермоде** вызывается, когда режим рендеринга — GL \_ SELECT, он возвращает число записей попаданий, скопированных в *буфер*, сбрасывает флаг переполнения и указатель на буфер выбора и инициализирует пустой стек имен.</span><span class="sxs-lookup"><span data-stu-id="e9994-140">Whenever **glRenderMode** is called while the render mode is GL\_SELECT, it returns the number of hit records copied to *buffer*, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty.</span></span> <span data-ttu-id="e9994-141">Если бит переполнения был установлен при вызове **глрендермоде** , возвращается отрицательное число записей попаданий.</span><span class="sxs-lookup"><span data-stu-id="e9994-141">If the overflow bit was set when **glRenderMode** was called, a negative hit record count is returned.</span></span>

<span data-ttu-id="e9994-142">Содержимое *буфера* не определено до тех пор, пока не будет вызван [**глрендермоде**](glrendermode.md) с аргументом, отличным от GL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="e9994-142">The contents of *buffer* are undefined until [**glRenderMode**](glrendermode.md) is called with an argument other than GL\_SELECT.</span></span>

<span data-ttu-id="e9994-143">**Глбегин** / **гленд** примитивы и вызовы [**глрастерпос**](glrasterpos-functions.md) могут привести к попаданию.</span><span class="sxs-lookup"><span data-stu-id="e9994-143">The **glBegin**/**glEnd** primitives and calls to [**glRasterPos**](glrasterpos-functions.md) can result in hits.</span></span>

<span data-ttu-id="e9994-144">Следующая функция получает сведения, связанные с **глселектбуффер**:</span><span class="sxs-lookup"><span data-stu-id="e9994-144">The following function retrieves information related to **glSelectBuffer**:</span></span>

<span data-ttu-id="e9994-145">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Длина стека имен GL \_</span><span class="sxs-lookup"><span data-stu-id="e9994-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="e9994-146">Требования</span><span class="sxs-lookup"><span data-stu-id="e9994-146">Requirements</span></span>



| <span data-ttu-id="e9994-147">Требование</span><span class="sxs-lookup"><span data-stu-id="e9994-147">Requirement</span></span> | <span data-ttu-id="e9994-148">Значение</span><span class="sxs-lookup"><span data-stu-id="e9994-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9994-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9994-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e9994-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9994-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e9994-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9994-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e9994-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e9994-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9994-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e9994-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9994-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9994-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e9994-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e9994-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9994-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9994-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9994-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e9994-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9994-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9994-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9994-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9994-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9994-160">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="e9994-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e9994-161">**гленд**</span><span class="sxs-lookup"><span data-stu-id="e9994-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e9994-162">**глфидбаккбуффер**</span><span class="sxs-lookup"><span data-stu-id="e9994-162">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="e9994-163">**глинитнамес**</span><span class="sxs-lookup"><span data-stu-id="e9994-163">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="e9994-164">**гллоаднаме**</span><span class="sxs-lookup"><span data-stu-id="e9994-164">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="e9994-165">**глпушнаме**</span><span class="sxs-lookup"><span data-stu-id="e9994-165">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="e9994-166">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="e9994-166">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





