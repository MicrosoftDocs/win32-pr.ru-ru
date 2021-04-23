---
title: эффект трехмерной таблицы подстановки
description: Таблица с трехмерным поиском — это эффект общего назначения, который используется для инкапсуляции любого эффектного создания образа 1 1 путем предварительного вычисления того, как эффект сопоставляет входные данные с выходами для подмножества всех входных значений.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0c6c5df1aa873d3458345d77a46f6f3fdae40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892777"
---
# <a name="3d-lookup-table-effect"></a><span data-ttu-id="fc9b4-103">эффект трехмерной таблицы подстановки</span><span class="sxs-lookup"><span data-stu-id="fc9b4-103">3D lookup table effect</span></span>

<span data-ttu-id="fc9b4-104">Таблица с трехмерным поиском — это эффект общего назначения, который используется для инкапсуляции любого эффектного создания образа 1:1 путем предварительного вычисления того, как эффект сопоставляет входные данные с выходами для подмножества всех входных значений.</span><span class="sxs-lookup"><span data-stu-id="fc9b4-104">A 3D look-up table is a general-purpose effect that is used to encapsulate any 1:1 imaging effect by pre-computing how the effect maps inputs to outputs for a subset of all input values.</span></span>

<span data-ttu-id="fc9b4-105">Эффект 3D-таблицы подстановки (LUT) изменяет входной образ, используя значение цвета RGB изображения для индексирования трехмерной текстуры, где текстура содержит предварительно вычисленное выходное значение для конвейера произвольных эффектов.</span><span class="sxs-lookup"><span data-stu-id="fc9b4-105">The 3D Lookup Table (LUT) effect modifies an input image by using the image's RGB color value to index a 3D texture, where the texture contains a precomputed output value of an arbitrary effect pipeline.</span></span>

