---
title: Функция Глуеррорстринг (GLU. h)
description: Функция Глуеррорстринг выдает строку ошибки из кода ошибки OpenGL или GLU. Строка ошибки — только ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- Функция Глуеррорстринг OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801990"
---
# <a name="gluerrorstring-function"></a><span data-ttu-id="405b2-105">Функция Глуеррорстринг</span><span class="sxs-lookup"><span data-stu-id="405b2-105">gluErrorString function</span></span>

<span data-ttu-id="405b2-106">Функция **глуеррорстринг** выдает строку ошибки из кода ошибки OpenGL или Glu.</span><span class="sxs-lookup"><span data-stu-id="405b2-106">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="405b2-107">Строка ошибки — только ANSI.</span><span class="sxs-lookup"><span data-stu-id="405b2-107">The error string is ANSI only.</span></span>

## <a name="syntax"></a><span data-ttu-id="405b2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="405b2-108">Syntax</span></span>


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a><span data-ttu-id="405b2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="405b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="405b2-110">*ерркоде*</span><span class="sxs-lookup"><span data-stu-id="405b2-110">*errCode*</span></span> 
</dt> <dd>

<span data-ttu-id="405b2-111">Код ошибки OpenGL или GLU.</span><span class="sxs-lookup"><span data-stu-id="405b2-111">An OpenGL or GLU error code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="405b2-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="405b2-112">Remarks</span></span>

<span data-ttu-id="405b2-113">Функция **глуеррорстринг** выдает строку ошибки из кода ошибки OpenGL или Glu.</span><span class="sxs-lookup"><span data-stu-id="405b2-113">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="405b2-114">Строка имеет формат ISO Latin 1.</span><span class="sxs-lookup"><span data-stu-id="405b2-114">The string is in an ISO Latin 1 format.</span></span> <span data-ttu-id="405b2-115">Например, **глуеррорстринг**( \_ \_ \_ неиспользуемая память GL) возвращает строку "недостаточно памяти".</span><span class="sxs-lookup"><span data-stu-id="405b2-115">For example, **gluErrorString**(GL\_OUT\_OF\_MEMORY) returns the string "out of memory".</span></span>

<span data-ttu-id="405b2-116">Стандартные коды ошибок GLU — GLU \_ недопустимое \_ перечисление, Glu \_ недопустимое \_ значение и Glu \_ нехватки \_ \_ памяти.</span><span class="sxs-lookup"><span data-stu-id="405b2-116">The standard GLU error codes are GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY.</span></span> <span data-ttu-id="405b2-117">Некоторые другие функции GLU могут возвращать специализированные коды ошибок с помощью обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="405b2-117">Certain other GLU functions can return specialized error codes through callbacks.</span></span> <span data-ttu-id="405b2-118">Список кодов ошибок OpenGL см. в разделе [**глжетеррор**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="405b2-118">For the list of OpenGL error codes, see [**glGetError**](glgeterror.md).</span></span>

<span data-ttu-id="405b2-119">Функция **глуеррорстринг** создает строки ошибок только в ANSI.</span><span class="sxs-lookup"><span data-stu-id="405b2-119">The **gluErrorString** function produces error strings in ANSI only.</span></span> <span data-ttu-id="405b2-120">Везде, где это возможно, используйте **глуеррорстрингвин**, что позволяет использовать строки ошибок ANSI или Unicode.</span><span class="sxs-lookup"><span data-stu-id="405b2-120">Whenever possible, use **gluErrorStringWIN**, which allows ANSI or Unicode error strings.</span></span> <span data-ttu-id="405b2-121">Это упрощает локализацию программы для использования с другим языком.</span><span class="sxs-lookup"><span data-stu-id="405b2-121">This makes it easier to localize your program for use with another language.</span></span>

## <a name="requirements"></a><span data-ttu-id="405b2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="405b2-122">Requirements</span></span>



| <span data-ttu-id="405b2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="405b2-123">Requirement</span></span> | <span data-ttu-id="405b2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="405b2-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="405b2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="405b2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="405b2-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="405b2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="405b2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="405b2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="405b2-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="405b2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="405b2-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="405b2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="405b2-130"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="405b2-130"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="405b2-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="405b2-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="405b2-132"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="405b2-132"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="405b2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="405b2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="405b2-134"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="405b2-134"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="405b2-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="405b2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="405b2-136">**глжетеррор**</span><span class="sxs-lookup"><span data-stu-id="405b2-136">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="405b2-137">*глунурбскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="405b2-137">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="405b2-138">*глукуадриккаллбакк*</span><span class="sxs-lookup"><span data-stu-id="405b2-138">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="405b2-139">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="405b2-139">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





