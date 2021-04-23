---
title: Перенос функций текстуры
description: Перенос функций текстуры
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Перенос GL по IRI, текстура
- Перенос из ДИАФРАГМы в ГК, текстура
- Перенос на OpenGL из IRI GL, текстура
- Перенос по стандарту OpenGL из IRI GL, текстура
- текстура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068200"
---
# <a name="porting-texture-functions"></a><span data-ttu-id="2810c-108">Перенос функций текстуры</span><span class="sxs-lookup"><span data-stu-id="2810c-108">Porting Texture Functions</span></span>

<span data-ttu-id="2810c-109">При переносе функций текстуры диафрагмы IRI на OpenGL учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="2810c-109">When porting IRIS GL texture functions to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="2810c-110">OpenGL не поддерживает таблицы текстур; в нем используется только одномерная текстура и двумерная текстура.</span><span class="sxs-lookup"><span data-stu-id="2810c-110">OpenGL doesn't maintain tables of textures; it uses either 1-D texture and 2-D texture only.</span></span> <span data-ttu-id="2810c-111">Чтобы повторно использовать текстуры из кода IRI в ГК, помещайте их в список дисплеев.</span><span class="sxs-lookup"><span data-stu-id="2810c-111">To reuse the textures from your IRIS GL code, put them in a display list.</span></span>
-   <span data-ttu-id="2810c-112">OpenGL не создает MIP-карты автоматически.</span><span class="sxs-lookup"><span data-stu-id="2810c-112">OpenGL doesn't automatically generate mipmaps.</span></span> <span data-ttu-id="2810c-113">Если вы используете MIP-карты, необходимо сначала вызвать функцию [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .</span><span class="sxs-lookup"><span data-stu-id="2810c-113">If you're using mipmaps, you must first call the [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) function.</span></span>
-   <span data-ttu-id="2810c-114">В OpenGL для включения и отключения возможностей текстурирования используются [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) .</span><span class="sxs-lookup"><span data-stu-id="2810c-114">In OpenGL, you use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) to turn texturing capabilities on and off.</span></span>
-   <span data-ttu-id="2810c-115">В OpenGL размер текстуры более строго регулируется, чем в IRI GL.</span><span class="sxs-lookup"><span data-stu-id="2810c-115">In OpenGL, texture size is more strictly regulated than in IRIS GL.</span></span> <span data-ttu-id="2810c-116">Размер текстуры OpenGL должен быть следующим:</span><span class="sxs-lookup"><span data-stu-id="2810c-116">The size of an OpenGL texture must be:</span></span>

    <span data-ttu-id="2810c-117">2 *n* + 2 *b*</span><span class="sxs-lookup"><span data-stu-id="2810c-117">2 *n* + 2 *b*</span></span>

    <span data-ttu-id="2810c-118">где *n* — целое число, а *b* —:</span><span class="sxs-lookup"><span data-stu-id="2810c-118">where *n* is an integer and *b* is:</span></span>

    -   <span data-ttu-id="2810c-119">0, если текстура не имеет границы</span><span class="sxs-lookup"><span data-stu-id="2810c-119">0, if the texture has no border</span></span>
    -   <span data-ttu-id="2810c-120">1, если текстура имеет границу пикселя (текстуры OpenGL могут иметь границы 1 пикселя).</span><span class="sxs-lookup"><span data-stu-id="2810c-120">1, if the texture has a border pixel (OpenGL textures can have 1-pixel borders.)</span></span>

<span data-ttu-id="2810c-121">В следующей таблице перечислены функции текстурирования ДИАФРАГМы и их общие эквиваленты OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2810c-121">The following table lists IRIS GL texture functions and their general OpenGL equivalents.</span></span>



