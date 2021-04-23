---
title: Функция Гледжефлагпоинтер (GL. h)
description: Функция Гледжефлагпоинтер определяет массив пограничных флагов.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- Функция Гледжефлагпоинтер OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802806"
---
# <a name="gledgeflagpointer-function"></a><span data-ttu-id="3bc24-104">Функция Гледжефлагпоинтер</span><span class="sxs-lookup"><span data-stu-id="3bc24-104">glEdgeFlagPointer function</span></span>

<span data-ttu-id="3bc24-105">Функция **гледжефлагпоинтер** определяет массив пограничных флагов.</span><span class="sxs-lookup"><span data-stu-id="3bc24-105">The **glEdgeFlagPointer** function defines an array of edge flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc24-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bc24-106">Syntax</span></span>


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="3bc24-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bc24-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc24-108">*шага*</span><span class="sxs-lookup"><span data-stu-id="3bc24-108">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc24-109">Смещение в байтах между последовательными флагами ребра.</span><span class="sxs-lookup"><span data-stu-id="3bc24-109">The byte offset between consecutive edge flags.</span></span> <span data-ttu-id="3bc24-110">Если *шаг* равен нулю, пограничные флаги жестко упакованы в массив.</span><span class="sxs-lookup"><span data-stu-id="3bc24-110">When *stride* is zero, the edge flags are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="3bc24-111">*указатель*</span><span class="sxs-lookup"><span data-stu-id="3bc24-111">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc24-112">Указатель на первый флаг границы в массиве.</span><span class="sxs-lookup"><span data-stu-id="3bc24-112">A pointer to the first edge flag in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bc24-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bc24-113">Return value</span></span>

<span data-ttu-id="3bc24-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3bc24-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3bc24-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3bc24-115">Error codes</span></span>

<span data-ttu-id="3bc24-116">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3bc24-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3bc24-117">Имя</span><span class="sxs-lookup"><span data-stu-id="3bc24-117">Name</span></span>                                                                                             | <span data-ttu-id="3bc24-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3bc24-118">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3bc24-119"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3bc24-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="3bc24-120">*шаг* или *число* были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="3bc24-120">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3bc24-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3bc24-121">Remarks</span></span>

<span data-ttu-id="3bc24-122">Функция **гледжефлагпоинтер** задает расположение и данные массива логических пограничных флагов, которые используются при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="3bc24-122">The **glEdgeFlagPointer** function specifies the location and data of an array of Boolean edge flags to use when rendering.</span></span> <span data-ttu-id="3bc24-123">Параметр *stride* определяет смещение в байтах от одного флага ребра к следующему, что позволяет упаковать вершины и атрибуты в одном массиве или хранилище в отдельные массивы.</span><span class="sxs-lookup"><span data-stu-id="3bc24-123">The *stride* parameter determines the byte offset from one edge flag to the next, which enables the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="3bc24-124">В некоторых реализациях хранение вершин и атрибутов в одном массиве может быть более эффективным, чем использование отдельных массивов.</span><span class="sxs-lookup"><span data-stu-id="3bc24-124">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span>

