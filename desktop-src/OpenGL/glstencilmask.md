---
title: Функция ГлстенЦилмаск (GL. h)
description: Функция ГлстенЦилмаск управляет записью отдельных битов на плоскости трафарета.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- Функция ГлстенЦилмаск OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137711"
---
# <a name="glstencilmask-function"></a><span data-ttu-id="7f900-104">Функция ГлстенЦилмаск</span><span class="sxs-lookup"><span data-stu-id="7f900-104">glStencilMask function</span></span>

<span data-ttu-id="7f900-105">Функция **глстенЦилмаск** управляет записью отдельных битов на плоскости трафарета.</span><span class="sxs-lookup"><span data-stu-id="7f900-105">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f900-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f900-106">Syntax</span></span>


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="7f900-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f900-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f900-108">*виде*</span><span class="sxs-lookup"><span data-stu-id="7f900-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="7f900-109">Битовая маска для включения и отключения записи отдельных битов на плоскости трафарета.</span><span class="sxs-lookup"><span data-stu-id="7f900-109">A bit mask to enable and disable writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="7f900-110">Изначально маска все равно.</span><span class="sxs-lookup"><span data-stu-id="7f900-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f900-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f900-111">Return value</span></span>

<span data-ttu-id="7f900-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7f900-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f900-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7f900-113">Error codes</span></span>

<span data-ttu-id="7f900-114">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7f900-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7f900-115">Имя</span><span class="sxs-lookup"><span data-stu-id="7f900-115">Name</span></span>                                                                                                  | <span data-ttu-id="7f900-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7f900-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f900-117"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f900-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7f900-118">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7f900-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7f900-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f900-119">Remarks</span></span>

<span data-ttu-id="7f900-120">Функция **глстенЦилмаск** управляет записью отдельных битов на плоскости трафарета.</span><span class="sxs-lookup"><span data-stu-id="7f900-120">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="7f900-121">Наименее важные *n* бит *маски*, где *n* — число битов в буфере шаблона, укажите маску.</span><span class="sxs-lookup"><span data-stu-id="7f900-121">The least significant *n* bits of *mask*, where *n* is the number of bits in the stencil buffer, specify a mask.</span></span> <span data-ttu-id="7f900-122">Когда в маске появляется один из них, соответствующий бит в буфере шаблона становится доступным для записи.</span><span class="sxs-lookup"><span data-stu-id="7f900-122">Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable.</span></span> <span data-ttu-id="7f900-123">Если отображается ноль, бит защищен от записи.</span><span class="sxs-lookup"><span data-stu-id="7f900-123">Where a zero appears, the bit is write-protected.</span></span> <span data-ttu-id="7f900-124">Изначально все биты включены для записи.</span><span class="sxs-lookup"><span data-stu-id="7f900-124">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="7f900-125">Следующие функции извлекают сведения, относящиеся к **глстенЦилмаск**:</span><span class="sxs-lookup"><span data-stu-id="7f900-125">The following functions retrieve information related to **glStencilMask**:</span></span>

<span data-ttu-id="7f900-126">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ трафарет \_ вритемаск</span><span class="sxs-lookup"><span data-stu-id="7f900-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_WRITEMASK</span></span>

<span data-ttu-id="7f900-127">Глжет с аргументом \_ биты шаблона GL \_</span><span class="sxs-lookup"><span data-stu-id="7f900-127">glGet with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="7f900-128">Требования</span><span class="sxs-lookup"><span data-stu-id="7f900-128">Requirements</span></span>



| <span data-ttu-id="7f900-129">Требование</span><span class="sxs-lookup"><span data-stu-id="7f900-129">Requirement</span></span> | <span data-ttu-id="7f900-130">Значение</span><span class="sxs-lookup"><span data-stu-id="7f900-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f900-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f900-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7f900-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f900-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7f900-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f900-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7f900-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f900-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f900-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f900-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f900-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f900-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7f900-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f900-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f900-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f900-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7f900-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7f900-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f900-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f900-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f900-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f900-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f900-142">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="7f900-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7f900-143">**глколормаск**</span><span class="sxs-lookup"><span data-stu-id="7f900-143">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="7f900-144">**глдепсмаск**</span><span class="sxs-lookup"><span data-stu-id="7f900-144">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="7f900-145">**гленд**</span><span class="sxs-lookup"><span data-stu-id="7f900-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7f900-146">**глиндексмаск**</span><span class="sxs-lookup"><span data-stu-id="7f900-146">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="7f900-147">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="7f900-147">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="7f900-148">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="7f900-148">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





