---
title: Функция Глдравбуффер (GL. h)
description: Функция Глдравбуффер определяет, в какие буферы цветов должны быть выведены.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- Функция Глдравбуффер OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661855"
---
# <a name="gldrawbuffer-function"></a><span data-ttu-id="260a8-104">Функция Глдравбуффер</span><span class="sxs-lookup"><span data-stu-id="260a8-104">glDrawBuffer function</span></span>

<span data-ttu-id="260a8-105">Функция **глдравбуффер** определяет, в какие буферы цветов должны быть выведены.</span><span class="sxs-lookup"><span data-stu-id="260a8-105">The **glDrawBuffer** function specifies which color buffers are to be drawn into.</span></span>

## <a name="syntax"></a><span data-ttu-id="260a8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="260a8-106">Syntax</span></span>


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="260a8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="260a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="260a8-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="260a8-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="260a8-109">Указывает до четырех буферов цветов для отображения в следующих допустимых символьных константах.</span><span class="sxs-lookup"><span data-stu-id="260a8-109">Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.</span></span>



| <span data-ttu-id="260a8-110">Значение</span><span class="sxs-lookup"><span data-stu-id="260a8-110">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="260a8-111">Значение</span><span class="sxs-lookup"><span data-stu-id="260a8-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <span data-ttu-id="260a8-112"><dt>**\_нет GL**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-112"><dt>**GL\_NONE**</dt></span></span> </dl>                                 | <span data-ttu-id="260a8-113">Буферы цветов не записываются.</span><span class="sxs-lookup"><span data-stu-id="260a8-113">No color buffers are written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <span data-ttu-id="260a8-114"><dt>**GL \_ спереди \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-114"><dt>**GL\_FRONT\_LEFT**</dt></span></span> </dl>              | <span data-ttu-id="260a8-115">Записывается только цветовой буфер, налевыйся спереди.</span><span class="sxs-lookup"><span data-stu-id="260a8-115">Only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <span data-ttu-id="260a8-116"><dt>**в ГК \_ спереди \_ справа**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-116"><dt>**GL\_FRONT\_RIGHT**</dt></span></span> </dl>           | <span data-ttu-id="260a8-117">Записывается только цветовой буфер, находящегося спереди справа.</span><span class="sxs-lookup"><span data-stu-id="260a8-117">Only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <span data-ttu-id="260a8-118"><dt>**Фин. \_ левый задний план \_**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-118"><dt>**GL\_BACK\_LEFT**</dt></span></span> </dl>                 | <span data-ttu-id="260a8-119">Записывается только цветовой буфер, расположенный в обратном левом углу.</span><span class="sxs-lookup"><span data-stu-id="260a8-119">Only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <span data-ttu-id="260a8-120"><dt>**в ГК \_ задний \_ правый**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-120"><dt>**GL\_BACK\_RIGHT**</dt></span></span> </dl>              | <span data-ttu-id="260a8-121">Записывается только цветовой буфер, подходящий для фона.</span><span class="sxs-lookup"><span data-stu-id="260a8-121">Only the back-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <span data-ttu-id="260a8-122"><dt>**GL \_ спереди**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-122"><dt>**GL\_FRONT**</dt></span></span> </dl>                              | <span data-ttu-id="260a8-123">Записываются только буферы цвета переднего левого края и переднего плана.</span><span class="sxs-lookup"><span data-stu-id="260a8-123">Only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="260a8-124">Если цветовой буфер отсутствует, то записывается только передний левый цвет буфера.</span><span class="sxs-lookup"><span data-stu-id="260a8-124">If there is no front-right color buffer, only the front left-color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <span data-ttu-id="260a8-125"><dt>**на \_ задний план**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-125"><dt>**GL\_BACK**</dt></span></span> </dl>                                 | <span data-ttu-id="260a8-126">Записываются только буферы цветового левого и заднего прав.</span><span class="sxs-lookup"><span data-stu-id="260a8-126">Only the back-left and back-right color buffers are written.</span></span> <span data-ttu-id="260a8-127">Если цветовой буфер не существует, то записывается только цветовой буфер, расположенный в обратном левом углу.</span><span class="sxs-lookup"><span data-stu-id="260a8-127">If there is no back-right color buffer, only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <span data-ttu-id="260a8-128"><dt>**по \_ левому краю**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-128"><dt>**GL\_LEFT**</dt></span></span> </dl>                                 | <span data-ttu-id="260a8-129">Записываются только буферы цвета переднего плана и заднего левого края.</span><span class="sxs-lookup"><span data-stu-id="260a8-129">Only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="260a8-130">Если цветовой буфер отсутствует, то записывается только передний левый цветовой буфер.</span><span class="sxs-lookup"><span data-stu-id="260a8-130">If there is no back-left color buffer, only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <span data-ttu-id="260a8-131"><dt>**по \_ правому краю**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-131"><dt>**GL\_RIGHT**</dt></span></span> </dl>                              | <span data-ttu-id="260a8-132">Записываются только фоновые буферы переднего плана и заднего правого цвета.</span><span class="sxs-lookup"><span data-stu-id="260a8-132">Only the front-right and back-right color buffers are written.</span></span> <span data-ttu-id="260a8-133">Если цветовой буфер отсутствует, то записывается только цветовой буфер, находящегося спереди справа.</span><span class="sxs-lookup"><span data-stu-id="260a8-133">If there is no back-right color buffer, only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <span data-ttu-id="260a8-134"><dt>**\_Передняя \_ и \_ задняя части GL**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-134"><dt>**GL\_FRONT\_AND\_BACK**</dt></span></span> </dl> | <span data-ttu-id="260a8-135">Все буферы переднего и фонового цветов (передний левый, передний правый, задний левый, задний правый) записываются.</span><span class="sxs-lookup"><span data-stu-id="260a8-135">All the front and back color buffers (front-left, front-right, back-left, back-right) are written.</span></span> <span data-ttu-id="260a8-136">Если буферы фона отсутствуют, записываются только фоновые буферы, расположенные спереди слева и спереди.</span><span class="sxs-lookup"><span data-stu-id="260a8-136">If there are no back color buffers, only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="260a8-137">Если буферы цвета отсутствуют, то записываются только буферы, расположенные спереди слева и в обратном цвете.</span><span class="sxs-lookup"><span data-stu-id="260a8-137">If there are no right color buffers, only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="260a8-138">Если буферы не имеют прав или обратного цвета, записывается только цветовой буфер, расположенный спереди.</span><span class="sxs-lookup"><span data-stu-id="260a8-138">If there are no right or back color buffers, only the front-left color buffer is written.</span></span><br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <span data-ttu-id="260a8-139"><dt>**\_АУКСИ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-139"><dt>**GL\_AUXi**</dt></span></span> </dl>       | <span data-ttu-id="260a8-140">Написан только вспомогательный цветовой буфер, который *я* написал.  в диапазоне от 0 до GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="260a8-140">Only the auxiliary color buffer *i* is written; *i* is between 0 and GL\_AUX\_BUFFERS - 1.</span></span> <span data-ttu-id="260a8-141">(GL \_ \_Дополнительные буферы не являются верхним пределами. Используйте [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) для запроса количества доступных вспомогательных буферов.)</span><span class="sxs-lookup"><span data-stu-id="260a8-141">(GL\_AUX\_BUFFERS is not the upper limit; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to query the number of available auxiliary buffers.)</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="260a8-142">Значение по умолчанию — GL \_ для однобуферных контекстов, а GL — \_ для контекстов с двойной буферизацией.</span><span class="sxs-lookup"><span data-stu-id="260a8-142">The default value is GL\_FRONT for single-buffered contexts, and GL\_BACK for double-buffered contexts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="260a8-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="260a8-143">Return value</span></span>

