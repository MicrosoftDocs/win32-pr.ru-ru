---
title: Функция Глматриксмоде (GL. h)
description: Функция Глматриксмоде указывает, какая матрица является текущей матрицей.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- Функция Глматриксмоде OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136566"
---
# <a name="glmatrixmode-function"></a><span data-ttu-id="24ddc-104">Функция Глматриксмоде</span><span class="sxs-lookup"><span data-stu-id="24ddc-104">glMatrixMode function</span></span>

<span data-ttu-id="24ddc-105">Функция **глматриксмоде** указывает, какая матрица является текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="24ddc-105">The **glMatrixMode** function specifies which matrix is the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ddc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24ddc-106">Syntax</span></span>


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="24ddc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24ddc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ddc-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="24ddc-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="24ddc-109">Стек матриц, который является целевым объектом для последующих операций с матрицей.</span><span class="sxs-lookup"><span data-stu-id="24ddc-109">The matrix stack that is the target for subsequent matrix operations.</span></span> <span data-ttu-id="24ddc-110">Параметр *mode* может принимать одно из трех значений.</span><span class="sxs-lookup"><span data-stu-id="24ddc-110">The *mode* parameter can assume one of three values.</span></span>



| <span data-ttu-id="24ddc-111">Значение</span><span class="sxs-lookup"><span data-stu-id="24ddc-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="24ddc-112">Значение</span><span class="sxs-lookup"><span data-stu-id="24ddc-112">Meaning</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <span data-ttu-id="24ddc-113"><dt>**\_МОДЕЛВИЕВ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-113"><dt>**GL\_MODELVIEW**</dt></span></span> </dl>    | <span data-ttu-id="24ddc-114">Применяет последующие операции с матрицей к стеку матрицы моделвиев.</span><span class="sxs-lookup"><span data-stu-id="24ddc-114">Applies subsequent matrix operations to the modelview matrix stack.</span></span><br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <span data-ttu-id="24ddc-115"><dt>**\_ПРОЕКЦИЯ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-115"><dt>**GL\_PROJECTION**</dt></span></span> </dl> | <span data-ttu-id="24ddc-116">Применяет последующие операции с матрицей к стеку матрицы проекции.</span><span class="sxs-lookup"><span data-stu-id="24ddc-116">Applies subsequent matrix operations to the projection matrix stack.</span></span><br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <span data-ttu-id="24ddc-117"><dt>**\_текстура GL**</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-117"><dt>**GL\_TEXTURE**</dt></span></span> </dl>          | <span data-ttu-id="24ddc-118">Применяет последующие операции с матрицей к стеку матриц текстуры.</span><span class="sxs-lookup"><span data-stu-id="24ddc-118">Applies subsequent matrix operations to the texture matrix stack.</span></span><br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ddc-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24ddc-119">Return value</span></span>

<span data-ttu-id="24ddc-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="24ddc-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="24ddc-121">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="24ddc-121">Error codes</span></span>

<span data-ttu-id="24ddc-122">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="24ddc-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="24ddc-123">Имя</span><span class="sxs-lookup"><span data-stu-id="24ddc-123">Name</span></span>                                                                                                  | <span data-ttu-id="24ddc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="24ddc-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24ddc-125"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="24ddc-126">*режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="24ddc-126">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="24ddc-127"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="24ddc-128">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="24ddc-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="24ddc-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24ddc-129">Remarks</span></span>

<span data-ttu-id="24ddc-130">Функция **глматриксмоде** устанавливает текущий режим матрицы.</span><span class="sxs-lookup"><span data-stu-id="24ddc-130">The **glMatrixMode** function sets the current matrix mode.</span></span>

<span data-ttu-id="24ddc-131">Следующая функция получает сведения, связанные с **глматриксмоде**:</span><span class="sxs-lookup"><span data-stu-id="24ddc-131">The following function retrieves information related to **glMatrixMode**:</span></span>

<span data-ttu-id="24ddc-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="24ddc-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="24ddc-133">Требования</span><span class="sxs-lookup"><span data-stu-id="24ddc-133">Requirements</span></span>



| <span data-ttu-id="24ddc-134">Требование</span><span class="sxs-lookup"><span data-stu-id="24ddc-134">Requirement</span></span> | <span data-ttu-id="24ddc-135">Значение</span><span class="sxs-lookup"><span data-stu-id="24ddc-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24ddc-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24ddc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="24ddc-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24ddc-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="24ddc-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24ddc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="24ddc-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24ddc-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24ddc-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="24ddc-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="24ddc-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="24ddc-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24ddc-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="24ddc-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="24ddc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="24ddc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24ddc-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24ddc-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24ddc-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24ddc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ddc-147">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="24ddc-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="24ddc-148">**гленд**</span><span class="sxs-lookup"><span data-stu-id="24ddc-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="24ddc-149">**гллоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="24ddc-149">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="24ddc-150">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="24ddc-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





