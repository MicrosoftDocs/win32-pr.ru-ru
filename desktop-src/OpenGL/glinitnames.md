---
title: Функция Глинитнамес (GL. h)
description: Функция Глинитнамес инициализирует стек имен.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- Функция Глинитнамес OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135178"
---
# <a name="glinitnames-function"></a><span data-ttu-id="68921-104">Функция Глинитнамес</span><span class="sxs-lookup"><span data-stu-id="68921-104">glInitNames function</span></span>

<span data-ttu-id="68921-105">Функция **глинитнамес** инициализирует стек имен.</span><span class="sxs-lookup"><span data-stu-id="68921-105">The **glInitNames** function initializes the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="68921-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68921-106">Syntax</span></span>


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a><span data-ttu-id="68921-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="68921-107">Parameters</span></span>

<span data-ttu-id="68921-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="68921-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68921-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68921-109">Return value</span></span>

<span data-ttu-id="68921-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="68921-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68921-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="68921-111">Error codes</span></span>

<span data-ttu-id="68921-112">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="68921-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="68921-113">Имя</span><span class="sxs-lookup"><span data-stu-id="68921-113">Name</span></span>                                                                                                  | <span data-ttu-id="68921-114">Значение</span><span class="sxs-lookup"><span data-stu-id="68921-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68921-115"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="68921-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="68921-116">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="68921-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="68921-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68921-117">Remarks</span></span>

<span data-ttu-id="68921-118">Функция **глинитнамес** приводит к инициализации стека имен в пустое состояние по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68921-118">The **glInitNames** function causes the name stack to be initialized to its default empty state.</span></span> <span data-ttu-id="68921-119">В режиме выбора используется стек имен, чтобы обеспечить уникальную идентификацию наборов команд отрисовки.</span><span class="sxs-lookup"><span data-stu-id="68921-119">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="68921-120">Он состоит из упорядоченного набора целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="68921-120">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="68921-121">Стек имен всегда пуст, пока режим рендеринга не является GL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="68921-121">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="68921-122">Вызовы **глинитнамес** , когда режим рендеринга не является GL \_ SELECT, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="68921-122">Calls to **glInitNames** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="68921-123">Следующие функции извлекают сведения, относящиеся к **глинитнамес**:</span><span class="sxs-lookup"><span data-stu-id="68921-123">The following functions retrieve information related to **glInitNames**:</span></span>

<span data-ttu-id="68921-124">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Длина стека имен GL \_</span><span class="sxs-lookup"><span data-stu-id="68921-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="68921-125">**глжет** с аргументом \_ , \_ \_ глубина стека максимальных имен \_</span><span class="sxs-lookup"><span data-stu-id="68921-125">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="68921-126">Требования</span><span class="sxs-lookup"><span data-stu-id="68921-126">Requirements</span></span>



| <span data-ttu-id="68921-127">Требование</span><span class="sxs-lookup"><span data-stu-id="68921-127">Requirement</span></span> | <span data-ttu-id="68921-128">Значение</span><span class="sxs-lookup"><span data-stu-id="68921-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68921-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68921-129">Minimum supported client</span></span><br/> | <span data-ttu-id="68921-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68921-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="68921-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68921-131">Minimum supported server</span></span><br/> | <span data-ttu-id="68921-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68921-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68921-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="68921-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="68921-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="68921-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="68921-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68921-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="68921-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68921-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="68921-137">DLL</span><span class="sxs-lookup"><span data-stu-id="68921-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68921-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68921-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68921-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68921-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68921-140">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="68921-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="68921-141">**гленд**</span><span class="sxs-lookup"><span data-stu-id="68921-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="68921-142">**гллоаднаме**</span><span class="sxs-lookup"><span data-stu-id="68921-142">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="68921-143">**глпушнаме**</span><span class="sxs-lookup"><span data-stu-id="68921-143">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="68921-144">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="68921-144">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="68921-145">**глселектбуффер**</span><span class="sxs-lookup"><span data-stu-id="68921-145">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





