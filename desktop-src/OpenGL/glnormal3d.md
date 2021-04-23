---
title: Функция glNormal3d (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3d (GL. h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- Функция glNormal3d OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ab158e298ff20cce635ab4002f38ca82fdaa2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081821"
---
# <a name="glnormal3d-function"></a><span data-ttu-id="9b31e-105">Функция glNormal3d</span><span class="sxs-lookup"><span data-stu-id="9b31e-105">glNormal3d function</span></span>

<span data-ttu-id="9b31e-106">Задает текущий вектор нормали.</span><span class="sxs-lookup"><span data-stu-id="9b31e-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b31e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b31e-107">Syntax</span></span>


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
);
```



## <a name="parameters"></a><span data-ttu-id="9b31e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b31e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b31e-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="9b31e-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="9b31e-110">Задает координату x для нового текущего вектора нормали.</span><span class="sxs-lookup"><span data-stu-id="9b31e-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="9b31e-111">*Йорк*</span><span class="sxs-lookup"><span data-stu-id="9b31e-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="9b31e-112">Задает координату y для нового текущего вектора нормали.</span><span class="sxs-lookup"><span data-stu-id="9b31e-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="9b31e-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="9b31e-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="9b31e-114">Задает координату z для нового текущего вектора нормали.</span><span class="sxs-lookup"><span data-stu-id="9b31e-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b31e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b31e-115">Return value</span></span>

<span data-ttu-id="9b31e-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9b31e-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b31e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b31e-117">Remarks</span></span>

<span data-ttu-id="9b31e-118">Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3d**.</span><span class="sxs-lookup"><span data-stu-id="9b31e-118">The current normal is set to the given coordinates whenever you call the **glNormal3d** function.</span></span>

<span data-ttu-id="9b31e-119">Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с помощью линейного сопоставления, которое сопоставляет наиболее положительное целочисленное значение 1,0 и самое отрицательное целочисленное значение с-1,0.</span><span class="sxs-lookup"><span data-stu-id="9b31e-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="9b31e-120">Нормали, заданные с помощью **glNormal3d** , не должны иметь длину единицы.</span><span class="sxs-lookup"><span data-stu-id="9b31e-120">Normals specified by using **glNormal3d** need not have unit length.</span></span> <span data-ttu-id="9b31e-121">Если нормализация включена, то нормали, заданные с помощью **glNormal3d** , нормализуются после преобразования.</span><span class="sxs-lookup"><span data-stu-id="9b31e-121">If normalization is enabled, then normals specified with **glNormal3d** are normalized after transformation.</span></span> <span data-ttu-id="9b31e-122">Нормализацию можно управлять с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации.</span><span class="sxs-lookup"><span data-stu-id="9b31e-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="9b31e-123">По умолчанию нормализация отключена.</span><span class="sxs-lookup"><span data-stu-id="9b31e-123">By default, normalization is disabled.</span></span> <span data-ttu-id="9b31e-124">Текущее нормальное состояние можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="9b31e-124">You can update the current normal at any time.</span></span> <span data-ttu-id="9b31e-125">В частности, можно вызвать **glNormal3d** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9b31e-125">In particular, you can call **glNormal3d** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="9b31e-126">Следующие функции извлекают сведения, относящиеся к **glNormal3d**:</span><span class="sxs-lookup"><span data-stu-id="9b31e-126">The following functions retrieve information related to **glNormal3d**:</span></span>

<span data-ttu-id="9b31e-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Текущая \_ нормальная</span><span class="sxs-lookup"><span data-stu-id="9b31e-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="9b31e-128">[**глисенабле**](glisenabled.md) с аргументом \_ нормализации GL</span><span class="sxs-lookup"><span data-stu-id="9b31e-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="9b31e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9b31e-129">Requirements</span></span>



| <span data-ttu-id="9b31e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9b31e-130">Requirement</span></span> | <span data-ttu-id="9b31e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9b31e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b31e-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b31e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9b31e-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9b31e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9b31e-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b31e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9b31e-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9b31e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b31e-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9b31e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b31e-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b31e-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9b31e-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b31e-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b31e-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b31e-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b31e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9b31e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b31e-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b31e-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b31e-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b31e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b31e-143">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="9b31e-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9b31e-144">**глколор**</span><span class="sxs-lookup"><span data-stu-id="9b31e-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="9b31e-145">**гленд**</span><span class="sxs-lookup"><span data-stu-id="9b31e-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9b31e-146">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="9b31e-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="9b31e-147">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="9b31e-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="9b31e-148">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="9b31e-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





