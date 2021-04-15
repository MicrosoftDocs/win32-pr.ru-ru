---
title: Преобразование тексжен
description: Функция IRI GL тексжен преобразуется в Глтексжен для OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Перенос GL по IRI, текстура
- Перенос из ДИАФРАГМы в ГК, текстура
- Перенос на OpenGL из IRI GL, текстура
- Перенос по стандарту OpenGL из IRI GL, текстура
- текстура
- Перенос GL в ГК, тексжен
- Перенос из IRI GL, тексжен
- перенос в OpenGL из IRI GL, тексжен
- Перенос по стандарту OpenGL из IRI GL, тексжен
- тексжен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661633"
---
# <a name="translating-texgen"></a><span data-ttu-id="f7815-113">Преобразование тексжен</span><span class="sxs-lookup"><span data-stu-id="f7815-113">Translating texgen</span></span>

<span data-ttu-id="f7815-114">Функция IRI GL **тексжен** преобразуется в [глтексжен](gltexgen-functions.md) для OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f7815-114">The IRIS GL function **texgen** is translated to [glTexGen](gltexgen-functions.md) for OpenGL.</span></span>

<span data-ttu-id="f7815-115">При использовании IRI GL вы вызываете **тексжен** дважды: один раз, чтобы одновременно задать уравнение режима и плоскости, и один раз для включения создания координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="f7815-115">With IRIS GL, you call **texgen** twice: once to set the mode and plane equation simultaneously, and once to enable texture-coordinate generation.</span></span> <span data-ttu-id="f7815-116">Пример:</span><span class="sxs-lookup"><span data-stu-id="f7815-116">For example:</span></span>


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



<span data-ttu-id="f7815-117">С помощью OpenGL вы выполняете три вызова: две к **глтексжен** (один раз, чтобы задать режим, и один раз, чтобы задать уравнение плоскости), а второй — [**гленабле**](glenable.md).</span><span class="sxs-lookup"><span data-stu-id="f7815-117">With OpenGL, you make three calls: two to **glTexGen** (once to set the mode and once to set the plane equation), and one to [**glEnable**](glenable.md).</span></span> <span data-ttu-id="f7815-118">Например, для кода OpenGL, эквивалентного приведенному выше коду в ГК, используется:</span><span class="sxs-lookup"><span data-stu-id="f7815-118">For example, the OpenGL equivalent to the IRIS GL code above is:</span></span>


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



<span data-ttu-id="f7815-119">В следующей таблице перечислены названия текстур текстуры в формате IRI и их эквиваленты OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f7815-119">The following table lists the IRIS GL texture-coordinate names and their OpenGL equivalents.</span></span>



