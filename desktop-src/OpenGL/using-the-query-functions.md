---
title: Использование функций запросов
description: Использование функций запросов
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, функции запросов
- функции запросов OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661572"
---
# <a name="using-the-query-functions"></a><span data-ttu-id="3d64d-105">Использование функций запросов</span><span class="sxs-lookup"><span data-stu-id="3d64d-105">Using the Query Functions</span></span>

<span data-ttu-id="3d64d-106">Существует четыре функции запроса для получения простых переменных состояния и один для определения того, включено или отключено определенное состояние:</span><span class="sxs-lookup"><span data-stu-id="3d64d-106">There are four query functions for obtaining simple state variables and one for determining whether a particular state is enabled or disabled:</span></span>

-   [<span data-ttu-id="3d64d-107">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="3d64d-107">**glGetBooleanv**</span></span>](glgetbooleanv.md)
-   [<span data-ttu-id="3d64d-108">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="3d64d-108">**glGetIntegerv**</span></span>](glgetintegerv.md)
-   [<span data-ttu-id="3d64d-109">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="3d64d-109">**glGetFloatv**</span></span>](glgetfloatv.md)
-   [<span data-ttu-id="3d64d-110">**глжетдаублев**</span><span class="sxs-lookup"><span data-stu-id="3d64d-110">**glGetDoublev**</span></span>](glgetdoublev.md)
-   [<span data-ttu-id="3d64d-111">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="3d64d-111">**glIsEnabled**</span></span>](glisenabled.md)

<span data-ttu-id="3d64d-112">Ниже приведены прототипы для функций запросов.</span><span class="sxs-lookup"><span data-stu-id="3d64d-112">The prototypes for the query functions are:</span></span>

