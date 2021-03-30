---
title: Указание обратных вызовов
description: Для тесселяции можно указать до пяти функций обратного вызова.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Служебная программа OpenGL (GLU), указание функций обратного вызова
- GLU (служебная программа OpenGL), указание функций обратного вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532414"
---
# <a name="specifying-callbacks"></a><span data-ttu-id="0f627-105">Указание обратных вызовов</span><span class="sxs-lookup"><span data-stu-id="0f627-105">Specifying Callbacks</span></span>

<span data-ttu-id="0f627-106">Для тесселяции можно указать до пяти функций обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0f627-106">You can specify up to five callback functions for a tessellation.</span></span> <span data-ttu-id="0f627-107">Любые функции, которые не были указаны, не вызываются во время тесселяции и не получают возвращаемые сведения.</span><span class="sxs-lookup"><span data-stu-id="0f627-107">Any functions that you do not specify are not called during the tessellation, and you do not get any information they might have returned.</span></span> <span data-ttu-id="0f627-108">Функции обратного вызова указываются с помощью [*глутесскаллбакк*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="0f627-108">You specify the callback functions with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="0f627-109">Функция **глутесскаллбакк** связывает функцию обратного вызова *fn* с объектом тесселяции *тессобж*.</span><span class="sxs-lookup"><span data-stu-id="0f627-109">The **gluTessCallback** function associates the callback function *fn* with the tessellation object *tessobj*.</span></span> <span data-ttu-id="0f627-110">Тип обратного вызова определяется *типом* параметра, который может быть **Glu \_ Begin**, **Glu, \_ \_ флагом границы**, **Glu \_ вершиной**, **Glu \_ End** или **Glu \_**.</span><span class="sxs-lookup"><span data-stu-id="0f627-110">The type of the callback is determined by the parameter *type*, which can be **GLU\_BEGIN**, **GLU\_EDGE\_FLAG**, **GLU\_VERTEX**, **GLU\_END**, or **GLU\_ERROR**.</span></span> <span data-ttu-id="0f627-111">Пять возможных функций обратного вызова имеют следующие прототипы.</span><span class="sxs-lookup"><span data-stu-id="0f627-111">The five possible callback functions have the following prototypes.</span></span>



| <span data-ttu-id="0f627-112">Функция обратного вызова</span><span class="sxs-lookup"><span data-stu-id="0f627-112">Callback function</span></span>   | <span data-ttu-id="0f627-113">Прототип</span><span class="sxs-lookup"><span data-stu-id="0f627-113">Prototype</span></span>                                    |
|---------------------|----------------------------------------------|
| <span data-ttu-id="0f627-114">**\_Начало Glu**</span><span class="sxs-lookup"><span data-stu-id="0f627-114">**GLU\_BEGIN**</span></span>      | <span data-ttu-id="0f627-115">**void** **Begin**(\**гленум \* \* \* Type* );</span><span class="sxs-lookup"><span data-stu-id="0f627-115">**void** **begin**(\**GLenum\*\*\*type* );</span></span>       |
| <span data-ttu-id="0f627-116">**\_флаг Glu ребра \_**</span><span class="sxs-lookup"><span data-stu-id="0f627-116">**GLU\_EDGE\_FLAG**</span></span> | <span data-ttu-id="0f627-117">**void** **Еджефлаг**(\**глбулеан \* \* \* флаг* );</span><span class="sxs-lookup"><span data-stu-id="0f627-117">**void** **edgeFlag**(\**GLboolean\*\*\*flag* );</span></span> |
| <span data-ttu-id="0f627-118">**\_вершина Glu**</span><span class="sxs-lookup"><span data-stu-id="0f627-118">**GLU\_VERTEX**</span></span>     | <span data-ttu-id="0f627-119">**void** **Vertex**(\**void \* \* \* \* Data* );</span><span class="sxs-lookup"><span data-stu-id="0f627-119">**void** **vertex**(\**void \*\*\*\*data* );</span></span>     |
| <span data-ttu-id="0f627-120">**GLU \_ конец**</span><span class="sxs-lookup"><span data-stu-id="0f627-120">**GLU\_END**</span></span>        | <span data-ttu-id="0f627-121"> **конец** void ( *void* );</span><span class="sxs-lookup"><span data-stu-id="0f627-121">**void** **end**( *void* );</span></span>                  |
| <span data-ttu-id="0f627-122">**GLU, \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="0f627-122">**GLU\_ERROR**</span></span>      | <span data-ttu-id="0f627-123">**void** **Error**(\*\*гленум \*\* \* \*);</span><span class="sxs-lookup"><span data-stu-id="0f627-123">**void** **error**(\**GLenum\*\*\*errno* );</span></span>      |



 

