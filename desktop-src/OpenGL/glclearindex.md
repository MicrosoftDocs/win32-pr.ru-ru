---
title: Функция Глклеариндекс (GL. h)
description: Функция Глклеариндекс указывает значение Clear для буферов цветового индекса.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- Функция Глклеариндекс OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491133"
---
# <a name="glclearindex-function"></a><span data-ttu-id="20bd0-104">Функция Глклеариндекс</span><span class="sxs-lookup"><span data-stu-id="20bd0-104">glClearIndex function</span></span>

<span data-ttu-id="20bd0-105">Функция **глклеариндекс** указывает значение Clear для буферов цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="20bd0-105">The **glClearIndex** function specifies the clear value for the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bd0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20bd0-106">Syntax</span></span>


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a><span data-ttu-id="20bd0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20bd0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20bd0-108">*c*</span><span class="sxs-lookup"><span data-stu-id="20bd0-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="20bd0-109">Индекс, используемый при очистке буферов цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="20bd0-109">The index used when the color-index buffers are cleared.</span></span> <span data-ttu-id="20bd0-110">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="20bd0-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20bd0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20bd0-111">Return value</span></span>

<span data-ttu-id="20bd0-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="20bd0-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="20bd0-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="20bd0-113">Error codes</span></span>

<span data-ttu-id="20bd0-114">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="20bd0-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="20bd0-115">Имя</span><span class="sxs-lookup"><span data-stu-id="20bd0-115">Name</span></span>                                                                                                  | <span data-ttu-id="20bd0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="20bd0-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20bd0-117"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="20bd0-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="20bd0-118">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="20bd0-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="20bd0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20bd0-119">Remarks</span></span>

<span data-ttu-id="20bd0-120">Функция **глклеариндекс** указывает индекс, используемый [**глклеар**](glclear.md) для очистки буферов цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="20bd0-120">The **glClearIndex** function specifies the index used by [**glClear**](glclear.md) to clear the color-index buffers.</span></span> <span data-ttu-id="20bd0-121">Параметр *c* не имеет фиксации.</span><span class="sxs-lookup"><span data-stu-id="20bd0-121">The *c* parameter is not clamped.</span></span> <span data-ttu-id="20bd0-122">Вместо этого *c* преобразуется в значение с фиксированной запятой с неуказанной точностью справа от двоичной точки.</span><span class="sxs-lookup"><span data-stu-id="20bd0-122">Rather, *c* is converted to a fixed-point value with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="20bd0-123">Затем целая часть этого значения маскируется 2 <sup>м</sup>  -1, где *m* — число битов в индексе цвета, который хранится в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="20bd0-123">The integer part of this value is then masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in a color index stored in the framebuffer.</span></span>

<span data-ttu-id="20bd0-124">Следующие функции извлекают сведения, относящиеся к **глклеариндекс**:</span><span class="sxs-lookup"><span data-stu-id="20bd0-124">The following functions retrieve information related to **glClearIndex**:</span></span>

<span data-ttu-id="20bd0-125">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ очистить \_ значение индекса GL"</span><span class="sxs-lookup"><span data-stu-id="20bd0-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="20bd0-126">**глжет** с аргументом \_ биты индекса GL \_</span><span class="sxs-lookup"><span data-stu-id="20bd0-126">**glGet** with argument GL\_INDEX\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="20bd0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="20bd0-127">Requirements</span></span>



| <span data-ttu-id="20bd0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="20bd0-128">Requirement</span></span> | <span data-ttu-id="20bd0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="20bd0-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20bd0-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20bd0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="20bd0-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20bd0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="20bd0-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20bd0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="20bd0-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20bd0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20bd0-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="20bd0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="20bd0-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="20bd0-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="20bd0-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20bd0-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="20bd0-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20bd0-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="20bd0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="20bd0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20bd0-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20bd0-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bd0-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20bd0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bd0-141">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="20bd0-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="20bd0-142">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="20bd0-142">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="20bd0-143">**гленд**</span><span class="sxs-lookup"><span data-stu-id="20bd0-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="20bd0-144">**глжет**</span><span class="sxs-lookup"><span data-stu-id="20bd0-144">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





