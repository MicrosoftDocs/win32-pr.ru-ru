---
title: Функция Глклеараккум (GL. h)
description: Функция Глклеараккум указывает четкие значения для буфера накопления.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- Функция Глклеараккум OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136198"
---
# <a name="glclearaccum-function"></a><span data-ttu-id="9c56c-104">Функция Глклеараккум</span><span class="sxs-lookup"><span data-stu-id="9c56c-104">glClearAccum function</span></span>

<span data-ttu-id="9c56c-105">Функция **глклеараккум** указывает четкие значения для буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="9c56c-105">The **glClearAccum** function specifies the clear values for the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c56c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c56c-106">Syntax</span></span>


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a><span data-ttu-id="9c56c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c56c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c56c-108">*отмечен*</span><span class="sxs-lookup"><span data-stu-id="9c56c-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="9c56c-109">Значение красного цвета, используемое при очистке буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="9c56c-109">The red value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="9c56c-110">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c56c-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c56c-111">*зеленого*</span><span class="sxs-lookup"><span data-stu-id="9c56c-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="9c56c-112">Зеленое значение, используемое при очистке буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="9c56c-112">The green value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="9c56c-113">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c56c-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c56c-114">*выделен*</span><span class="sxs-lookup"><span data-stu-id="9c56c-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="9c56c-115">Значение синего цвета, используемое при очистке буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="9c56c-115">The blue value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="9c56c-116">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c56c-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c56c-117">*буквы*</span><span class="sxs-lookup"><span data-stu-id="9c56c-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="9c56c-118">Альфа-значение, используемое при очистке буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="9c56c-118">The alpha value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="9c56c-119">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c56c-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c56c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c56c-120">Return value</span></span>

<span data-ttu-id="9c56c-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9c56c-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9c56c-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9c56c-122">Error codes</span></span>

<span data-ttu-id="9c56c-123">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c56c-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9c56c-124">Имя</span><span class="sxs-lookup"><span data-stu-id="9c56c-124">Name</span></span>                                                                                                  | <span data-ttu-id="9c56c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9c56c-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c56c-126"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9c56c-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9c56c-127">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9c56c-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9c56c-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c56c-128">Remarks</span></span>

<span data-ttu-id="9c56c-129">Функция **глклеараккум** задает красный, зеленый, синий и альфа-значения, используемые [**глклеар**](glclear.md) для очистки буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="9c56c-129">The **glClearAccum** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the accumulation buffer.</span></span>

<span data-ttu-id="9c56c-130">Значения, заданные параметром **глклеараккум** , записываются в диапазон \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="9c56c-130">Values specified by **glClearAccum** are clamped to the range \[1,1\].</span></span>

<span data-ttu-id="9c56c-131">Следующая функция получает сведения, связанные с **глклеараккум**:</span><span class="sxs-lookup"><span data-stu-id="9c56c-131">The following function retrieves information related to **glClearAccum**:</span></span>

<span data-ttu-id="9c56c-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ « \_ Удаление накопленной \_ стоимости GL»</span><span class="sxs-lookup"><span data-stu-id="9c56c-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="9c56c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="9c56c-133">Requirements</span></span>



| <span data-ttu-id="9c56c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="9c56c-134">Requirement</span></span> | <span data-ttu-id="9c56c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9c56c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c56c-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c56c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9c56c-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c56c-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c56c-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c56c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9c56c-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c56c-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c56c-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c56c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c56c-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c56c-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9c56c-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c56c-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c56c-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c56c-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c56c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9c56c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c56c-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c56c-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c56c-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c56c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c56c-147">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="9c56c-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9c56c-148">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="9c56c-148">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="9c56c-149">**гленд**</span><span class="sxs-lookup"><span data-stu-id="9c56c-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9c56c-150">**глжет**</span><span class="sxs-lookup"><span data-stu-id="9c56c-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





