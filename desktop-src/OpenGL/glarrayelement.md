---
title: Функция Гларрайелемент (GL. h)
description: Функция Гларрайелемент указывает элементы массива, используемые для отрисовки вершины.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- Функция Гларрайелемент OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681914"
---
# <a name="glarrayelement-function"></a><span data-ttu-id="36a0a-104">Функция Гларрайелемент</span><span class="sxs-lookup"><span data-stu-id="36a0a-104">glArrayElement function</span></span>

<span data-ttu-id="36a0a-105">Функция **гларрайелемент** указывает элементы массива, используемые для отрисовки вершины.</span><span class="sxs-lookup"><span data-stu-id="36a0a-105">The **glArrayElement** function specifies the array elements used to render a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a0a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36a0a-106">Syntax</span></span>


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a><span data-ttu-id="36a0a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="36a0a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a0a-108">*index*</span><span class="sxs-lookup"><span data-stu-id="36a0a-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="36a0a-109">Индекс в включенных массивах.</span><span class="sxs-lookup"><span data-stu-id="36a0a-109">An index in the enabled arrays.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36a0a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36a0a-110">Return value</span></span>

<span data-ttu-id="36a0a-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="36a0a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36a0a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36a0a-112">Remarks</span></span>

<span data-ttu-id="36a0a-113">Используйте функцию **гларрайелемент** в парах [**глбегин**](glbegin.md) и [**гленд**](glend.md) , чтобы указать данные вершин и атрибутов для примитивов, линий и многоугольников.</span><span class="sxs-lookup"><span data-stu-id="36a0a-113">Use the **glArrayElement** function within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs to specify vertex and attribute data for point, line, and polygon primitives.</span></span> <span data-ttu-id="36a0a-114">Функция **гларрайелемент** указывает данные для отдельной вершины, используя данные вершин и атрибутов, расположенные по *индексу* включенных массивов вершин.</span><span class="sxs-lookup"><span data-stu-id="36a0a-114">The **glArrayElement** function specifies the data for a single vertex using vertex and attribute data located at the *index* of the enabled vertex arrays.</span></span>

<span data-ttu-id="36a0a-115">**Гларрайелемент** можно использовать для создания примитивов путем индексирования данных вершин, а не потоковой передачи через массивы данных в порядке «первый к последнему».</span><span class="sxs-lookup"><span data-stu-id="36a0a-115">You can use **glArrayElement** to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order.</span></span> <span data-ttu-id="36a0a-116">Поскольку **гларрайелемент** указывает только одну вершину, можно явно указать атрибуты для отдельных примитивов.</span><span class="sxs-lookup"><span data-stu-id="36a0a-116">Because **glArrayElement** specifies a single vertex only, you can explicitly specify attributes for individual primitives.</span></span> <span data-ttu-id="36a0a-117">Например, для каждого отдельного треугольника можно задать одну нормальную обычную.</span><span class="sxs-lookup"><span data-stu-id="36a0a-117">For example, you can set a single normal for each individual triangle.</span></span>

<span data-ttu-id="36a0a-118">При включении вызовов **гларрайелемент** в списках вывода необходимые данные массива, определяемые указателями на массивы и включающие значения, также добавляются в список просмотра.</span><span class="sxs-lookup"><span data-stu-id="36a0a-118">When you include calls to **glArrayElement** in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also.</span></span> <span data-ttu-id="36a0a-119">Указатели на массив и включение значений определяются при создании списков вывода, а не при выполнении списков вывода.</span><span class="sxs-lookup"><span data-stu-id="36a0a-119">Array pointer and enable values are determined when display lists are created, not when display lists are executed.</span></span>

<span data-ttu-id="36a0a-120">Данные статического массива можно считывать и кэшировать в любое время с помощью **гларрайелемент**.</span><span class="sxs-lookup"><span data-stu-id="36a0a-120">You can read and cache static array data at any time with **glArrayElement**.</span></span> <span data-ttu-id="36a0a-121">При изменении элементов статического массива без повторного указания массива результаты всех последующих вызовов **гларрайелемент** не определены.</span><span class="sxs-lookup"><span data-stu-id="36a0a-121">When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to **glArrayElement** are undefined.</span></span>

<span data-ttu-id="36a0a-122">При вызове **гларрайелемент** без предварительного вызова **гленаблеклиентстате**( \_ массив вершин \_ в GL) не происходит прорисовка, но атрибуты, соответствующие включенным массивам, изменяются.</span><span class="sxs-lookup"><span data-stu-id="36a0a-122">When you call **glArrayElement** without first calling **glEnableClientState**(GL\_VERTEX\_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified.</span></span> <span data-ttu-id="36a0a-123">Хотя при указании массива в парах **глбегин** и **гленд** не возникает ошибок, результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="36a0a-123">Although no error is generated when you specify an array within **glBegin** and **glEnd** pairs, the results are undefined.</span></span>

> [!Note]  
> <span data-ttu-id="36a0a-124">Функция **гларрайелемент** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="36a0a-124">The **glArrayElement** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="36a0a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="36a0a-125">Requirements</span></span>



| <span data-ttu-id="36a0a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="36a0a-126">Requirement</span></span> | <span data-ttu-id="36a0a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="36a0a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36a0a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36a0a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="36a0a-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36a0a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="36a0a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36a0a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="36a0a-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36a0a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36a0a-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36a0a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="36a0a-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="36a0a-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="36a0a-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36a0a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="36a0a-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36a0a-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="36a0a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="36a0a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36a0a-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36a0a-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a0a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36a0a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a0a-139">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="36a0a-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="36a0a-140">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="36a0a-140">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="36a0a-141">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="36a0a-141">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="36a0a-142">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="36a0a-142">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="36a0a-143">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="36a0a-143">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="36a0a-144">**гленд**</span><span class="sxs-lookup"><span data-stu-id="36a0a-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="36a0a-145">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="36a0a-145">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="36a0a-146">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="36a0a-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="36a0a-147">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="36a0a-147">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="36a0a-148">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="36a0a-148">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="36a0a-149">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="36a0a-149">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="36a0a-150">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="36a0a-150">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





