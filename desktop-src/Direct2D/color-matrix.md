---
title: Цветовая матрица
description: Используйте цветовую матрицу для изменения значений RGBA точечного рисунка.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- Цветовая матрица
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071500"
---
# <a name="color-matrix-effect"></a><span data-ttu-id="ad1d3-104">Цветовая матрица</span><span class="sxs-lookup"><span data-stu-id="ad1d3-104">Color matrix effect</span></span>

<span data-ttu-id="ad1d3-105">Используйте цветовую матрицу для изменения значений RGBA точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-105">Use the color matrix effect to alter the RGBA values of a bitmap.</span></span>

<span data-ttu-id="ad1d3-106">Этот результат можно использовать для:</span><span class="sxs-lookup"><span data-stu-id="ad1d3-106">You can use this effect to:</span></span>

-   <span data-ttu-id="ad1d3-107">Удаляет цветовой канал из изображения.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-107">Remove a color channel from an image.</span></span>
-   <span data-ttu-id="ad1d3-108">Уменьшите цвет в изображении.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-108">Reduce the color in an image.</span></span>
-   <span data-ttu-id="ad1d3-109">Переключение цветовых каналов.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-109">Swap color channels.</span></span>
-   <span data-ttu-id="ad1d3-110">Объединение цветовых каналов.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-110">Combine color channels.</span></span>

<span data-ttu-id="ad1d3-111">Многие встроенные эффекты — это специализации цветовой матрицы, оптимизированные для предполагаемого использования эффектов.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-111">Many built-in effects are specializations of color matrix that are optimized for the intended use of the effects.</span></span> <span data-ttu-id="ad1d3-112">К примерам относятся [насыщенность](saturation.md), [цветовой тон](hue-rotate.md), [выцветшей](sepia-effect.md), [температура и оттенок](temperature-and-tint-effect.md).</span><span class="sxs-lookup"><span data-stu-id="ad1d3-112">Examples include [saturation](saturation.md), [hue rotate](hue-rotate.md), [sepia](sepia-effect.md), and [temperature and tint](temperature-and-tint-effect.md).</span></span>

<span data-ttu-id="ad1d3-113">Идентификатором CLSID для этого действия является CLSID \_ D2D1ColorMatrix.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-113">The CLSID for this effect is CLSID\_D2D1ColorMatrix.</span></span>