<span data-ttu-id="3d64d-113">**void** **глжетбулеанв**(**гленум** *pname* , **глбулеан \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="3d64d-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span></span>

<span data-ttu-id="3d64d-114">**void** **глжетинтежерв**(**гленум** *pname* , **глинт \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="3d64d-114">**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \*** *params* );</span></span>

<span data-ttu-id="3d64d-115">**void** **глжетфлоатв**(**гленум** *pname* , **глфлоат \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="3d64d-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span></span>

<span data-ttu-id="3d64d-116">**void** **глжетдаублев**(**гленум** *pname* , **глдаубле \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="3d64d-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span></span>

<span data-ttu-id="3d64d-117">Соответственно, функции запросов получают переменные состояния Boolean, Integer, с плавающей запятой или значения двойной точности.</span><span class="sxs-lookup"><span data-stu-id="3d64d-117">Respectively, the query functions obtain Boolean, integer, floating-point, or double-precision state variables.</span></span> <span data-ttu-id="3d64d-118">Параметр *pname* является символьной константой, указывающей на возвращаемую переменную состояния, а *params* — это указатель на массив указанного типа, в который следует поместить возвращаемые данные.</span><span class="sxs-lookup"><span data-stu-id="3d64d-118">The *pname* parameter is a symbolic constant indicating the state variable to return, and *params* is a pointer to an array of the indicated type in which to place the returned data.</span></span> <span data-ttu-id="3d64d-119">Возможные значения для *pname* перечислены в [переменных состояния OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="3d64d-119">The possible values for *pname* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span> <span data-ttu-id="3d64d-120">Преобразование типа выполняется, если необходимо вернуть требуемую переменную в качестве запрошенного типа данных.</span><span class="sxs-lookup"><span data-stu-id="3d64d-120">A type conversion is performed if necessary to return the desired variable as the requested data type.</span></span>

<span data-ttu-id="3d64d-121">Прототип для [**глисенаблед**](glisenabled.md) :</span><span class="sxs-lookup"><span data-stu-id="3d64d-121">The prototype for [**glIsEnabled**](glisenabled.md) is:</span></span>

<span data-ttu-id="3d64d-122">**Глбулеан** **глисенаблед**(гленум *Cap* );</span><span class="sxs-lookup"><span data-stu-id="3d64d-122">**GLboolean** **glIsEnabled**(GLenum *cap* );</span></span>

<span data-ttu-id="3d64d-123">Если включен режим, заданный параметром *Cap* , **ГЛИСЕНАБЛЕД** возвращает \_ значение GL true.</span><span class="sxs-lookup"><span data-stu-id="3d64d-123">If the mode specified by *cap* is enabled, **glIsEnabled** returns GL\_TRUE.</span></span> <span data-ttu-id="3d64d-124">Если режим, заданный параметром *Cap* , отключен, **ГЛИСЕНАБЛЕД** возвращает \_ значение ГК false.</span><span class="sxs-lookup"><span data-stu-id="3d64d-124">If the mode specified by *cap* is disabled, **glIsEnabled** returns GL\_FALSE.</span></span> <span data-ttu-id="3d64d-125">Возможные значения для *Cap* перечислены в [переменных состояния OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="3d64d-125">The possible values for *cap* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span>

<span data-ttu-id="3d64d-126">Другие специализированные функции возвращают определенные переменные состояния.</span><span class="sxs-lookup"><span data-stu-id="3d64d-126">Other specialized functions return specific state variables.</span></span> <span data-ttu-id="3d64d-127">Чтобы узнать, когда использовать эти функции, см. раздел переменные состояния OpenGL и *справочное руководство по OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="3d64d-127">To find out when to use these functions, see OpenGL State Variables and the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="3d64d-128">Дополнительные сведения о средстве обработки ошибок OpenGL и функции **глжетеррор** см. в разделе [Обработка ошибок](error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="3d64d-128">For more information on OpenGL's error handling facility and the **glGetError** function, see [Error Handling](error-handling.md).</span></span>

<span data-ttu-id="3d64d-129">Функции, возвращающие определенные переменные состояния:</span><span class="sxs-lookup"><span data-stu-id="3d64d-129">The functions that return specific state variables are:</span></span>

-   [<span data-ttu-id="3d64d-130">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="3d64d-130">**glGetClipPlane**</span></span>](glgetclipplane.md)
-   [<span data-ttu-id="3d64d-131">**глжетеррор**</span><span class="sxs-lookup"><span data-stu-id="3d64d-131">**glGetError**</span></span>](glgeterror.md)
-   [<span data-ttu-id="3d64d-132">**глжетлигхт**</span><span class="sxs-lookup"><span data-stu-id="3d64d-132">**glGetLight**</span></span>](glgetlight.md)
-   [<span data-ttu-id="3d64d-133">**глжетмап**</span><span class="sxs-lookup"><span data-stu-id="3d64d-133">**glGetMap**</span></span>](glgetmap.md)
-   [<span data-ttu-id="3d64d-134">**глжетматериал**</span><span class="sxs-lookup"><span data-stu-id="3d64d-134">**glGetMaterial**</span></span>](glgetmaterial.md)
-   [<span data-ttu-id="3d64d-135">**глжетпикселмап**</span><span class="sxs-lookup"><span data-stu-id="3d64d-135">**glGetPixelMap**</span></span>](glgetpixelmap.md)
-   [<span data-ttu-id="3d64d-136">**глжетполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="3d64d-136">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
-   [<span data-ttu-id="3d64d-137">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="3d64d-137">**glGetString**</span></span>](glgetstring.md)
-   [<span data-ttu-id="3d64d-138">**глжеттексенв**</span><span class="sxs-lookup"><span data-stu-id="3d64d-138">**glGetTexEnv**</span></span>](glgettexenv.md)
-   [<span data-ttu-id="3d64d-139">**глжеттексжен**</span><span class="sxs-lookup"><span data-stu-id="3d64d-139">**glGetTexGen**</span></span>](glgettexgen.md)
-   [<span data-ttu-id="3d64d-140">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="3d64d-140">**glGetTexImage**</span></span>](glgetteximage.md)
-   [<span data-ttu-id="3d64d-141">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="3d64d-141">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
-   [<span data-ttu-id="3d64d-142">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="3d64d-142">**glGetTexParameter**</span></span>](glgettexparameter.md)

 

 