| <span data-ttu-id="f7815-120">Координата текстуры IRI GL</span><span class="sxs-lookup"><span data-stu-id="f7815-120">IRIS GL texture coordinate</span></span> | <span data-ttu-id="f7815-121">Координата текстуры OpenGL</span><span class="sxs-lookup"><span data-stu-id="f7815-121">OpenGL texture coordinate</span></span> | <span data-ttu-id="f7815-122">Гленабле, аргумент</span><span class="sxs-lookup"><span data-stu-id="f7815-122">glEnable argument</span></span>   |
|----------------------------|---------------------------|---------------------|
| <span data-ttu-id="f7815-123">TX \_ S</span><span class="sxs-lookup"><span data-stu-id="f7815-123">TX\_S</span></span>                      | <span data-ttu-id="f7815-124">ГК \_ S</span><span class="sxs-lookup"><span data-stu-id="f7815-124">GL\_S</span></span>                     | <span data-ttu-id="f7815-125">\_Gen текстура GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7815-125">GL\_TEXTURE\_GEN\_S</span></span> |
| <span data-ttu-id="f7815-126">TX \_ T</span><span class="sxs-lookup"><span data-stu-id="f7815-126">TX\_T</span></span>                      | <span data-ttu-id="f7815-127">ГК \_ T</span><span class="sxs-lookup"><span data-stu-id="f7815-127">GL\_T</span></span>                     | <span data-ttu-id="f7815-128">\_Gen текстура GL \_ \_ T</span><span class="sxs-lookup"><span data-stu-id="f7815-128">GL\_TEXTURE\_GEN\_T</span></span> |
| <span data-ttu-id="f7815-129">TX \_ R</span><span class="sxs-lookup"><span data-stu-id="f7815-129">TX\_R</span></span>                      | <span data-ttu-id="f7815-130">GL ( \_ R)</span><span class="sxs-lookup"><span data-stu-id="f7815-130">GL\_R</span></span>                     | <span data-ttu-id="f7815-131">заполнение текстур главной книги \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7815-131">GL\_TEXTURE\_GEN\_R</span></span> |
| <span data-ttu-id="f7815-132">Передача \_ Q</span><span class="sxs-lookup"><span data-stu-id="f7815-132">TX\_Q</span></span>                      | <span data-ttu-id="f7815-133">ГК \_ Q</span><span class="sxs-lookup"><span data-stu-id="f7815-133">GL\_Q</span></span>                     | <span data-ttu-id="f7815-134">\_ \_ Общие вопросы о ТЕКСТУРе GL \_</span><span class="sxs-lookup"><span data-stu-id="f7815-134">GL\_TEXTURE\_GEN\_Q</span></span> |



 

<span data-ttu-id="f7815-135">В следующей таблице перечислены режимы формирования текстуры IRI в ГК, а также их эквивалентные режимы текстур OpenGL и имена плоскостей.</span><span class="sxs-lookup"><span data-stu-id="f7815-135">The following table lists the IRIS GL texture-generation modes and their equivalent OpenGL texture modes and plane names.</span></span>



| <span data-ttu-id="f7815-136">Режим текстуры IRI GL</span><span class="sxs-lookup"><span data-stu-id="f7815-136">IRIS GL texture mode</span></span> | <span data-ttu-id="f7815-137">Режим текстуры OpenGL</span><span class="sxs-lookup"><span data-stu-id="f7815-137">OpenGL texture mode</span></span> | <span data-ttu-id="f7815-138">Имя плоскости OpenGL</span><span class="sxs-lookup"><span data-stu-id="f7815-138">OpenGL plane name</span></span> |
|----------------------|---------------------|-------------------|
| <span data-ttu-id="f7815-139">\_Линейная TG</span><span class="sxs-lookup"><span data-stu-id="f7815-139">TG\_LINEAR</span></span>           | <span data-ttu-id="f7815-140">\_ \_ Линейный объект GL</span><span class="sxs-lookup"><span data-stu-id="f7815-140">GL\_OBJECT\_LINEAR</span></span>  | <span data-ttu-id="f7815-141">\_плоскость объектов \_ GL</span><span class="sxs-lookup"><span data-stu-id="f7815-141">GL\_OBJECT\_PLANE</span></span> |
| <span data-ttu-id="f7815-142">\_профиль TG</span><span class="sxs-lookup"><span data-stu-id="f7815-142">TG\_CONTOUR</span></span>          | <span data-ttu-id="f7815-143">\_линейный глаз в ГК \_</span><span class="sxs-lookup"><span data-stu-id="f7815-143">GL\_EYE\_LINEAR</span></span>     | <span data-ttu-id="f7815-144">\_плоскость для глаз в ГК \_</span><span class="sxs-lookup"><span data-stu-id="f7815-144">GL\_EYE\_PLANE</span></span>    |
| <span data-ttu-id="f7815-145">TG \_ сферемап</span><span class="sxs-lookup"><span data-stu-id="f7815-145">TG\_SPHEREMAP</span></span>        | <span data-ttu-id="f7815-146">\_геосхема сферы GL \_</span><span class="sxs-lookup"><span data-stu-id="f7815-146">GL\_SPHERE\_MAP</span></span>     |                   |



 

 

 




