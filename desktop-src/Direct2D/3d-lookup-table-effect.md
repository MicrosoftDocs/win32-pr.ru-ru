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
# <a name="3d-lookup-table-effect"></a>эффект трехмерной таблицы подстановки

Таблица с трехмерным поиском — это эффект общего назначения, который используется для инкапсуляции любого эффектного создания образа 1:1 путем предварительного вычисления того, как эффект сопоставляет входные данные с выходами для подмножества всех входных значений.

Эффект 3D-таблицы подстановки (LUT) изменяет входной образ, используя значение цвета RGB изображения для индексирования трехмерной текстуры, где текстура содержит предварительно вычисленное выходное значение для конвейера произвольных эффектов.

Трехмерный LUT должен быть загружен в ресурс текстуры GPU для подготовки к просмотру, и это может быть дорогостоящим в зависимости от размера текстуры и возможностей устройства. Разработчики приложений могут указать, когда следует платить за эту стоимость с помощью ресурса D2D [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) . **ID2D1LookupTable3D** имеет следующие атрибуты:

-   Предоставляет абстрактное представление ресурса GPU трехмерного LUT.
-   В зависимости от возможностей устройства будет создана либо двухмерная, либо трехмерная текстура, которая заполняется предоставленными данными LUT.
-   Может передаваться в свойство LUT эффект 3D для отрисовки.

Идентификатором CLSID для этого действия является CLSID \_ D2D1LookupTable3D.

-   [Пример изображения](#example-image)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [См. также](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/3dlookuptable-effect.png)

## <a name="sample-code"></a>Пример кода

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

## <a name="effect-properties"></a>Свойства эффектов

Свойства для результата «таблица уточняющих запросов» определяются перечислением [**D2D1 \_ LOOKUPTABLE3D- \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Минимальная версия сервера | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |

## <a name="related-topics"></a>См. также

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
