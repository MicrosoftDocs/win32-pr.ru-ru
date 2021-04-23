---
title: Функция Гленд (GL. h)
description: Функции Глбегин и гленд разделяют вершины примитива или группы похожих примитивов. | Функция Гленд (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- Функция Гленд OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664875"
---
# <a name="glend-function"></a><span data-ttu-id="32b5f-105">Функция Гленд</span><span class="sxs-lookup"><span data-stu-id="32b5f-105">glEnd function</span></span>

<span data-ttu-id="32b5f-106">Функции [**глбегин**](glbegin.md) и **гленд** разделяют вершины примитива или группы похожих примитивов.</span><span class="sxs-lookup"><span data-stu-id="32b5f-106">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b5f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32b5f-107">Syntax</span></span>


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a><span data-ttu-id="32b5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="32b5f-108">Parameters</span></span>

<span data-ttu-id="32b5f-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="32b5f-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32b5f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32b5f-110">Return value</span></span>

<span data-ttu-id="32b5f-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="32b5f-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="32b5f-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="32b5f-112">Error codes</span></span>

<span data-ttu-id="32b5f-113">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="32b5f-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="32b5f-114">Имя</span><span class="sxs-lookup"><span data-stu-id="32b5f-114">Name</span></span>                                                                                                  | <span data-ttu-id="32b5f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="32b5f-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32b5f-116"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="32b5f-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="32b5f-117">Функция, отличная от **глвертекс**, **глколор**, **глиндекс**, **глнормал**, **глтекскурд**, **глевалкурд**, **глевалпоинт**, **Глматериал**, **гледжефлаг**, **glCallList** или **glCallLists** , была вызвана между **glBegin** и соответствующим **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="32b5f-117">A function other than **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList**, or **glCallLists** was called between **glBegin** and the corresponding **glEnd**.</span></span> <span data-ttu-id="32b5f-118">Функция **гленд** была вызвана до вызова соответствующего **глбегин** , или **глбегин** была вызвана в последовательности **глбегин** / **гленд** .</span><span class="sxs-lookup"><span data-stu-id="32b5f-118">The function **glEnd** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glEnd** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="32b5f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32b5f-119">Remarks</span></span>

<span data-ttu-id="32b5f-120">Функции [**глбегин**](glbegin.md) и **гленд** разделяют вершины, определяющие примитив или группу похожих примитивов.</span><span class="sxs-lookup"><span data-stu-id="32b5f-120">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="32b5f-121">Функция **глбегин** принимает один аргумент, указывающий, какой из десяти примитивов будет составлять вершины.</span><span class="sxs-lookup"><span data-stu-id="32b5f-121">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="32b5f-122">При отсчете *n* в виде целого числа, начиная с единицы, и *n* в качестве общего числа указанных вершин используются следующие интерпретации.</span><span class="sxs-lookup"><span data-stu-id="32b5f-122">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="32b5f-123">Можно использовать только подмножество функций OpenGL между **глбегин** и **гленд**.</span><span class="sxs-lookup"><span data-stu-id="32b5f-123">You can use only a subset of OpenGL functions between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="32b5f-124">Вы можете использовать следующие функции:</span><span class="sxs-lookup"><span data-stu-id="32b5f-124">The functions you can use are:</span></span>

    -   [<span data-ttu-id="32b5f-125">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="32b5f-125">**glVertex**</span></span>](glvertex-functions.md)
    -   [<span data-ttu-id="32b5f-126">**глколор**</span><span class="sxs-lookup"><span data-stu-id="32b5f-126">**glColor**</span></span>](glcolor-functions.md)
    -   [<span data-ttu-id="32b5f-127">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="32b5f-127">**glIndex**</span></span>](glindex-functions.md)
    -   [<span data-ttu-id="32b5f-128">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="32b5f-128">**glNormal**</span></span>](glnormal-functions.md)
    -   [<span data-ttu-id="32b5f-129">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="32b5f-129">**glTexCoord**</span></span>](gltexcoord-functions.md)
    -   [<span data-ttu-id="32b5f-130">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="32b5f-130">**glEvalCoord**</span></span>](glevalcoord-functions.md)
    -   [<span data-ttu-id="32b5f-131">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="32b5f-131">**glEvalPoint**</span></span>](glevalpoint.md)
    -   [<span data-ttu-id="32b5f-132">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="32b5f-132">**glMaterial**</span></span>](glmaterial-functions.md)
    -   [<span data-ttu-id="32b5f-133">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="32b5f-133">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="32b5f-134">Можно также использовать [**глкалллист**](glcalllist.md) или [**глкалллистс**](glcalllists.md) для выполнения списков вывода, включающих только предыдущие функции.</span><span class="sxs-lookup"><span data-stu-id="32b5f-134">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="32b5f-135">Если между **глбегин** и **гленд** вызывается любая другая функция OpenGL, устанавливается флаг ошибки и функция игнорируется.</span><span class="sxs-lookup"><span data-stu-id="32b5f-135">If any other OpenGL function is called between **glBegin** and **glEnd**, the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="32b5f-136">Независимо от значения, выбранного для *режима* в **глбегин**, количество вершин, которые можно определить между **глбегин** и **гленд**, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="32b5f-136">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="32b5f-137">Линии, треугольники, куадрилатералс и многоугольники, которые не были заданы, не рисуются.</span><span class="sxs-lookup"><span data-stu-id="32b5f-137">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="32b5f-138">Неполные результаты спецификации, если указано слишком мало вершин для указания даже одного примитива или если задано неверное кратное для вершин.</span><span class="sxs-lookup"><span data-stu-id="32b5f-138">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="32b5f-139">Неполный примитив не учитывается; рисуются все примитивы.</span><span class="sxs-lookup"><span data-stu-id="32b5f-139">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="32b5f-140">Минимальная спецификация вершин для каждого примитива:</span><span class="sxs-lookup"><span data-stu-id="32b5f-140">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="32b5f-141">Минимальное число вершин</span><span class="sxs-lookup"><span data-stu-id="32b5f-141">Minimum number of vertices</span></span> | <span data-ttu-id="32b5f-142">Тип примитива</span><span class="sxs-lookup"><span data-stu-id="32b5f-142">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="32b5f-143">1</span><span class="sxs-lookup"><span data-stu-id="32b5f-143">1</span></span>                          | <span data-ttu-id="32b5f-144">point</span><span class="sxs-lookup"><span data-stu-id="32b5f-144">point</span></span>             |
    | <span data-ttu-id="32b5f-145">2</span><span class="sxs-lookup"><span data-stu-id="32b5f-145">2</span></span>                          | <span data-ttu-id="32b5f-146">line</span><span class="sxs-lookup"><span data-stu-id="32b5f-146">line</span></span>              |
    | <span data-ttu-id="32b5f-147">3</span><span class="sxs-lookup"><span data-stu-id="32b5f-147">3</span></span>                          | <span data-ttu-id="32b5f-148">треугольник</span><span class="sxs-lookup"><span data-stu-id="32b5f-148">triangle</span></span>          |
    | <span data-ttu-id="32b5f-149">4</span><span class="sxs-lookup"><span data-stu-id="32b5f-149">4</span></span>                          | <span data-ttu-id="32b5f-150">грани четырехсторонней</span><span class="sxs-lookup"><span data-stu-id="32b5f-150">quadrilateral</span></span>     |
    | <span data-ttu-id="32b5f-151">3</span><span class="sxs-lookup"><span data-stu-id="32b5f-151">3</span></span>                          | <span data-ttu-id="32b5f-152">polygon</span><span class="sxs-lookup"><span data-stu-id="32b5f-152">polygon</span></span>           |

    

     

-   <span data-ttu-id="32b5f-153">Режимы, для которых требуется несколько вершин, — это \_ строки GL (2), \_ треугольники GL (3), \_ четыре четырехъядерных (4) и \_ четыре четырехъядерных \_ лент (2).</span><span class="sxs-lookup"><span data-stu-id="32b5f-153">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="32b5f-154">Требования</span><span class="sxs-lookup"><span data-stu-id="32b5f-154">Requirements</span></span>



| <span data-ttu-id="32b5f-155">Требование</span><span class="sxs-lookup"><span data-stu-id="32b5f-155">Requirement</span></span> | <span data-ttu-id="32b5f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="32b5f-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32b5f-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32b5f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="32b5f-158">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="32b5f-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="32b5f-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32b5f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="32b5f-160">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="32b5f-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32b5f-161">Заголовок</span><span class="sxs-lookup"><span data-stu-id="32b5f-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b5f-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="32b5f-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="32b5f-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32b5f-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="32b5f-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32b5f-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="32b5f-165">DLL</span><span class="sxs-lookup"><span data-stu-id="32b5f-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32b5f-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32b5f-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b5f-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32b5f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b5f-168">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="32b5f-168">**glBegin**</span></span>](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[<span data-ttu-id="32b5f-169">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="32b5f-169">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="32b5f-170">**глколор**</span><span class="sxs-lookup"><span data-stu-id="32b5f-170">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="32b5f-171">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="32b5f-171">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="32b5f-172">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="32b5f-172">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="32b5f-173">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="32b5f-173">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="32b5f-174">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="32b5f-174">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="32b5f-175">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="32b5f-175">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="32b5f-176">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="32b5f-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="32b5f-177">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="32b5f-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="32b5f-178">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="32b5f-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

