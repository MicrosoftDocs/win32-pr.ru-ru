---
title: Функция Глполигонстиппле (GL. h)
description: Функция Глполигонстиппле задает шаблон стипплинг многоугольника.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- Функция Глполигонстиппле OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491127"
---
# <a name="glpolygonstipple-function"></a><span data-ttu-id="befb8-104">Функция Глполигонстиппле</span><span class="sxs-lookup"><span data-stu-id="befb8-104">glPolygonStipple function</span></span>

<span data-ttu-id="befb8-105">Функция **глполигонстиппле** задает шаблон стипплинг многоугольника.</span><span class="sxs-lookup"><span data-stu-id="befb8-105">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="befb8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="befb8-106">Syntax</span></span>


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="befb8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="befb8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="befb8-108">*виде*</span><span class="sxs-lookup"><span data-stu-id="befb8-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="befb8-109">Указатель на шаблон размером 32x32 стиппле, который будет распакован из памяти таким же образом, как [**глдравпикселс**](gldrawpixels.md) распаковать Пиксели.</span><span class="sxs-lookup"><span data-stu-id="befb8-109">A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that [**glDrawPixels**](gldrawpixels.md) unpacks pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="befb8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="befb8-110">Return value</span></span>

<span data-ttu-id="befb8-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="befb8-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="befb8-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="befb8-112">Error codes</span></span>

<span data-ttu-id="befb8-113">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="befb8-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="befb8-114">Имя</span><span class="sxs-lookup"><span data-stu-id="befb8-114">Name</span></span>                                                                                                  | <span data-ttu-id="befb8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="befb8-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="befb8-116"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="befb8-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="befb8-117">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="befb8-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="befb8-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="befb8-118">Remarks</span></span>

<span data-ttu-id="befb8-119">Функция **глполигонстиппле** задает шаблон стипплинг многоугольника.</span><span class="sxs-lookup"><span data-stu-id="befb8-119">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span> <span data-ttu-id="befb8-120">Многоугольник стипплинг, как и Line стипплинг (см. [**гллинестиппле**](gllinestipple.md)), маскирует определенные фрагменты, созданные с помощью растрирования, создавая шаблон.</span><span class="sxs-lookup"><span data-stu-id="befb8-120">Polygon stippling, like line stippling (see [**glLineStipple**](gllinestipple.md)), masks out certain fragments produced by rasterization, creating a pattern.</span></span> <span data-ttu-id="befb8-121">Стипплинг не зависит от сглаживания многоугольников.</span><span class="sxs-lookup"><span data-stu-id="befb8-121">Stippling is independent of polygon antialiasing.</span></span>

<span data-ttu-id="befb8-122">Параметр *Mask* является указателем на шаблон размером 32x32 стиппле, который хранится в памяти, так же, как данные пикселей, передаваемые в **глдравпикселс** с *высотой* и *шириной* , равной 32, *Формат* пикселей для \_ индекса цвета GL \_ и *тип* данных \_ точечного рисунка GL.</span><span class="sxs-lookup"><span data-stu-id="befb8-122">The *mask* parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to **glDrawPixels** with *height* and *width* both equal to 32, a pixel *format* of GL\_COLOR\_INDEX, and data *type* of GL\_BITMAP.</span></span> <span data-ttu-id="befb8-123">Таким образом, шаблон стиппле представляется в виде массива размером 32 x 1-разрядных индексов цвета, упакованных в байты без знака.</span><span class="sxs-lookup"><span data-stu-id="befb8-123">That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes.</span></span> <span data-ttu-id="befb8-124">Параметры функции [**глпикселсторе**](glpixelstore-functions.md) , такие как GL \_ RePack \_ reswap \_ bytes и GL \_ RePack \_ ЛСБ, в \_ первую очередь влияют на сборку битов в шаблон стиппле.</span><span class="sxs-lookup"><span data-stu-id="befb8-124">The [**glPixelStore**](glpixelstore-functions.md) function parameters, such as GL\_UNPACK\_SWAP\_BYTES and GL\_UNPACK\_LSB\_FIRST, affect the assembling of the bits into a stipple pattern.</span></span> <span data-ttu-id="befb8-125">Однако операции перемещения пикселей (сдвиг, смещение и схема пикселей) не применяются к изображению стиппле.</span><span class="sxs-lookup"><span data-stu-id="befb8-125">Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.</span></span>

<span data-ttu-id="befb8-126">Многоугольник стипплинг включен и отключен с [**гленабле**](glenable.md) и **глдисабле** с использованием аргумента GL \_ Polygon \_ стиппле.</span><span class="sxs-lookup"><span data-stu-id="befb8-126">Polygon stippling is enabled and disabled with [**glEnable**](glenable.md) and **glDisable**, using argument GL\_POLYGON\_STIPPLE.</span></span> <span data-ttu-id="befb8-127">Если этот параметр включен, растровый фрагмент многоугольника с координатами окна *x*<sub>w</sub> и *y*<sub>w</sub> отправляется на следующий этап OpenGL только в том случае, если *бит (\*\*x*<sub>w</sub> <sub>Mod 32</sub> ) в строке шаблона стиппле имеет значение One.</span><span class="sxs-lookup"><span data-stu-id="befb8-127">If enabled, a rasterized polygon fragment with window coordinates *x*<sub>w</sub> and *y*<sub>w</sub> is sent to the next stage of OpenGL if and only if the (*x*<sub>w</sub> mod 32)th bit in the (*y*<sub>w</sub> mod 32)th row of the stipple pattern is one.</span></span> <span data-ttu-id="befb8-128">Если параметр Polygon стипплинг отключен, это так, как если бы шаблон стиппле был все.</span><span class="sxs-lookup"><span data-stu-id="befb8-128">When polygon stippling is disabled, it is as if the stipple pattern were all ones.</span></span>

<span data-ttu-id="befb8-129">Следующие функции извлекают сведения, относящиеся к **глполигонстиппле**:</span><span class="sxs-lookup"><span data-stu-id="befb8-129">The following functions retrieve information related to **glPolygonStipple**:</span></span>

[<span data-ttu-id="befb8-130">**глжетполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="befb8-130">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)

<span data-ttu-id="befb8-131">[**глисенаблед**](glisenabled.md) с аргументом GL \_ Polygon \_ стиппле</span><span class="sxs-lookup"><span data-stu-id="befb8-131">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="befb8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="befb8-132">Requirements</span></span>



| <span data-ttu-id="befb8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="befb8-133">Requirement</span></span> | <span data-ttu-id="befb8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="befb8-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="befb8-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="befb8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="befb8-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="befb8-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="befb8-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="befb8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="befb8-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="befb8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="befb8-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="befb8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="befb8-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="befb8-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="befb8-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="befb8-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="befb8-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="befb8-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="befb8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="befb8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="befb8-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="befb8-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befb8-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="befb8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befb8-146">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="befb8-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="befb8-147">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="befb8-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="befb8-148">**гленд**</span><span class="sxs-lookup"><span data-stu-id="befb8-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="befb8-149">**гллинестиппле**</span><span class="sxs-lookup"><span data-stu-id="befb8-149">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="befb8-150">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="befb8-150">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="befb8-151">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="befb8-151">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> </dl>

 

 





