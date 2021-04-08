---
title: Преобразование тексдеф
description: Следующий пример кода является определением текстуры ДИАФРАГМы в ГК
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Перенос GL по IRI, текстура
- Перенос из ДИАФРАГМы в ГК, текстура
- Перенос на OpenGL из IRI GL, текстура
- Перенос по стандарту OpenGL из IRI GL, текстура
- текстура
- Перенос GL в ГК, тексдеф
- Перенос из IRI GL, тексдеф
- перенос в OpenGL из IRI GL, тексдеф
- Перенос по стандарту OpenGL из IRI GL, тексдеф
- тексдеф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889047"
---
# <a name="translating-texdef"></a><span data-ttu-id="c31ec-113">Преобразование тексдеф</span><span class="sxs-lookup"><span data-stu-id="c31ec-113">Translating texdef</span></span>

<span data-ttu-id="c31ec-114">В следующем примере кода демонстрируется определение текстуры ДИАФРАГМы в ГК:</span><span class="sxs-lookup"><span data-stu-id="c31ec-114">The following code example is an IRIS GL texture definition:</span></span>


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



<span data-ttu-id="c31ec-115">В предыдущем примере **тексдеф** указывает фильтр точек TX как как увеличение, так и как \_ Фильтр минимизации, а TX \_ Repeat — как механизм упаковки.</span><span class="sxs-lookup"><span data-stu-id="c31ec-115">In the preceding example, **texdef** specifies the TX\_POINT filter as both the magnification and the minimizing filter, and TX\_REPEAT as the wrapping mechanism.</span></span> <span data-ttu-id="c31ec-116">Он также указывает изображение текстуры: **Granite \_ текстура**.</span><span class="sxs-lookup"><span data-stu-id="c31ec-116">It also specifies the texture image: **granite\_texture**.</span></span>

<span data-ttu-id="c31ec-117">В OpenGL [**глтексимаже**](glteximage1d.md) указывает образ, а [глтекспараметер](gltexparameter-functions.md) задает свойство.</span><span class="sxs-lookup"><span data-stu-id="c31ec-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifies the image and [glTexParameter](gltexparameter-functions.md) sets the property.</span></span> <span data-ttu-id="c31ec-118">Для преобразования определений текстур IRI GL замените функцию **текстдеф** на **глтексимаже** и один или несколько вызовов **глтекспараметер**.</span><span class="sxs-lookup"><span data-stu-id="c31ec-118">To translate IRIS GL texture definitions, replace the **textdef** function with **glTexImage** and one or more calls to **glTexParameter**.</span></span>

<span data-ttu-id="c31ec-119">Предыдущий код IRI GL выглядит следующим образом при переводе в OpenGL:</span><span class="sxs-lookup"><span data-stu-id="c31ec-119">The preceding IRIS GL code looks like this when translated to OpenGL:</span></span>


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



<span data-ttu-id="c31ec-120">В следующей таблице перечислены параметры текстуры диафрагмы IRI и их эквивалентные параметры OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c31ec-120">The following table lists the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="c31ec-121">Параметр текстуры IRI GL</span><span class="sxs-lookup"><span data-stu-id="c31ec-121">IRIS GL texture parameter</span></span> | <span data-ttu-id="c31ec-122">Параметр текстуры OpenGL</span><span class="sxs-lookup"><span data-stu-id="c31ec-122">OpenGL texture parameter</span></span>                                  |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c31ec-123">\_МИНФИЛТЕР TX</span><span class="sxs-lookup"><span data-stu-id="c31ec-123">TX\_MINFILTER</span></span>             | <span data-ttu-id="c31ec-124">\_ \_ Фильтр min текстуры \_ GL</span><span class="sxs-lookup"><span data-stu-id="c31ec-124">GL\_TEXTURE\_MIN\_FILTER</span></span>                                  |
| <span data-ttu-id="c31ec-125">\_МАГФИЛТЕР TX</span><span class="sxs-lookup"><span data-stu-id="c31ec-125">TX\_MAGFILTER</span></span>             | <span data-ttu-id="c31ec-126">\_ \_ Фильтр MAG текстуры \_ GL</span><span class="sxs-lookup"><span data-stu-id="c31ec-126">GL\_TEXTURE\_MAG\_FILTER</span></span>                                  |
| <span data-ttu-id="c31ec-127">\_Перенос переноса, передача \_ переносов по словам \_ S</span><span class="sxs-lookup"><span data-stu-id="c31ec-127">TX\_WRAP, TX\_WRAP\_S</span></span>     | <span data-ttu-id="c31ec-128">\_Перенос текстуры в ГК \_ \_</span><span class="sxs-lookup"><span data-stu-id="c31ec-128">GL\_TEXTURE\_WRAP\_S</span></span>                                      |
| <span data-ttu-id="c31ec-129">\_Перенос переноса, передача по \_ словам \_ T</span><span class="sxs-lookup"><span data-stu-id="c31ec-129">TX\_WRAP, TX\_WRAP\_T</span></span>     | <span data-ttu-id="c31ec-130">\_текстура GL — \_ Перенос \_ \_ \_ цвета границы текстуры тгл \_</span><span class="sxs-lookup"><span data-stu-id="c31ec-130">GL\_TEXTURE\_WRAP\_TGL\_TEXTURE\_BORDER\_COLOR</span></span><br/> |



 

