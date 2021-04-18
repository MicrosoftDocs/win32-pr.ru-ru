---
title: Функция Глуунпрожект (GLU. h)
description: Функция Глуунпрожект сопоставляет координаты окна с координатами объекта.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- Функция Глуунпрожект OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682100"
---
# <a name="gluunproject-function"></a><span data-ttu-id="9f199-104">Функция Глуунпрожект</span><span class="sxs-lookup"><span data-stu-id="9f199-104">gluUnProject function</span></span>

<span data-ttu-id="9f199-105">Функция **глуунпрожект** сопоставляет координаты окна с координатами объекта.</span><span class="sxs-lookup"><span data-stu-id="9f199-105">The **gluUnProject** function maps window coordinates to object coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f199-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f199-106">Syntax</span></span>


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a><span data-ttu-id="9f199-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f199-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f199-108">*винкс*</span><span class="sxs-lookup"><span data-stu-id="9f199-108">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-109">Координата окна x для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9f199-109">The x window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="9f199-110">*вини*</span><span class="sxs-lookup"><span data-stu-id="9f199-110">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-111">Координата окна y для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9f199-111">The y window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="9f199-112">*винз*</span><span class="sxs-lookup"><span data-stu-id="9f199-112">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-113">Координата окна z для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9f199-113">The z window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="9f199-114">*моделматрикс*</span><span class="sxs-lookup"><span data-stu-id="9f199-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-115">Матрица моделвиев (как в вызове [**глжетдаублев**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="9f199-115">The modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="9f199-116">*прожматрикс*</span><span class="sxs-lookup"><span data-stu-id="9f199-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-117">Матрица проекции (как в вызове **глжетдаублев** ).</span><span class="sxs-lookup"><span data-stu-id="9f199-117">The projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="9f199-118">*просмотра*</span><span class="sxs-lookup"><span data-stu-id="9f199-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-119">Окно просмотра (как в вызове [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="9f199-119">The viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="9f199-120">*обжкс*</span><span class="sxs-lookup"><span data-stu-id="9f199-120">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-121">Координата вычисленного объекта x.</span><span class="sxs-lookup"><span data-stu-id="9f199-121">The computed x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9f199-122">*обжи*</span><span class="sxs-lookup"><span data-stu-id="9f199-122">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-123">Координата вычисленного объекта y.</span><span class="sxs-lookup"><span data-stu-id="9f199-123">The computed y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9f199-124">*обжз*</span><span class="sxs-lookup"><span data-stu-id="9f199-124">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="9f199-125">Объектная координата вычисленного z.</span><span class="sxs-lookup"><span data-stu-id="9f199-125">The computed z object coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f199-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f199-126">Return value</span></span>

<span data-ttu-id="9f199-127">Если функция выполнена удачно, возвращается значение GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="9f199-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="9f199-128">Если функция завершается ошибкой, возвращается значение GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="9f199-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f199-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f199-129">Remarks</span></span>

<span data-ttu-id="9f199-130">Функция **глуунпрожект** сопоставляет указанные координаты окна с координатами объекта с помощью *моделматрикс*, *прожматрикс* и *окна просмотра*.</span><span class="sxs-lookup"><span data-stu-id="9f199-130">The **gluUnProject** function maps the specified window coordinates into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="9f199-131">Результат сохраняется в *обжкс*, *обжи* и *обжз*.</span><span class="sxs-lookup"><span data-stu-id="9f199-131">The result is stored in *objx*, *objy*, and *objz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f199-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9f199-132">Requirements</span></span>



| <span data-ttu-id="9f199-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9f199-133">Requirement</span></span> | <span data-ttu-id="9f199-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9f199-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9f199-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f199-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9f199-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f199-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9f199-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f199-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9f199-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f199-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9f199-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f199-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f199-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f199-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9f199-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f199-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f199-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f199-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f199-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9f199-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f199-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f199-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f199-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f199-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f199-146">**глжет**</span><span class="sxs-lookup"><span data-stu-id="9f199-146">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9f199-147">**глжетдаублев**</span><span class="sxs-lookup"><span data-stu-id="9f199-147">**glGetDoublev**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9f199-148">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="9f199-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9f199-149">**глупрожект**</span><span class="sxs-lookup"><span data-stu-id="9f199-149">**gluProject**</span></span>](gluproject.md)
</dt> </dl>

 

 





