---
title: Функция Глжетполигонстиппле (GL. h)
description: Функция Глжетполигонстиппле Возвращает шаблон стиппле многоугольника.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- Функция Глжетполигонстиппле OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891585"
---
# <a name="glgetpolygonstipple-function"></a><span data-ttu-id="8570b-104">Функция Глжетполигонстиппле</span><span class="sxs-lookup"><span data-stu-id="8570b-104">glGetPolygonStipple function</span></span>

<span data-ttu-id="8570b-105">Функция **глжетполигонстиппле** Возвращает шаблон стиппле многоугольника.</span><span class="sxs-lookup"><span data-stu-id="8570b-105">The **glGetPolygonStipple** function returns the polygon stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="8570b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8570b-106">Syntax</span></span>


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="8570b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8570b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8570b-108">*виде*</span><span class="sxs-lookup"><span data-stu-id="8570b-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="8570b-109">Возвращает шаблон стиппле.</span><span class="sxs-lookup"><span data-stu-id="8570b-109">Returns the stipple pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8570b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8570b-110">Return value</span></span>

<span data-ttu-id="8570b-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8570b-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8570b-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8570b-112">Error codes</span></span>

<span data-ttu-id="8570b-113">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="8570b-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8570b-114">Имя</span><span class="sxs-lookup"><span data-stu-id="8570b-114">Name</span></span>                                                                                                  | <span data-ttu-id="8570b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8570b-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8570b-116"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8570b-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8570b-117">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8570b-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8570b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8570b-118">Remarks</span></span>

<span data-ttu-id="8570b-119">Функция **глжетполигонстиппле** Возвращает шаблон стиппле размером 32x32 многоугольника с помощью параметра *Mask* .</span><span class="sxs-lookup"><span data-stu-id="8570b-119">The **glGetPolygonStipple** function returns a 32x32 polygon stipple pattern through the *mask* parameter.</span></span> <span data-ttu-id="8570b-120">Шаблон упаковывается в память, как если бы [**глреадпикселс**](glreadpixels.md) с *высотой* и *шириной* 32, *типом* \_ точечного рисунка GL и *форматом* индекса GL, \_ \_ а шаблон стиппле хранился во внутреннем буфере цветового индекса 32x32.</span><span class="sxs-lookup"><span data-stu-id="8570b-120">The pattern is packed into memory as if [**glReadPixels**](glreadpixels.md) with both *height* and *width* of 32, *type* of GL\_BITMAP, and *format* of GL\_COLOR\_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer.</span></span> <span data-ttu-id="8570b-121">Однако в отличие от **глреадпикселс**, операции перемещения пикселей (Shift, offset и Map) не применяются к возвращаемому изображению стиппле.</span><span class="sxs-lookup"><span data-stu-id="8570b-121">Unlike **glReadPixels**, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.</span></span>

<span data-ttu-id="8570b-122">Если возникает ошибка, содержимое *маски* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8570b-122">If an error is generated, no change is made to the contents of *mask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8570b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8570b-123">Requirements</span></span>



| <span data-ttu-id="8570b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8570b-124">Requirement</span></span> | <span data-ttu-id="8570b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8570b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8570b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8570b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8570b-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8570b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8570b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8570b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8570b-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8570b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8570b-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8570b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8570b-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8570b-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8570b-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8570b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="8570b-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8570b-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8570b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8570b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8570b-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8570b-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8570b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8570b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8570b-137">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="8570b-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8570b-138">**гленд**</span><span class="sxs-lookup"><span data-stu-id="8570b-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8570b-139">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="8570b-139">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="8570b-140">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="8570b-140">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="8570b-141">**глполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="8570b-141">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="8570b-142">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="8570b-142">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