| <span data-ttu-id="2810c-122">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="2810c-122">IRIS GL function</span></span> | <span data-ttu-id="2810c-123">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="2810c-123">OpenGL function</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="2810c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2810c-124">Meaning</span></span>                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2810c-125">**textdef2d**</span><span class="sxs-lookup"><span data-stu-id="2810c-125">**textdef2d**</span></span>    | <span data-ttu-id="2810c-126">[**glTexImage2D**](glteximage2d.md)[**глтекспараметер**](gltexparameter-functions.md)</span><span class="sxs-lookup"><span data-stu-id="2810c-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span></span><br/> [<span data-ttu-id="2810c-127">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="2810c-127">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/>                                                                                                           | <span data-ttu-id="2810c-128">Задает изображение двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="2810c-128">Specifies a 2-D texture image.</span></span>                                                              |
| <span data-ttu-id="2810c-129">**текстбинд**</span><span class="sxs-lookup"><span data-stu-id="2810c-129">**textbind**</span></span>     | <span data-ttu-id="2810c-130">**glTexImage2DglTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2810c-130">**glTexImage2DglTexParameter**</span></span><br/> <span data-ttu-id="2810c-131">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="2810c-131">**gluBuild2DMipmaps**</span></span><br/>                                                                                                                                                                                            | <span data-ttu-id="2810c-132">Выбирает функцию текстуры.</span><span class="sxs-lookup"><span data-stu-id="2810c-132">Selects a texture function.</span></span>                                                                 |
| <span data-ttu-id="2810c-133">**тевдеф**</span><span class="sxs-lookup"><span data-stu-id="2810c-133">**tevdef**</span></span>       | [<span data-ttu-id="2810c-134">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="2810c-134">**glTexEnv**</span></span>](gltexenv-functions.md)                                                                                                                                                                                                                                | <span data-ttu-id="2810c-135">Определяет среду сопоставления текстур.</span><span class="sxs-lookup"><span data-stu-id="2810c-135">Defines a texture-mapping environment.</span></span>                                                      |
| <span data-ttu-id="2810c-136">**тевбинд**</span><span class="sxs-lookup"><span data-stu-id="2810c-136">**tevbind**</span></span>      | <span data-ttu-id="2810c-137">**глтексенв**[**glTexImage1D**](glteximage1d.md)</span><span class="sxs-lookup"><span data-stu-id="2810c-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span></span><br/>                                                                                                                                                                                                           | <span data-ttu-id="2810c-138">Выбирает среду текстуры.</span><span class="sxs-lookup"><span data-stu-id="2810c-138">Selects a texture environment.</span></span>                                                              |
| <span data-ttu-id="2810c-139">**T2**</span><span class="sxs-lookup"><span data-stu-id="2810c-139">**t2**</span></span>           | [<span data-ttu-id="2810c-140">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="2810c-140">**glTexCoord**</span></span>](gltexcoord-functions.md)                                                                                                                                                                                                                            | <span data-ttu-id="2810c-141">Задает текущие координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="2810c-141">Sets the current texture coordinates.</span></span>                                                       |
| <span data-ttu-id="2810c-142">**тексжен**</span><span class="sxs-lookup"><span data-stu-id="2810c-142">**texgen**</span></span>       | <span data-ttu-id="2810c-143">[**глтексжен**](gltexgen-functions.md)[**глжеттекспараметер**](glgettexparameter.md)</span><span class="sxs-lookup"><span data-stu-id="2810c-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span></span><br/> [<span data-ttu-id="2810c-144">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="2810c-144">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)<br/> [<span data-ttu-id="2810c-145">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="2810c-145">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/> [<span data-ttu-id="2810c-146">**глускалеимаже**</span><span class="sxs-lookup"><span data-stu-id="2810c-146">**gluScaleImage**</span></span>](gluscaleimage.md)<br/> | <span data-ttu-id="2810c-147">Управляет созданием координат текстуры. Масштабирует изображение до произвольного размера.</span><span class="sxs-lookup"><span data-stu-id="2810c-147">Controls generation of texture coordinates.Scales an image to an arbitrary size.</span></span><br/> |



 

<span data-ttu-id="2810c-148">Дополнительные сведения о текстурировании см. в разделе с *руководством по программированию OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="2810c-148">For more information on texturing, see the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="2810c-149">Этот раздел содержит сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="2810c-149">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="2810c-150">Преобразование тевдеф</span><span class="sxs-lookup"><span data-stu-id="2810c-150">Translating tevdef</span></span>](translating-tevdef.md)
-   [<span data-ttu-id="2810c-151">Преобразование тексдеф</span><span class="sxs-lookup"><span data-stu-id="2810c-151">Translating texdef</span></span>](translating-texdef.md)
-   [<span data-ttu-id="2810c-152">Преобразование тексжен</span><span class="sxs-lookup"><span data-stu-id="2810c-152">Translating texgen</span></span>](translating-texgen.md)

 

 





