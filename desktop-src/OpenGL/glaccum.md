---
title: Функция Глаккум (GL. h)
description: Функция Глаккум работает с буфером накопления.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- Функция Глаккум OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802609"
---
# <a name="glaccum-function"></a><span data-ttu-id="86212-104">Функция Глаккум</span><span class="sxs-lookup"><span data-stu-id="86212-104">glAccum function</span></span>

<span data-ttu-id="86212-105">Функция **Глаккум** работает с буфером накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-105">The **glAccum** function operates on the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="86212-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86212-106">Syntax</span></span>


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a><span data-ttu-id="86212-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="86212-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86212-108">*операцион*</span><span class="sxs-lookup"><span data-stu-id="86212-108">*op*</span></span> 
</dt> <dd>

<span data-ttu-id="86212-109">Операция с буфером накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-109">The accumulation buffer operation.</span></span> <span data-ttu-id="86212-110">Допустимые символьные константы приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="86212-110">The accepted symbolic constants are as follows.</span></span>



| <span data-ttu-id="86212-111">Значение</span><span class="sxs-lookup"><span data-stu-id="86212-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="86212-112">Значение</span><span class="sxs-lookup"><span data-stu-id="86212-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <span data-ttu-id="86212-113"><dt>**\_накопленный счет ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="86212-113"><dt>**GL\_ACCUM**</dt></span></span> </dl>    | <span data-ttu-id="86212-114">Получает R, G, B и значения из буфера, выбранного в данный момент для чтения (см. [**глреадбуффер**](glreadbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="86212-114">Obtains R, G, B, and A values from the buffer currently selected for reading (see [**glReadBuffer**](glreadbuffer.md)).</span></span> <span data-ttu-id="86212-115">Значение каждого компонента делится на 2 *n*  1, где *n* — число битов, выделенных для каждого компонента цвета в выбранном буфере.</span><span class="sxs-lookup"><span data-stu-id="86212-115">Each component value is divided by 2 *n*  1, where *n* is the number of bits allocated to each color component in the currently selected buffer.</span></span> <span data-ttu-id="86212-116">Результатом является значение с плавающей запятой в диапазоне \[ 0, 1 \] , умноженное на *значение* и добавленное в соответствующий компонент пикселя в буфере накопления, тем самым обновляя буфер накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-116">The result is a floating-point value in the range \[0,1\], which is multiplied by *value* and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.</span></span><br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <span data-ttu-id="86212-117"><dt>**\_Загрузка GL**</dt></span><span class="sxs-lookup"><span data-stu-id="86212-117"><dt>**GL\_LOAD**</dt></span></span> </dl>       | <span data-ttu-id="86212-118">Аналогично \_ накоплению GL, за исключением того, что текущее значение в буфере накопления не используется при вычислении нового значения.</span><span class="sxs-lookup"><span data-stu-id="86212-118">Similar to GL\_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value.</span></span> <span data-ttu-id="86212-119">То есть R, G, B и значения из выбранного в данный момент буфера делятся на 2 *n*  1, умноженные на *значение*, а затем сохраняются в соответствующей ячейке буфера накопления, переписывая текущее значение.</span><span class="sxs-lookup"><span data-stu-id="86212-119">That is, the R, G, B, and A values from the currently selected buffer are divided by 2 *n*  1, multiplied by *value*, and then stored in the corresponding accumulation buffer cell, overwriting the current value.</span></span><br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <span data-ttu-id="86212-120"><dt>**Добавление в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="86212-120"><dt>**GL\_ADD**</dt></span></span> </dl>          | <span data-ttu-id="86212-121">Добавляет *значение* в каждый R, G, B и A в буфер накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-121">Adds *value* to each R, G, B, and A in the accumulation buffer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <span data-ttu-id="86212-122"><dt>**\_mult GL**</dt></span><span class="sxs-lookup"><span data-stu-id="86212-122"><dt>**GL\_MULT**</dt></span></span> </dl>       | <span data-ttu-id="86212-123">Умножает каждый R, G, B и A в буфер накопления по *значению* и возвращает масштабируемый компонент в соответствующее место в буфере накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-123">Multiplies each R, G, B, and A in the accumulation buffer by *value* and returns the scaled component to its corresponding accumulation buffer location.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <span data-ttu-id="86212-124"><dt>**\_Возврат GL**</dt></span><span class="sxs-lookup"><span data-stu-id="86212-124"><dt>**GL\_RETURN**</dt></span></span> </dl> | <span data-ttu-id="86212-125">Передает значения буфера накопления в буфер цветов или буферы, выбранные для записи.</span><span class="sxs-lookup"><span data-stu-id="86212-125">Transfers accumulation buffer values to the color buffer or buffers currently selected for writing.</span></span> <span data-ttu-id="86212-126">Каждый R, G, B и компонент умножается на *значение*, затем умножается на 2 *n*  1, а затем в диапазон \[ 0, 2 *n*  1 \] и сохраняется в соответствующей ячейке буфера вывода.</span><span class="sxs-lookup"><span data-stu-id="86212-126">Each R, G, B, and A component is multiplied by *value*, then multiplied by 2 *n*  1, clamped to the range \[0, 2 *n*  1 \], and stored in the corresponding display buffer cell.</span></span> <span data-ttu-id="86212-127">Единственными операциями фрагмента, применяемыми к этой операции, являются владение пикселями, распашная, дизеринг и цвет вритемаскс.</span><span class="sxs-lookup"><span data-stu-id="86212-127">The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.</span></span><br/>                                                                        |



 

</dd> <dt>

<span data-ttu-id="86212-128">*value*</span><span class="sxs-lookup"><span data-stu-id="86212-128">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="86212-129">Значение с плавающей запятой, используемое в операции с буфером накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-129">A floating-point value used in the accumulation buffer operation.</span></span> <span data-ttu-id="86212-130">Параметр *Op* определяет, как используется *значение* .</span><span class="sxs-lookup"><span data-stu-id="86212-130">The *op* parameter determines how *value* is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86212-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86212-131">Return value</span></span>

<span data-ttu-id="86212-132">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="86212-132">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86212-133">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="86212-133">Error codes</span></span>

<span data-ttu-id="86212-134">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="86212-134">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="86212-135">Имя</span><span class="sxs-lookup"><span data-stu-id="86212-135">Name</span></span>                                                                                                  | <span data-ttu-id="86212-136">Значение</span><span class="sxs-lookup"><span data-stu-id="86212-136">Meaning</span></span>                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86212-137"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="86212-137"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="86212-138">*Операция* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="86212-138">*op* was not an accepted value.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="86212-139"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="86212-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="86212-140">Не удалось получить буфер накопления, или функция **Глаккум** была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="86212-140">There was no accumulation buffer or the function **glAccum** was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="86212-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86212-141">Remarks</span></span>

<span data-ttu-id="86212-142">Буфер накопления — это цветовой буфер расширенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="86212-142">The accumulation buffer is an extended-range color buffer.</span></span> <span data-ttu-id="86212-143">Изображения не подготавливаются к просмотру.</span><span class="sxs-lookup"><span data-stu-id="86212-143">Images are not rendered into it.</span></span> <span data-ttu-id="86212-144">Вместо этого изображения, отображаемые в один из буферов цветов, добавляются к содержимому буфера накопления после подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="86212-144">Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering.</span></span> <span data-ttu-id="86212-145">Вы можете создавать такие эффекты, как сглаживание (точки, линии и многоугольники), размытие движения и глубина поля, путем накопления изображений, созданных с помощью различных матриц преобразования.</span><span class="sxs-lookup"><span data-stu-id="86212-145">You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.</span></span>

<span data-ttu-id="86212-146">Каждый пиксель в буфере накопления состоит из значений красного, зеленого, синего и альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="86212-146">Each pixel in the accumulation buffer consists of red, green, blue, and alpha values.</span></span> <span data-ttu-id="86212-147">Количество битов на компонент в буфере накопления зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="86212-147">The number of bits per component in the accumulation buffer depends on the implementation.</span></span> <span data-ttu-id="86212-148">Вы можете проверить это число, вызвав [**глжетинтежерв**](glgetintegerv.md) четыре раза, используя аргументы, \_ накопленные красные биты, счета ГК, накопленные \_ \_ \_ \_ \_ \_ \_ синие \_ биты, а также \_ альфа-биты главной накопления \_ \_ , соответственно.</span><span class="sxs-lookup"><span data-stu-id="86212-148">You can examine this number by calling [**glGetIntegerv**](glgetintegerv.md) four times, with the arguments GL\_ACCUM\_RED\_BITS, GL\_ACCUM\_GREEN\_BITS, GL\_ACCUM\_BLUE\_BITS, and GL\_ACCUM\_ALPHA\_BITS, respectively.</span></span> <span data-ttu-id="86212-149">Независимо от количества битов на каждый компонент, диапазон значений, хранящихся в каждом компоненте, равен \[ 1,? 1 \] .</span><span class="sxs-lookup"><span data-stu-id="86212-149">Regardless of the number of bits per component, however, the range of values stored by each component is \[ 1,?1\].</span></span> <span data-ttu-id="86212-150">Пикселы буфера накопления сопоставляются один к одному с буфера кадров пикселами.</span><span class="sxs-lookup"><span data-stu-id="86212-150">The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.</span></span>

<span data-ttu-id="86212-151">Функция **Глаккум** работает с буфером накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-151">The **glAccum** function operates on the accumulation buffer.</span></span> <span data-ttu-id="86212-152">Первый аргумент *Op*— это символьная константа, которая выбирает операцию с буфером накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-152">The first argument, *op*, is a symbolic constant that selects an accumulation buffer operation.</span></span> <span data-ttu-id="86212-153">Вторым аргументом, *value*, является значение с плавающей запятой, которое будет использоваться в этой операции.</span><span class="sxs-lookup"><span data-stu-id="86212-153">The second argument, *value*, is a floating-point value to be used in that operation.</span></span> <span data-ttu-id="86212-154">Указаны пять операций: счет ГК \_ , Загрузка GL \_ , \_ Добавление в ГК, GL \_ mult и возврат ГК \_ .</span><span class="sxs-lookup"><span data-stu-id="86212-154">Five operations are specified: GL\_ACCUM, GL\_LOAD, GL\_ADD, GL\_MULT, and GL\_RETURN.</span></span>

<span data-ttu-id="86212-155">Все операции с буфером накопления ограничены областью текущего прямоугольного поля и применяются к красному, зеленому, синему и альфа-компонентам каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="86212-155">All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel.</span></span> <span data-ttu-id="86212-156">Содержимое компонента пикселей буфера накопления не определено, если операция **Глаккум** приводит к получению значения за пределами диапазона \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="86212-156">The contents of an accumulation buffer pixel component are undefined if the **glAccum** operation results in a value outside the range \[ 1,1\].</span></span>

<span data-ttu-id="86212-157">Чтобы очистить буфер накопления, используйте функцию [**глклеараккум**](glclearaccum.md) , чтобы указать R, G, B и значения, чтобы присвоить ей значение, и выдать функцию [**глклеар**](glclear.md) с включенным буфером накопления.</span><span class="sxs-lookup"><span data-stu-id="86212-157">To clear the accumulation buffer, use the [**glClearAccum**](glclearaccum.md) function to specify R, G, B, and A values to set it to, and issue a [**glClear**](glclear.md) function with the accumulation buffer enabled.</span></span>

<span data-ttu-id="86212-158">Любая операция **Глаккум** обновляет только те Пиксели в пределах текущей прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="86212-158">Only those pixels within the current scissor box are updated by any **glAccum** operation.</span></span>

<span data-ttu-id="86212-159">Следующие функции извлекают сведения, относящиеся к функции **Глаккум** :</span><span class="sxs-lookup"><span data-stu-id="86212-159">The following functions retrieve information related to the **glAccum** function:</span></span>

<span data-ttu-id="86212-160">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Накопл. \_ красный \_ бит</span><span class="sxs-lookup"><span data-stu-id="86212-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_RED\_BITS</span></span>

<span data-ttu-id="86212-161">**глжет** с аргументом GL \_ накопленные \_ зеленые \_ биты</span><span class="sxs-lookup"><span data-stu-id="86212-161">**glGet** with argument GL\_ACCUM\_GREEN\_BITS</span></span>

<span data-ttu-id="86212-162">**глжет** с аргументом GL \_ Накопл. \_ синие \_ биты</span><span class="sxs-lookup"><span data-stu-id="86212-162">**glGet** with argument GL\_ACCUM\_BLUE\_BITS</span></span>

<span data-ttu-id="86212-163">**глжет** с аргументом " \_ накопленные \_ альфа- \_ биты GL"</span><span class="sxs-lookup"><span data-stu-id="86212-163">**glGet** with argument GL\_ACCUM\_ALPHA\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="86212-164">Требования</span><span class="sxs-lookup"><span data-stu-id="86212-164">Requirements</span></span>



| <span data-ttu-id="86212-165">Требование</span><span class="sxs-lookup"><span data-stu-id="86212-165">Requirement</span></span> | <span data-ttu-id="86212-166">Значение</span><span class="sxs-lookup"><span data-stu-id="86212-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86212-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86212-167">Minimum supported client</span></span><br/> | <span data-ttu-id="86212-168">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86212-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="86212-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86212-169">Minimum supported server</span></span><br/> | <span data-ttu-id="86212-170">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86212-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86212-171">Заголовок</span><span class="sxs-lookup"><span data-stu-id="86212-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="86212-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="86212-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="86212-173">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86212-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="86212-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86212-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="86212-175">DLL</span><span class="sxs-lookup"><span data-stu-id="86212-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86212-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86212-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86212-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86212-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86212-178">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="86212-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="86212-179">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="86212-179">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="86212-180">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="86212-180">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="86212-181">**глклеараккум**</span><span class="sxs-lookup"><span data-stu-id="86212-181">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="86212-182">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="86212-182">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="86212-183">**гленд**</span><span class="sxs-lookup"><span data-stu-id="86212-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="86212-184">**глжет**</span><span class="sxs-lookup"><span data-stu-id="86212-184">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="86212-185">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="86212-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="86212-186">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="86212-186">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="86212-187">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="86212-187">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="86212-188">**глреадбуффер**</span><span class="sxs-lookup"><span data-stu-id="86212-188">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="86212-189">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="86212-189">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="86212-190">**глсЦиссор**</span><span class="sxs-lookup"><span data-stu-id="86212-190">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="86212-191">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="86212-191">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





