---
title: Функция glNormal3sv (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3sv (GL. h)
ms.assetid: 59cdebc9-594a-429f-ba5d-7c63a533cc11
keywords:
- Функция glNormal3sv OpenGL
topic_type:
- apiref
api_name:
- glNormal3sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf639364ead2e4188e56677bb68930592c4e5d5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000251"
---
# <a name="glnormal3sv-function"></a><span data-ttu-id="ec055-105">Функция glNormal3sv</span><span class="sxs-lookup"><span data-stu-id="ec055-105">glNormal3sv function</span></span>

<span data-ttu-id="ec055-106">Задает текущий вектор нормали.</span><span class="sxs-lookup"><span data-stu-id="ec055-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec055-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec055-107">Syntax</span></span>


```C++
void WINAPI glNormal3sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="ec055-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec055-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec055-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="ec055-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="ec055-110">Указатель на массив из трех элементов: координаты x, y и z нового текущего нормального значения.</span><span class="sxs-lookup"><span data-stu-id="ec055-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec055-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec055-111">Return value</span></span>

<span data-ttu-id="ec055-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ec055-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec055-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec055-113">Remarks</span></span>

<span data-ttu-id="ec055-114">Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3sv** .</span><span class="sxs-lookup"><span data-stu-id="ec055-114">The current normal is set to the given coordinates whenever you call the **glNormal3sv** function.</span></span>

<span data-ttu-id="ec055-115">Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с линейным сопоставлением, которое сопоставляет наиболее положительное целочисленное значение с 1,0 и самое отрицательное целочисленное значение с-1,0.</span><span class="sxs-lookup"><span data-stu-id="ec055-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="ec055-116">Нормали, заданные с помощью **glNormal3sv** , не должны иметь длину единицы.</span><span class="sxs-lookup"><span data-stu-id="ec055-116">Normals specified by using **glNormal3sv** need not have unit length.</span></span> <span data-ttu-id="ec055-117">Если нормализация включена, то нормали, заданные с помощью **glNormal3sv** , нормализуются после преобразования.</span><span class="sxs-lookup"><span data-stu-id="ec055-117">If normalization is enabled, then normals specified with **glNormal3sv** are normalized after transformation.</span></span> <span data-ttu-id="ec055-118">Нормализацию можно управлять с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации.</span><span class="sxs-lookup"><span data-stu-id="ec055-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="ec055-119">По умолчанию нормализация отключена.</span><span class="sxs-lookup"><span data-stu-id="ec055-119">By default, normalization is disabled.</span></span> <span data-ttu-id="ec055-120">Текущее нормальное состояние можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="ec055-120">You can update the current normal at any time.</span></span> <span data-ttu-id="ec055-121">В частности, можно вызвать **glNormal3sv** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ec055-121">In particular, you can call **glNormal3sv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="ec055-122">Следующие функции извлекают сведения, относящиеся к **glNormal3sv**:</span><span class="sxs-lookup"><span data-stu-id="ec055-122">The following functions retrieve information related to **glNormal3sv**:</span></span>

<span data-ttu-id="ec055-123">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Текущая \_ нормальная</span><span class="sxs-lookup"><span data-stu-id="ec055-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="ec055-124">[**глисенабле**](glisenabled.md) с аргументом \_ нормализации GL</span><span class="sxs-lookup"><span data-stu-id="ec055-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="ec055-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ec055-125">Requirements</span></span>



| <span data-ttu-id="ec055-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ec055-126">Requirement</span></span> | <span data-ttu-id="ec055-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ec055-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec055-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec055-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec055-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec055-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ec055-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec055-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec055-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec055-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec055-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ec055-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec055-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec055-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ec055-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ec055-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec055-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec055-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ec055-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ec055-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec055-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec055-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec055-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec055-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec055-139">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="ec055-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ec055-140">**глколор**</span><span class="sxs-lookup"><span data-stu-id="ec055-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ec055-141">**гленд**</span><span class="sxs-lookup"><span data-stu-id="ec055-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ec055-142">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="ec055-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ec055-143">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="ec055-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ec055-144">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="ec055-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





