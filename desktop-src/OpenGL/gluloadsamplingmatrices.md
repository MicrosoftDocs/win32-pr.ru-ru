---
title: Функция Глулоадсамплингматрицес (GLU. h)
description: Функция Глулоадсамплингматрицес загружает неоднородное рациональное распределение B-сплайна (НУРБС) и матрицы отбора.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- Функция Глулоадсамплингматрицес OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661859"
---
# <a name="gluloadsamplingmatrices-function"></a><span data-ttu-id="86e21-104">Функция Глулоадсамплингматрицес</span><span class="sxs-lookup"><span data-stu-id="86e21-104">gluLoadSamplingMatrices function</span></span>

<span data-ttu-id="86e21-105">Функция **глулоадсамплингматрицес** загружает неоднородное рациональное распределение B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)) и матрицы отбора.</span><span class="sxs-lookup"><span data-stu-id="86e21-105">The **gluLoadSamplingMatrices** function loads Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) sampling and culling matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e21-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86e21-106">Syntax</span></span>


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="86e21-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="86e21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e21-108">*нобж*</span><span class="sxs-lookup"><span data-stu-id="86e21-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="86e21-109">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="86e21-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="86e21-110">*моделматрикс*</span><span class="sxs-lookup"><span data-stu-id="86e21-110">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="86e21-111">Матрица моделвиев (как в вызове [**глжетфлоатв**](glgetfloatv.md) ).</span><span class="sxs-lookup"><span data-stu-id="86e21-111">A modelview matrix (as from a [**glGetFloatv**](glgetfloatv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="86e21-112">*прожматрикс*</span><span class="sxs-lookup"><span data-stu-id="86e21-112">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="86e21-113">Матрица проекции (как в вызове **глжетфлоатв** ).</span><span class="sxs-lookup"><span data-stu-id="86e21-113">A projection matrix (as from a **glGetFloatv** call).</span></span>

</dd> <dt>

<span data-ttu-id="86e21-114">*просмотра*</span><span class="sxs-lookup"><span data-stu-id="86e21-114">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="86e21-115">Окно просмотра (как в вызове [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="86e21-115">A viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e21-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86e21-116">Return value</span></span>

<span data-ttu-id="86e21-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="86e21-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e21-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86e21-118">Remarks</span></span>

<span data-ttu-id="86e21-119">Функция **глулоадсамплингматрицес** использует *моделматрикс*, *прожматрикс* и *окно просмотра* , чтобы повторно вычислить матрицы выборки и отбора, хранящиеся в *нобж*.</span><span class="sxs-lookup"><span data-stu-id="86e21-119">The **gluLoadSamplingMatrices** function uses *modelMatrix*, *projMatrix*, and *viewport* to recompute the sampling and culling matrices stored in *nobj*.</span></span> <span data-ttu-id="86e21-120">Матрица выборки определяет, насколько точно НУРБС кривую или поверхность, чтобы удовлетворить допуск выборки (как определено в \_ \_ свойстве допуска Glu выборки).</span><span class="sxs-lookup"><span data-stu-id="86e21-120">The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU\_SAMPLING\_TOLERANCE property).</span></span> <span data-ttu-id="86e21-121">Матрица отбора используется для принятия решения о том, следует ли исключать НУРБС кривую или поверхность до подготовки к просмотру (если включено свойство исходящего GLU \_ ).</span><span class="sxs-lookup"><span data-stu-id="86e21-121">The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU\_CULLING property is turned on).</span></span>

<span data-ttu-id="86e21-122">Функция **глулоадсамплингматрицес** необходима только в том случае, если \_ \_ свойство МАТРИЦы автоматической загрузки Glu отключено \_ (см. [**глунурбспроперти**](glunurbsproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="86e21-122">The **gluLoadSamplingMatrices** function is necessary only if the GLU\_AUTO\_LOAD\_MATRIX property is turned off (see [**gluNurbsProperty**](glunurbsproperty.md)).</span></span> <span data-ttu-id="86e21-123">Несмотря на то \_ \_ , что свойство матрицы автозагрузки Glu можно оставить \_ включенным, это требует кругового обращения к серверу OpenGL для получения текущих значений матрицы моделвиев, матрицы проекции и окна просмотра.)</span><span class="sxs-lookup"><span data-stu-id="86e21-123">Although it can be convenient to leave the GLU\_AUTO\_LOAD\_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)</span></span>

## <a name="requirements"></a><span data-ttu-id="86e21-124">Требования</span><span class="sxs-lookup"><span data-stu-id="86e21-124">Requirements</span></span>



| <span data-ttu-id="86e21-125">Требование</span><span class="sxs-lookup"><span data-stu-id="86e21-125">Requirement</span></span> | <span data-ttu-id="86e21-126">Значение</span><span class="sxs-lookup"><span data-stu-id="86e21-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="86e21-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86e21-127">Minimum supported client</span></span><br/> | <span data-ttu-id="86e21-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86e21-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="86e21-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86e21-129">Minimum supported server</span></span><br/> | <span data-ttu-id="86e21-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="86e21-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="86e21-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="86e21-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="86e21-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="86e21-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="86e21-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86e21-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="86e21-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86e21-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="86e21-135">DLL</span><span class="sxs-lookup"><span data-stu-id="86e21-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e21-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e21-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e21-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86e21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e21-138">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="86e21-138">**glGetFloatv**</span></span>](glgetfloatv.md)
</dt> <dt>

[<span data-ttu-id="86e21-139">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="86e21-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="86e21-140">**глужетнурбспроперти**</span><span class="sxs-lookup"><span data-stu-id="86e21-140">**gluGetNurbsProperty**</span></span>](glugetnurbsproperty.md)
</dt> <dt>

[<span data-ttu-id="86e21-141">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="86e21-141">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





