---
title: Функция Глжетклипплане (GL. h)
description: Функция Глжетклипплане возвращает коэффициенты указанной плоскости отсечения.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- Функция Глжетклипплане OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682157"
---
# <a name="glgetclipplane-function"></a><span data-ttu-id="ff6ab-104">Функция Глжетклипплане</span><span class="sxs-lookup"><span data-stu-id="ff6ab-104">glGetClipPlane function</span></span>

<span data-ttu-id="ff6ab-105">Функция **глжетклипплане** возвращает коэффициенты указанной плоскости отсечения.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-105">The **glGetClipPlane** function returns the coefficients of the specified clipping plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff6ab-106">Syntax</span></span>


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="ff6ab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff6ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff6ab-108">*плоскости*</span><span class="sxs-lookup"><span data-stu-id="ff6ab-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="ff6ab-109">Плоскость обрезки.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-109">A clipping plane.</span></span> <span data-ttu-id="ff6ab-110">Количество обтравочных плоскостей зависит от реализации, но поддерживаются по крайней мере шесть плоскостей обрезки.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-110">The number of clipping planes depends on the implementation, but at least six clipping planes are supported.</span></span> <span data-ttu-id="ff6ab-111">Они идентифицируются символами в виде \_ \_ плоскости Clip плоскость *i* , где 0 = *я* < \_ Максимальное число \_ плоскостей для вырезок \_ .</span><span class="sxs-lookup"><span data-stu-id="ff6ab-111">They are identified by symbolic names of the form GL\_CLIP\_PLANE *i* where 0 = *i* < GL\_MAX\_CLIP\_PLANES.</span></span>

</dd> <dt>

<span data-ttu-id="ff6ab-112">*Дробь*</span><span class="sxs-lookup"><span data-stu-id="ff6ab-112">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="ff6ab-113">Возвращает четыре значения двойной точности, которые являются коэффициентами в уравнении плоскости *плоскости* в координатах глаза.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-113">Returns four double-precision values that are the coefficients of the plane equation of *plane* in eye coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff6ab-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff6ab-114">Return value</span></span>

<span data-ttu-id="ff6ab-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff6ab-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ff6ab-116">Error codes</span></span>

<span data-ttu-id="ff6ab-117">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ff6ab-118">Имя</span><span class="sxs-lookup"><span data-stu-id="ff6ab-118">Name</span></span>                                                                                                  | <span data-ttu-id="ff6ab-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ff6ab-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff6ab-120"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ff6ab-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ff6ab-121">*плоскость* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="ff6ab-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ff6ab-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ff6ab-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ff6ab-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ff6ab-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff6ab-124">Remarks</span></span>

<span data-ttu-id="ff6ab-125">Функция **глжетклипплане** возвращает в *уравнениях* четыре коэффициента уравнения плоскости для *плоскости*.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-125">The **glGetClipPlane** function returns in *equation* the four coefficients of the plane equation for *plane*.</span></span>

<span data-ttu-id="ff6ab-126">Это всегда так, что GL — это « \_ \_  \_ \_ PLANE0». </span><span class="sxs-lookup"><span data-stu-id="ff6ab-126">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="ff6ab-127">Если возникает ошибка, в содержимое *уравнения* не вносятся никакие изменения.</span><span class="sxs-lookup"><span data-stu-id="ff6ab-127">If an error is generated, no change is made to the contents of *equation*.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff6ab-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ff6ab-128">Requirements</span></span>



| <span data-ttu-id="ff6ab-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ff6ab-129">Requirement</span></span> | <span data-ttu-id="ff6ab-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ff6ab-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6ab-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff6ab-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ff6ab-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff6ab-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ff6ab-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff6ab-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ff6ab-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff6ab-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff6ab-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff6ab-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff6ab-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff6ab-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ff6ab-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff6ab-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff6ab-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff6ab-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff6ab-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ff6ab-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff6ab-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff6ab-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff6ab-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff6ab-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff6ab-142">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="ff6ab-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ff6ab-143">**глклипплане**</span><span class="sxs-lookup"><span data-stu-id="ff6ab-143">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="ff6ab-144">**гленд**</span><span class="sxs-lookup"><span data-stu-id="ff6ab-144">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





