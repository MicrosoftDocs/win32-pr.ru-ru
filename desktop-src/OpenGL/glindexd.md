---
title: Функция Глиндексд (GL. h)
description: Функция Глиндексд задает текущий индекс цвета.
ms.assetid: 4cd72d32-e796-4c94-94cb-591f1ee3b26e
keywords:
- Функция Глиндексд OpenGL
topic_type:
- apiref
api_name:
- glIndexd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d1e7cce6ad2ae39e5ca107ef89b3b86147596e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988358"
---
# <a name="glindexd-function"></a><span data-ttu-id="7a5ce-104">Функция Глиндексд</span><span class="sxs-lookup"><span data-stu-id="7a5ce-104">glIndexd function</span></span>

<span data-ttu-id="7a5ce-105">Функция **глиндексд** задает текущий индекс цвета.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-105">The **glIndexd** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5ce-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a5ce-106">Syntax</span></span>


```C++
void WINAPI glIndexd(
   GLdouble c
);
```



## <a name="parameters"></a><span data-ttu-id="7a5ce-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a5ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5ce-108">*c*</span><span class="sxs-lookup"><span data-stu-id="7a5ce-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="7a5ce-109">Новое значение для текущего индекса цвета.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-109">The new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5ce-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a5ce-110">Return value</span></span>

<span data-ttu-id="7a5ce-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a5ce-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a5ce-112">Remarks</span></span>

<span data-ttu-id="7a5ce-113">Функция **глиндексд** обновляет текущий (однозначный) цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-113">The **glIndexd** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="7a5ce-114">Он принимает один аргумент: новое значение для текущего индекса цвета.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="7a5ce-115">Текущий индекс хранится в виде значения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="7a5ce-116">Целочисленные значения преобразуются непосредственно в значения с плавающей запятой без специального сопоставления.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="7a5ce-117">Значения индекса за пределами представимого диапазона буфера цветового индекса не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="7a5ce-118">Однако перед тем, как индекс переносится (если он включен) и записывается в буфера кадров, он преобразуется в формат с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="7a5ce-119">Все биты в целой части результирующего значения с фиксированной запятой, которые не соответствуют битам в буфера кадров, маскируются.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="7a5ce-120">Текущий индекс можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="7a5ce-120">The current index can be updated at any time.</span></span> <span data-ttu-id="7a5ce-121">В частности, **глиндексд** можно вызывать между вызовом [**глбегин**](/windows/desktop/OpenGL/glbegin) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7a5ce-121">In particular, **glIndexd** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="7a5ce-122">Следующая функция получает сведения, связанные с **глиндексд**:</span><span class="sxs-lookup"><span data-stu-id="7a5ce-122">The following function retrieves information related to **glIndexd**:</span></span>

<span data-ttu-id="7a5ce-123">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущий \_ индекс GL</span><span class="sxs-lookup"><span data-stu-id="7a5ce-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5ce-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7a5ce-124">Requirements</span></span>



| <span data-ttu-id="7a5ce-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7a5ce-125">Requirement</span></span> | <span data-ttu-id="7a5ce-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7a5ce-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5ce-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a5ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5ce-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a5ce-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7a5ce-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a5ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5ce-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a5ce-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a5ce-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7a5ce-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5ce-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5ce-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7a5ce-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a5ce-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a5ce-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a5ce-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a5ce-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7a5ce-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a5ce-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a5ce-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a5ce-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a5ce-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5ce-138">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="7a5ce-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7a5ce-139">**глколор**</span><span class="sxs-lookup"><span data-stu-id="7a5ce-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="7a5ce-140">**гленд**</span><span class="sxs-lookup"><span data-stu-id="7a5ce-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7a5ce-141">**глжет**</span><span class="sxs-lookup"><span data-stu-id="7a5ce-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

