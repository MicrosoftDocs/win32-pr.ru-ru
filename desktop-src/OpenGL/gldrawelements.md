---
title: Функция Глдравелементс (GL. h)
description: Функция Глдравелементс отображает примитивы из данных массива.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- Функция Глдравелементс OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534487"
---
# <a name="gldrawelements-function"></a><span data-ttu-id="a743f-104">Функция Глдравелементс</span><span class="sxs-lookup"><span data-stu-id="a743f-104">glDrawElements function</span></span>

<span data-ttu-id="a743f-105">Функция **глдравелементс** отображает примитивы из данных массива.</span><span class="sxs-lookup"><span data-stu-id="a743f-105">The **glDrawElements** function renders primitives from array data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a743f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a743f-106">Syntax</span></span>


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a><span data-ttu-id="a743f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a743f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a743f-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="a743f-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="a743f-109">Тип отображаемых примитивов.</span><span class="sxs-lookup"><span data-stu-id="a743f-109">The kind of primitives to render.</span></span> <span data-ttu-id="a743f-110">Это может быть одно из следующих символьных значений: \_ «Points», « \_ линейка строк GL \_ », « \_ линейный \_ цикл ГК», «строки GL», «вершина треугольника GL», « \_ \_ \_ радиальный \_ \_ Вентилятор», \_ \_ \_ \_ \_ «кривые», «четыре» и «многоугольник».</span><span class="sxs-lookup"><span data-stu-id="a743f-110">It can assume one of the following symbolic values: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="a743f-111">*count*</span><span class="sxs-lookup"><span data-stu-id="a743f-111">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="a743f-112">Число отображаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="a743f-112">The number of elements to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a743f-113">*type*</span><span class="sxs-lookup"><span data-stu-id="a743f-113">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="a743f-114">Тип значений в индексах.</span><span class="sxs-lookup"><span data-stu-id="a743f-114">The type of the values in indices.</span></span> <span data-ttu-id="a743f-115">Должен быть одним из \_ НЕподписанного \_ байта, неподписанного \_ \_ короткого или неподписанного \_ \_ целого числа в формате GL.</span><span class="sxs-lookup"><span data-stu-id="a743f-115">Must be one of GL\_UNSIGNED\_BYTE, GL\_UNSIGNED\_SHORT, or GL\_UNSIGNED\_INT.</span></span>

</dd> <dt>

<span data-ttu-id="a743f-116">*увеличивают*</span><span class="sxs-lookup"><span data-stu-id="a743f-116">*indices*</span></span> 
</dt> <dd>

<span data-ttu-id="a743f-117">Указатель на расположение, в котором хранятся индексы.</span><span class="sxs-lookup"><span data-stu-id="a743f-117">A pointer to the location where the indices are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a743f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a743f-118">Return value</span></span>

<span data-ttu-id="a743f-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a743f-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a743f-120">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a743f-120">Error codes</span></span>

<span data-ttu-id="a743f-121">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="a743f-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a743f-122">Имя</span><span class="sxs-lookup"><span data-stu-id="a743f-122">Name</span></span>                                                                                                  | <span data-ttu-id="a743f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a743f-123">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a743f-124"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a743f-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a743f-125">*режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="a743f-125">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="a743f-126"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a743f-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a743f-127">*Count* было отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="a743f-127">*count* was a negative value.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="a743f-128"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a743f-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a743f-129">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a743f-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a743f-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a743f-130">Remarks</span></span>

<span data-ttu-id="a743f-131">Функция **глдравелементс** позволяет указать несколько геометрических примитивов с небольшими вызовами функций.</span><span class="sxs-lookup"><span data-stu-id="a743f-131">The **glDrawElements** function enables you to specify multiple geometric primitives with very few function calls.</span></span> <span data-ttu-id="a743f-132">Вместо вызова функции OpenGL для передачи каждой отдельной вершины, нормали или цвета можно заранее указать отдельные массивы вершин, нормали и цвета и использовать их для определения последовательности примитивов (всех тех же типов) с одним вызовом **глдравелементс**.</span><span class="sxs-lookup"><span data-stu-id="a743f-132">Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to **glDrawElements**.</span></span>

