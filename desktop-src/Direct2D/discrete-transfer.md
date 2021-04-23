---
title: Дискретный результат перемещения
description: Используйте дискретный результат передачи, чтобы связать цветовой интенситиес изображения с помощью функции передачи шага, созданной из списка предоставленных значений.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- Дискретный результат перемещения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104569006"
---
# <a name="discrete-transfer-effect"></a><span data-ttu-id="32af9-104">Дискретный результат перемещения</span><span class="sxs-lookup"><span data-stu-id="32af9-104">Discrete transfer effect</span></span>

<span data-ttu-id="32af9-105">Используйте дискретный результат передачи, чтобы связать цветовой интенситиес изображения с помощью функции передачи шага, созданной из списка предоставленных значений.</span><span class="sxs-lookup"><span data-stu-id="32af9-105">Use the discrete transfer effect to map the color intensities of an image using a step transfer function created from a list of values you provide.</span></span>

<span data-ttu-id="32af9-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1DiscreteTransfer.</span><span class="sxs-lookup"><span data-stu-id="32af9-106">The CLSID for this effect is CLSID\_D2D1DiscreteTransfer.</span></span>

-   [<span data-ttu-id="32af9-107">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="32af9-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="32af9-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="32af9-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="32af9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="32af9-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="32af9-110">См. также</span><span class="sxs-lookup"><span data-stu-id="32af9-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="32af9-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="32af9-111">Example image</span></span>

<span data-ttu-id="32af9-112">На рисунке показано входные и выходные данные дискретного результата передачи.</span><span class="sxs-lookup"><span data-stu-id="32af9-112">The image here shows the input and output of the discrete transfer effect.</span></span>



| <span data-ttu-id="32af9-113">До</span><span class="sxs-lookup"><span data-stu-id="32af9-113">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)        |
| <span data-ttu-id="32af9-115">После</span><span class="sxs-lookup"><span data-stu-id="32af9-115">After</span></span>                                                             |
| ![изображение после преобразования.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="32af9-117">Функция перемещения основана на списке входных данных: V = (v0, v1, v2, v3, V?</span><span class="sxs-lookup"><span data-stu-id="32af9-117">The transfer function is based on the list of inputs: V=(V0,V1,V2,V3,V?</span></span> <span data-ttu-id="32af9-118">, V<sub>n</sub>), где N — число элементов-1.</span><span class="sxs-lookup"><span data-stu-id="32af9-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="32af9-119">Интенсивность входных пикселей представлена как C. Интенсивность выходных пикселов, C вычисляется с помощью уравнения:</span><span class="sxs-lookup"><span data-stu-id="32af9-119">The input pixel intensity is represented as C. The output pixel intensity, C  is calculated with the equation:</span></span>

<span data-ttu-id="32af9-120">Для значения C выберите значение k, например:</span><span class="sxs-lookup"><span data-stu-id="32af9-120">For a value C, pick a value k, such that:</span></span>

![Формула для процесса.](images/discrete-transfer1.png)

<span data-ttu-id="32af9-122">Выходные данные C можно вычислить с помощью уравнения: C ' = V?</span><span class="sxs-lookup"><span data-stu-id="32af9-122">The output C  can be calculated using the equation: C' = V?</span></span>

<span data-ttu-id="32af9-123">Этот результат работает с прямыми и предварительно умноженными альфа-образами.</span><span class="sxs-lookup"><span data-stu-id="32af9-123">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="32af9-124">Результат выводит предварительно умноженные альфа-точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="32af9-124">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="32af9-125">Вот как выглядит график дискретной функции перемещения, если входные данные имеют значение `[0.25, 0.5, 0.75, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="32af9-125">Here is what the graph of discrete transfer function looks like if the inputs are `[0.25, 0.5, 0.75, 1.0]`.</span></span>

![Диаграмма интенсивности пикселей для дискретной функции перемещения.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="32af9-127">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="32af9-127">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="32af9-128">Значения всех каналов дискретных свойств перемещения не поддерживают модуль и имеют не менее 0,0 и не более 1,0.</span><span class="sxs-lookup"><span data-stu-id="32af9-128">The values of all channels of the discrete transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="32af9-129">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="32af9-129">Display name and index enumeration</span></span>                                              | <span data-ttu-id="32af9-130">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="32af9-130">Type and default value</span></span>                       | <span data-ttu-id="32af9-131">Описание</span><span class="sxs-lookup"><span data-stu-id="32af9-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32af9-132">редтабле</span><span class="sxs-lookup"><span data-stu-id="32af9-132">RedTable</span></span><br/> <span data-ttu-id="32af9-133">D2D1 \_ дискрететрансфер \_ , \_ Красная \_ Таблица</span><span class="sxs-lookup"><span data-stu-id="32af9-133">D2D1\_DISCRETETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="32af9-134">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="32af9-134">FLOAT\[\]</span></span><br/> <span data-ttu-id="32af9-135">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="32af9-135">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="32af9-136">Список значений, используемых для определения функции передачи для красного канала.</span><span class="sxs-lookup"><span data-stu-id="32af9-136">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="32af9-137">реддисабле</span><span class="sxs-lookup"><span data-stu-id="32af9-137">RedDisable</span></span><br/> <span data-ttu-id="32af9-138">\_ \_ \_ Отключить красный D2D1 дискрететрансфер \_ prop</span><span class="sxs-lookup"><span data-stu-id="32af9-138">D2D1\_DISCRETETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="32af9-139">BOOL</span><span class="sxs-lookup"><span data-stu-id="32af9-139">BOOL</span></span><br/> <span data-ttu-id="32af9-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="32af9-140">FALSE</span></span><br/>             | <span data-ttu-id="32af9-141">Если присвоить этому параметру значение TRUE, функция передачи не будет применена к красному каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-141">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="32af9-142">Если присвоить этому параметру значение FALSE, то в результате функция Реддискрететрансфер будет применена к красному каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-142">If you set this to FALSE the effect applies the RedDiscreteTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="32af9-143">гринтабле</span><span class="sxs-lookup"><span data-stu-id="32af9-143">GreenTable</span></span><br/> <span data-ttu-id="32af9-144">\_ \_ \_ Зеленая таблица D2D1 дискрететрансфер \_ prop</span><span class="sxs-lookup"><span data-stu-id="32af9-144">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="32af9-145">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="32af9-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="32af9-146">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="32af9-146">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="32af9-147">Список значений, определяющих функцию передачи для зеленого канала.</span><span class="sxs-lookup"><span data-stu-id="32af9-147">The list of values that define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="32af9-148">гриндисабле</span><span class="sxs-lookup"><span data-stu-id="32af9-148">GreenDisable</span></span><br/> <span data-ttu-id="32af9-149">D2D1 \_ дискрететрансфер \_ , \_ зеленый \_ запрет</span><span class="sxs-lookup"><span data-stu-id="32af9-149">D2D1\_DISCRETETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="32af9-150">BOOL</span><span class="sxs-lookup"><span data-stu-id="32af9-150">BOOL</span></span><br/> <span data-ttu-id="32af9-151">FALSE</span><span class="sxs-lookup"><span data-stu-id="32af9-151">FALSE</span></span><br/>             | <span data-ttu-id="32af9-152">Если присвоить этому параметру значение TRUE, функция передачи не будет применена к зеленому каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-152">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="32af9-153">Если присвоить этому параметру значение FALSE, то в результате функция Гриндискрететрансфер будет применена к зеленому каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-153">If you set this to FALSE the effect applies the GreenDiscreteTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="32af9-154">блуетабле</span><span class="sxs-lookup"><span data-stu-id="32af9-154">BlueTable</span></span><br/> <span data-ttu-id="32af9-155">D2D1 \_ дискрететрансфер \_ prop, \_ синяя \_ Таблица</span><span class="sxs-lookup"><span data-stu-id="32af9-155">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="32af9-156">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="32af9-156">FLOAT\[\]</span></span><br/> <span data-ttu-id="32af9-157">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="32af9-157">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="32af9-158">Список значений, определяющих функцию передачи для синего канала.</span><span class="sxs-lookup"><span data-stu-id="32af9-158">The list of values that define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="32af9-159">блуедисабле</span><span class="sxs-lookup"><span data-stu-id="32af9-159">BlueDisable</span></span><br/> <span data-ttu-id="32af9-160">D2D1 \_ дискрететрансфер \_ prop \_ Blue, \_ Отключение</span><span class="sxs-lookup"><span data-stu-id="32af9-160">D2D1\_DISCRETETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="32af9-161">BOOL</span><span class="sxs-lookup"><span data-stu-id="32af9-161">BOOL</span></span><br/> <span data-ttu-id="32af9-162">FALSE</span><span class="sxs-lookup"><span data-stu-id="32af9-162">FALSE</span></span><br/>             | <span data-ttu-id="32af9-163">Если присвоить этому параметру значение TRUE, то функция передачи не будет применяться к синему каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-163">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="32af9-164">Если присвоить этому параметру значение FALSE, то в результате функция Блуедискрететрансфер будет применена к синему каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-164">If you set this to FALSE the effect applies the BlueDiscreteTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="32af9-165">алфатабле</span><span class="sxs-lookup"><span data-stu-id="32af9-165">AlphaTable</span></span><br/> <span data-ttu-id="32af9-166">\_Альфа- \_ \_ \_ Таблица D2D1 дискрететрансфер Prop</span><span class="sxs-lookup"><span data-stu-id="32af9-166">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>     | <span data-ttu-id="32af9-167">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="32af9-167">FLOAT\[\]</span></span><br/> <span data-ttu-id="32af9-168">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="32af9-168">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="32af9-169">Список значений, определяющих функцию передачи для альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="32af9-169">The list of values that define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="32af9-170">алфадисабле</span><span class="sxs-lookup"><span data-stu-id="32af9-170">AlphaDisable</span></span><br/> <span data-ttu-id="32af9-171">D2D1 \_ дискрететрансфер \_ prop \_ альфа- \_ Отключение</span><span class="sxs-lookup"><span data-stu-id="32af9-171">D2D1\_DISCRETETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="32af9-172">BOOL</span><span class="sxs-lookup"><span data-stu-id="32af9-172">BOOL</span></span><br/> <span data-ttu-id="32af9-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="32af9-173">FALSE</span></span><br/>             | <span data-ttu-id="32af9-174">Если присвоить этому параметру значение TRUE, то это не применяет функцию передачи к альфа-каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-174">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="32af9-175">Если присвоить этому параметру значение FALSE, то действие применяет функцию Алфадискрететрансфер к альфа-каналу.</span><span class="sxs-lookup"><span data-stu-id="32af9-175">If you set this to FALSE the effect applies the AlphaDiscreteTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="32af9-176">клампаутпут</span><span class="sxs-lookup"><span data-stu-id="32af9-176">ClampOutput</span></span><br/> <span data-ttu-id="32af9-177">\_ \_ \_ Выходные данные среза D2D1 дискрететрансфер \_</span><span class="sxs-lookup"><span data-stu-id="32af9-177">D2D1\_DISCRETETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="32af9-178">BOOL</span><span class="sxs-lookup"><span data-stu-id="32af9-178">BOOL</span></span><br/> <span data-ttu-id="32af9-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="32af9-179">FALSE</span></span><br/>             | <span data-ttu-id="32af9-180">Будет ли результат заменять цветовые значения в диапазоне от 0 до 1 перед тем, как результат передаст значения следующему результату в графе.</span><span class="sxs-lookup"><span data-stu-id="32af9-180">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="32af9-181">Этот результат выполняет фиксацию значений перед тем, как он умножает альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="32af9-181">The effect clamps the values before it premultiplies the alpha.</span></span><br/> <span data-ttu-id="32af9-182">Если присвоить этому параметру значение TRUE, то действие будет выполнять фиксацию значений.</span><span class="sxs-lookup"><span data-stu-id="32af9-182">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="32af9-183">Если присвоить этому параметру значение FALSE, то эффект не будет выполнять фиксацию цветовых значений, но другие эффекты и поверхность вывода могут попытаться отразить значения, если они не имеют достаточно высокой точности.</span><span class="sxs-lookup"><span data-stu-id="32af9-183">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32af9-184">Требования</span><span class="sxs-lookup"><span data-stu-id="32af9-184">Requirements</span></span>



| <span data-ttu-id="32af9-185">Требование</span><span class="sxs-lookup"><span data-stu-id="32af9-185">Requirement</span></span> | <span data-ttu-id="32af9-186">Значение</span><span class="sxs-lookup"><span data-stu-id="32af9-186">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32af9-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32af9-187">Minimum supported client</span></span> | <span data-ttu-id="32af9-188">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="32af9-188">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="32af9-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32af9-189">Minimum supported server</span></span> | <span data-ttu-id="32af9-190">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="32af9-190">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="32af9-191">Header</span><span class="sxs-lookup"><span data-stu-id="32af9-191">Header</span></span>                   | <span data-ttu-id="32af9-192">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="32af9-192">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="32af9-193">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32af9-193">Library</span></span>                  | <span data-ttu-id="32af9-194">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="32af9-194">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="32af9-195">См. также</span><span class="sxs-lookup"><span data-stu-id="32af9-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32af9-196">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="32af9-196">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

