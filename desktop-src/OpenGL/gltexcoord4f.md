---
title: Функция glTexCoord4f (GL. h)
description: Задает текущие координаты текстуры. | Функция glTexCoord4f (GL. h)
ms.assetid: d2c190cd-3af2-425b-985b-0c66be11ef28
keywords:
- Функция glTexCoord4f OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6720effb93f233338b3e8dfbce44f4651a1061b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674651"
---
# <a name="gltexcoord4f-function"></a><span data-ttu-id="58471-105">Функция glTexCoord4f</span><span class="sxs-lookup"><span data-stu-id="58471-105">glTexCoord4f function</span></span>

<span data-ttu-id="58471-106">Задает текущие координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="58471-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="58471-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58471-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4f(
   GLfloat s,
   GLfloat t,
   GLfloat r,
   GLfloat q
);
```



## <a name="parameters"></a><span data-ttu-id="58471-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="58471-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58471-109">*s*</span><span class="sxs-lookup"><span data-stu-id="58471-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="58471-110">Координата текстуры "s".</span><span class="sxs-lookup"><span data-stu-id="58471-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="58471-111">*t*</span><span class="sxs-lookup"><span data-stu-id="58471-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="58471-112">Координата текстуры t.</span><span class="sxs-lookup"><span data-stu-id="58471-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="58471-113">*r*</span><span class="sxs-lookup"><span data-stu-id="58471-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="58471-114">Координата текстуры r.</span><span class="sxs-lookup"><span data-stu-id="58471-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="58471-115">*формате*</span><span class="sxs-lookup"><span data-stu-id="58471-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="58471-116">Координата текстуры q.</span><span class="sxs-lookup"><span data-stu-id="58471-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58471-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58471-117">Return value</span></span>

<span data-ttu-id="58471-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="58471-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58471-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58471-119">Remarks</span></span>

<span data-ttu-id="58471-120">Функция [**глтекскурд**](gltexcoord-functions.md) задает текущие координаты текстуры, которые являются частью данных, связанных с вершинами многоугольников.</span><span class="sxs-lookup"><span data-stu-id="58471-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="58471-121">Функция **глтекскурд** задает координаты текстуры в одном, двух, трех или четырех измерениях.</span><span class="sxs-lookup"><span data-stu-id="58471-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="58471-122">Функция glTexCoord1 устанавливает для текущих координат текстуры значение (s, 0, 0, 1); вызов glTexCoord2 задает для них значение (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="58471-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="58471-123">Аналогичным образом glTexCoord3 определяет координаты текстуры как (s, t, r, 1), а glTexCoord4 определяет все четыре компонента явным образом (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="58471-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="58471-124">Текущие координаты текстуры можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="58471-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="58471-125">В частности, можно вызвать Глтекскурд между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="58471-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="58471-126">Следующая функция получает сведения, связанные с **глтекскурд**:</span><span class="sxs-lookup"><span data-stu-id="58471-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="58471-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в качестве \_ \_ координат текущей текстуры главной книги \_</span><span class="sxs-lookup"><span data-stu-id="58471-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="58471-128">Требования</span><span class="sxs-lookup"><span data-stu-id="58471-128">Requirements</span></span>



| <span data-ttu-id="58471-129">Требование</span><span class="sxs-lookup"><span data-stu-id="58471-129">Requirement</span></span> | <span data-ttu-id="58471-130">Значение</span><span class="sxs-lookup"><span data-stu-id="58471-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58471-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58471-131">Minimum supported client</span></span><br/> | <span data-ttu-id="58471-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="58471-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="58471-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58471-133">Minimum supported server</span></span><br/> | <span data-ttu-id="58471-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="58471-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58471-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="58471-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="58471-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="58471-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="58471-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="58471-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="58471-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58471-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="58471-139">DLL</span><span class="sxs-lookup"><span data-stu-id="58471-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58471-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58471-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58471-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58471-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58471-142">глвертекс</span><span class="sxs-lookup"><span data-stu-id="58471-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





