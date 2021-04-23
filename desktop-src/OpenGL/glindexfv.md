---
title: Функция Глиндексфв (GL. h)
description: Функция Глиндексфв задает текущий индекс цвета.
ms.assetid: 355d1896-ea9d-4a80-9dee-285f3bf638e5
keywords:
- Функция Глиндексфв OpenGL
topic_type:
- apiref
api_name:
- glIndexfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a649f15dd6fad637d9e742a97235fdcd99d82794
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071358"
---
# <a name="glindexfv-function"></a><span data-ttu-id="7000d-104">Функция Глиндексфв</span><span class="sxs-lookup"><span data-stu-id="7000d-104">glIndexfv function</span></span>

<span data-ttu-id="7000d-105">Функция **глиндексфв** задает текущий индекс цвета.</span><span class="sxs-lookup"><span data-stu-id="7000d-105">The **glIndexfv** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7000d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7000d-106">Syntax</span></span>


```C++
void WINAPI glIndexfv(
   const GLfloat *c
);
```



## <a name="parameters"></a><span data-ttu-id="7000d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7000d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7000d-108">*c*</span><span class="sxs-lookup"><span data-stu-id="7000d-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="7000d-109">Указатель на одноэлементный массив, который содержит новое значение для текущего индекса цвета.</span><span class="sxs-lookup"><span data-stu-id="7000d-109">A pointer to a one-element array that contains the new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7000d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7000d-110">Return value</span></span>

<span data-ttu-id="7000d-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7000d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7000d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7000d-112">Remarks</span></span>

<span data-ttu-id="7000d-113">Функция **глиндексфв** обновляет текущий (однозначный) цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="7000d-113">The **glIndexfv** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="7000d-114">Он принимает один аргумент: новое значение для текущего индекса цвета.</span><span class="sxs-lookup"><span data-stu-id="7000d-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="7000d-115">Текущий индекс хранится в виде значения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="7000d-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="7000d-116">Целочисленные значения преобразуются непосредственно в значения с плавающей запятой без специального сопоставления.</span><span class="sxs-lookup"><span data-stu-id="7000d-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="7000d-117">Значения индекса за пределами представимого диапазона буфера цветового индекса не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="7000d-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="7000d-118">Однако перед тем, как индекс переносится (если он включен) и записывается в буфера кадров, он преобразуется в формат с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="7000d-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="7000d-119">Все биты в целой части результирующего значения с фиксированной запятой, которые не соответствуют битам в буфера кадров, маскируются.</span><span class="sxs-lookup"><span data-stu-id="7000d-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="7000d-120">Текущий индекс можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="7000d-120">The current index can be updated at any time.</span></span> <span data-ttu-id="7000d-121">В частности, **глиндексфв** можно вызывать между вызовом [**глбегин**](/windows/desktop/OpenGL/glbegin) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7000d-121">In particular, **glIndexfv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="7000d-122">Следующая функция получает сведения, связанные с **глиндексфв**:</span><span class="sxs-lookup"><span data-stu-id="7000d-122">The following function retrieves information related to **glIndexfv**:</span></span>

<span data-ttu-id="7000d-123">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущий \_ индекс GL</span><span class="sxs-lookup"><span data-stu-id="7000d-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="7000d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7000d-124">Requirements</span></span>



| <span data-ttu-id="7000d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7000d-125">Requirement</span></span> | <span data-ttu-id="7000d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7000d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7000d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7000d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7000d-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7000d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7000d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7000d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7000d-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7000d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7000d-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7000d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7000d-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7000d-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7000d-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7000d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7000d-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7000d-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7000d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7000d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7000d-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7000d-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7000d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7000d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7000d-138">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="7000d-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7000d-139">**глколор**</span><span class="sxs-lookup"><span data-stu-id="7000d-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="7000d-140">**гленд**</span><span class="sxs-lookup"><span data-stu-id="7000d-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7000d-141">**глжет**</span><span class="sxs-lookup"><span data-stu-id="7000d-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