<span data-ttu-id="fc9b4-106">Трехмерный LUT должен быть загружен в ресурс текстуры GPU для подготовки к просмотру, и это может быть дорогостоящим в зависимости от размера текстуры и возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="fc9b4-106">The 3D LUT must be loaded into a GPU texture resource in order to be rendered, and this can be expensive depending on the size of the texture and the device capabilities.</span></span> <span data-ttu-id="fc9b4-107">Разработчики приложений могут указать, когда следует платить за эту стоимость с помощью ресурса D2D [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) .</span><span class="sxs-lookup"><span data-stu-id="fc9b4-107">Application developers can specify when to pay this cost using the [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D resource.</span></span> <span data-ttu-id="fc9b4-108">**ID2D1LookupTable3D** имеет следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="fc9b4-108">**ID2D1LookupTable3D** has the following attributes:</span></span>

-   <span data-ttu-id="fc9b4-109">Предоставляет абстрактное представление ресурса GPU трехмерного LUT.</span><span class="sxs-lookup"><span data-stu-id="fc9b4-109">Provides an abstracted representation of 3D LUT's GPU resource.</span></span>
-   <span data-ttu-id="fc9b4-110">В зависимости от возможностей устройства будет создана либо двухмерная, либо трехмерная текстура, которая заполняется предоставленными данными LUT.</span><span class="sxs-lookup"><span data-stu-id="fc9b4-110">Depending on the device capabilities, either a 2D or 3D texture will be created and filled with the provided LUT data.</span></span>
-   <span data-ttu-id="fc9b4-111">Может передаваться в свойство LUT эффект 3D для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fc9b4-111">Can be passed to the 3D LUT effect's property for rendering.</span></span>

<span data-ttu-id="fc9b4-112">Идентификатором CLSID для этого действия является CLSID \_ D2D1LookupTable3D.</span><span class="sxs-lookup"><span data-stu-id="fc9b4-112">The CLSID for this effect is CLSID\_D2D1LookupTable3D.</span></span>

-   [<span data-ttu-id="fc9b4-113">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="fc9b4-113">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="fc9b4-114">Образец кода</span><span class="sxs-lookup"><span data-stu-id="fc9b4-114">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="fc9b4-115">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="fc9b4-115">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="fc9b4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fc9b4-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="fc9b4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="fc9b4-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="fc9b4-118">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="fc9b4-118">Example image</span></span>

![Пример выходных данных эффектов](images/3dlookuptable-effect.png)

## <a name="sample-code"></a><span data-ttu-id="fc9b4-120">Пример кода</span><span class="sxs-lookup"><span data-stu-id="fc9b4-120">Sample code</span></span>

```cpp
//
    // 1. Generate the lookup table data and create an ID2D1LookupTable3D.
    //
 
    // Create a 16x16x16 LUT of arbitrary data type T.
    UINT extents[] = { 16, 16, 16 };
    UINT cElements = extents[0] * extents[1] * extents[2] * 4;
    UINT cbElements = cElements * formatSize;
 
    // Compute the step size in each direction to vary the RGB 
    // channels uniformly over the range [0, 1]
    float steps[] = 
    { 
        1.0f / static_cast<float>(extents[0] - 1),
        1.0f / static_cast<float>(extents[1] - 1),
        1.0f / static_cast<float>(extents[2] - 1),
    };
 
    CArray<BYTE> lutData;
    IFR(lutData.Resize(cbElements));
 
    T* pData = reinterpret_cast<T *>(lutData.GetData());
    T oneValue = ConvertValue<T>(1.0f);
    
    // Generate the LUT by applying an imaging pipeline to RGB values.
    for (UINT iR = 0; iR < extents[2]; iR++)
    {
        for (UINT iG = 0; iG < extents[1]; iG++)
        {
            for (UINT iB = 0; iB < extents[0]; iB++)
            {
                T outputColor[3];
                ApplyPipeline(iR * steps[2], iG * steps[1], iB * steps[0], &outputColor);
 
                pData[0] = outColor[0];
                pData[1] = outColor[1];
                pData[2] = outColor[2];
 
                // Set opaque alpha in the output
                pData[3] = oneValue;
 
                // Advance the pointer
                pData += sizeof(T) * 4;
            }
        }
    }
    
    // Compute the strides of the LUT data.
    UINT strides[2];
    IFR(UIntMult(sizeof(T) * 4, extents[0], &strides[0]));
    IFR(UIntMult(strides[0], extents[1], &strides[1]));
    
    D2D1_BUFFER_PRECISION precision = GetBufferPrecision<T>();
 
    // Create an ID2D1LookupTable3D from the LUT data.
    CComPtr<ID2D1LookupTable3D> sp3dLut;
    IFR(_spEffectContext1->CreateLookupTable3D(
        precision,
        extents,
        lutData.GetData(),
        lutData.GetCount(),
        strides,
        &sp3dLut
        )); 
 
    //
    // 2. To apply the lookup table to an input image, create a LookupTable3D effect
    //    and pass the ID2D1LookupTable3D to the effect as a property.
    //
 
    // Create a 3D LUT effect to render our LUT.
    CComPtr<ID2D1Effect> sp3dLutEffect;
    IFR(pEffectContext->CreateEffect(CLSID_D2D1LookupTable3D, &sp3dLutEffect)); 
 
    // Set the LUT as a property on the effect.
    IFR(sp3dLutEffect->SetValue(D2D1_LOOKUPTABLE3D_PROP_LUT, _spLut));
```

## <a name="effect-properties"></a><span data-ttu-id="fc9b4-121">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="fc9b4-121">Effect properties</span></span>

<span data-ttu-id="fc9b4-122">Свойства для результата «таблица уточняющих запросов» определяются перечислением [**D2D1 \_ LOOKUPTABLE3D- \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) .</span><span class="sxs-lookup"><span data-stu-id="fc9b4-122">The properties for the 3D lookup table effect are defined by the [**D2D1\_LOOKUPTABLE3D\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc9b4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fc9b4-123">Requirements</span></span>



| <span data-ttu-id="fc9b4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fc9b4-124">Requirement</span></span> | <span data-ttu-id="fc9b4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fc9b4-125">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="fc9b4-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc9b4-126">Minimum supported client</span></span> | <span data-ttu-id="fc9b4-127">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="fc9b4-127">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fc9b4-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc9b4-128">Minimum supported server</span></span> | <span data-ttu-id="fc9b4-129">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="fc9b4-129">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fc9b4-130">Header</span><span class="sxs-lookup"><span data-stu-id="fc9b4-130">Header</span></span>                   | <span data-ttu-id="fc9b4-131">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="fc9b4-131">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="fc9b4-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc9b4-132">Library</span></span>                  | <span data-ttu-id="fc9b4-133">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="fc9b4-133">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="fc9b4-134">См. также</span><span class="sxs-lookup"><span data-stu-id="fc9b4-134">Related topics</span></span>

* [<span data-ttu-id="fc9b4-135">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="fc9b4-135">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
