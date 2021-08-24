---
title: Правила упаковки для константных переменных
description: Правила упаковки определяют, насколько тесно данные могут быть упорядочены при их хранении.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49b10f6383344821c7659ac40b367a77e0421d33be68a374c59920a62d37697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120088"
---
# <a name="packing-rules-for-constant-variables"></a>Правила упаковки для константных переменных

Правила упаковки определяют, насколько тесно данные могут быть упорядочены при их хранении. HLSL реализует правила упаковки для выходных данных VS, входные и выходные данные GS и входные и выходные данные PS. (Данные не упаковываются для входных данных VS, так как на этапе IA не удается распаковать данные.)

правила упаковки HLSL похожи на выполнение **\# директивы pragma pack 4** с Visual Studio, который упаковывает данные в 4-байтовые границы. Кроме того, HLSL упаковывает данные таким образом, чтобы они не пересекали 16-байтовую границу. Переменные упаковываются в данный вектор с четырьмя компонентами до тех пор, пока переменная не получит 4-векторную границу. следующие переменные будут передаваться на следующий вектор с четырьмя компонентами.

Каждая структура принудительно запускает следующую переменную в следующем векторе из четырех компонентов. Иногда это приводит к созданию заполнения для массивов структур. Итоговый размер любой структуры всегда будет равномерно кратен **sizeof**(*вектор с четырьмя компонентами*).

По умолчанию массивы не упаковываются в HLSL. Во избежание принудительного использования шейдера с незначительными издержками для смещенных вычислений каждый элемент массива хранится в векторе из четырех компонентов. Обратите внимание, что можно выполнить упаковку для массивов (и вычисление адресов) с помощью приведения.

Ниже приведены примеры структур и их соответствующих упакованных размеров (заданный: **float1** занимает 4 байта):


```
//  2 x 16byte elements
cbuffer IE
{
    float4 Val1;
    float2 Val2;  // starts a new vector
    float2 Val3;
};

//  3 x 16byte elements
cbuffer IE
{
    float2 Val1;
    float4 Val2;  // starts a new vector
    float2 Val3;  // starts a new vector
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val2;
    float2 Val3;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float2 Val2;
    float1 Val3;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float1 Val1;
    float2 Val2;    // starts a new vector
};


//  1 x 16byte elements
cbuffer IE
{
    float3 Val1;
    float1 Val2;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float3 Val2;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float3 Val2;        // starts a new vector
};


// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;

    struct     {
        float4 SVal1;    // starts a new vector
        float1 SVal2;    // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;  
    struct     {
        float1 SVal1;     // starts a new vector
        float4 SVal2;     // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    struct     {
        float4 SVal1;
        float1 SVal2;    // starts a new vector
    } Val1;

    float1 Val2; 
};
```



## <a name="more-aggressive-packing"></a>Более агрессивная упаковка

Массив можно упаковать более агрессивно. Например, при наличии массива переменных с плавающей запятой:


```
float4 array[16];
```



Вы можете упаковать его следующим образом без пробелов в массиве:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



Более тесная упаковка является компромиссом, а не потребностью в дополнительных инструкциях шейдера для вычисления адреса.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модель шейдера 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




