---
title: Функция glColor3f (GL. h)
description: Задает текущий цвет. | Функция glColor3f (GL. h)
ms.assetid: 3d6706f4-1028-4b23-b956-720f5611cd88
keywords:
- Функция glColor3f OpenGL
topic_type:
- apiref
api_name:
- glColor3f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd58db9ed0111f854f5580a8865d2e919a84a959
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914664"
---
# <a name="glcolor3f-function"></a><span data-ttu-id="9f480-105">Функция glColor3f</span><span class="sxs-lookup"><span data-stu-id="9f480-105">glColor3f function</span></span>

<span data-ttu-id="9f480-106">Задает текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="9f480-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f480-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f480-107">Syntax</span></span>


```C++
void WINAPI glColor3f(
   GLfloat red,
   GLfloat green,
   GLfloat blue
);
```



## <a name="parameters"></a><span data-ttu-id="9f480-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f480-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f480-109">*отмечен*</span><span class="sxs-lookup"><span data-stu-id="9f480-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="9f480-110">Новое Красное значение для текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="9f480-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="9f480-111">*зеленого*</span><span class="sxs-lookup"><span data-stu-id="9f480-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="9f480-112">Новое зеленое значение для текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="9f480-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="9f480-113">*выделен*</span><span class="sxs-lookup"><span data-stu-id="9f480-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="9f480-114">Новое синее значение для текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="9f480-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f480-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f480-115">Return value</span></span>

<span data-ttu-id="9f480-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9f480-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f480-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f480-117">Remarks</span></span>

<span data-ttu-id="9f480-118">В GL хранится и текущий однозначный цветовой индекс, и текущий цвет RGBA с четырьмя значениями.</span><span class="sxs-lookup"><span data-stu-id="9f480-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="9f480-119">**глколор** задает новый цвет RGBA с четырьмя значениями.</span><span class="sxs-lookup"><span data-stu-id="9f480-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="9f480-120">**глколор** имеет два основных варианта: **glcolor3** и **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="9f480-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="9f480-121">**glcolor3** варианты задают явно новые значения красного, зеленого и синего типа и устанавливают текущее значение альфа равным 1,0 (Полная интенсивность) неявно.</span><span class="sxs-lookup"><span data-stu-id="9f480-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="9f480-122">**glcolor4** варианты указывают все четыре компонента цвета явным образом.</span><span class="sxs-lookup"><span data-stu-id="9f480-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="9f480-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** и **glcolor4i** принимают в качестве аргументов три или четыре байта со знаком, короткие или длинные целые числа.</span><span class="sxs-lookup"><span data-stu-id="9f480-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="9f480-124">Когда к имени добавляется v, команды Color могут принимать указатель на массив таких значений.</span><span class="sxs-lookup"><span data-stu-id="9f480-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="9f480-125">Текущие значения цвета хранятся в формате с плавающей запятой с неопределенным значением мантисса и размером экспоненты.</span><span class="sxs-lookup"><span data-stu-id="9f480-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="9f480-126">Неподписанные целочисленные компоненты цвета, если они заданы, линейно сопоставляются со значениями с плавающей запятой, что наибольшее представимое значение соответствует 1,0 (Полная интенсивность), а 0 сопоставляется с 0,0 (нулевой интенсивностью).</span><span class="sxs-lookup"><span data-stu-id="9f480-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="9f480-127">Компоненты цветового целого числа со знаком, если они заданы, линейно сопоставляются со значениями с плавающей запятой, что наиболее положительное представление сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="9f480-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="9f480-128">(Обратите внимание, что это сопоставление не преобразует значение 0 точно в 0,0.) Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="9f480-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="9f480-129">Ни одно из целочисленных значений с плавающей запятой и со знаком не передается в диапазон \[ 0, 1 \] до обновления текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="9f480-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="9f480-130">Однако компоненты цвета отправляются в этот диапазон до того, как они интерполируются или записаны в буфер цвета.</span><span class="sxs-lookup"><span data-stu-id="9f480-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f480-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9f480-131">Requirements</span></span>



| <span data-ttu-id="9f480-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9f480-132">Requirement</span></span> | <span data-ttu-id="9f480-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9f480-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f480-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f480-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9f480-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f480-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9f480-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f480-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9f480-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f480-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f480-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f480-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f480-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f480-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9f480-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f480-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f480-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f480-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f480-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9f480-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f480-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f480-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f480-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f480-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f480-145">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="9f480-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9f480-146">**гленд**</span><span class="sxs-lookup"><span data-stu-id="9f480-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9f480-147">**Глжетбулеанв, Глжетдаублев, Глжетфлоатв, Глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="9f480-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9f480-148">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="9f480-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





