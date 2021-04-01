---
title: Преобразование тевдеф
description: В следующем примере кода представлено определение среды диафрагмы IRI, в котором указывается \_ параметр среды декал для ТВ-вещания.
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Перенос GL по IRI, текстура
- Перенос из ДИАФРАГМы в ГК, текстура
- Перенос на OpenGL из IRI GL, текстура
- Перенос по стандарту OpenGL из IRI GL, текстура
- текстура
- Перенос GL в ГК, тевдеф
- Перенос из IRI GL, тевдеф
- перенос в OpenGL из IRI GL, тевдеф
- Перенос по стандарту OpenGL из IRI GL, тевдеф
- тевдеф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986792"
---
# <a name="translating-tevdef"></a><span data-ttu-id="1ecb8-113">Преобразование тевдеф</span><span class="sxs-lookup"><span data-stu-id="1ecb8-113">Translating tevdef</span></span>

<span data-ttu-id="1ecb8-114">В следующем примере кода представлено определение среды диафрагмы IRI, в котором указывается \_ параметр среды декал для ТВ-вещания.</span><span class="sxs-lookup"><span data-stu-id="1ecb8-114">The following code example is an IRIS GL texture-environment definition that specifies the TV\_DECAL texture-environment parameter:</span></span>


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



<span data-ttu-id="1ecb8-115">и тот же код, переведенный в OpenGL:</span><span class="sxs-lookup"><span data-stu-id="1ecb8-115">and the same code translated to OpenGL:</span></span>


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



<span data-ttu-id="1ecb8-116">В следующей таблице перечислены параметры окружения "Текстура" для ДИАФРАГМы и их эквиваленты параметров OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1ecb8-116">The following table lists the IRIS GL texture-environment parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="1ecb8-117">Параметр IRI GL</span><span class="sxs-lookup"><span data-stu-id="1ecb8-117">IRIS GL parameter</span></span>     | <span data-ttu-id="1ecb8-118">Параметр OpenGL</span><span class="sxs-lookup"><span data-stu-id="1ecb8-118">OpenGL parameter</span></span>             |
|-----------------------|------------------------------|
| <span data-ttu-id="1ecb8-119">ТЕЛЕВИЗИОНная \_ модуляция</span><span class="sxs-lookup"><span data-stu-id="1ecb8-119">TV\_MODULATE</span></span>          | <span data-ttu-id="1ecb8-120">GL для \_ модуляции</span><span class="sxs-lookup"><span data-stu-id="1ecb8-120">GL\_MODULATE</span></span>                 |
| <span data-ttu-id="1ecb8-121">ТВ- \_ декал</span><span class="sxs-lookup"><span data-stu-id="1ecb8-121">TV\_DECAL</span></span>             | <span data-ttu-id="1ecb8-122">\_ДЕКАЛ GL</span><span class="sxs-lookup"><span data-stu-id="1ecb8-122">GL\_DECAL</span></span>                    |
| <span data-ttu-id="1ecb8-123">Телевизор \_ Blend</span><span class="sxs-lookup"><span data-stu-id="1ecb8-123">TV\_BLEND</span></span>             | <span data-ttu-id="1ecb8-124">ГК \_ Blend</span><span class="sxs-lookup"><span data-stu-id="1ecb8-124">GL\_BLEND</span></span>                    |
| <span data-ttu-id="1ecb8-125">ТВ- \_ Цвет</span><span class="sxs-lookup"><span data-stu-id="1ecb8-125">TV\_COLOR</span></span>             | <span data-ttu-id="1ecb8-126">\_Цвет текстуры в главной \_ env \_</span><span class="sxs-lookup"><span data-stu-id="1ecb8-126">GL\_TEXTURE\_ENV\_COLOR</span></span>      |
| <span data-ttu-id="1ecb8-127">\_альфа-канал ТВ</span><span class="sxs-lookup"><span data-stu-id="1ecb8-127">TV\_ALPHA</span></span>             | <span data-ttu-id="1ecb8-128">Нет прямого эквивалента OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1ecb8-128">No direct OpenGL equivalent.</span></span> |
| <span data-ttu-id="1ecb8-129">Выбор ТВ- \_ компонента \_</span><span class="sxs-lookup"><span data-stu-id="1ecb8-129">TV\_COMPONENT\_SELECT</span></span> | <span data-ttu-id="1ecb8-130">Нет прямого эквивалента OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1ecb8-130">No direct OpenGL equivalent.</span></span> |



 

<span data-ttu-id="1ecb8-131">Дополнительные сведения о параметрах среды текстуры см. в разделе [**глтексенв**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1ecb8-131">For more information about texture-environment parameters, see [**glTexEnv**](gltexenv-functions.md).</span></span>

 

 




