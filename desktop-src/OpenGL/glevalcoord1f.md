---
title: Функция glEvalCoord1f (GL. h)
description: Функция glEvalCoord1f оценивает включенные одномерные карты.
ms.assetid: 520e2d31-b9c2-4b06-ab61-c2c7aa18448a
keywords:
- Функция glEvalCoord1f OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d1b7faebf155c6027b715c64573fbb9463868
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489729"
---
# <a name="glevalcoord1f-function"></a><span data-ttu-id="f89bc-104">Функция glEvalCoord1f</span><span class="sxs-lookup"><span data-stu-id="f89bc-104">glEvalCoord1f function</span></span>

<span data-ttu-id="f89bc-105">Функция **glEvalCoord1f** оценивает включенные одномерные карты.</span><span class="sxs-lookup"><span data-stu-id="f89bc-105">The **glEvalCoord1f** function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89bc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f89bc-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1f(
   GLfloat u
);
```



## <a name="parameters"></a><span data-ttu-id="f89bc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f89bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89bc-108">*u*</span><span class="sxs-lookup"><span data-stu-id="f89bc-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="f89bc-109">Значение, которое является координатой в *домене, для* базовой функции, определенной в предыдущей функции [**glMap1**](glmap1.md) .</span><span class="sxs-lookup"><span data-stu-id="f89bc-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap1**](glmap1.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f89bc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f89bc-110">Return value</span></span>

<span data-ttu-id="f89bc-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f89bc-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f89bc-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f89bc-112">Remarks</span></span>

<span data-ttu-id="f89bc-113">Функция **glEvalCoord1f** вычисляет включенные одномерные карты в аргументе *u*.</span><span class="sxs-lookup"><span data-stu-id="f89bc-113">The **glEvalCoord1f** function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="f89bc-114">Определение сопоставлений с помощью [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="f89bc-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="f89bc-115">Включите или отключите их с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="f89bc-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="f89bc-116">При выдаче одной из функций **глевалкурд** вычисляются все включенные в данный момент карты указанного измерения.</span><span class="sxs-lookup"><span data-stu-id="f89bc-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="f89bc-117">Затем для каждой включенной схемы будет так, как если бы соответствующая функция OpenGL была выдана вместе с вычисленным значением.</span><span class="sxs-lookup"><span data-stu-id="f89bc-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="f89bc-118">То есть, если включен индекс GL \_ «Карта1» \_ index или GL \_ MAP2 \_ , то функция [**глиндекс**](glindex-functions.md) моделируется.</span><span class="sxs-lookup"><span data-stu-id="f89bc-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="f89bc-119">Если \_ включен «КАРТА1» GL \_ Color \_ 4 или GL \_ map2, то \_ \_ функция **глколор** моделируется.</span><span class="sxs-lookup"><span data-stu-id="f89bc-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="f89bc-120">Если включен стандарт GL \_ «Карта1» \_ Обычная или GL \_ MAP2 \_ , создается стандартный вектор, и если любая из GL \_ «Карта1» \_ текстура \_ курд \_ 1, GL \_ «Карта1» \_ текстура \_ курд \_ 2, GL \_ «КАРТА1» \_ текстура \_ курд \_ 3, GL \_ «Карта1» \_ текстура курд \_ \_ 4, GL \_ MAP2 текстура 1, GL курд текстуры MAP2 2, GL курд текстуры MAP2 3 и GL курд текстура MAP2 4, \_ \_ \_ \_ \_ \_ то будет \_ \_ \_ \_ \_ \_ \_ \_ \_ смоделирована соответствующая [**курд**](gltexcoord-functions.md) функция.</span><span class="sxs-lookup"><span data-stu-id="f89bc-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="f89bc-121">OpenGL использует вычисленные значения вместо текущих значений для включенных оценок, а текущие значения — для цвета, индекса цвета, нормали и координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="f89bc-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="f89bc-122">Однако вычисленные значения не обновляют текущие значения.</span><span class="sxs-lookup"><span data-stu-id="f89bc-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="f89bc-123">Таким словами, если функции [**глвертекс**](glvertex-functions.md) вместе с функциями **глевалкурд** , значения, созданные функциями **глевалкурд** , не влияют на цвет, нормальную координату и координаты текстуры, связанные с функциями **глвертекс** , но только с самыми последними функциями [**глколор**](glcolor-functions.md), [**глиндекс**](glindex-functions.md), [**глнормал**](glnormal-functions.md)и [**глтекскурд**](gltexcoord-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="f89bc-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="f89bc-124">Следующие функции извлекают сведения, относящиеся к функции **glEvalCoord1f** :</span><span class="sxs-lookup"><span data-stu-id="f89bc-124">The following functions retrieve information related to the **glEvalCoord1f** function:</span></span>

<span data-ttu-id="f89bc-125">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="f89bc-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="f89bc-126">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ вершина \_ 4</span><span class="sxs-lookup"><span data-stu-id="f89bc-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="f89bc-127">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ index</span><span class="sxs-lookup"><span data-stu-id="f89bc-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="f89bc-128">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="f89bc-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="f89bc-129">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="f89bc-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="f89bc-130">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="f89bc-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="f89bc-131">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="f89bc-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="f89bc-132">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="f89bc-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="f89bc-133">[**глисенаблед**](glisenabled.md) с аргументом GL \_ «Карта1» \_ текстура \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="f89bc-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="f89bc-134">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="f89bc-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="f89bc-135">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ вершина \_ 4</span><span class="sxs-lookup"><span data-stu-id="f89bc-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="f89bc-136">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ index</span><span class="sxs-lookup"><span data-stu-id="f89bc-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="f89bc-137">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="f89bc-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="f89bc-138">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="f89bc-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="f89bc-139">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="f89bc-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="f89bc-140">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="f89bc-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="f89bc-141">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="f89bc-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="f89bc-142">[**глисенаблед**](glisenabled.md) с аргументом GL \_ MAP2 \_ текстура \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="f89bc-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="f89bc-143">[**глисенаблед**](glisenabled.md) с аргументом \_ " \_ Обычная настройка"</span><span class="sxs-lookup"><span data-stu-id="f89bc-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="f89bc-144">Требования</span><span class="sxs-lookup"><span data-stu-id="f89bc-144">Requirements</span></span>



| <span data-ttu-id="f89bc-145">Требование</span><span class="sxs-lookup"><span data-stu-id="f89bc-145">Requirement</span></span> | <span data-ttu-id="f89bc-146">Значение</span><span class="sxs-lookup"><span data-stu-id="f89bc-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f89bc-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f89bc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f89bc-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f89bc-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f89bc-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f89bc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f89bc-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f89bc-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f89bc-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f89bc-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f89bc-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f89bc-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f89bc-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f89bc-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="f89bc-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f89bc-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f89bc-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f89bc-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f89bc-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f89bc-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f89bc-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f89bc-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89bc-158">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="f89bc-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f89bc-159">**глколор**</span><span class="sxs-lookup"><span data-stu-id="f89bc-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f89bc-160">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="f89bc-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="f89bc-161">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="f89bc-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="f89bc-162">**гленд**</span><span class="sxs-lookup"><span data-stu-id="f89bc-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f89bc-163">**глевалмеш**</span><span class="sxs-lookup"><span data-stu-id="f89bc-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="f89bc-164">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="f89bc-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="f89bc-165">**глжетмап**</span><span class="sxs-lookup"><span data-stu-id="f89bc-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="f89bc-166">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="f89bc-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f89bc-167">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="f89bc-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="f89bc-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="f89bc-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="f89bc-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="f89bc-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="f89bc-170">**глмапгрид**</span><span class="sxs-lookup"><span data-stu-id="f89bc-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="f89bc-171">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="f89bc-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="f89bc-172">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="f89bc-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f89bc-173">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="f89bc-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