<span data-ttu-id="c31ec-131">В следующей таблице перечислены возможные значения параметров текстуры диафрагмы IRI и их эквивалентные параметры OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c31ec-131">The following table lists the possible values of the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="c31ec-132">Параметр текстуры IRI GL</span><span class="sxs-lookup"><span data-stu-id="c31ec-132">IRIS GL texture parameter</span></span> | <span data-ttu-id="c31ec-133">Параметр текстуры OpenGL</span><span class="sxs-lookup"><span data-stu-id="c31ec-133">OpenGL texture parameter</span></span>     |
|---------------------------|------------------------------|
| <span data-ttu-id="c31ec-134">\_точка передачи</span><span class="sxs-lookup"><span data-stu-id="c31ec-134">TX\_POINT</span></span>                 | <span data-ttu-id="c31ec-135">\_Ближайшая к GL</span><span class="sxs-lookup"><span data-stu-id="c31ec-135">GL\_NEAREST</span></span>                  |
| <span data-ttu-id="c31ec-136">\_БИЛИНЕЙНОЙ TX</span><span class="sxs-lookup"><span data-stu-id="c31ec-136">TX\_BILINEAR</span></span>              | <span data-ttu-id="c31ec-137">Линейная (GL) \_</span><span class="sxs-lookup"><span data-stu-id="c31ec-137">GL\_LINEAR</span></span>                   |
| <span data-ttu-id="c31ec-138">\_точка mipmap \_ TX</span><span class="sxs-lookup"><span data-stu-id="c31ec-138">TX\_MIPMAP\_POINT</span></span>         | <span data-ttu-id="c31ec-139">Ближайшая к GL Ближайшая \_ \_ mipmap \_</span><span class="sxs-lookup"><span data-stu-id="c31ec-139">GL\_NEAREST\_MIPMAP\_NEAREST</span></span> |
| <span data-ttu-id="c31ec-140">TX \_ mipmap \_ билинейной</span><span class="sxs-lookup"><span data-stu-id="c31ec-140">TX\_MIPMAP\_BILINEAR</span></span>      | <span data-ttu-id="c31ec-141">\_Линейная \_ MIPMAPа GL \_</span><span class="sxs-lookup"><span data-stu-id="c31ec-141">GL\_LINEAR\_MIPMAP\_NEAREST</span></span>  |
| <span data-ttu-id="c31ec-142">\_ \_ Линейная mipmap TX</span><span class="sxs-lookup"><span data-stu-id="c31ec-142">TX\_MIPMAP\_LINEAR</span></span>        | <span data-ttu-id="c31ec-143">\_Ближайшая \_ Линейная MIPMAPа GL \_</span><span class="sxs-lookup"><span data-stu-id="c31ec-143">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>  |
| <span data-ttu-id="c31ec-144">\_ТРИЛИНЕЙНОЙ TX</span><span class="sxs-lookup"><span data-stu-id="c31ec-144">TX\_TRILINEAR</span></span>             | <span data-ttu-id="c31ec-145">линейное \_ \_ MIPMAPе GL \_</span><span class="sxs-lookup"><span data-stu-id="c31ec-145">GL\_LINEAR\_MIPMAP\_LINEAR</span></span>   |



 

 

 





