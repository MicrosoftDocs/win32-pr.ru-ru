---
title: Функция glColor3ui (GL. h)
description: Задает текущий цвет. | Функция glColor3ui (GL. h)
ms.assetid: 4a04ad4d-91a8-4d70-93e5-9c8f4ec4d9d2
keywords:
- Функция glColor3ui OpenGL
topic_type:
- apiref
api_name:
- glColor3ui
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b09368fb8aba65c78eddb9ceb135476f6cfe13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664857"
---
# <a name="glcolor3ui-function"></a><span data-ttu-id="069f0-105">Функция glColor3ui</span><span class="sxs-lookup"><span data-stu-id="069f0-105">glColor3ui function</span></span>

<span data-ttu-id="069f0-106">Задает текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="069f0-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="069f0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="069f0-107">Syntax</span></span>


```C++
void WINAPI glColor3ui(
   GLuint red,
   GLuint green,
   GLuint blue
);
```



## <a name="parameters"></a><span data-ttu-id="069f0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="069f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="069f0-109">*отмечен*</span><span class="sxs-lookup"><span data-stu-id="069f0-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="069f0-110">Новое Красное значение для текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="069f0-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="069f0-111">*зеленого*</span><span class="sxs-lookup"><span data-stu-id="069f0-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="069f0-112">Новое зеленое значение для текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="069f0-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="069f0-113">*выделен*</span><span class="sxs-lookup"><span data-stu-id="069f0-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="069f0-114">Новое синее значение для текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="069f0-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="069f0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="069f0-115">Return value</span></span>

<span data-ttu-id="069f0-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="069f0-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="069f0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="069f0-117">Remarks</span></span>

<span data-ttu-id="069f0-118">В GL хранится и текущий однозначный цветовой индекс, и текущий цвет RGBA с четырьмя значениями.</span><span class="sxs-lookup"><span data-stu-id="069f0-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="069f0-119">**глколор** задает новый цвет RGBA с четырьмя значениями.</span><span class="sxs-lookup"><span data-stu-id="069f0-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="069f0-120">**глколор** имеет два основных варианта: **glcolor3** и **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="069f0-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="069f0-121">**glcolor3** варианты задают явно новые значения красного, зеленого и синего типа и устанавливают текущее значение альфа равным 1,0 (Полная интенсивность) неявно.</span><span class="sxs-lookup"><span data-stu-id="069f0-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="069f0-122">**glcolor4** варианты указывают все четыре компонента цвета явным образом.</span><span class="sxs-lookup"><span data-stu-id="069f0-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="069f0-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** и **glcolor4i** принимают в качестве аргументов три или четыре байта со знаком, короткие или длинные целые числа.</span><span class="sxs-lookup"><span data-stu-id="069f0-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="069f0-124">Когда к имени добавляется v, команды Color могут принимать указатель на массив таких значений.</span><span class="sxs-lookup"><span data-stu-id="069f0-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="069f0-125">Текущие значения цвета хранятся в формате с плавающей запятой с неопределенным значением мантисса и размером экспоненты.</span><span class="sxs-lookup"><span data-stu-id="069f0-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="069f0-126">Неподписанные целочисленные компоненты цвета, если они заданы, линейно сопоставляются со значениями с плавающей запятой, что наибольшее представимое значение соответствует 1,0 (Полная интенсивность), а 0 сопоставляется с 0,0 (нулевой интенсивностью).</span><span class="sxs-lookup"><span data-stu-id="069f0-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="069f0-127">Компоненты цветового целого числа со знаком, если они заданы, линейно сопоставляются со значениями с плавающей запятой, что наиболее положительное представление сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="069f0-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="069f0-128">(Обратите внимание, что это сопоставление не преобразует значение 0 точно в 0,0.) Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="069f0-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="069f0-129">Ни одно из целочисленных значений с плавающей запятой и со знаком не передается в диапазон \[ 0, 1 \] до обновления текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="069f0-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="069f0-130">Однако компоненты цвета отправляются в этот диапазон до того, как они интерполируются или записаны в буфер цвета.</span><span class="sxs-lookup"><span data-stu-id="069f0-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="069f0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="069f0-131">Requirements</span></span>



| <span data-ttu-id="069f0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="069f0-132">Requirement</span></span> | <span data-ttu-id="069f0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="069f0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="069f0-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="069f0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="069f0-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="069f0-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="069f0-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="069f0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="069f0-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="069f0-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="069f0-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="069f0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="069f0-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="069f0-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="069f0-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="069f0-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="069f0-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="069f0-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="069f0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="069f0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="069f0-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="069f0-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069f0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="069f0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069f0-145">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="069f0-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="069f0-146">**гленд**</span><span class="sxs-lookup"><span data-stu-id="069f0-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="069f0-147">**Глжетбулеанв, Глжетдаублев, Глжетфлоатв, Глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="069f0-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="069f0-148">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="069f0-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