-   [<span data-ttu-id="ad1d3-114">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="ad1d3-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ad1d3-115">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="ad1d3-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ad1d3-116">Режимы альфа</span><span class="sxs-lookup"><span data-stu-id="ad1d3-116">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="ad1d3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ad1d3-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ad1d3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ad1d3-118">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ad1d3-119">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="ad1d3-119">Example image</span></span>

<span data-ttu-id="ad1d3-120">В этом примере показаны входные и выходные изображения для цветового влияния, которое меняет местами красный и синий каналы.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-120">The example here shows the input and output images of the color matrix effect that swaps the red and blue channels.</span></span>



| <span data-ttu-id="ad1d3-121">До</span><span class="sxs-lookup"><span data-stu-id="ad1d3-121">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)   |
| <span data-ttu-id="ad1d3-123">После</span><span class="sxs-lookup"><span data-stu-id="ad1d3-123">After</span></span>                                                        |
| ![изображение после преобразования.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="ad1d3-125">Этот результат умножает значения RGBA изображения на 5x4, столбец основной матрицы, как показано в этом уравнении.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-125">This effect multiplies the RGBA values of the image by a 5x4, column major matrix as shown in this equation.</span></span>

![Пример определения матрицы.](images/color-matrix-formula.png)

<span data-ttu-id="ad1d3-127">Этот результат работает с прямыми и предварительно умноженными альфа-образами.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-127">This effect works on straight and premultiplied alpha images.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ad1d3-128">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="ad1d3-128">Effect properties</span></span>



| <span data-ttu-id="ad1d3-129">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="ad1d3-129">Display name and index enumeration</span></span>                                       | <span data-ttu-id="ad1d3-130">Описание</span><span class="sxs-lookup"><span data-stu-id="ad1d3-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1d3-131">колорматрикс</span><span class="sxs-lookup"><span data-stu-id="ad1d3-131">ColorMatrix</span></span><br/> <span data-ttu-id="ad1d3-132">\_ \_ \_ Матрица цветов D2D1 КолорМатрикс Prop \_</span><span class="sxs-lookup"><span data-stu-id="ad1d3-132">D2D1\_COLORMATRIX\_PROP\_COLOR\_MATRIX</span></span><br/> | <span data-ttu-id="ad1d3-133">5x4 матрица значений float.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-133">A 5x4 matrix of float values.</span></span> <span data-ttu-id="ad1d3-134">Элементы в матрице не привязаны и не имеют модулей.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-134">The elements in the matrix are not bounded and are unitless.</span></span><br/> <span data-ttu-id="ad1d3-135">По умолчанию используется матрица идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-135">The default is the identity matrix.</span></span><br/> <span data-ttu-id="ad1d3-136">Тип — D2D1 \_ Matrix \_ 5x4 \_ F.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-136">The type is D2D1\_MATRIX\_5X4\_F.</span></span><br/> <span data-ttu-id="ad1d3-137">Значения по умолчанию: Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="ad1d3-137">The default value is Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span></span> <br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="ad1d3-138">алфамоде</span><span class="sxs-lookup"><span data-stu-id="ad1d3-138">AlphaMode</span></span><br/> <span data-ttu-id="ad1d3-139">D2D1 \_ КолорМатрикс \_ prop \_ , \_ режим альфа</span><span class="sxs-lookup"><span data-stu-id="ad1d3-139">D2D1\_COLORMATRIX\_PROP\_ALPHA\_MODE</span></span><br/>     | <span data-ttu-id="ad1d3-140">Режим альфа для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-140">The alpha mode of the output.</span></span> <span data-ttu-id="ad1d3-141">Дополнительные сведения см. в разделе [режимы альфа-канала](#alpha-modes) .</span><span class="sxs-lookup"><span data-stu-id="ad1d3-141">See [Alpha modes](#alpha-modes) for more info.</span></span> <br/> <span data-ttu-id="ad1d3-142">Тип — D2D1 \_ КолорМатрикс \_ Alpha \_ mode.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-142">The type is D2D1\_COLORMATRIX\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="ad1d3-143">Значение по умолчанию — D2D1 КолорМатрикс Alpha с предварительным \_ \_ \_ \_ умножением.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-143">The default value is D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ad1d3-144">клампаутпут</span><span class="sxs-lookup"><span data-stu-id="ad1d3-144">ClampOutput</span></span><br/> <span data-ttu-id="ad1d3-145">\_ \_ \_ Выходные данные среза D2D1 КолорМатрикс \_</span><span class="sxs-lookup"><span data-stu-id="ad1d3-145">D2D1\_COLORMATRIX\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="ad1d3-146">Будет ли результат заменять цветовые значения в диапазоне от 0 до 1 перед тем, как результат передаст значения следующему результату в графе.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-146">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="ad1d3-147">Этот результат выполняет фиксацию значений перед тем, как он умножает альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-147">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="ad1d3-148">Если присвоить этому параметру значение TRUE, то действие будет выполнять фиксацию значений.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-148">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="ad1d3-149">Если присвоить этому параметру значение FALSE, то эффект не будет выполнять фиксацию цветовых значений, но другие эффекты и поверхность вывода могут попытаться отразить значения, если они не имеют достаточно высокой точности.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-149">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="ad1d3-150">Тип — BOOL.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-150">The type is BOOL.</span></span><br/> <span data-ttu-id="ad1d3-151">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-151">The default value is FALSE.</span></span><br/> |



 

## <a name="alpha-modes"></a><span data-ttu-id="ad1d3-152">Режимы альфа</span><span class="sxs-lookup"><span data-stu-id="ad1d3-152">Alpha modes</span></span>



| <span data-ttu-id="ad1d3-153">Имя</span><span class="sxs-lookup"><span data-stu-id="ad1d3-153">Name</span></span>                                          | <span data-ttu-id="ad1d3-154">Описание</span><span class="sxs-lookup"><span data-stu-id="ad1d3-154">Description</span></span>                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1d3-155">Предварительное \_ \_ \_ \_ умножение режима альфа-D2D1 КолорМатрикс</span><span class="sxs-lookup"><span data-stu-id="ad1d3-155">D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="ad1d3-156">Этот результат не выполняет предварительную умножение входных данных, применяет цветовую матрицу и предварительно умножает результат.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-156">The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.</span></span><br/> |
| <span data-ttu-id="ad1d3-157">D2D1 \_ КолорМатрикс \_ Alpha \_ , \_ прямой режим</span><span class="sxs-lookup"><span data-stu-id="ad1d3-157">D2D1\_COLORMATRIX\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="ad1d3-158">Этот результат применяет матрицу цветов непосредственно к входным данным и не выполняет предварительного умножения выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ad1d3-158">The effect applies the color matrix directly to the input, and doesn't premultiply the output.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad1d3-159">Требования</span><span class="sxs-lookup"><span data-stu-id="ad1d3-159">Requirements</span></span>



| <span data-ttu-id="ad1d3-160">Требование</span><span class="sxs-lookup"><span data-stu-id="ad1d3-160">Requirement</span></span> | <span data-ttu-id="ad1d3-161">Значение</span><span class="sxs-lookup"><span data-stu-id="ad1d3-161">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1d3-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad1d3-162">Minimum supported client</span></span> | <span data-ttu-id="ad1d3-163">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="ad1d3-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ad1d3-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad1d3-164">Minimum supported server</span></span> | <span data-ttu-id="ad1d3-165">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="ad1d3-165">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ad1d3-166">Header</span><span class="sxs-lookup"><span data-stu-id="ad1d3-166">Header</span></span>                   | <span data-ttu-id="ad1d3-167">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ad1d3-167">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ad1d3-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad1d3-168">Library</span></span>                  | <span data-ttu-id="ad1d3-169">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="ad1d3-169">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ad1d3-170">См. также</span><span class="sxs-lookup"><span data-stu-id="ad1d3-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad1d3-171">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ad1d3-171">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

