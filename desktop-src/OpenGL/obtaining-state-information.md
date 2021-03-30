---
title: Получение сведений о состоянии
description: Получение сведений о состоянии
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, сведения о состоянии
- OpenGL, переменные состояния
- сведения о состоянии OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775254"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="b96e7-106">Получение сведений о состоянии</span><span class="sxs-lookup"><span data-stu-id="b96e7-106">Obtaining State Information</span></span>

<span data-ttu-id="b96e7-107">OpenGL поддерживает множество переменных состояния, влияющих на поведение многих функций.</span><span class="sxs-lookup"><span data-stu-id="b96e7-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="b96e7-108">Некоторые из этих переменных имеют специализированные функции запросов.</span><span class="sxs-lookup"><span data-stu-id="b96e7-108">Some of these variables have specialized query functions.</span></span>



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="b96e7-109">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="b96e7-109">**glGetClipPlane**</span></span>](glgetclipplane.md) | [<span data-ttu-id="b96e7-110">**глжетпикселмап**</span><span class="sxs-lookup"><span data-stu-id="b96e7-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)             | [<span data-ttu-id="b96e7-111">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="b96e7-111">**glGetTexImage**</span></span>](glgetteximage.md)                   |
| [<span data-ttu-id="b96e7-112">**глжетлигхт**</span><span class="sxs-lookup"><span data-stu-id="b96e7-112">**glGetLight**</span></span>](glgetlight.md)         | [<span data-ttu-id="b96e7-113">**глжетполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="b96e7-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | [<span data-ttu-id="b96e7-114">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="b96e7-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |
| [<span data-ttu-id="b96e7-115">**глжетмап**</span><span class="sxs-lookup"><span data-stu-id="b96e7-115">**glGetMap**</span></span>](glgetmap.md)             | [<span data-ttu-id="b96e7-116">**глжеттексенв**</span><span class="sxs-lookup"><span data-stu-id="b96e7-116">**glGetTexEnv**</span></span>](glgettexenv.md)                 | [<span data-ttu-id="b96e7-117">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="b96e7-117">**glGetTexParameter**</span></span>](glgettexparameter.md)           |
| [<span data-ttu-id="b96e7-118">**глжетматериал**</span><span class="sxs-lookup"><span data-stu-id="b96e7-118">**glGetMaterial**</span></span>](glgetmaterial.md)   | [<span data-ttu-id="b96e7-119">**глжеттексжен**</span><span class="sxs-lookup"><span data-stu-id="b96e7-119">**glGetTexGen**</span></span>](glgettexgen.md)                 |                                                          |



 

<span data-ttu-id="b96e7-120">Чтобы получить значения других переменных состояния, используйте [**глжетбулеанв**](glgetbooleanv.md), [**глжетдаублев**](glgetdoublev.md), [**глжетфлоатв**](glgetfloatv.md)или [**глжетинтежерв**](glgetintegerv.md), если это уместно.</span><span class="sxs-lookup"><span data-stu-id="b96e7-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="b96e7-121">Сведения об использовании этих функций см. в разделе [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="b96e7-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="b96e7-122">Другие функции запросов, которые вы можете использовать, — [**глжетеррор**](glgeterror.md), [**глжетстринг**](glgetstring.md)и [**глисенаблед**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="b96e7-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="b96e7-123">(Дополнительные сведения о функциях, связанных с обработкой ошибок, см. в разделе [Обработка ошибок](handling-errors.md) .) Чтобы сохранить и восстановить наборы переменных состояния, используйте [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="b96e7-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="b96e7-124">Использование функций запросов</span><span class="sxs-lookup"><span data-stu-id="b96e7-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="b96e7-125">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="b96e7-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="b96e7-126">Коды ошибок OpenGL</span><span class="sxs-lookup"><span data-stu-id="b96e7-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="b96e7-127">Сохранение и восстановление наборов переменных состояния</span><span class="sxs-lookup"><span data-stu-id="b96e7-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="b96e7-128">Переменные состояния OpenGL</span><span class="sxs-lookup"><span data-stu-id="b96e7-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="b96e7-129">Справочник по сведениям о состоянии</span><span class="sxs-lookup"><span data-stu-id="b96e7-129">State Information Reference</span></span>](state-information-reference.md)

 

 




