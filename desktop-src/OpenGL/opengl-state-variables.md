---
title: Переменные состояния OpenGL
description: В следующих разделах перечислены имена переменных состояния, которые можно запросить.
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Переменные состояния OpenGL
- переменные состояния, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661558"
---
# <a name="opengl-state-variables"></a><span data-ttu-id="2eb86-105">Переменные состояния OpenGL</span><span class="sxs-lookup"><span data-stu-id="2eb86-105">OpenGL State Variables</span></span>

<span data-ttu-id="2eb86-106">В следующих разделах перечислены имена переменных состояния, которые можно запрашивать:</span><span class="sxs-lookup"><span data-stu-id="2eb86-106">The following topics list the names of state variables that can be queried:</span></span>

-   [<span data-ttu-id="2eb86-107">**Переменные состояния для текущих значений и связанных данных**</span><span class="sxs-lookup"><span data-stu-id="2eb86-107">**State Variables for Current Values and Associated Data**</span></span>](state-variables-for-current-values-and-associated-data.md)
-   [<span data-ttu-id="2eb86-108">**Переменные состояния преобразования**</span><span class="sxs-lookup"><span data-stu-id="2eb86-108">**Transformation State Variables**</span></span>](transformation-state-variables.md)
-   [<span data-ttu-id="2eb86-109">**Переменные состояния цвета**</span><span class="sxs-lookup"><span data-stu-id="2eb86-109">**Coloring State Variables**</span></span>](coloring-state-variables.md)
-   [<span data-ttu-id="2eb86-110">**Переменные состояния освещения**</span><span class="sxs-lookup"><span data-stu-id="2eb86-110">**Lighting State Variables**</span></span>](lighting-state-variables.md)
-   [<span data-ttu-id="2eb86-111">**Переменные состояния растрирования**</span><span class="sxs-lookup"><span data-stu-id="2eb86-111">**Rasterization State Variables**</span></span>](rasterization-state-variables.md)
-   [<span data-ttu-id="2eb86-112">**Текстурирование переменных состояния**</span><span class="sxs-lookup"><span data-stu-id="2eb86-112">**Texturing State Variables**</span></span>](texturing-state-variables.md)
-   [<span data-ttu-id="2eb86-113">**Операции с пикселами**</span><span class="sxs-lookup"><span data-stu-id="2eb86-113">**Pixel Operations**</span></span>](pixel-operations.md)
-   [<span data-ttu-id="2eb86-114">**Переменные состояния элемента управления буфера кадров**</span><span class="sxs-lookup"><span data-stu-id="2eb86-114">**Framebuffer Control State Variables**</span></span>](framebuffer-control-state-variables.md)
-   [<span data-ttu-id="2eb86-115">**Переменные состояния пикселей**</span><span class="sxs-lookup"><span data-stu-id="2eb86-115">**Pixel State Variables**</span></span>](pixel-state-variables.md)
-   [<span data-ttu-id="2eb86-116">**Переменные состояния оценщика**</span><span class="sxs-lookup"><span data-stu-id="2eb86-116">**Evaluator State Variables**</span></span>](evaluator-state-variables.md)
-   [<span data-ttu-id="2eb86-117">**Переменные состояния подсказки**</span><span class="sxs-lookup"><span data-stu-id="2eb86-117">**Hint State Variables**</span></span>](hint-state-variables.md)
-   [<span data-ttu-id="2eb86-118">**Переменные состояния, зависящие от реализации**</span><span class="sxs-lookup"><span data-stu-id="2eb86-118">**Implementation-Dependent State Variables**</span></span>](implementation-dependent-state-variables.md)
-   [<span data-ttu-id="2eb86-119">**Зависимые от реализации переменные состояния Pixel-Depth**</span><span class="sxs-lookup"><span data-stu-id="2eb86-119">**Implementation-Dependent Pixel-Depth State Variables**</span></span>](implementation-dependent-pixel-depth-state-variables.md)
-   [<span data-ttu-id="2eb86-120">**Переменные состояния "Разное"**</span><span class="sxs-lookup"><span data-stu-id="2eb86-120">**Miscellaneous State Variables**</span></span>](miscellaneous-state-variables.md)

<span data-ttu-id="2eb86-121">Для каждой переменной в разделе содержится описание, группа атрибутов, начальное или минимальное значение, а также предлагаемая [**функция \* глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) , используемая для ее получения.</span><span class="sxs-lookup"><span data-stu-id="2eb86-121">For each variable, the topic lists a description, attribute group, initial or minimum value, and the suggested [**glGet\***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) function to use for obtaining it.</span></span>

<span data-ttu-id="2eb86-122">Переменные состояния, которые можно получить с помощью [**глжетбулеанв**](glgetbooleanv.md), [**глжетинтежерв**](glgetintegerv.md), [**глжетфлоатв**](glgetfloatv.md)или [**глжетдаублев**](glgetdoublev.md) , перечислены только в одном из этих функтионссе, наиболее подходящем для типа возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="2eb86-122">State variables that you can obtain using [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetDoublev**](glgetdoublev.md) are listed with just one of these functionsthe one that is most appropriate for the type of data to be returned.</span></span> <span data-ttu-id="2eb86-123">Эти переменные состояния нельзя получить с помощью [**глисенаблед**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="2eb86-123">You cannot obtain these state variables using [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="2eb86-124">Однако можно получить переменные состояния, для которых **глисенаблед** указан в качестве функции запроса с **глжетбулеанв**, **глжетинтежерв**, **глжетфлоатв** и **глжетдаублев**.</span><span class="sxs-lookup"><span data-stu-id="2eb86-124">However, you can obtain state variables for which **glIsEnabled** is listed as the query function with **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv**, and **glGetDoublev**.</span></span> <span data-ttu-id="2eb86-125">Можно получить переменные состояния, для которых любая другая функция указана как функция запроса только с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="2eb86-125">You can obtain state variables for which any other function is listed as the query function only by using that function.</span></span> <span data-ttu-id="2eb86-126">Если группа атрибутов не указана, переменная не принадлежит ни к одной группе.</span><span class="sxs-lookup"><span data-stu-id="2eb86-126">If no attribute group is listed, the variable doesn't belong to any group.</span></span> <span data-ttu-id="2eb86-127">Все переменные состояния, которые можно запрашивать, за исключением тех, которые являются зависимыми от реализации, имеют начальные значения.</span><span class="sxs-lookup"><span data-stu-id="2eb86-127">All state variables that you can query, except those that are implementation dependent, have initial values.</span></span> <span data-ttu-id="2eb86-128">Чтобы определить начальное значение переменной, для которой не указано начальное значение, см. раздел ссылка на эту переменную или</span><span class="sxs-lookup"><span data-stu-id="2eb86-128">To determine the initial value of a variable for which no initial value is listed, see that variable's reference or the</span></span>

<span data-ttu-id="2eb86-129">*Справочное руководство по OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="2eb86-129">*OpenGL Reference Manual*.</span></span>

 

 




