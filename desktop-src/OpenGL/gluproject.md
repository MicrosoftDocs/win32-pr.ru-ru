---
title: Функция Глупрожект (GLU. h)
description: Функция Глупрожект сопоставляет координаты объектов с координатами окна.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- Функция Глупрожект OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491916"
---
# <a name="gluproject-function"></a><span data-ttu-id="30375-104">Функция Глупрожект</span><span class="sxs-lookup"><span data-stu-id="30375-104">gluProject function</span></span>

<span data-ttu-id="30375-105">Функция **глупрожект** сопоставляет координаты объектов с координатами окна.</span><span class="sxs-lookup"><span data-stu-id="30375-105">The **gluProject** function maps object coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="30375-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30375-106">Syntax</span></span>


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a><span data-ttu-id="30375-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="30375-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30375-108">*обжкс*</span><span class="sxs-lookup"><span data-stu-id="30375-108">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-109">Координата объекта x.</span><span class="sxs-lookup"><span data-stu-id="30375-109">The x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="30375-110">*обжи*</span><span class="sxs-lookup"><span data-stu-id="30375-110">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-111">Координата объекта y.</span><span class="sxs-lookup"><span data-stu-id="30375-111">The y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="30375-112">*обжз*</span><span class="sxs-lookup"><span data-stu-id="30375-112">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-113">Координата объекта z.</span><span class="sxs-lookup"><span data-stu-id="30375-113">The z object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="30375-114">*моделматрикс*</span><span class="sxs-lookup"><span data-stu-id="30375-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-115">Текущая матрица моделвиев (как в вызове [**глжетдаублев**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="30375-115">The current modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="30375-116">*прожматрикс*</span><span class="sxs-lookup"><span data-stu-id="30375-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-117">Матрица текущей проекции (как в вызове **глжетдаублев** ).</span><span class="sxs-lookup"><span data-stu-id="30375-117">The current projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="30375-118">*просмотра*</span><span class="sxs-lookup"><span data-stu-id="30375-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-119">Текущее окно просмотра (как в вызове [**глжетинтежерв**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="30375-119">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="30375-120">*винкс*</span><span class="sxs-lookup"><span data-stu-id="30375-120">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-121">Координата вычисленного x окна.</span><span class="sxs-lookup"><span data-stu-id="30375-121">The computed x window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="30375-122">*вини*</span><span class="sxs-lookup"><span data-stu-id="30375-122">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-123">Координата окна вычисленного y.</span><span class="sxs-lookup"><span data-stu-id="30375-123">The computed y window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="30375-124">*винз*</span><span class="sxs-lookup"><span data-stu-id="30375-124">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="30375-125">Координата вычисленного z окна.</span><span class="sxs-lookup"><span data-stu-id="30375-125">The computed z window coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30375-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30375-126">Return value</span></span>

<span data-ttu-id="30375-127">Если функция выполнена удачно, возвращается значение GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="30375-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="30375-128">Если функция завершается ошибкой, возвращается значение GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="30375-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="30375-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30375-129">Remarks</span></span>

<span data-ttu-id="30375-130">Функция **глупрожект** Преобразует указанные координаты объекта в координаты окна с помощью *моделматрикс*, *прожматрикс* и *окна просмотра*.</span><span class="sxs-lookup"><span data-stu-id="30375-130">The **gluProject** function transforms the specified object coordinates into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="30375-131">Результат сохраняется в *Винкс*, *Вини* и *Винз*.</span><span class="sxs-lookup"><span data-stu-id="30375-131">The result is stored in *winx*, *winy*, and *winz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="30375-132">Требования</span><span class="sxs-lookup"><span data-stu-id="30375-132">Requirements</span></span>



| <span data-ttu-id="30375-133">Требование</span><span class="sxs-lookup"><span data-stu-id="30375-133">Requirement</span></span> | <span data-ttu-id="30375-134">Значение</span><span class="sxs-lookup"><span data-stu-id="30375-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30375-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30375-135">Minimum supported client</span></span><br/> | <span data-ttu-id="30375-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30375-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="30375-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30375-137">Minimum supported server</span></span><br/> | <span data-ttu-id="30375-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30375-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30375-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="30375-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="30375-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="30375-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="30375-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="30375-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="30375-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30375-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="30375-143">DLL</span><span class="sxs-lookup"><span data-stu-id="30375-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30375-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30375-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30375-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30375-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30375-146">**глжетдаублев**</span><span class="sxs-lookup"><span data-stu-id="30375-146">**glGetDoublev**</span></span>](glgetdoublev.md)
</dt> <dt>

[<span data-ttu-id="30375-147">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="30375-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="30375-148">**глуунпрожект**</span><span class="sxs-lookup"><span data-stu-id="30375-148">**gluUnProject**</span></span>](gluunproject.md)
</dt> </dl>

 

 





