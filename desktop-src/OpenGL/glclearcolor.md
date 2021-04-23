---
title: Функция Глклеарколор (GL. h)
description: Функция Глклеарколор указывает четкие значения для буферов цветов.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- Функция Глклеарколор OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802603"
---
# <a name="glclearcolor-function"></a><span data-ttu-id="cbf45-104">Функция Глклеарколор</span><span class="sxs-lookup"><span data-stu-id="cbf45-104">glClearColor function</span></span>

<span data-ttu-id="cbf45-105">Функция **глклеарколор** указывает четкие значения для буферов цветов.</span><span class="sxs-lookup"><span data-stu-id="cbf45-105">The **glClearColor** function specifies clear values for the color buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf45-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbf45-106">Syntax</span></span>


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a><span data-ttu-id="cbf45-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbf45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf45-108">*отмечен*</span><span class="sxs-lookup"><span data-stu-id="cbf45-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf45-109">Красное значение, которое [**глклеар**](glclear.md) использует для очистки буферов цветов.</span><span class="sxs-lookup"><span data-stu-id="cbf45-109">The red value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="cbf45-110">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cbf45-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="cbf45-111">*зеленого*</span><span class="sxs-lookup"><span data-stu-id="cbf45-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf45-112">Зеленое значение, которое [**глклеар**](glclear.md) использует для очистки буферов цветов.</span><span class="sxs-lookup"><span data-stu-id="cbf45-112">The green value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="cbf45-113">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cbf45-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="cbf45-114">*выделен*</span><span class="sxs-lookup"><span data-stu-id="cbf45-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf45-115">Синее значение, которое [**глклеар**](glclear.md) использует для очистки буферов цветов.</span><span class="sxs-lookup"><span data-stu-id="cbf45-115">The blue value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="cbf45-116">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cbf45-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="cbf45-117">*буквы*</span><span class="sxs-lookup"><span data-stu-id="cbf45-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="cbf45-118">Альфа-значение, используемое [**глклеар**](glclear.md) для очистки буферов цветов.</span><span class="sxs-lookup"><span data-stu-id="cbf45-118">The alpha value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="cbf45-119">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="cbf45-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf45-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbf45-120">Return value</span></span>

<span data-ttu-id="cbf45-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cbf45-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbf45-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cbf45-122">Error codes</span></span>

<span data-ttu-id="cbf45-123">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="cbf45-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cbf45-124">Имя</span><span class="sxs-lookup"><span data-stu-id="cbf45-124">Name</span></span>                                                                                                  | <span data-ttu-id="cbf45-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cbf45-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbf45-126"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbf45-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cbf45-127">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cbf45-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cbf45-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbf45-128">Remarks</span></span>

<span data-ttu-id="cbf45-129">Функция **глклеарколор** задает красный, зеленый, синий и альфа-значения, используемые [**глклеар**](glclear.md) для очистки буферов цветов.</span><span class="sxs-lookup"><span data-stu-id="cbf45-129">The **glClearColor** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the color buffers.</span></span> <span data-ttu-id="cbf45-130">Значения, заданные параметром **глклеарколор** , записываются в диапазон \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="cbf45-130">Values specified by **glClearColor** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="cbf45-131">Следующие функции извлекают сведения, относящиеся к функции **глклеарколор** :</span><span class="sxs-lookup"><span data-stu-id="cbf45-131">The following functions retrieve information related to the **glClearColor** function:</span></span>

<span data-ttu-id="cbf45-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ « \_ Удаление накопленной \_ стоимости GL»</span><span class="sxs-lookup"><span data-stu-id="cbf45-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="cbf45-133">**глжет** с аргументом \_ " \_ очистить \_ значение цвета GL"</span><span class="sxs-lookup"><span data-stu-id="cbf45-133">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf45-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cbf45-134">Requirements</span></span>



| <span data-ttu-id="cbf45-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cbf45-135">Requirement</span></span> | <span data-ttu-id="cbf45-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cbf45-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf45-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbf45-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf45-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cbf45-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cbf45-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbf45-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf45-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cbf45-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cbf45-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cbf45-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbf45-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf45-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cbf45-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbf45-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="cbf45-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbf45-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cbf45-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cbf45-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbf45-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbf45-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf45-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbf45-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf45-148">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="cbf45-148">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cbf45-149">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="cbf45-149">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="cbf45-150">**гленд**</span><span class="sxs-lookup"><span data-stu-id="cbf45-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cbf45-151">**глжет**</span><span class="sxs-lookup"><span data-stu-id="cbf45-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





