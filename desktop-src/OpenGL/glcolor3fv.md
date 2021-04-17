---
title: Функция glColor3fv (GL. h)
description: Задает текущий цвет из уже существующего массива значений цвета. | Функция glColor3fv (GL. h)
ms.assetid: 4ffaaa7e-4fa3-45b8-acf0-850e1e9d9a60
keywords:
- Функция glColor3fv OpenGL
topic_type:
- apiref
api_name:
- glColor3fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234930f573d492fe03ef39b8d3217649322095aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684966"
---
# <a name="glcolor3fv-function"></a><span data-ttu-id="59f7d-105">Функция glColor3fv</span><span class="sxs-lookup"><span data-stu-id="59f7d-105">glColor3fv function</span></span>

<span data-ttu-id="59f7d-106">Задает текущий цвет из уже существующего массива значений цвета.</span><span class="sxs-lookup"><span data-stu-id="59f7d-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f7d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59f7d-107">Syntax</span></span>


```C++
void WINAPI glColor3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="59f7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="59f7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f7d-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="59f7d-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="59f7d-110">Указатель на массив, содержащий красные, зеленые и синие значения.</span><span class="sxs-lookup"><span data-stu-id="59f7d-110">A pointer to an array that contains red, green, and blue values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59f7d-111">Return value</span></span>

<span data-ttu-id="59f7d-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="59f7d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59f7d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59f7d-113">Remarks</span></span>

<span data-ttu-id="59f7d-114">В GL хранится и текущий однозначный цветовой индекс, и текущий цвет RGBA с четырьмя значениями.</span><span class="sxs-lookup"><span data-stu-id="59f7d-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="59f7d-115">**глколор** задает новый цвет RGBA с четырьмя значениями.</span><span class="sxs-lookup"><span data-stu-id="59f7d-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="59f7d-116">**глколор** имеет два основных варианта: **glcolor3** и **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="59f7d-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="59f7d-117">**glcolor3** варианты задают явно новые значения красного, зеленого и синего типа и устанавливают текущее значение альфа равным 1,0 (Полная интенсивность) неявно.</span><span class="sxs-lookup"><span data-stu-id="59f7d-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="59f7d-118">**glcolor4** варианты указывают все четыре компонента цвета явным образом.</span><span class="sxs-lookup"><span data-stu-id="59f7d-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="59f7d-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** и **glcolor4i** принимают в качестве аргументов три или четыре байта со знаком, короткие или длинные целые числа.</span><span class="sxs-lookup"><span data-stu-id="59f7d-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="59f7d-120">Когда к имени добавляется v, команды Color могут принимать указатель на массив таких значений.</span><span class="sxs-lookup"><span data-stu-id="59f7d-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="59f7d-121">Текущие значения цвета хранятся в формате с плавающей запятой с неопределенным значением мантисса и размером экспоненты.</span><span class="sxs-lookup"><span data-stu-id="59f7d-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="59f7d-122">Неподписанные целочисленные компоненты цвета, если они заданы, линейно сопоставляются со значениями с плавающей запятой, что наибольшее представимое значение соответствует 1,0 (Полная интенсивность), а 0 сопоставляется с 0,0 (нулевой интенсивностью).</span><span class="sxs-lookup"><span data-stu-id="59f7d-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="59f7d-123">Компоненты цветового целого числа со знаком, если они заданы, линейно сопоставляются со значениями с плавающей запятой, что наиболее положительное представление сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="59f7d-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="59f7d-124">(Обратите внимание, что это сопоставление не преобразует значение 0 точно в 0,0.) Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="59f7d-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="59f7d-125">Ни одно из целочисленных значений с плавающей запятой и со знаком не передается в диапазон \[ 0, 1 \] до обновления текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="59f7d-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="59f7d-126">Однако компоненты цвета отправляются в этот диапазон до того, как они интерполируются или записаны в буфер цвета.</span><span class="sxs-lookup"><span data-stu-id="59f7d-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="59f7d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="59f7d-127">Requirements</span></span>



| <span data-ttu-id="59f7d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="59f7d-128">Requirement</span></span> | <span data-ttu-id="59f7d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="59f7d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59f7d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59f7d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="59f7d-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59f7d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="59f7d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59f7d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="59f7d-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59f7d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59f7d-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="59f7d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="59f7d-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="59f7d-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="59f7d-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59f7d-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="59f7d-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59f7d-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="59f7d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="59f7d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59f7d-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59f7d-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59f7d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59f7d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f7d-141">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="59f7d-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="59f7d-142">**гленд**</span><span class="sxs-lookup"><span data-stu-id="59f7d-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="59f7d-143">**Глжетбулеанв, Глжетдаублев, Глжетфлоатв, Глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="59f7d-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="59f7d-144">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="59f7d-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





