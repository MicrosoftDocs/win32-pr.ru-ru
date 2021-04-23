---
title: Функция glEvalCoord2dv (GL. h)
description: Функция glEvalCoord2dv оценивает включенные одномерные карты.
ms.assetid: 726a0c0c-d69e-46dc-b78e-a0d1e9ad97cd
keywords:
- Функция glEvalCoord2dv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a685606fb1445c6841efdf506a1f2d4747da838
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104571144"
---
# <a name="glevalcoord2dv-function"></a><span data-ttu-id="bd411-104">Функция glEvalCoord2dv</span><span class="sxs-lookup"><span data-stu-id="bd411-104">glEvalCoord2dv function</span></span>

<span data-ttu-id="bd411-105">Функция **glEvalCoord2dv** оценивает включенные одномерные карты.</span><span class="sxs-lookup"><span data-stu-id="bd411-105">The **glEvalCoord2dv** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd411-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd411-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2dv(
   const GLdouble *u
);
```



## <a name="parameters"></a><span data-ttu-id="bd411-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd411-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd411-108">*u*</span><span class="sxs-lookup"><span data-stu-id="bd411-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="bd411-109">Указатель на массив, содержащий координату домена *u*.</span><span class="sxs-lookup"><span data-stu-id="bd411-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd411-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd411-110">Return value</span></span>

<span data-ttu-id="bd411-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bd411-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd411-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd411-112">Remarks</span></span>

<span data-ttu-id="bd411-113">Функция **glEvalCoord2dv** оценивает включенные двухмерные карты, используя два значения домена, *u* и *v*.</span><span class="sxs-lookup"><span data-stu-id="bd411-113">The **glEvalCoord2dv** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="bd411-114">Определение сопоставлений с помощью [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="bd411-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="bd411-115">Включите или отключите их с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="bd411-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="bd411-116">При выдаче одной из функций **глевалкурд** вычисляются все включенные в данный момент карты указанного измерения.</span><span class="sxs-lookup"><span data-stu-id="bd411-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="bd411-117">Затем для каждой включенной схемы будет так, как если бы соответствующая функция OpenGL была выдана вместе с вычисленным значением.</span><span class="sxs-lookup"><span data-stu-id="bd411-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="bd411-118">То есть, если включен индекс GL \_ «Карта1» \_ index или GL \_ MAP2 \_ , то функция [**глиндекс**](glindex-functions.md) моделируется.</span><span class="sxs-lookup"><span data-stu-id="bd411-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="bd411-119">Если \_ включен «КАРТА1» GL \_ Color \_ 4 или GL \_ map2, то \_ \_ функция **глколор** моделируется.</span><span class="sxs-lookup"><span data-stu-id="bd411-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="bd411-120">Если включен стандарт GL \_ «Карта1» \_ Обычная или GL \_ MAP2 \_ , создается стандартный вектор, и если любая из GL \_ «Карта1» \_ текстура \_ курд \_ 1, GL \_ «Карта1» \_ текстура \_ курд \_ 2, GL \_ «КАРТА1» \_ текстура \_ курд \_ 3, GL \_ «Карта1» \_ текстура курд \_ \_ 4, GL \_ MAP2 текстура 1, GL курд текстуры MAP2 2, GL курд текстуры MAP2 3 и GL курд текстура MAP2 4, \_ \_ \_ \_ \_ \_ то будет \_ \_ \_ \_ \_ \_ \_ \_ \_ смоделирована соответствующая [**курд**](gltexcoord-functions.md) функция.</span><span class="sxs-lookup"><span data-stu-id="bd411-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="bd411-121">OpenGL использует вычисленные значения вместо текущих значений для включенных оценок, а текущие значения — для цвета, индекса цвета, нормали и координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="bd411-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="bd411-122">Однако вычисленные значения не обновляют текущие значения.</span><span class="sxs-lookup"><span data-stu-id="bd411-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="bd411-123">Таким словами, если функции [**глвертекс**](glvertex-functions.md) вместе с функциями **глевалкурд** , значения, созданные функциями **глевалкурд** , не влияют на цвет, нормальную координату и координаты текстуры, связанные с функциями **глвертекс** , но только с самыми последними функциями [**глколор**](glcolor-functions.md), [**глиндекс**](glindex-functions.md), [**глнормал**](glnormal-functions.md)и [**глтекскурд**](gltexcoord-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="bd411-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="bd411-124">Если включено автоматическое нормальное создание, **glEvalCoord2dv** вызывает [**гленабле**](glenable.md) с аргументом GL "Auto", \_ \_ чтобы формировать нормальные нормали Surface, независимо от содержимого или включения \_ \_ стандартной схемы ГК map2.</span><span class="sxs-lookup"><span data-stu-id="bd411-124">If automatic normal generation is enabled, **glEvalCoord2dv** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="bd411-125">Let</span><span class="sxs-lookup"><span data-stu-id="bd411-125">Let</span></span>

![Формула, показывающая значение перекрестного произведения для Map m.](images/evlcrd01.png)

<span data-ttu-id="bd411-127">Созданная нормальная **n** имеет значение</span><span class="sxs-lookup"><span data-stu-id="bd411-127">The generated normal **n** is</span></span>

![Формула, отображающая созданную нормальную n для схемы.](images/evlcrd02.png)

<span data-ttu-id="bd411-129">Следующие функции извлекают сведения, относящиеся к функции **glEvalCoord2dv** :</span><span class="sxs-lookup"><span data-stu-id="bd411-129">The following functions retrieve information related to the **glEvalCoord2dv** function:</span></span>

<span data-ttu-id="bd411-130">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="bd411-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="bd411-131">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ вершина \_ 4</span><span class="sxs-lookup"><span data-stu-id="bd411-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="bd411-132">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ index</span><span class="sxs-lookup"><span data-stu-id="bd411-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="bd411-133">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="bd411-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="bd411-134">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="bd411-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="bd411-135">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="bd411-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="bd411-136">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="bd411-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="bd411-137">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="bd411-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="bd411-138">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="bd411-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="bd411-139">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="bd411-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="bd411-140">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ вершина \_ 4</span><span class="sxs-lookup"><span data-stu-id="bd411-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="bd411-141">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ index</span><span class="sxs-lookup"><span data-stu-id="bd411-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="bd411-142">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="bd411-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="bd411-143">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="bd411-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="bd411-144">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="bd411-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="bd411-145">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="bd411-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="bd411-146">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="bd411-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="bd411-147">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="bd411-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="bd411-148">[**глисенаблед**](glisenabled.md) с аргументом \_ " \_ Обычная настройка"</span><span class="sxs-lookup"><span data-stu-id="bd411-148">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="bd411-149">Требования</span><span class="sxs-lookup"><span data-stu-id="bd411-149">Requirements</span></span>



| <span data-ttu-id="bd411-150">Требование</span><span class="sxs-lookup"><span data-stu-id="bd411-150">Requirement</span></span> | <span data-ttu-id="bd411-151">Значение</span><span class="sxs-lookup"><span data-stu-id="bd411-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd411-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd411-152">Minimum supported client</span></span><br/> | <span data-ttu-id="bd411-153">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd411-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bd411-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd411-154">Minimum supported server</span></span><br/> | <span data-ttu-id="bd411-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd411-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd411-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bd411-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd411-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd411-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bd411-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bd411-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd411-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd411-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd411-160">DLL</span><span class="sxs-lookup"><span data-stu-id="bd411-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd411-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd411-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd411-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd411-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd411-163">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="bd411-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bd411-164">**глколор**</span><span class="sxs-lookup"><span data-stu-id="bd411-164">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="bd411-165">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="bd411-165">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="bd411-166">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="bd411-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="bd411-167">**гленд**</span><span class="sxs-lookup"><span data-stu-id="bd411-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bd411-168">**глевалмеш**</span><span class="sxs-lookup"><span data-stu-id="bd411-168">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="bd411-169">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="bd411-169">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="bd411-170">**глжетмап**</span><span class="sxs-lookup"><span data-stu-id="bd411-170">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="bd411-171">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="bd411-171">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="bd411-172">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="bd411-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="bd411-173">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="bd411-173">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="bd411-174">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="bd411-174">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="bd411-175">**глмапгрид**</span><span class="sxs-lookup"><span data-stu-id="bd411-175">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="bd411-176">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="bd411-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="bd411-177">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="bd411-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="bd411-178">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="bd411-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