<span data-ttu-id="0f627-124">Чтобы изменить функцию обратного вызова, вызовите [*глутесскаллбакк*](glutess.md) с помощью новой функции.</span><span class="sxs-lookup"><span data-stu-id="0f627-124">To change a callback function, call [*gluTessCallback*](glutess.md) with the new function.</span></span> <span data-ttu-id="0f627-125">Чтобы исключить функцию обратного вызова, не заменяя ее новой, передайте **глутесскаллбакк** указатель null для соответствующей функции.</span><span class="sxs-lookup"><span data-stu-id="0f627-125">To eliminate a callback function without replacing it with a new one, pass **gluTessCallback** a null pointer for the appropriate function.</span></span>

<span data-ttu-id="0f627-126">По мере выполнения тесселяции функции обратного вызова вызываются способом, аналогичным использованию функций OpenGL [**глбегин**](glbegin.md), [гледжефлаг](gledgeflag-functions.md), [глвертекс](glvertex-functions.md)и [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0f627-126">As tessellation proceeds, the callback functions are called in a manner similar to the way you would use the OpenGL functions [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md), and [**glEnd**](glend.md).</span></span>

<span data-ttu-id="0f627-127">Функция обратного вызова **Glu \_ Begin** вызывается с одним из трех возможных параметров:</span><span class="sxs-lookup"><span data-stu-id="0f627-127">The **GLU\_BEGIN** callback function is invoked with one of three possible parameters:</span></span>

-   <span data-ttu-id="0f627-128">\_вентилятор с треугольником GL \_</span><span class="sxs-lookup"><span data-stu-id="0f627-128">GL\_TRIANGLE\_FAN</span></span>
-   <span data-ttu-id="0f627-129">\_полоса треугольников GL \_</span><span class="sxs-lookup"><span data-stu-id="0f627-129">GL\_TRIANGLE\_STRIP</span></span>
-   <span data-ttu-id="0f627-130">\_треугольники GL</span><span class="sxs-lookup"><span data-stu-id="0f627-130">GL\_TRIANGLES</span></span>

<span data-ttu-id="0f627-131">После вызова функции обратного вызова Glu и перед вызовом функции обратного вызова, связанной с **Glu \_ End**, вызывается некоторое сочетание **\_ \_ флага Glu ребра** и обратных вызовов **Glu в \_ вершинах** . **\_**</span><span class="sxs-lookup"><span data-stu-id="0f627-131">After calling the **GLU\_BEGIN** callback function, and before calling the callback function associated with **GLU\_END**, some combination of the **GLU\_EDGE\_FLAG** and **GLU\_VERTEX** callbacks is invoked.</span></span> <span data-ttu-id="0f627-132">Связанные вершины и пограничные флаги интерпретируется точно так же, как в OpenGL между **глбегин**( \_ \_ радиальный вентилятор GL), **глбегин**( \_ полоса треугольников GL) \_ или **глбегин**( \_ треугольники GL **)** и соответствующим **гленд**.</span><span class="sxs-lookup"><span data-stu-id="0f627-132">The associated vertices and edge flags are interpreted exactly as they are in OpenGL between **glBegin**(GL\_TRIANGLE\_FAN), **glBegin**(GL\_TRIANGLE\_STRIP), or **glBegin**(GL\_TRIANGLES **)** and the matching **glEnd**.</span></span>

<span data-ttu-id="0f627-133">Поскольку флаги краев не имеют смысла в битовом вентиляторе или полоске треугольника, при наличии функции обратного вызова, связанной с **\_ \_ флагом Glu ребра**, метод обратного вызова **Glu \_ Begin** вызывается только с **\_ треугольниками GL**.</span><span class="sxs-lookup"><span data-stu-id="0f627-133">Because edge flags make no sense in a triangle fan or triangle strip, if there is a callback function associated with **GLU\_EDGE\_FLAG**, the **GLU\_BEGIN** callback is called only with **GL\_TRIANGLES**.</span></span> <span data-ttu-id="0f627-134">Функция обратного вызова с **\_ \_ флагом Glu пограничных** функций работает аналогично функции OpenGL [гледжефлаг](gledgeflag-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="0f627-134">The **GLU\_EDGE\_FLAG** callback function works analogously to the OpenGL [glEdgeFlag](gledgeflag-functions.md) function.</span></span>

<span data-ttu-id="0f627-135">Если во время тесселяции возникает ошибка, вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="0f627-135">If there is an error during the tessellation, the error callback function is invoked.</span></span> <span data-ttu-id="0f627-136">Функции обратного вызова ошибки передан номер ошибки GLU.</span><span class="sxs-lookup"><span data-stu-id="0f627-136">The error callback function is passed a GLU error number.</span></span> <span data-ttu-id="0f627-137">Можно получить строку символов, описывающую ошибку, с помощью функции [**глуеррорстринг**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="0f627-137">You can obtain a character string describing the error with the [**gluErrorString**](gluerrorstring.md) function.</span></span>

 

 




