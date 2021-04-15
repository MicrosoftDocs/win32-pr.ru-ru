---
title: Функция Глпопаттриб (GL. h)
description: Извлекает стек атрибутов.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- Функция Глпопаттриб OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661929"
---
# <a name="glpopattrib-function"></a><span data-ttu-id="16590-104">Функция Глпопаттриб</span><span class="sxs-lookup"><span data-stu-id="16590-104">glPopAttrib function</span></span>

<span data-ttu-id="16590-105">Извлекает стек атрибутов.</span><span class="sxs-lookup"><span data-stu-id="16590-105">Pops the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="16590-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16590-106">Syntax</span></span>


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="16590-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="16590-107">Parameters</span></span>

<span data-ttu-id="16590-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="16590-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16590-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16590-109">Return value</span></span>

<span data-ttu-id="16590-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="16590-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="16590-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="16590-111">Error codes</span></span>

<span data-ttu-id="16590-112">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="16590-112">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="16590-113">Имя</span><span class="sxs-lookup"><span data-stu-id="16590-113">Name</span></span>                                                                                                  | <span data-ttu-id="16590-114">Значение</span><span class="sxs-lookup"><span data-stu-id="16590-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16590-115"><dt>**\_ \_ потеря значимости СТЕКа GL**</dt></span><span class="sxs-lookup"><span data-stu-id="16590-115"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="16590-116">Функция была вызвана, пока стек атрибутов не был пустым.</span><span class="sxs-lookup"><span data-stu-id="16590-116">The function was called while the attribute stack was empty.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="16590-117"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="16590-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="16590-118">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="16590-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="16590-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16590-119">Remarks</span></span>

<span data-ttu-id="16590-120">Функция [**глпушаттриб**](glpushattrib.md) принимает один аргумент — маску, указывающую, какие группы переменных состояния следует сохранять в стеке атрибутов.</span><span class="sxs-lookup"><span data-stu-id="16590-120">The [**glPushAttrib**](glpushattrib.md) function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="16590-121">Символьные константы используются для установки битов в маске.</span><span class="sxs-lookup"><span data-stu-id="16590-121">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="16590-122">Параметр маски обычно создается **или** объединяет несколько этих констант.</span><span class="sxs-lookup"><span data-stu-id="16590-122">The mask parameter is typically constructed by **OR** ing several of these constants together.</span></span> <span data-ttu-id="16590-123">\_ \_ \_ Для сохранения всех состояний с накоплением можно использовать специальную маску GL для всех attrib.</span><span class="sxs-lookup"><span data-stu-id="16590-123">The special mask GL\_ALL\_ATTRIB\_BITS can be used to save all stackable states.</span></span>

<span data-ttu-id="16590-124">Функция **глпопаттриб** восстанавливает значения переменных состояния, сохраненные с помощью последней команды [**глпушаттриб**](glpushattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="16590-124">The **glPopAttrib** function restores the values of the state variables saved with the last [**glPushAttrib**](glpushattrib.md) command.</span></span> <span data-ttu-id="16590-125">Несохраненные данные остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="16590-125">Those not saved are left unchanged.</span></span>

<span data-ttu-id="16590-126">При принудительной отправке атрибутов в полный стек или при отключении атрибутов к пустому стеку возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="16590-126">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="16590-127">В любом случае устанавливается флаг ошибки, а в состояние OpenGL другие изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="16590-127">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="16590-128">Изначально стек атрибутов пуст.</span><span class="sxs-lookup"><span data-stu-id="16590-128">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="16590-129">Не все значения для состояния OpenGL можно сохранить в стеке атрибутов.</span><span class="sxs-lookup"><span data-stu-id="16590-129">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="16590-130">Например, невозможно сохранить пакет пикселей и состояние распаковки, состояние режима рендеринга, а затем выбрать и состояние обратной связи.</span><span class="sxs-lookup"><span data-stu-id="16590-130">For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.</span></span>

<span data-ttu-id="16590-131">Глубина стека атрибутов зависит от реализации, но должна быть не меньше 16.</span><span class="sxs-lookup"><span data-stu-id="16590-131">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="16590-132">Следующие функции извлекают сведения, относящиеся к [**глпушаттриб**](glpushattrib.md) и **глпопаттриб**:</span><span class="sxs-lookup"><span data-stu-id="16590-132">The following functions retrieve information related to [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**:</span></span>

<span data-ttu-id="16590-133">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ attrib, \_ глубина стека \_</span><span class="sxs-lookup"><span data-stu-id="16590-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="16590-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ Максимальная \_ глубина стека \_ "</span><span class="sxs-lookup"><span data-stu-id="16590-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="16590-135">Требования</span><span class="sxs-lookup"><span data-stu-id="16590-135">Requirements</span></span>



| <span data-ttu-id="16590-136">Требование</span><span class="sxs-lookup"><span data-stu-id="16590-136">Requirement</span></span> | <span data-ttu-id="16590-137">Значение</span><span class="sxs-lookup"><span data-stu-id="16590-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16590-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16590-138">Minimum supported client</span></span><br/> | <span data-ttu-id="16590-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16590-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="16590-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16590-140">Minimum supported server</span></span><br/> | <span data-ttu-id="16590-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16590-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16590-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="16590-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="16590-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="16590-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="16590-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16590-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="16590-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16590-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="16590-146">DLL</span><span class="sxs-lookup"><span data-stu-id="16590-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16590-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16590-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16590-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16590-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16590-149">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="16590-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="16590-150">**гленд**</span><span class="sxs-lookup"><span data-stu-id="16590-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="16590-151">**глжет**</span><span class="sxs-lookup"><span data-stu-id="16590-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="16590-152">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="16590-152">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="16590-153">**глжетеррор**</span><span class="sxs-lookup"><span data-stu-id="16590-153">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="16590-154">**глжетлигхт**</span><span class="sxs-lookup"><span data-stu-id="16590-154">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="16590-155">**глжетмап**</span><span class="sxs-lookup"><span data-stu-id="16590-155">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="16590-156">**глжетматериал**</span><span class="sxs-lookup"><span data-stu-id="16590-156">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="16590-157">**глжетпикселмап**</span><span class="sxs-lookup"><span data-stu-id="16590-157">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="16590-158">**глжетполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="16590-158">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="16590-159">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="16590-159">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="16590-160">**глжеттексенв**</span><span class="sxs-lookup"><span data-stu-id="16590-160">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="16590-161">**глжеттексжен**</span><span class="sxs-lookup"><span data-stu-id="16590-161">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="16590-162">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="16590-162">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="16590-163">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="16590-163">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="16590-164">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="16590-164">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="16590-165">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="16590-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





