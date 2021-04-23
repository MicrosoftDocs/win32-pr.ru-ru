---
title: Функция glNormal3s (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3s (GL. h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- Функция glNormal3s OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7941fa4e2c4e5ef00a5a14ce1eb913fb22a1f58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273516"
---
# <a name="glnormal3s-function"></a><span data-ttu-id="db8ff-105">Функция glNormal3s</span><span class="sxs-lookup"><span data-stu-id="db8ff-105">glNormal3s function</span></span>

<span data-ttu-id="db8ff-106">Задает текущий вектор нормали.</span><span class="sxs-lookup"><span data-stu-id="db8ff-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="db8ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db8ff-107">Syntax</span></span>


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a><span data-ttu-id="db8ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="db8ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db8ff-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="db8ff-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="db8ff-110">Задает координату x нового текущего вектора нормали.</span><span class="sxs-lookup"><span data-stu-id="db8ff-110">Specifies the x-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="db8ff-111">*Йорк*</span><span class="sxs-lookup"><span data-stu-id="db8ff-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="db8ff-112">Задает координату по оси y нового текущего вектора нормали.</span><span class="sxs-lookup"><span data-stu-id="db8ff-112">Specifies the y-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="db8ff-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="db8ff-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="db8ff-114">Задает z-координату нового текущего вектора нормали.</span><span class="sxs-lookup"><span data-stu-id="db8ff-114">Specifies the z-coordinate of the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db8ff-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db8ff-115">Return value</span></span>

<span data-ttu-id="db8ff-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="db8ff-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db8ff-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db8ff-117">Remarks</span></span>

<span data-ttu-id="db8ff-118">Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3s**.</span><span class="sxs-lookup"><span data-stu-id="db8ff-118">The current normal is set to the given coordinates whenever you call the **glNormal3s** function.</span></span>

<span data-ttu-id="db8ff-119">Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с линейным сопоставлением, которое сопоставляет наиболее положительное целочисленное значение с 1,0 и самое отрицательное целочисленное значение с-1,0.</span><span class="sxs-lookup"><span data-stu-id="db8ff-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="db8ff-120">Нормали, заданные с помощью **glNormal3s** , не должны иметь длину единицы.</span><span class="sxs-lookup"><span data-stu-id="db8ff-120">Normals specified by using **glNormal3s** need not have unit length.</span></span> <span data-ttu-id="db8ff-121">Если нормализация включена, то нормали, заданные с помощью **glNormal3s** , нормализуются после преобразования.</span><span class="sxs-lookup"><span data-stu-id="db8ff-121">If normalization is enabled, then normals specified with **glNormal3s** are normalized after transformation.</span></span> <span data-ttu-id="db8ff-122">Вы можете управлять нормализатионби с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации.</span><span class="sxs-lookup"><span data-stu-id="db8ff-122">You can control normalizationby using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="db8ff-123">По умолчанию нормализация отключена.</span><span class="sxs-lookup"><span data-stu-id="db8ff-123">By default, normalization is disabled.</span></span> <span data-ttu-id="db8ff-124">Текущее нормальное состояние можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="db8ff-124">You can update the current normal at any time.</span></span> <span data-ttu-id="db8ff-125">В частности, можно вызвать **glNormal3s** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="db8ff-125">In particular, you can call **glNormal3s** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="db8ff-126">Следующие функции извлекают сведения, относящиеся к **glNormal3s**:</span><span class="sxs-lookup"><span data-stu-id="db8ff-126">The following functions retrieve information related to **glNormal3s**:</span></span>

<span data-ttu-id="db8ff-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Текущая \_ нормальная</span><span class="sxs-lookup"><span data-stu-id="db8ff-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="db8ff-128">[**глисенабле**](glisenabled.md) с аргументом \_ нормализации GL</span><span class="sxs-lookup"><span data-stu-id="db8ff-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="db8ff-129">Требования</span><span class="sxs-lookup"><span data-stu-id="db8ff-129">Requirements</span></span>



| <span data-ttu-id="db8ff-130">Требование</span><span class="sxs-lookup"><span data-stu-id="db8ff-130">Requirement</span></span> | <span data-ttu-id="db8ff-131">Значение</span><span class="sxs-lookup"><span data-stu-id="db8ff-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db8ff-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db8ff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="db8ff-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db8ff-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="db8ff-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db8ff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="db8ff-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="db8ff-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db8ff-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="db8ff-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="db8ff-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="db8ff-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="db8ff-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db8ff-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="db8ff-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db8ff-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="db8ff-140">DLL</span><span class="sxs-lookup"><span data-stu-id="db8ff-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db8ff-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db8ff-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8ff-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db8ff-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8ff-143">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="db8ff-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="db8ff-144">**глколор**</span><span class="sxs-lookup"><span data-stu-id="db8ff-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="db8ff-145">**гленд**</span><span class="sxs-lookup"><span data-stu-id="db8ff-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="db8ff-146">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="db8ff-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="db8ff-147">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="db8ff-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="db8ff-148">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="db8ff-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





