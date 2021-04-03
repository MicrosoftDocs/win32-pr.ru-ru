---
title: Функция glTexCoord4s (GL. h)
description: Задает текущие координаты текстуры. | Функция glTexCoord4s (GL. h)
ms.assetid: 948c63f5-a94d-4e55-9aa4-a320452fc29f
keywords:
- Функция glTexCoord4s OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a164b091c62b31523baa5be96d1578e1cbfa80
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914572"
---
# <a name="gltexcoord4s-function"></a><span data-ttu-id="5539c-105">Функция glTexCoord4s</span><span class="sxs-lookup"><span data-stu-id="5539c-105">glTexCoord4s function</span></span>

<span data-ttu-id="5539c-106">Задает текущие координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="5539c-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5539c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5539c-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4s(
   GLshort s,
   GLshort t,
   GLshort r,
   GLshort q
);
```



## <a name="parameters"></a><span data-ttu-id="5539c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5539c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5539c-109">*s*</span><span class="sxs-lookup"><span data-stu-id="5539c-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="5539c-110">Координата текстуры "s".</span><span class="sxs-lookup"><span data-stu-id="5539c-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="5539c-111">*t*</span><span class="sxs-lookup"><span data-stu-id="5539c-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="5539c-112">Координата текстуры t.</span><span class="sxs-lookup"><span data-stu-id="5539c-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="5539c-113">*r*</span><span class="sxs-lookup"><span data-stu-id="5539c-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="5539c-114">Координата текстуры r.</span><span class="sxs-lookup"><span data-stu-id="5539c-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="5539c-115">*формате*</span><span class="sxs-lookup"><span data-stu-id="5539c-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="5539c-116">Координата текстуры q.</span><span class="sxs-lookup"><span data-stu-id="5539c-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5539c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5539c-117">Return value</span></span>

<span data-ttu-id="5539c-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5539c-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5539c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5539c-119">Remarks</span></span>

<span data-ttu-id="5539c-120">Функция [**глтекскурд**](gltexcoord-functions.md) задает текущие координаты текстуры, которые являются частью данных, связанных с вершинами многоугольников.</span><span class="sxs-lookup"><span data-stu-id="5539c-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="5539c-121">Функция **глтекскурд** задает координаты текстуры в одном, двух, трех или четырех измерениях.</span><span class="sxs-lookup"><span data-stu-id="5539c-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="5539c-122">Функция glTexCoord1 устанавливает для текущих координат текстуры значение (s, 0, 0, 1); вызов glTexCoord2 задает для них значение (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="5539c-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="5539c-123">Аналогичным образом glTexCoord3 определяет координаты текстуры как (s, t, r, 1), а glTexCoord4 определяет все четыре компонента явным образом (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="5539c-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="5539c-124">Текущие координаты текстуры можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="5539c-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="5539c-125">В частности, можно вызвать Глтекскурд между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5539c-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="5539c-126">Следующая функция получает сведения, связанные с **глтекскурд**:</span><span class="sxs-lookup"><span data-stu-id="5539c-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="5539c-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в качестве \_ \_ координат текущей текстуры главной книги \_</span><span class="sxs-lookup"><span data-stu-id="5539c-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="5539c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5539c-128">Requirements</span></span>



| <span data-ttu-id="5539c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5539c-129">Requirement</span></span> | <span data-ttu-id="5539c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5539c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5539c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5539c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5539c-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5539c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5539c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5539c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5539c-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5539c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5539c-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5539c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5539c-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5539c-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5539c-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5539c-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="5539c-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5539c-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5539c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5539c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5539c-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5539c-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5539c-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5539c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5539c-142">глвертекс</span><span class="sxs-lookup"><span data-stu-id="5539c-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





