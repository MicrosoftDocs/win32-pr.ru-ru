---
title: Действие перемещения таблицы
description: Используйте перенос таблицы, чтобы связать цвет интенситиес изображения с помощью функции передачи, созданной при интерполяции предоставленного списка значений.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- действие перемещения таблицы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490644"
---
# <a name="table-transfer-effect"></a><span data-ttu-id="5612e-104">Действие перемещения таблицы</span><span class="sxs-lookup"><span data-stu-id="5612e-104">Table transfer effect</span></span>

<span data-ttu-id="5612e-105">Используйте перенос таблицы, чтобы связать цвет интенситиес изображения с помощью функции передачи, созданной при интерполяции предоставленного списка значений.</span><span class="sxs-lookup"><span data-stu-id="5612e-105">Use the table transfer effect to map the color intensities of an image using a transfer function created from interpolating a list of values you provide.</span></span>

<span data-ttu-id="5612e-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1TableTransfer.</span><span class="sxs-lookup"><span data-stu-id="5612e-106">The CLSID for this effect is CLSID\_D2D1TableTransfer.</span></span>

-   [<span data-ttu-id="5612e-107">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="5612e-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="5612e-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="5612e-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5612e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="5612e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5612e-110">См. также</span><span class="sxs-lookup"><span data-stu-id="5612e-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5612e-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="5612e-111">Example image</span></span>

<span data-ttu-id="5612e-112">На рисунке показано входные и выходные данные влияния передачи таблицы.</span><span class="sxs-lookup"><span data-stu-id="5612e-112">The image here shows the input and output of the table transfer effect.</span></span>



| <span data-ttu-id="5612e-113">До</span><span class="sxs-lookup"><span data-stu-id="5612e-113">Before</span></span>                                                         |
|----------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)     |
| <span data-ttu-id="5612e-115">После</span><span class="sxs-lookup"><span data-stu-id="5612e-115">After</span></span>                                                          |
| ![изображение после преобразования.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="5612e-117">Функция перемещения основана на списке входных данных V = (v0, v1, v2, v3, V?</span><span class="sxs-lookup"><span data-stu-id="5612e-117">The transfer function is based on a list of inputs V=(V0,V1,V2,V3, V?</span></span> <span data-ttu-id="5612e-118">, V<sub>n</sub>), где N — число элементов-1.</span><span class="sxs-lookup"><span data-stu-id="5612e-118">,V<sub>N</sub>) where N is the number of elements - 1.</span></span>

<span data-ttu-id="5612e-119">Интенсивность входных пикселей представлена как C. Интенсивность выходных пикселов, C может быть рассчитана с помощью уравнения.</span><span class="sxs-lookup"><span data-stu-id="5612e-119">The input pixel intensity is represented as C. The output pixel intensity, C  can be calculated with the equation.</span></span>

<span data-ttu-id="5612e-120">Для значения C выберите значение k, например: k/N = C < (k + 1)/N</span><span class="sxs-lookup"><span data-stu-id="5612e-120">For a value C, pick a value k, such that: k/N = C < (k+1)/N</span></span>

<span data-ttu-id="5612e-121">Выходные данные C рассчитываются с использованием следующего уравнения: C ' = V?</span><span class="sxs-lookup"><span data-stu-id="5612e-121">The output C  is calculated using the following equation: C' = V?</span></span> <span data-ttu-id="5612e-122">+ (C-k/N) \* N \* (V??? одного?</span><span class="sxs-lookup"><span data-stu-id="5612e-122">+ (C -  k/N) \* N \* (V???1?</span></span> <span data-ttu-id="5612e-123">-V?)</span><span class="sxs-lookup"><span data-stu-id="5612e-123">- V?)</span></span>

<span data-ttu-id="5612e-124">Этот результат работает с прямыми и предварительно умноженными альфа-образами.</span><span class="sxs-lookup"><span data-stu-id="5612e-124">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="5612e-125">Результат выводит предварительно умноженные альфа-точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="5612e-125">The effect outputs premultiplied alpha bitmaps.</span></span>

<span data-ttu-id="5612e-126">Вот как выглядит график функции перемещения таблиц, если свойство Table имеет значение `[0.0, 0.25, 1.0]` .</span><span class="sxs-lookup"><span data-stu-id="5612e-126">Here is what the graph of table transfer function looks like if the table property is set to `[0.0, 0.25, 1.0]`.</span></span>

![Диаграмма интенсивности пикселей для функции перемещения таблиц.](images/table-transfer-graph.png)

## <a name="effect-properties"></a><span data-ttu-id="5612e-128">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="5612e-128">Effect properties</span></span>

> [!Note]  
> <span data-ttu-id="5612e-129">Значения всех каналов в свойствах перенаправления таблицы не поддерживают модуль и имеют не менее 0,0 и не более 1,0.</span><span class="sxs-lookup"><span data-stu-id="5612e-129">The values of all channels of the table transfer properties are unitless and have a minimum of 0.0 and a maximum 1.0.</span></span>

 



| <span data-ttu-id="5612e-130">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="5612e-130">Display name and index enumeration</span></span>                                           | <span data-ttu-id="5612e-131">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5612e-131">Type and default value</span></span>                       | <span data-ttu-id="5612e-132">Описание</span><span class="sxs-lookup"><span data-stu-id="5612e-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5612e-133">редтабле</span><span class="sxs-lookup"><span data-stu-id="5612e-133">RedTable</span></span><br/> <span data-ttu-id="5612e-134">D2D1 \_ таблетрансфер \_ , \_ Красная \_ Таблица</span><span class="sxs-lookup"><span data-stu-id="5612e-134">D2D1\_TABLETRANSFER\_PROP\_RED\_TABLE</span></span><br/>         | <span data-ttu-id="5612e-135">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="5612e-135">FLOAT\[\]</span></span><br/> <span data-ttu-id="5612e-136">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="5612e-136">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="5612e-137">Список значений, используемых для определения функции передачи для красного канала.</span><span class="sxs-lookup"><span data-stu-id="5612e-137">The list of values used to define the transfer function for the Red channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5612e-138">реддисабле</span><span class="sxs-lookup"><span data-stu-id="5612e-138">RedDisable</span></span><br/> <span data-ttu-id="5612e-139">\_ \_ \_ Отключить красный D2D1 таблетрансфер \_ prop</span><span class="sxs-lookup"><span data-stu-id="5612e-139">D2D1\_TABLETRANSFER\_PROP\_RED\_DISABLE</span></span><br/>     | <span data-ttu-id="5612e-140">BOOL</span><span class="sxs-lookup"><span data-stu-id="5612e-140">BOOL</span></span><br/> <span data-ttu-id="5612e-141">FALSE</span><span class="sxs-lookup"><span data-stu-id="5612e-141">FALSE</span></span><br/>             | <span data-ttu-id="5612e-142">Если присвоить этому параметру значение TRUE, функция передачи не будет применена к красному каналу.</span><span class="sxs-lookup"><span data-stu-id="5612e-142">If you set this to TRUE the effect does not apply the transfer function to the Red channel.</span></span> <span data-ttu-id="5612e-143">Если присвоить этому параметру значение FALSE, функция Редтаблетрансфер будет применена к красному каналу.</span><span class="sxs-lookup"><span data-stu-id="5612e-143">If you set this to FALSE it applies the RedTableTransfer function to the Red channel.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5612e-144">гринтабле</span><span class="sxs-lookup"><span data-stu-id="5612e-144">GreenTable</span></span><br/> <span data-ttu-id="5612e-145">\_ \_ \_ Зеленая таблица D2D1 таблетрансфер \_ prop</span><span class="sxs-lookup"><span data-stu-id="5612e-145">D2D1\_TABLETRANSFER\_PROP\_GREEN\_TABLE</span></span><br/>     | <span data-ttu-id="5612e-146">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="5612e-146">FLOAT\[\]</span></span><br/> <span data-ttu-id="5612e-147">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="5612e-147">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="5612e-148">Список значений, используемых для определения функции передачи для зеленого канала.</span><span class="sxs-lookup"><span data-stu-id="5612e-148">The list of values used to define the transfer function for the Green channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5612e-149">гриндисабле</span><span class="sxs-lookup"><span data-stu-id="5612e-149">GreenDisable</span></span><br/> <span data-ttu-id="5612e-150">D2D1 \_ таблетрансфер \_ , \_ зеленый \_ запрет</span><span class="sxs-lookup"><span data-stu-id="5612e-150">D2D1\_TABLETRANSFER\_PROP\_GREEN\_DISABLE</span></span><br/> | <span data-ttu-id="5612e-151">BOOL</span><span class="sxs-lookup"><span data-stu-id="5612e-151">BOOL</span></span><br/> <span data-ttu-id="5612e-152">FALSE</span><span class="sxs-lookup"><span data-stu-id="5612e-152">FALSE</span></span><br/>             | <span data-ttu-id="5612e-153">Если присвоить этому параметру значение TRUE, функция передачи не будет применена к зеленому каналу.</span><span class="sxs-lookup"><span data-stu-id="5612e-153">If you set this to TRUE the effect does not apply the transfer function to the Green channel.</span></span> <span data-ttu-id="5612e-154">Если присвоить этому параметру значение FALSE, функция Гринтаблетрансфер будет применена к зеленому каналу.</span><span class="sxs-lookup"><span data-stu-id="5612e-154">If you set this to FALSE it applies the GreenTableTransfer function to the Green channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="5612e-155">блуетабле</span><span class="sxs-lookup"><span data-stu-id="5612e-155">BlueTable</span></span><br/> <span data-ttu-id="5612e-156">D2D1 \_ таблетрансфер \_ prop, \_ синяя \_ Таблица</span><span class="sxs-lookup"><span data-stu-id="5612e-156">D2D1\_TABLETRANSFER\_PROP\_BLUE\_TABLE</span></span><br/>       | <span data-ttu-id="5612e-157">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="5612e-157">FLOAT\[\]</span></span><br/> <span data-ttu-id="5612e-158">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="5612e-158">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="5612e-159">Список значений, используемых для определения функции передачи для синего канала.</span><span class="sxs-lookup"><span data-stu-id="5612e-159">The list of values used to define the transfer function for the Blue channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5612e-160">блуедисабле</span><span class="sxs-lookup"><span data-stu-id="5612e-160">BlueDisable</span></span><br/> <span data-ttu-id="5612e-161">D2D1 \_ таблетрансфер \_ prop \_ Blue, \_ Отключение</span><span class="sxs-lookup"><span data-stu-id="5612e-161">D2D1\_TABLETRANSFER\_PROP\_BLUE\_DISABLE</span></span><br/>   | <span data-ttu-id="5612e-162">BOOL</span><span class="sxs-lookup"><span data-stu-id="5612e-162">BOOL</span></span><br/> <span data-ttu-id="5612e-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="5612e-163">FALSE</span></span><br/>             | <span data-ttu-id="5612e-164">Если присвоить этому параметру значение TRUE, то функция передачи не будет применяться к синему каналу.</span><span class="sxs-lookup"><span data-stu-id="5612e-164">If you set this to TRUE the effect does not apply the transfer function to the Blue channel.</span></span> <span data-ttu-id="5612e-165">Если присвоить этому параметру значение FALSE, то функция Блуетаблетрансфер будет применена к синему каналу.</span><span class="sxs-lookup"><span data-stu-id="5612e-165">If you set this to FALSE it applies the BlueTableTransfer function to the Blue channel.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5612e-166">алфатабле</span><span class="sxs-lookup"><span data-stu-id="5612e-166">AlphaTable</span></span><br/> <span data-ttu-id="5612e-167">\_Альфа- \_ \_ \_ Таблица "Prop \_ " таблицы D2D1</span><span class="sxs-lookup"><span data-stu-id="5612e-167">D2D1\_TABLE\_TRANSFER\_PROP\_ALPHA\_TABLE</span></span><br/>   | <span data-ttu-id="5612e-168">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="5612e-168">FLOAT\[\]</span></span><br/> <span data-ttu-id="5612e-169">{0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="5612e-169">{0.0f, 1.0f}</span></span><br/> | <span data-ttu-id="5612e-170">Список значений, используемых для определения функции передачи для альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="5612e-170">The list of values used to define the transfer function for the Alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5612e-171">алфадисабле</span><span class="sxs-lookup"><span data-stu-id="5612e-171">AlphaDisable</span></span><br/> <span data-ttu-id="5612e-172">D2D1 \_ таблетрансфер \_ prop \_ альфа- \_ Отключение</span><span class="sxs-lookup"><span data-stu-id="5612e-172">D2D1\_TABLETRANSFER\_PROP\_ALPHA\_DISABLE</span></span><br/> | <span data-ttu-id="5612e-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="5612e-173">BOOL</span></span><br/> <span data-ttu-id="5612e-174">FALSE</span><span class="sxs-lookup"><span data-stu-id="5612e-174">FALSE</span></span><br/>             | <span data-ttu-id="5612e-175">Если присвоить этому параметру значение TRUE, то это не применяет функцию передачи к альфа-каналу.</span><span class="sxs-lookup"><span data-stu-id="5612e-175">If you set this to TRUE the effect does not apply the transfer function to the Alpha channel.</span></span> <span data-ttu-id="5612e-176">Если задано значение FALSE, то к альфа-каналу применяется функция Алфатаблетрансфер.</span><span class="sxs-lookup"><span data-stu-id="5612e-176">If you set this to FALSE it applies the AlphaTableTransfer function to the Alpha channel.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="5612e-177">клампаутпут</span><span class="sxs-lookup"><span data-stu-id="5612e-177">ClampOutput</span></span><br/> <span data-ttu-id="5612e-178">\_ \_ \_ Выходные данные среза D2D1 таблетрансфер \_</span><span class="sxs-lookup"><span data-stu-id="5612e-178">D2D1\_TABLETRANSFER\_PROP\_CLAMP\_OUTPUT</span></span><br/>   | <span data-ttu-id="5612e-179">BOOL</span><span class="sxs-lookup"><span data-stu-id="5612e-179">BOOL</span></span><br/> <span data-ttu-id="5612e-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="5612e-180">FALSE</span></span><br/>             | <span data-ttu-id="5612e-181">Будет ли результат заменять цветовые значения в диапазоне от 0 до 1 перед тем, как результат передаст значения следующему результату в графе.</span><span class="sxs-lookup"><span data-stu-id="5612e-181">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="5612e-182">Этот результат выполняет фиксацию значений перед тем, как он умножает альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="5612e-182">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="5612e-183">Если присвоить этому параметру значение TRUE, то действие будет выполнять фиксацию значений.</span><span class="sxs-lookup"><span data-stu-id="5612e-183">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="5612e-184">Если присвоить этому параметру значение FALSE, то эффект не будет выполнять фиксацию цветовых значений, но другие эффекты и поверхность вывода могут попытаться отразить значения, если они не имеют достаточно высокой точности.</span><span class="sxs-lookup"><span data-stu-id="5612e-184">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5612e-185">Требования</span><span class="sxs-lookup"><span data-stu-id="5612e-185">Requirements</span></span>



| <span data-ttu-id="5612e-186">Требование</span><span class="sxs-lookup"><span data-stu-id="5612e-186">Requirement</span></span> | <span data-ttu-id="5612e-187">Значение</span><span class="sxs-lookup"><span data-stu-id="5612e-187">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5612e-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5612e-188">Minimum supported client</span></span> | <span data-ttu-id="5612e-189">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="5612e-189">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5612e-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5612e-190">Minimum supported server</span></span> | <span data-ttu-id="5612e-191">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="5612e-191">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5612e-192">Header</span><span class="sxs-lookup"><span data-stu-id="5612e-192">Header</span></span>                   | <span data-ttu-id="5612e-193">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="5612e-193">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="5612e-194">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5612e-194">Library</span></span>                  | <span data-ttu-id="5612e-195">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="5612e-195">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="5612e-196">См. также</span><span class="sxs-lookup"><span data-stu-id="5612e-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5612e-197">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="5612e-197">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