<span data-ttu-id="3bc24-125">Массив флагов ребра включается при указании \_ \_ константы массива флагов GL в ГК \_ с [**гленаблеклиентстате**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="3bc24-125">An edge-flag array is enabled when you specify the GL\_EDGE\_FLAG\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="3bc24-126">Если параметр включен, [**глдраваррайс**](gldrawarrays.md) или [**гларрайелемент**](glarrayelement.md) использует массив флагов ребра.</span><span class="sxs-lookup"><span data-stu-id="3bc24-126">When enabled, [**glDrawArrays**](gldrawarrays.md) or [**glArrayElement**](glarrayelement.md) uses the edge-flag array.</span></span> <span data-ttu-id="3bc24-127">По умолчанию массив флагов ребра отключен.</span><span class="sxs-lookup"><span data-stu-id="3bc24-127">By default the edge-flag array is disabled.</span></span>

<span data-ttu-id="3bc24-128">Используйте **глдраваррайс** для создания последовательности примитивов (всех тех же типов) из предопределенных массивов атрибутов вершин и вершин.</span><span class="sxs-lookup"><span data-stu-id="3bc24-128">Use **glDrawArrays** to construct a sequence of primitives (all of the same type) from prespecified vertex and vertex attribute arrays.</span></span> <span data-ttu-id="3bc24-129">Используйте **гларрайелемент** для указания примитивов путем индексирования вершин и атрибутов вершин, а [**глдравелементс**](gldrawelements.md) для создания последовательности примитивов путем индексирования вершин и атрибутов вершин.</span><span class="sxs-lookup"><span data-stu-id="3bc24-129">Use **glArrayElement** to specify primitives by indexing vertices and vertex attributes, and [**glDrawElements**](gldrawelements.md) to construct a sequence of primitives by indexing vertices and vertex attributes.</span></span>

<span data-ttu-id="3bc24-130">Невозможно включить **гледжефлагпоинтер** в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="3bc24-130">You cannot include **glEdgeFlagPointer** in display lists.</span></span>

<span data-ttu-id="3bc24-131">При указании массива флагов ребра с помощью **гледжефлагпоинтер** значения всех параметров массива флагов границ функции сохраняются в состоянии на стороне клиента, а статические элементы массива могут быть кэшированы.</span><span class="sxs-lookup"><span data-stu-id="3bc24-131">When you specify an edge-flag array using **glEdgeFlagPointer**, the values of all the function's edge-flag array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="3bc24-132">Так как параметры массива пограничных флагов находятся в состоянии на стороне клиента, [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md) не сохраняют и не восстанавливают их значения.</span><span class="sxs-lookup"><span data-stu-id="3bc24-132">Because the edge-flag array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore their values.</span></span>

<span data-ttu-id="3bc24-133">Хотя вызов **гледжефлагпоинтер** в паре [**глбегин**](glbegin.md) / [**гленд**](glend.md) не создает ошибку, результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="3bc24-133">Although calling **glEdgeFlagPointer** within a [**glBegin**](glbegin.md)/[**glend**](glend.md) pair does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="3bc24-134">Следующие функции извлекают сведения, относящиеся к функции **гледжефлагпоинтер** :</span><span class="sxs-lookup"><span data-stu-id="3bc24-134">The following functions retrieve information related to the **glEdgeFlagPointer** function:</span></span>

<span data-ttu-id="3bc24-135">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом "шаг" для \_ \_ массива флагов ребра \_ \_</span><span class="sxs-lookup"><span data-stu-id="3bc24-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="3bc24-136">**глжет** с аргументом \_ \_ \_ число МАССИВов флагов ребра GL \_</span><span class="sxs-lookup"><span data-stu-id="3bc24-136">**glGet** with argument GL\_EDGE\_FLAG\_ARRAY\_COUNT</span></span>

<span data-ttu-id="3bc24-137">[**глжетпоинтерв**](glgetpointerv.md) с аргументом \_ , \_ \_ указатель массива флага ребра GL \_</span><span class="sxs-lookup"><span data-stu-id="3bc24-137">[**glGetPointerv**](glgetpointerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_POINTER</span></span>

<span data-ttu-id="3bc24-138">[**глисенаблед**](glisenabled.md) с аргументом \_ \_ массива флагов ребра GL \_</span><span class="sxs-lookup"><span data-stu-id="3bc24-138">[**glIsEnabled**](glisenabled.md) with argument GL\_EDGE\_FLAG\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc24-139">Требования</span><span class="sxs-lookup"><span data-stu-id="3bc24-139">Requirements</span></span>



| <span data-ttu-id="3bc24-140">Требование</span><span class="sxs-lookup"><span data-stu-id="3bc24-140">Requirement</span></span> | <span data-ttu-id="3bc24-141">Значение</span><span class="sxs-lookup"><span data-stu-id="3bc24-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc24-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3bc24-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc24-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3bc24-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3bc24-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3bc24-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc24-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3bc24-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3bc24-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3bc24-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bc24-147"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bc24-147"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3bc24-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3bc24-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="3bc24-149"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bc24-149"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3bc24-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3bc24-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bc24-151"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bc24-151"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc24-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bc24-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc24-153">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="3bc24-153">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="3bc24-154">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="3bc24-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3bc24-155">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3bc24-155">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="3bc24-156">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="3bc24-156">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="3bc24-157">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="3bc24-157">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="3bc24-158">**гленд**</span><span class="sxs-lookup"><span data-stu-id="3bc24-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3bc24-159">**глжет**</span><span class="sxs-lookup"><span data-stu-id="3bc24-159">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3bc24-160">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="3bc24-160">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="3bc24-161">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="3bc24-161">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="3bc24-162">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="3bc24-162">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="3bc24-163">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="3bc24-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="3bc24-164">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3bc24-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="3bc24-165">**глпопаттриб**</span><span class="sxs-lookup"><span data-stu-id="3bc24-165">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="3bc24-166">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="3bc24-166">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="3bc24-167">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3bc24-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="3bc24-168">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="3bc24-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





