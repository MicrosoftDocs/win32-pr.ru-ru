---
title: Функция glNormal3iv (GL. h)
description: Задает текущий вектор нормали. | Функция glNormal3iv (GL. h)
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- Функция glNormal3iv OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5629a12d6c388da2aa133fbe72177646b4f95d63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000274"
---
# <a name="glnormal3iv-function"></a><span data-ttu-id="43d59-105">Функция glNormal3iv</span><span class="sxs-lookup"><span data-stu-id="43d59-105">glNormal3iv function</span></span>

<span data-ttu-id="43d59-106">Задает текущий вектор нормали.</span><span class="sxs-lookup"><span data-stu-id="43d59-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43d59-107">Syntax</span></span>


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="43d59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43d59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d59-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="43d59-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="43d59-110">Указатель на массив из трех элементов: координаты x, y и z нового текущего нормального значения.</span><span class="sxs-lookup"><span data-stu-id="43d59-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d59-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43d59-111">Return value</span></span>

<span data-ttu-id="43d59-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="43d59-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d59-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43d59-113">Remarks</span></span>

<span data-ttu-id="43d59-114">Текущее значение нормали задается для заданных координат при каждом вызове функции **glNormal3iv**.</span><span class="sxs-lookup"><span data-stu-id="43d59-114">The current normal is set to the given coordinates whenever you call the **glNormal3iv** function.</span></span>

<span data-ttu-id="43d59-115">Аргументы Byte, short или Integer преобразуются в формат с плавающей запятой с линейным сопоставлением, которое сопоставляет наиболее положительное целочисленное значение с 1,0 и самое отрицательное целочисленное значение с-1,0.</span><span class="sxs-lookup"><span data-stu-id="43d59-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="43d59-116">Нормали, заданные с помощью **glNormal3iv** , не должны иметь длину единицы.</span><span class="sxs-lookup"><span data-stu-id="43d59-116">Normals specified by using **glNormal3iv** need not have unit length.</span></span> <span data-ttu-id="43d59-117">Если нормализация включена, то нормали, заданные с помощью **glNormal3iv** , нормализуются после преобразования.</span><span class="sxs-lookup"><span data-stu-id="43d59-117">If normalization is enabled, then normals specified with **glNormal3iv** are normalized after transformation.</span></span> <span data-ttu-id="43d59-118">Нормализацию можно управлять с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализации.</span><span class="sxs-lookup"><span data-stu-id="43d59-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="43d59-119">По умолчанию нормализация отключена.</span><span class="sxs-lookup"><span data-stu-id="43d59-119">By default, normalization is disabled.</span></span> <span data-ttu-id="43d59-120">Текущее нормальное состояние можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="43d59-120">You can update the current normal at any time.</span></span> <span data-ttu-id="43d59-121">В частности, можно вызвать **glNormal3iv** между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="43d59-121">In particular, you can call **glNormal3iv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="43d59-122">Следующие функции извлекают сведения, относящиеся к **glNormal3iv**:</span><span class="sxs-lookup"><span data-stu-id="43d59-122">The following functions retrieve information related to **glNormal3iv**:</span></span>

<span data-ttu-id="43d59-123">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Текущая \_ нормальная</span><span class="sxs-lookup"><span data-stu-id="43d59-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="43d59-124">[**глисенабле**](glisenabled.md) с аргументом \_ нормализации GL</span><span class="sxs-lookup"><span data-stu-id="43d59-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="43d59-125">Требования</span><span class="sxs-lookup"><span data-stu-id="43d59-125">Requirements</span></span>



| <span data-ttu-id="43d59-126">Требование</span><span class="sxs-lookup"><span data-stu-id="43d59-126">Requirement</span></span> | <span data-ttu-id="43d59-127">Значение</span><span class="sxs-lookup"><span data-stu-id="43d59-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43d59-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43d59-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43d59-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43d59-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="43d59-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43d59-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43d59-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43d59-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43d59-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="43d59-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d59-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="43d59-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="43d59-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43d59-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="43d59-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43d59-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="43d59-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43d59-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43d59-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43d59-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d59-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43d59-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d59-139">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="43d59-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="43d59-140">**глколор**</span><span class="sxs-lookup"><span data-stu-id="43d59-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="43d59-141">**гленд**</span><span class="sxs-lookup"><span data-stu-id="43d59-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="43d59-142">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="43d59-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="43d59-143">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="43d59-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="43d59-144">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="43d59-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





