---
title: Функция Глдепсранже (GL. h)
description: Функция Глдепсранже указывает сопоставление значений z от нормализованных координат устройства до координат окна.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- Функция Глдепсранже OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415129"
---
# <a name="gldepthrange-function"></a><span data-ttu-id="3cbbd-104">Функция Глдепсранже</span><span class="sxs-lookup"><span data-stu-id="3cbbd-104">glDepthRange function</span></span>

<span data-ttu-id="3cbbd-105">Функция **глдепсранже** указывает сопоставление значений *z* от нормализованных координат устройства до координат окна.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-105">The **glDepthRange** function specifies the mapping of *z* values from normalized device coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbbd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cbbd-106">Syntax</span></span>


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a><span data-ttu-id="3cbbd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cbbd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cbbd-108">*знеар*</span><span class="sxs-lookup"><span data-stu-id="3cbbd-108">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="3cbbd-109">Сопоставление ближней плоскости отсечения с координатами окна.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-109">The mapping of the near clipping plane to window coordinates.</span></span> <span data-ttu-id="3cbbd-110">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="3cbbd-111">*зфар*</span><span class="sxs-lookup"><span data-stu-id="3cbbd-111">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="3cbbd-112">Сопоставление дальней плоскости с координатами окна.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-112">The mapping of the far clipping plane to window coordinates.</span></span> <span data-ttu-id="3cbbd-113">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-113">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cbbd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cbbd-114">Return value</span></span>

<span data-ttu-id="3cbbd-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3cbbd-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3cbbd-116">Error codes</span></span>

<span data-ttu-id="3cbbd-117">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3cbbd-118">Имя</span><span class="sxs-lookup"><span data-stu-id="3cbbd-118">Name</span></span>                                                                                                  | <span data-ttu-id="3cbbd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3cbbd-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3cbbd-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3cbbd-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3cbbd-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3cbbd-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3cbbd-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cbbd-122">Remarks</span></span>

<span data-ttu-id="3cbbd-123">После отсечения и деления на *w* координаты *z* находятся в диапазоне от 0,0 до 1,0, соответствующих ближайшим и далеко обрезанным плоскостям.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-123">After clipping and division by *w*, *z* -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes.</span></span> <span data-ttu-id="3cbbd-124">Функция **глдепсранже** задает линейное сопоставление нормализованных координат *z* в этом диапазоне с координатами окна по *оси z*.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-124">The **glDepthRange** function specifies a linear mapping of the normalized *z*-coordinates in this range to window *z*-coordinates.</span></span> <span data-ttu-id="3cbbd-125">Независимо от фактической реализации буфера глубины, значения глубины координат окна обрабатываются так, как будто они находятся в диапазоне от 0,0 до 1,0 (например, цветовые компоненты).</span><span class="sxs-lookup"><span data-stu-id="3cbbd-125">Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components).</span></span> <span data-ttu-id="3cbbd-126">Поэтому значения, принимаемые функцией **глдепсранже** , преобразуются в этот диапазон до их принятия.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-126">Thus, the values accepted by **glDepthRange** are both clamped to this range before they are accepted.</span></span>

<span data-ttu-id="3cbbd-127">Сопоставление по умолчанию (0, 1) сопоставляет ближайшую плоскость с 0 и дальней плоскости с 1.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-127">The default mapping of (0,1) maps the near plane to 0 and the far plane to 1.</span></span> <span data-ttu-id="3cbbd-128">При таком сопоставлении диапазон буферов глубины используется полностью.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-128">With this mapping, the depth buffer range is fully utilized.</span></span>

<span data-ttu-id="3cbbd-129">Не обязательно, чтобы *знеар* был меньше *зфар*.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-129">It is not necessary that *zNear* be less than *zFar*.</span></span> <span data-ttu-id="3cbbd-130">Обратные сопоставления, такие как (1, 0), приемлемы.</span><span class="sxs-lookup"><span data-stu-id="3cbbd-130">Reverse mappings such as (1,0) are acceptable.</span></span>

<span data-ttu-id="3cbbd-131">Следующая функция получает сведения, связанные с **глдепсранже**:</span><span class="sxs-lookup"><span data-stu-id="3cbbd-131">The following function retrieves information related to **glDepthRange**:</span></span>

<span data-ttu-id="3cbbd-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ диапазона глубины GL \_</span><span class="sxs-lookup"><span data-stu-id="3cbbd-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_RANGE</span></span>

## <a name="requirements"></a><span data-ttu-id="3cbbd-133">Требования</span><span class="sxs-lookup"><span data-stu-id="3cbbd-133">Requirements</span></span>



| <span data-ttu-id="3cbbd-134">Требование</span><span class="sxs-lookup"><span data-stu-id="3cbbd-134">Requirement</span></span> | <span data-ttu-id="3cbbd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3cbbd-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbbd-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cbbd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3cbbd-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3cbbd-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3cbbd-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cbbd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3cbbd-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3cbbd-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3cbbd-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3cbbd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cbbd-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cbbd-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3cbbd-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3cbbd-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="3cbbd-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cbbd-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3cbbd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3cbbd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cbbd-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cbbd-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cbbd-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cbbd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cbbd-147">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="3cbbd-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3cbbd-148">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="3cbbd-148">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="3cbbd-149">**гленд**</span><span class="sxs-lookup"><span data-stu-id="3cbbd-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3cbbd-150">**глжет**</span><span class="sxs-lookup"><span data-stu-id="3cbbd-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3cbbd-151">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="3cbbd-151">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