<span data-ttu-id="a743f-133">При вызове функции **глдравелементс** используется *подсчет* последовательных элементов из *индексов* для создания последовательности геометрических примитивов.</span><span class="sxs-lookup"><span data-stu-id="a743f-133">When you call the **glDrawElements** function, it uses *count* sequential elements from *indices* to construct a sequence of geometric primitives.</span></span> <span data-ttu-id="a743f-134">Параметр *mode* определяет тип создаваемых примитивов и то, как элементы массива используются для создания этих примитивов.</span><span class="sxs-lookup"><span data-stu-id="a743f-134">The *mode* parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives.</span></span> <span data-ttu-id="a743f-135">Если \_ массив ВЕРШИН GL \_ не включен, геометрические примитивы не создаются.</span><span class="sxs-lookup"><span data-stu-id="a743f-135">If GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated.</span></span>

<span data-ttu-id="a743f-136">Атрибуты вершин, измененные **глдравелементс** , имеют неопределенное значение после возврата **глдравелементс** .</span><span class="sxs-lookup"><span data-stu-id="a743f-136">Vertex attributes that are modified by **glDrawElements** have an unspecified value after **glDrawElements** returns.</span></span> <span data-ttu-id="a743f-137">Например, если \_ \_ включен массив цветов GL, значение текущего цвета не определено после выполнения **глдравелементс** .</span><span class="sxs-lookup"><span data-stu-id="a743f-137">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawElements** executes.</span></span> <span data-ttu-id="a743f-138">Атрибуты, которые не изменяются, остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="a743f-138">Attributes that aren't modified remain unchanged.</span></span>

<span data-ttu-id="a743f-139">Функцию **глдравелементс** можно включить в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="a743f-139">You can include the **glDrawElements** function in display lists.</span></span> <span data-ttu-id="a743f-140">Если **глдравелементс** включен в список вывода, необходимые данные массива (определяемые указателями на массивы и включенные) также помещаются в список отображаемых данных.</span><span class="sxs-lookup"><span data-stu-id="a743f-140">When **glDrawElements** is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list.</span></span> <span data-ttu-id="a743f-141">Поскольку указатели на массивы и включают переменные состояния на стороне клиента, их значения влияют на списки отображения при создании списков, а не при выполнении списков.</span><span class="sxs-lookup"><span data-stu-id="a743f-141">Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.</span></span>

> [!Note]  
> <span data-ttu-id="a743f-142">Функция **глдравелементс** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="a743f-142">The **glDrawElements** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a743f-143">Требования</span><span class="sxs-lookup"><span data-stu-id="a743f-143">Requirements</span></span>



| <span data-ttu-id="a743f-144">Требование</span><span class="sxs-lookup"><span data-stu-id="a743f-144">Requirement</span></span> | <span data-ttu-id="a743f-145">Значение</span><span class="sxs-lookup"><span data-stu-id="a743f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a743f-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a743f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a743f-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a743f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a743f-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a743f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a743f-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a743f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a743f-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a743f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="a743f-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a743f-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a743f-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a743f-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="a743f-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a743f-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a743f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="a743f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a743f-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a743f-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a743f-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a743f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a743f-157">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="a743f-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="a743f-158">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="a743f-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a743f-159">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="a743f-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="a743f-160">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="a743f-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="a743f-161">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="a743f-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="a743f-162">**гленд**</span><span class="sxs-lookup"><span data-stu-id="a743f-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a743f-163">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="a743f-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="a743f-164">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="a743f-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="a743f-165">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="a743f-165">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="a743f-166">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="a743f-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="a743f-167">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="a743f-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





