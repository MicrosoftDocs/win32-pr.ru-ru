---
title: Гистограмма
description: Используйте эффекты гистограммы, чтобы создать гистограмму для входного точечного рисунка на основе указанного числа ячеек.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- Гистограмма
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415368"
---
# <a name="histogram-effect"></a><span data-ttu-id="38e01-104">Гистограмма</span><span class="sxs-lookup"><span data-stu-id="38e01-104">Histogram effect</span></span>

<span data-ttu-id="38e01-105">Используйте эффекты гистограммы, чтобы создать гистограмму для входного точечного рисунка на основе указанного числа ячеек.</span><span class="sxs-lookup"><span data-stu-id="38e01-105">Use the histogram effect to generate a histogram for the input bitmap based on the specified number of bins.</span></span>

<span data-ttu-id="38e01-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1Histogram.</span><span class="sxs-lookup"><span data-stu-id="38e01-106">The CLSID for this effect is CLSID\_D2D1Histogram.</span></span>

-   [<span data-ttu-id="38e01-107">Пример</span><span class="sxs-lookup"><span data-stu-id="38e01-107">Example</span></span>](#example)
-   [<span data-ttu-id="38e01-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="38e01-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="38e01-109">Селекторы каналов</span><span class="sxs-lookup"><span data-stu-id="38e01-109">Channel selectors</span></span>](#channel-selectors)
-   [<span data-ttu-id="38e01-110">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="38e01-110">Data output</span></span>](#data-output)
-   [<span data-ttu-id="38e01-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="38e01-111">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="38e01-112">Требования</span><span class="sxs-lookup"><span data-stu-id="38e01-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="38e01-113">См. также</span><span class="sxs-lookup"><span data-stu-id="38e01-113">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="38e01-114">Пример</span><span class="sxs-lookup"><span data-stu-id="38e01-114">Example</span></span>



| <span data-ttu-id="38e01-115">До</span><span class="sxs-lookup"><span data-stu-id="38e01-115">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg) |
| <span data-ttu-id="38e01-117">Диаграмма выходных данных гистограммы</span><span class="sxs-lookup"><span data-stu-id="38e01-117">Graph of the histogram output data</span></span>                         |
| ![изображение после преобразования.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a><span data-ttu-id="38e01-119">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="38e01-119">Effect properties</span></span>

<span data-ttu-id="38e01-120">Вот уравнение для создания выходных данных.</span><span class="sxs-lookup"><span data-stu-id="38e01-120">Here's the equation to generate the output.</span></span>

![Уравнение для формирования выходных данных для гистограммы.](images/histogram-formula.png)

<span data-ttu-id="38e01-122">*i* вычисляется от 0 до количества ячеек. Этот результат создает гистограмму для значений пикселей от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="38e01-122">*i* is evaluated from 0 to the number of bins. The effect generates a histogram for pixel values between 0 and 1.</span></span> <span data-ttu-id="38e01-123">Значения за пределами этого диапазона записываются в диапазон.</span><span class="sxs-lookup"><span data-stu-id="38e01-123">Values outside of this range are clamped to the range.</span></span> <span data-ttu-id="38e01-124">Диапазон конкретного контейнера зависит от количества сегментов.</span><span class="sxs-lookup"><span data-stu-id="38e01-124">The range of a particular bucket depends on the number of buckets.</span></span> <span data-ttu-id="38e01-125">Этот результат работает с прямыми растровыми пикселями.</span><span class="sxs-lookup"><span data-stu-id="38e01-125">This effect works on straight bitmap pixels.</span></span> <span data-ttu-id="38e01-126">Цветовые каналы входного точечного рисунка делятся на альфа-канал, чтобы вычислить этот результат.</span><span class="sxs-lookup"><span data-stu-id="38e01-126">The color channels of the input bitmap are divided by the alpha channel to compute this effect.</span></span>



| <span data-ttu-id="38e01-127">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="38e01-127">Display name and index enumeration</span></span>                                             | <span data-ttu-id="38e01-128">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="38e01-128">Type and default value</span></span>                                                   | <span data-ttu-id="38e01-129">Описание</span><span class="sxs-lookup"><span data-stu-id="38e01-129">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e01-130">нумбинс</span><span class="sxs-lookup"><span data-stu-id="38e01-130">NumBins</span></span><br/> <span data-ttu-id="38e01-131">\_ \_ \_ Число ячеек в D2D1 гистограммы \_</span><span class="sxs-lookup"><span data-stu-id="38e01-131">D2D1\_HISTOGRAM\_PROP\_NUM\_BINS</span></span><br/>                 | <span data-ttu-id="38e01-132">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="38e01-132">UINT32</span></span><br/> <span data-ttu-id="38e01-133">256</span><span class="sxs-lookup"><span data-stu-id="38e01-133">256</span></span><br/>                                         | <span data-ttu-id="38e01-134">Указывает количество ячеек, используемых для гистограммы.</span><span class="sxs-lookup"><span data-stu-id="38e01-134">Specifies the number of bins used for the histogram.</span></span> <span data-ttu-id="38e01-135">Диапазон значений интенсивности, попавших в определенный контейнер, зависит от числа указанных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="38e01-135">The range of intensity values that fall into a particular bucket depend on the number of specified buckets.</span></span>                              |
| <span data-ttu-id="38e01-136">чаннелселект</span><span class="sxs-lookup"><span data-stu-id="38e01-136">ChannelSelect</span></span><br/> <span data-ttu-id="38e01-137">\_ \_ \_ Выбор канала Prop гистограммы D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="38e01-137">D2D1\_HISTOGRAM\_PROP\_CHANNEL\_SELECT</span></span><br/>     | <span data-ttu-id="38e01-138">\_Выбор канала \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="38e01-138">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="38e01-139">\_Выбор канала \_ D2D1 \_ R</span><span class="sxs-lookup"><span data-stu-id="38e01-139">D2D1\_CHANNEL\_SELECTOR\_R</span></span><br/> | <span data-ttu-id="38e01-140">Указывает канал, используемый для создания гистограммы.</span><span class="sxs-lookup"><span data-stu-id="38e01-140">Specifies the channel used to generate the histogram.</span></span> <span data-ttu-id="38e01-141">Этот результат имеет один выход данных, соответствующий указанному каналу.</span><span class="sxs-lookup"><span data-stu-id="38e01-141">This effect has a single data output corresponding to the specified channel.</span></span> <span data-ttu-id="38e01-142">Дополнительные сведения см. в разделе [Селекторы каналов](#channel-selectors) .</span><span class="sxs-lookup"><span data-stu-id="38e01-142">See [Channel selectors](#channel-selectors) for more info.</span></span> |
| <span data-ttu-id="38e01-143">хистограмаутпут</span><span class="sxs-lookup"><span data-stu-id="38e01-143">HistogramOutput</span></span><br/> <span data-ttu-id="38e01-144">\_ \_ \_ Выходные данные гистограммы свойств D2D1 гистограммы \_</span><span class="sxs-lookup"><span data-stu-id="38e01-144">D2D1\_HISTOGRAM\_PROP\_HISTOGRAM\_OUTPUT</span></span><br/> | <span data-ttu-id="38e01-145">СДЕЛАТЬ\[\]</span><span class="sxs-lookup"><span data-stu-id="38e01-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="38e01-146">Только свойство Output.</span><span class="sxs-lookup"><span data-stu-id="38e01-146">Output property only.</span></span><br/>                    | <span data-ttu-id="38e01-147">Выходной массив.</span><span class="sxs-lookup"><span data-stu-id="38e01-147">The output array.</span></span>                                                                                                                                                                             |



 

## <a name="channel-selectors"></a><span data-ttu-id="38e01-148">Селекторы каналов</span><span class="sxs-lookup"><span data-stu-id="38e01-148">Channel selectors</span></span>



| <span data-ttu-id="38e01-149">Перечисление</span><span class="sxs-lookup"><span data-stu-id="38e01-149">Enumeration</span></span>                | <span data-ttu-id="38e01-150">Описание</span><span class="sxs-lookup"><span data-stu-id="38e01-150">Description</span></span>                                                           |
|----------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="38e01-151">\_Выбор канала \_ D2D1 \_ R</span><span class="sxs-lookup"><span data-stu-id="38e01-151">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="38e01-152">Результат создает гистограмму на основе красного канала.</span><span class="sxs-lookup"><span data-stu-id="38e01-152">The effect generates the histogram output based on the red channel.</span></span>   |
| <span data-ttu-id="38e01-153">\_Селектор канала \_ D2D1 \_ G</span><span class="sxs-lookup"><span data-stu-id="38e01-153">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="38e01-154">Результат создает гистограмму на основе зеленого канала.</span><span class="sxs-lookup"><span data-stu-id="38e01-154">The effect generates the histogram output based on the green channel.</span></span> |
| <span data-ttu-id="38e01-155">\_Селектор каналов \_ D2D1 \_ B</span><span class="sxs-lookup"><span data-stu-id="38e01-155">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="38e01-156">Результат создает гистограмму на основе синего канала.</span><span class="sxs-lookup"><span data-stu-id="38e01-156">The effect generates the histogram output based on the blue channel.</span></span>  |
| <span data-ttu-id="38e01-157">\_Селектор каналов \_ D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="38e01-157">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="38e01-158">Результат создает гистограмму на основе альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="38e01-158">The effect generates the histogram output based on the alpha channel.</span></span> |



 

## <a name="data-output"></a><span data-ttu-id="38e01-159">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="38e01-159">Data output</span></span>

<span data-ttu-id="38e01-160">Этот результат выводит число с плавающей запятой \[ \] с количеством элементов, соответствующим количеству указанных ячеек. Каждый элемент в FLOAT \[ \] имеет тип float.</span><span class="sxs-lookup"><span data-stu-id="38e01-160">This effect outputs a FLOAT\[\], with the number of elements corresponding to the number of specified bins. Each element in the FLOAT\[\] is a float.</span></span> <span data-ttu-id="38e01-161">Значение элемента соответствует количеству элементов в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="38e01-161">The value of the element corresponds to the number of elements in that bin.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e01-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38e01-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="38e01-163">Метод [**креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) завершается ошибкой, если устройство не поддерживает DirectCompute и возвращает HRESULT = D2DERR \_ недостаточные \_ \_ возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="38e01-163">The [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method fails if the device doesn't support DirectCompute and returns HRESULT = D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES.</span></span> <span data-ttu-id="38e01-164">Все карточки DirectX11 и карты DirectX10, поддерживающие DirectCompute, могут использовать этот результат.</span><span class="sxs-lookup"><span data-stu-id="38e01-164">All DirectX11 cards and DirectX10 cards that support DirectCompute can use the effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38e01-165">Требования</span><span class="sxs-lookup"><span data-stu-id="38e01-165">Requirements</span></span>



| <span data-ttu-id="38e01-166">Требование</span><span class="sxs-lookup"><span data-stu-id="38e01-166">Requirement</span></span> | <span data-ttu-id="38e01-167">Значение</span><span class="sxs-lookup"><span data-stu-id="38e01-167">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38e01-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38e01-168">Minimum supported client</span></span> | <span data-ttu-id="38e01-169">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="38e01-169">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="38e01-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38e01-170">Minimum supported server</span></span> | <span data-ttu-id="38e01-171">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="38e01-171">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="38e01-172">Header</span><span class="sxs-lookup"><span data-stu-id="38e01-172">Header</span></span>                   | <span data-ttu-id="38e01-173">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="38e01-173">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="38e01-174">Библиотека</span><span class="sxs-lookup"><span data-stu-id="38e01-174">Library</span></span>                  | <span data-ttu-id="38e01-175">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="38e01-175">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="38e01-176">См. также</span><span class="sxs-lookup"><span data-stu-id="38e01-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38e01-177">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="38e01-177">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

