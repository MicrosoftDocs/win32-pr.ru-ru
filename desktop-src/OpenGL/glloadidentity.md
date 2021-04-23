---
title: Функция Гллоадидентити (GL. h)
description: Функция Гллоадидентити заменяет текущую матрицу матрицей идентификаторов.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- Функция Гллоадидентити OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104566316"
---
# <a name="glloadidentity-function"></a><span data-ttu-id="8a635-104">Функция Гллоадидентити</span><span class="sxs-lookup"><span data-stu-id="8a635-104">glLoadIdentity function</span></span>

<span data-ttu-id="8a635-105">Функция **гллоадидентити** заменяет текущую матрицу матрицей идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="8a635-105">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a635-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a635-106">Syntax</span></span>


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a><span data-ttu-id="8a635-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a635-107">Parameters</span></span>

<span data-ttu-id="8a635-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="8a635-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a635-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a635-109">Return value</span></span>

<span data-ttu-id="8a635-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8a635-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a635-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8a635-111">Error codes</span></span>

<span data-ttu-id="8a635-112">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="8a635-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8a635-113">Имя</span><span class="sxs-lookup"><span data-stu-id="8a635-113">Name</span></span>                                                                                                  | <span data-ttu-id="8a635-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8a635-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a635-115"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8a635-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8a635-116">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8a635-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8a635-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a635-117">Remarks</span></span>

<span data-ttu-id="8a635-118">Функция **гллоадидентити** заменяет текущую матрицу матрицей идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="8a635-118">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span> <span data-ttu-id="8a635-119">Он семантически эквивалентен вызову [**гллоадматрикс**](glloadmatrix.md) со следующей матрицей идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="8a635-119">It is semantically equivalent to calling [**glLoadMatrix**](glloadmatrix.md) with the following identity matrix.</span></span>

![Схема, показывающая матрицу идентификаторов, Гллоадидентити вызовы.](images/load01.png)

<span data-ttu-id="8a635-121">Однако в некоторых случаях это более эффективно.</span><span class="sxs-lookup"><span data-stu-id="8a635-121">However, in some cases, it is more efficient.</span></span>

<span data-ttu-id="8a635-122">Следующие функции извлекают сведения, относящиеся к **гллоадидентити**:</span><span class="sxs-lookup"><span data-stu-id="8a635-122">The following functions retrieve information related to **glLoadIdentity**:</span></span>

<span data-ttu-id="8a635-123">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="8a635-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="8a635-124">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="8a635-124">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="8a635-125">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="8a635-125">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="8a635-126">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="8a635-126">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="8a635-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8a635-127">Requirements</span></span>



| <span data-ttu-id="8a635-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8a635-128">Requirement</span></span> | <span data-ttu-id="8a635-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8a635-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a635-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a635-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8a635-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a635-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8a635-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a635-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8a635-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a635-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a635-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8a635-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a635-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a635-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8a635-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a635-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a635-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a635-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a635-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8a635-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a635-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a635-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a635-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a635-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a635-141">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="8a635-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8a635-142">**гленд**</span><span class="sxs-lookup"><span data-stu-id="8a635-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8a635-143">**гллоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="8a635-143">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="8a635-144">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="8a635-144">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="8a635-145">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="8a635-145">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="8a635-146">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="8a635-146">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





