---
title: Функция Глунурбскаллбакк (GLU. h)
description: Функция Глунурбскаллбакк определяет обратный вызов для неравномерного рационального объекта B-сплайна (НУРБС).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- Функция Глунурбскаллбакк OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672561"
---
# <a name="glunurbscallback-function"></a><span data-ttu-id="82583-104">Функция Глунурбскаллбакк</span><span class="sxs-lookup"><span data-stu-id="82583-104">gluNurbsCallback function</span></span>

<span data-ttu-id="82583-105">Функция **глунурбскаллбакк** определяет обратный вызов для неравномерного рационального объекта B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="82583-105">The **gluNurbsCallback** function defines a callback for a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="82583-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82583-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="82583-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="82583-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82583-108">*нобж*</span><span class="sxs-lookup"><span data-stu-id="82583-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="82583-109">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="82583-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="82583-110">*какую*</span><span class="sxs-lookup"><span data-stu-id="82583-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="82583-111">Определяемый обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="82583-111">The callback being defined.</span></span> <span data-ttu-id="82583-112">Единственное допустимое значение — GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="82583-112">The only valid value is GLU\_ERROR.</span></span> <span data-ttu-id="82583-113">Значение \_ ошибки Glu означает, что функция error вызывается при обнаружении ошибки.</span><span class="sxs-lookup"><span data-stu-id="82583-113">The meaning of GLU\_ERROR means that the error function is called when an error is encountered.</span></span> <span data-ttu-id="82583-114">Его единственный аргумент имеет тип **гленум** и указывает конкретную ошибку, которая возникла.</span><span class="sxs-lookup"><span data-stu-id="82583-114">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="82583-115">Существует 37 ошибок, уникальных для НУРБС, с именем GLU \_ нурбс \_ ERROR1 до Glu \_ нурбс \_ ERROR37.</span><span class="sxs-lookup"><span data-stu-id="82583-115">There are 37 errors unique to NURBS, named GLU\_NURBS\_ERROR1 through GLU\_NURBS\_ERROR37.</span></span> <span data-ttu-id="82583-116">Символьные строки, описывающие эти ошибки, можно получить с помощью [**глуеррорстринг**](gluerrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="82583-116">Character strings describing these errors can be retrieved with [**gluErrorString**](gluerrorstring.md).</span></span>

</dd> <dt>

<span data-ttu-id="82583-117">*FN*</span><span class="sxs-lookup"><span data-stu-id="82583-117">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="82583-118">Указатель на функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="82583-118">A pointer to the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82583-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82583-119">Return value</span></span>

<span data-ttu-id="82583-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="82583-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82583-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82583-121">Remarks</span></span>

<span data-ttu-id="82583-122">Используйте **глунурбскаллбакк** для определения обратного вызова, который будет использоваться объектом нурбс.</span><span class="sxs-lookup"><span data-stu-id="82583-122">Use **gluNurbsCallback** to define a callback to be used by a NURBS object.</span></span> <span data-ttu-id="82583-123">Если указанный обратный вызов уже определен, он заменяется.</span><span class="sxs-lookup"><span data-stu-id="82583-123">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="82583-124">Если *fn* имеет **значение NULL**, то любой существующий обратный вызов удаляется.</span><span class="sxs-lookup"><span data-stu-id="82583-124">If *fn* is **NULL**, then any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="82583-125">Требования</span><span class="sxs-lookup"><span data-stu-id="82583-125">Requirements</span></span>



| <span data-ttu-id="82583-126">Требование</span><span class="sxs-lookup"><span data-stu-id="82583-126">Requirement</span></span> | <span data-ttu-id="82583-127">Значение</span><span class="sxs-lookup"><span data-stu-id="82583-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82583-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82583-128">Minimum supported client</span></span><br/> | <span data-ttu-id="82583-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82583-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="82583-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82583-130">Minimum supported server</span></span><br/> | <span data-ttu-id="82583-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="82583-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="82583-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="82583-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="82583-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="82583-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="82583-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82583-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="82583-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82583-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="82583-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82583-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82583-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82583-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82583-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82583-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82583-139">**глуеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="82583-139">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="82583-140">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="82583-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





