---
title: Функция Гллоаднаме (GL. h)
description: Функция Гллоаднаме загружает имя в стек имен.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- Функция Гллоаднаме OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137719"
---
# <a name="glloadname-function"></a><span data-ttu-id="4d140-104">Функция Гллоаднаме</span><span class="sxs-lookup"><span data-stu-id="4d140-104">glLoadName function</span></span>

<span data-ttu-id="4d140-105">Функция **гллоаднаме** загружает имя в стек имен.</span><span class="sxs-lookup"><span data-stu-id="4d140-105">The **glLoadName** function loads a name onto the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d140-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d140-106">Syntax</span></span>


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="4d140-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d140-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d140-108">*name*</span><span class="sxs-lookup"><span data-stu-id="4d140-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="4d140-109">Имя, которое заменит верхнее значение в стеке имен.</span><span class="sxs-lookup"><span data-stu-id="4d140-109">A name that will replace the top value on the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d140-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d140-110">Return value</span></span>

<span data-ttu-id="4d140-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4d140-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d140-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4d140-112">Error codes</span></span>

<span data-ttu-id="4d140-113">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d140-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4d140-114">Имя</span><span class="sxs-lookup"><span data-stu-id="4d140-114">Name</span></span>                                                                                                  | <span data-ttu-id="4d140-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4d140-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d140-116"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4d140-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4d140-117">Функция была вызвана, пока стек имен не был пустым.</span><span class="sxs-lookup"><span data-stu-id="4d140-117">The function was called while the name stack was empty.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="4d140-118"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4d140-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4d140-119">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4d140-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4d140-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d140-120">Remarks</span></span>

<span data-ttu-id="4d140-121">Функция **гллоаднаме** заставляет *имя* заменить значение в верхней части стека имен, которое изначально пустое.</span><span class="sxs-lookup"><span data-stu-id="4d140-121">The **glLoadName** function causes *name* to replace the value on the top of the name stack, which is initially empty.</span></span> <span data-ttu-id="4d140-122">В режиме выбора используется стек имен, чтобы обеспечить уникальную идентификацию наборов команд отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4d140-122">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="4d140-123">Он состоит из упорядоченного набора целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="4d140-123">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="4d140-124">Стек имен всегда пуст, пока режим рендеринга не является GL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="4d140-124">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="4d140-125">Вызовы **гллоаднаме** , когда режим рендеринга не является GL \_ SELECT, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="4d140-125">Calls to **glLoadName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="4d140-126">Следующие функции извлекают сведения, относящиеся к **гллоаднаме**:</span><span class="sxs-lookup"><span data-stu-id="4d140-126">The following functions retrieve information related to **glLoadName**:</span></span>

<span data-ttu-id="4d140-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Длина стека имен GL \_</span><span class="sxs-lookup"><span data-stu-id="4d140-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="4d140-128">**глжет** с аргументом \_ , \_ \_ глубина стека максимальных имен \_</span><span class="sxs-lookup"><span data-stu-id="4d140-128">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="4d140-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4d140-129">Requirements</span></span>



| <span data-ttu-id="4d140-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4d140-130">Requirement</span></span> | <span data-ttu-id="4d140-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4d140-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d140-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d140-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4d140-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4d140-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4d140-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d140-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4d140-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4d140-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d140-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4d140-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d140-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d140-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4d140-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4d140-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d140-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d140-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d140-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4d140-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d140-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d140-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d140-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d140-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d140-143">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="4d140-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4d140-144">**гленд**</span><span class="sxs-lookup"><span data-stu-id="4d140-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4d140-145">**глинитнамес**</span><span class="sxs-lookup"><span data-stu-id="4d140-145">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="4d140-146">**глпушнаме**</span><span class="sxs-lookup"><span data-stu-id="4d140-146">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="4d140-147">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="4d140-147">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="4d140-148">**глселектбуффер**</span><span class="sxs-lookup"><span data-stu-id="4d140-148">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





