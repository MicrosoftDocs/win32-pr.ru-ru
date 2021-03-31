---
title: Функция Глужетнурбспроперти (GLU. h)
description: Функция Глужетнурбспроперти возвращает неравномерное рациональное свойство B-сплайна (НУРБС).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- Функция Глужетнурбспроперти OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135659"
---
# <a name="glugetnurbsproperty-function"></a><span data-ttu-id="2b2c7-104">Функция Глужетнурбспроперти</span><span class="sxs-lookup"><span data-stu-id="2b2c7-104">gluGetNurbsProperty function</span></span>

<span data-ttu-id="2b2c7-105">Функция **глужетнурбспроперти** возвращает неравномерное рациональное свойство B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="2b2c7-105">The **gluGetNurbsProperty** function gets a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b2c7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b2c7-106">Syntax</span></span>


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a><span data-ttu-id="2b2c7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b2c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b2c7-108">*нобж*</span><span class="sxs-lookup"><span data-stu-id="2b2c7-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="2b2c7-109">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="2b2c7-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2b2c7-110">*property*</span><span class="sxs-lookup"><span data-stu-id="2b2c7-110">*property*</span></span> 
</dt> <dd>

<span data-ttu-id="2b2c7-111">Свойство, значение которого необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="2b2c7-112">Допустимы следующие значения: допустимость \_ выборки Glu \_ , \_ режим экрана Glu \_ , GLUное извлечение \_ , Glu \_ автоматической \_ загрузки \_ матрицы, \_ GLU \_ нечувствительность, \_ Glu \_ метод выборки, Glu \_ U \_ Step и Glu \_ V \_ Step.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-112">The following values are valid: GLU\_SAMPLING\_TOLERANCE, GLU\_DISPLAY\_MODE, GLU\_CULLING, GLU\_AUTO\_LOAD\_MATRIX, GLU\_PARAMETRIC\_TOLERANCE, GLU\_SAMPLING\_METHOD, GLU\_U\_STEP, and GLU\_V\_STEP.</span></span>

</dd> <dt>

<span data-ttu-id="2b2c7-113">*value*</span><span class="sxs-lookup"><span data-stu-id="2b2c7-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="2b2c7-114">Указатель на расположение, в которое записывается значение именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-114">A pointer to the location into which the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b2c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b2c7-115">Return value</span></span>

<span data-ttu-id="2b2c7-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2c7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b2c7-117">Remarks</span></span>

<span data-ttu-id="2b2c7-118">Используйте **глужетнурбспроперти** для получения свойств, хранящихся в объекте нурбс.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-118">Use **gluGetNurbsProperty** to retrieve properties stored in a NURBS object.</span></span> <span data-ttu-id="2b2c7-119">Эти свойства влияют на способ отрисовки НУРБС кривых и поверхностей.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-119">These properties affect the way NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="2b2c7-120">Дополнительные сведения о свойствах НУРБС см. в разделе [**глунурбспроперти**](glunurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="2b2c7-120">For information about NURBS properties, see [**gluNurbsProperty**](glunurbsproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2c7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2b2c7-121">Requirements</span></span>



| <span data-ttu-id="2b2c7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2b2c7-122">Requirement</span></span> | <span data-ttu-id="2b2c7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2b2c7-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2c7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b2c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2b2c7-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b2c7-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2b2c7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b2c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2b2c7-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b2c7-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2b2c7-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b2c7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b2c7-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b2c7-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="2b2c7-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b2c7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b2c7-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b2c7-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b2c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2b2c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b2c7-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b2c7-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b2c7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b2c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2c7-135">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-135">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="2b2c7-136">**глунурбспроперти**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-136">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





