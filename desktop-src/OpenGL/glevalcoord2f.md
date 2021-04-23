---
title: Функция glEvalCoord2f (GL. h)
description: Функция glEvalCoord2f оценивает включенные одномерные карты.
ms.assetid: feb2a324-9148-4e3f-8e6e-c545e36962c6
keywords:
- Функция glEvalCoord2f OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e586991b319e047957ae53362534c1bb0c90590
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350912"
---
# <a name="glevalcoord2f-function"></a><span data-ttu-id="63c21-104">Функция glEvalCoord2f</span><span class="sxs-lookup"><span data-stu-id="63c21-104">glEvalCoord2f function</span></span>

<span data-ttu-id="63c21-105">Функция [**glEvalCoord2f**](glevalcoord2d.md) оценивает включенные одномерные карты.</span><span class="sxs-lookup"><span data-stu-id="63c21-105">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c21-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63c21-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2f(
   GLfloat u,
   GLfloat v
);
```



## <a name="parameters"></a><span data-ttu-id="63c21-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="63c21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c21-108">*u*</span><span class="sxs-lookup"><span data-stu-id="63c21-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="63c21-109">Значение, которое является координатой в *домене, для* базовой функции, определенной в предыдущей функции [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="63c21-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="63c21-110">*3,3*</span><span class="sxs-lookup"><span data-stu-id="63c21-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="63c21-111">Значение, которое является координатой домена *v* для базовой функции, определенной в предыдущей функции [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="63c21-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c21-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63c21-112">Return value</span></span>

<span data-ttu-id="63c21-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="63c21-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63c21-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63c21-114">Remarks</span></span>

<span data-ttu-id="63c21-115">Функция [**glEvalCoord2f**](glevalcoord2d.md) оценивает включенные двухмерные карты, используя два значения домена, *u* и *v*.</span><span class="sxs-lookup"><span data-stu-id="63c21-115">The [**glEvalCoord2f**](glevalcoord2d.md) function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="63c21-116">Определение сопоставлений с помощью [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="63c21-116">Define maps with [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="63c21-117">Включите или отключите их с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="63c21-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="63c21-118">При выдаче одной из функций **глевалкурд** вычисляются все включенные в данный момент карты указанного измерения.</span><span class="sxs-lookup"><span data-stu-id="63c21-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="63c21-119">Затем для каждой включенной схемы будет так, как если бы соответствующая функция OpenGL была выдана вместе с вычисленным значением.</span><span class="sxs-lookup"><span data-stu-id="63c21-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="63c21-120">То есть, если включен индекс GL \_ «Карта1» \_ index или GL \_ MAP2 \_ , то функция [**глиндекс**](glindex-functions.md) моделируется.</span><span class="sxs-lookup"><span data-stu-id="63c21-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="63c21-121">Если \_ включен «КАРТА1» GL \_ Color \_ 4 или GL \_ map2, то \_ \_ функция **глколор** моделируется.</span><span class="sxs-lookup"><span data-stu-id="63c21-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="63c21-122">Если включен стандарт GL \_ «Карта1» \_ Обычная или GL \_ MAP2 \_ , создается стандартный вектор, и если любая из GL \_ «Карта1» \_ текстура \_ курд \_ 1, GL \_ «Карта1» \_ текстура \_ курд \_ 2, GL \_ «КАРТА1» \_ текстура \_ курд \_ 3, GL \_ «Карта1» \_ текстура курд \_ \_ 4, GL \_ MAP2 текстура 1, GL курд текстуры MAP2 2, GL курд текстуры MAP2 3 и GL курд текстура MAP2 4, \_ \_ \_ \_ \_ \_ то будет \_ \_ \_ \_ \_ \_ \_ \_ \_ смоделирована соответствующая [**курд**](gltexcoord-functions.md) функция.</span><span class="sxs-lookup"><span data-stu-id="63c21-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="63c21-123">OpenGL использует вычисленные значения вместо текущих значений для включенных оценок, а текущие значения — для цвета, индекса цвета, нормали и координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="63c21-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="63c21-124">Однако вычисленные значения не обновляют текущие значения.</span><span class="sxs-lookup"><span data-stu-id="63c21-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="63c21-125">Таким словами, если функции [**глвертекс**](glvertex-functions.md) вместе с функциями **глевалкурд** , значения, созданные функциями **глевалкурд** , не влияют на цвет, нормальную координату и координаты текстуры, связанные с функциями **глвертекс** , но только с самыми последними функциями [**глколор**](glcolor-functions.md), [**глиндекс**](glindex-functions.md), [**глнормал**](glnormal-functions.md)и [**глтекскурд**](gltexcoord-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="63c21-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="63c21-126">Если включено автоматическое нормальное создание, [**glEvalCoord2f**](glevalcoord2d.md) вызывает [**гленабле**](glenable.md) с аргументом GL "Auto", \_ \_ чтобы формировать нормальные нормали Surface, независимо от содержимого или включения \_ \_ стандартной схемы ГК map2.</span><span class="sxs-lookup"><span data-stu-id="63c21-126">If automatic normal generation is enabled, [**glEvalCoord2f**](glevalcoord2d.md) calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="63c21-127">Let</span><span class="sxs-lookup"><span data-stu-id="63c21-127">Let</span></span>

![Формула, показывающая значение перекрестного произведения для Map m.](images/evlcrd01.png)

<span data-ttu-id="63c21-129">Созданная нормальная **n** имеет значение</span><span class="sxs-lookup"><span data-stu-id="63c21-129">The generated normal **n** is</span></span>

![Формула, отображающая созданную нормальную n для схемы.](images/evlcrd02.png)

<span data-ttu-id="63c21-131">Следующие функции извлекают сведения, относящиеся к функции [**glEvalCoord2f**](glevalcoord2d.md) :</span><span class="sxs-lookup"><span data-stu-id="63c21-131">The following functions retrieve information related to the [**glEvalCoord2f**](glevalcoord2d.md) function:</span></span>

<span data-ttu-id="63c21-132">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="63c21-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="63c21-133">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ вершина \_ 4</span><span class="sxs-lookup"><span data-stu-id="63c21-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="63c21-134">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ index</span><span class="sxs-lookup"><span data-stu-id="63c21-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="63c21-135">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="63c21-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="63c21-136">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="63c21-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="63c21-137">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="63c21-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="63c21-138">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="63c21-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="63c21-139">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="63c21-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="63c21-140">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="63c21-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="63c21-141">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="63c21-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="63c21-142">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ вершина \_ 4</span><span class="sxs-lookup"><span data-stu-id="63c21-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="63c21-143">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ index</span><span class="sxs-lookup"><span data-stu-id="63c21-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="63c21-144">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="63c21-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="63c21-145">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="63c21-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="63c21-146">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="63c21-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="63c21-147">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="63c21-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="63c21-148">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="63c21-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="63c21-149">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="63c21-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="63c21-150">[**глисенаблед**](glisenabled.md) с аргументом \_ " \_ Обычная настройка"</span><span class="sxs-lookup"><span data-stu-id="63c21-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="63c21-151">Требования</span><span class="sxs-lookup"><span data-stu-id="63c21-151">Requirements</span></span>



| <span data-ttu-id="63c21-152">Требование</span><span class="sxs-lookup"><span data-stu-id="63c21-152">Requirement</span></span> | <span data-ttu-id="63c21-153">Значение</span><span class="sxs-lookup"><span data-stu-id="63c21-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63c21-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63c21-154">Minimum supported client</span></span><br/> | <span data-ttu-id="63c21-155">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63c21-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63c21-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63c21-156">Minimum supported server</span></span><br/> | <span data-ttu-id="63c21-157">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63c21-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63c21-158">Заголовок</span><span class="sxs-lookup"><span data-stu-id="63c21-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="63c21-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="63c21-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="63c21-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63c21-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="63c21-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63c21-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="63c21-162">DLL</span><span class="sxs-lookup"><span data-stu-id="63c21-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63c21-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c21-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c21-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63c21-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c21-165">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="63c21-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="63c21-166">**глколор**</span><span class="sxs-lookup"><span data-stu-id="63c21-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="63c21-167">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="63c21-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="63c21-168">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="63c21-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="63c21-169">**гленд**</span><span class="sxs-lookup"><span data-stu-id="63c21-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="63c21-170">**глевалмеш**</span><span class="sxs-lookup"><span data-stu-id="63c21-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="63c21-171">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="63c21-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="63c21-172">**глжетмап**</span><span class="sxs-lookup"><span data-stu-id="63c21-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="63c21-173">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="63c21-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="63c21-174">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="63c21-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="63c21-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="63c21-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="63c21-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="63c21-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="63c21-177">**глмапгрид**</span><span class="sxs-lookup"><span data-stu-id="63c21-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="63c21-178">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="63c21-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="63c21-179">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="63c21-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="63c21-180">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="63c21-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





