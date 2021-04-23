---
title: Функция glTexCoord4d (GL. h)
description: Задает текущие координаты текстуры. | Функция glTexCoord4d (GL. h)
ms.assetid: d9045a2e-81f3-4f63-8eee-e882c586b8fe
keywords:
- Функция glTexCoord4d OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6671b5eee2fab966438075d56de1da2ca4537793
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674652"
---
# <a name="gltexcoord4d-function"></a><span data-ttu-id="bc806-105">Функция glTexCoord4d</span><span class="sxs-lookup"><span data-stu-id="bc806-105">glTexCoord4d function</span></span>

<span data-ttu-id="bc806-106">Задает текущие координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="bc806-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc806-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc806-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4d(
   GLdouble s,
   GLdouble t,
   GLdouble r,
   GLdouble q
);
```



## <a name="parameters"></a><span data-ttu-id="bc806-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc806-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc806-109">*s*</span><span class="sxs-lookup"><span data-stu-id="bc806-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-110">Координата текстуры "s".</span><span class="sxs-lookup"><span data-stu-id="bc806-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="bc806-111">*t*</span><span class="sxs-lookup"><span data-stu-id="bc806-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-112">Координата текстуры t.</span><span class="sxs-lookup"><span data-stu-id="bc806-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="bc806-113">*r*</span><span class="sxs-lookup"><span data-stu-id="bc806-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-114">Координата текстуры r.</span><span class="sxs-lookup"><span data-stu-id="bc806-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="bc806-115">*формате*</span><span class="sxs-lookup"><span data-stu-id="bc806-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="bc806-116">Координата текстуры q.</span><span class="sxs-lookup"><span data-stu-id="bc806-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc806-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc806-117">Return value</span></span>

<span data-ttu-id="bc806-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bc806-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc806-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc806-119">Remarks</span></span>

<span data-ttu-id="bc806-120">Функция [**глтекскурд**](gltexcoord-functions.md) задает текущие координаты текстуры, которые являются частью данных, связанных с вершинами многоугольников.</span><span class="sxs-lookup"><span data-stu-id="bc806-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="bc806-121">Функция **глтекскурд** задает координаты текстуры в одном, двух, трех или четырех измерениях.</span><span class="sxs-lookup"><span data-stu-id="bc806-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="bc806-122">Функция glTexCoord1 устанавливает для текущих координат текстуры значение (s, 0, 0, 1); вызов glTexCoord2 задает для них значение (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bc806-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="bc806-123">Аналогичным образом glTexCoord3 определяет координаты текстуры как (s, t, r, 1), а glTexCoord4 определяет все четыре компонента явным образом (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="bc806-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="bc806-124">Текущие координаты текстуры можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="bc806-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="bc806-125">В частности, можно вызвать Глтекскурд между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bc806-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="bc806-126">Следующая функция получает сведения, связанные с **глтекскурд**:</span><span class="sxs-lookup"><span data-stu-id="bc806-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="bc806-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в качестве \_ \_ координат текущей текстуры главной книги \_</span><span class="sxs-lookup"><span data-stu-id="bc806-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="bc806-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bc806-128">Requirements</span></span>



| <span data-ttu-id="bc806-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bc806-129">Requirement</span></span> | <span data-ttu-id="bc806-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bc806-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc806-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc806-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bc806-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc806-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc806-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc806-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bc806-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bc806-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc806-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bc806-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc806-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc806-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bc806-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc806-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc806-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc806-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc806-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bc806-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc806-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc806-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc806-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc806-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc806-142">глвертекс</span><span class="sxs-lookup"><span data-stu-id="bc806-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