<span data-ttu-id="260a8-144">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="260a8-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="260a8-145">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="260a8-145">Error codes</span></span>

<span data-ttu-id="260a8-146">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="260a8-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="260a8-147">Имя</span><span class="sxs-lookup"><span data-stu-id="260a8-147">Name</span></span>                                                                                                  | <span data-ttu-id="260a8-148">Значение</span><span class="sxs-lookup"><span data-stu-id="260a8-148">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="260a8-149"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-149"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="260a8-150">*режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="260a8-150">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="260a8-151"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="260a8-152">Ни один из буферов, указанных в *режиме* , не существовал.</span><span class="sxs-lookup"><span data-stu-id="260a8-152">None of the buffers indicated by *mode* existed.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="260a8-153"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="260a8-154">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="260a8-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |


## <a name="remarks"></a><span data-ttu-id="260a8-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="260a8-155">Remarks</span></span>

<span data-ttu-id="260a8-156">Когда цвета записываются в буфера кадров, они записываются в буферы цветов, заданные параметром **глдравбуффер**.</span><span class="sxs-lookup"><span data-stu-id="260a8-156">When colors are written to the framebuffer, they are written into the color buffers specified by **glDrawBuffer**.</span></span>

<span data-ttu-id="260a8-157">Если для рисования выбрано более одного цветового буфера, то операции смешения или логических операций вычисляются и применяются независимо для каждого цветового буфера и могут формировать разные результаты в каждом буфере.</span><span class="sxs-lookup"><span data-stu-id="260a8-157">If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.</span></span>

<span data-ttu-id="260a8-158">Однообластные контексты включают только левые буферы, а стереоскопик контексты включают как левые, так и правый буферы.</span><span class="sxs-lookup"><span data-stu-id="260a8-158">Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers.</span></span> <span data-ttu-id="260a8-159">Аналогичным образом, однобуферные контексты включают только интерфейсы переднего плана, а контексты с двойной буферизацией включают в себя как передний, так и задний буфер.</span><span class="sxs-lookup"><span data-stu-id="260a8-159">Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers.</span></span> <span data-ttu-id="260a8-160">Контекст выбирается при инициализации OpenGL.</span><span class="sxs-lookup"><span data-stu-id="260a8-160">The context is selected at OpenGL initialization.</span></span>

<span data-ttu-id="260a8-161">Это всегда так, что GL \_ AUX *i* = GL \_ AUX0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="260a8-161">It is always the case that GL\_AUX *i* = GL\_AUX0 + *i*.</span></span>

<span data-ttu-id="260a8-162">Следующие функции извлекают сведения, относящиеся к функции **глдравбуффер** :</span><span class="sxs-lookup"><span data-stu-id="260a8-162">The following functions retrieve information related to the **glDrawBuffer** function:</span></span>

<span data-ttu-id="260a8-163">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ буфера рисования GL \_</span><span class="sxs-lookup"><span data-stu-id="260a8-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DRAW\_BUFFER</span></span>

<span data-ttu-id="260a8-164">**глжет** с аргументом "дополнительные \_ \_ буферы GL"</span><span class="sxs-lookup"><span data-stu-id="260a8-164">**glGet** with argument GL\_AUX\_BUFFERS</span></span>

## <a name="requirements"></a><span data-ttu-id="260a8-165">Требования</span><span class="sxs-lookup"><span data-stu-id="260a8-165">Requirements</span></span>



| <span data-ttu-id="260a8-166">Требование</span><span class="sxs-lookup"><span data-stu-id="260a8-166">Requirement</span></span> | <span data-ttu-id="260a8-167">Значение</span><span class="sxs-lookup"><span data-stu-id="260a8-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="260a8-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="260a8-168">Minimum supported client</span></span><br/> | <span data-ttu-id="260a8-169">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="260a8-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="260a8-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="260a8-170">Minimum supported server</span></span><br/> | <span data-ttu-id="260a8-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="260a8-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="260a8-172">Заголовок</span><span class="sxs-lookup"><span data-stu-id="260a8-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="260a8-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="260a8-174">Библиотека</span><span class="sxs-lookup"><span data-stu-id="260a8-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="260a8-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="260a8-176">DLL</span><span class="sxs-lookup"><span data-stu-id="260a8-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="260a8-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="260a8-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="260a8-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="260a8-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260a8-179">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="260a8-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="260a8-180">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="260a8-180">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="260a8-181">**глколормаск**</span><span class="sxs-lookup"><span data-stu-id="260a8-181">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="260a8-182">**гленд**</span><span class="sxs-lookup"><span data-stu-id="260a8-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="260a8-183">**глжет**</span><span class="sxs-lookup"><span data-stu-id="260a8-183">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="260a8-184">**глиндексмаск**</span><span class="sxs-lookup"><span data-stu-id="260a8-184">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="260a8-185">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="260a8-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="260a8-186">**глреадбуффер**</span><span class="sxs-lookup"><span data-stu-id="260a8-186">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





