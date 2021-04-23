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
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: 004d7881dc9ff92ea394cd2331774e13b1e7f13c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "103789426"
---
# <a name="packing-rules-for-constant-variables"></a><span data-ttu-id="05447-103">Правила упаковки для константных переменных</span><span class="sxs-lookup"><span data-stu-id="05447-103">Packing Rules for Constant Variables</span></span>

<span data-ttu-id="05447-104">Правила упаковки определяют, насколько тесно данные могут быть упорядочены при их хранении.</span><span class="sxs-lookup"><span data-stu-id="05447-104">Packing rules dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="05447-105">HLSL реализует правила упаковки для выходных данных VS, входные и выходные данные GS и входные и выходные данные PS.</span><span class="sxs-lookup"><span data-stu-id="05447-105">HLSL implements packing rules for VS output data, GS input and output data, and PS input and output data.</span></span> <span data-ttu-id="05447-106">(Данные не упаковываются для входных данных VS, так как на этапе IA не удается распаковать данные.)</span><span class="sxs-lookup"><span data-stu-id="05447-106">(Data is not packed for VS inputs because the IA stage cannot unpack data.)</span></span>

<span data-ttu-id="05447-107">Правила упаковки HLSL похожи на выполнение **\# директивы pragma Pack 4** с Visual Studio, которая упаковывает данные в 4-байтовые границы.</span><span class="sxs-lookup"><span data-stu-id="05447-107">HLSL packing rules are similar to performing a **\#pragma pack 4** with Visual Studio, which packs data into 4-byte boundaries.</span></span> <span data-ttu-id="05447-108">Кроме того, HLSL упаковывает данные таким образом, чтобы они не пересекали 16-байтовую границу.</span><span class="sxs-lookup"><span data-stu-id="05447-108">Additionally, HLSL packs data so that it does not cross a 16-byte boundary.</span></span> <span data-ttu-id="05447-109">Переменные упаковываются в данный вектор с четырьмя компонентами до тех пор, пока переменная не получит 4-векторную границу. следующие переменные будут передаваться на следующий вектор с четырьмя компонентами.</span><span class="sxs-lookup"><span data-stu-id="05447-109">Variables are packed into a given four-component vector until the variable will straddle a 4-vector boundary; the next variables will be bounced to the next four-component vector.</span></span>

<span data-ttu-id="05447-110">Каждая структура принудительно запускает следующую переменную в следующем векторе из четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="05447-110">Each structure forces the next variable to start on the next four-component vector.</span></span> <span data-ttu-id="05447-111">Иногда это приводит к созданию заполнения для массивов структур.</span><span class="sxs-lookup"><span data-stu-id="05447-111">This sometimes generates padding for arrays of structures.</span></span> <span data-ttu-id="05447-112">Итоговый размер любой структуры всегда будет равномерно кратен **sizeof**(*вектор с четырьмя компонентами*).</span><span class="sxs-lookup"><span data-stu-id="05447-112">The resulting size of any structure will always be evenly divisible by **sizeof**(*four-component vector*).</span></span>

<span data-ttu-id="05447-113">По умолчанию массивы не упаковываются в HLSL.</span><span class="sxs-lookup"><span data-stu-id="05447-113">Arrays are not packed in HLSL by default.</span></span> <span data-ttu-id="05447-114">Во избежание принудительного использования шейдера с незначительными издержками для смещенных вычислений каждый элемент массива хранится в векторе из четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="05447-114">To avoid forcing the shader to take on ALU overhead for offset computations, every element in an array is stored in a four-component vector.</span></span> <span data-ttu-id="05447-115">Обратите внимание, что можно выполнить упаковку для массивов (и вычисление адресов) с помощью приведения.</span><span class="sxs-lookup"><span data-stu-id="05447-115">Note that you can achieve packing for arrays (and incur the addressing calculations) by using casting.</span></span>

<span data-ttu-id="05447-116">Ниже приведены примеры структур и их соответствующих упакованных размеров (заданный: **float1** занимает 4 байта):</span><span class="sxs-lookup"><span data-stu-id="05447-116">Following are examples of structures and their corresponding packed sizes (given: a **float1** occupies 4 bytes):</span></span>


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



## <a name="more-aggressive-packing"></a><span data-ttu-id="05447-117">Более агрессивная упаковка</span><span class="sxs-lookup"><span data-stu-id="05447-117">More Aggressive Packing</span></span>

<span data-ttu-id="05447-118">Массив можно упаковать более агрессивно.</span><span class="sxs-lookup"><span data-stu-id="05447-118">You could pack an array more aggressively.</span></span> <span data-ttu-id="05447-119">Например, при наличии массива переменных с плавающей запятой:</span><span class="sxs-lookup"><span data-stu-id="05447-119">For instance, given an array of float variables:</span></span>


```
float4 array[16];
```



<span data-ttu-id="05447-120">Вы можете упаковать его следующим образом без пробелов в массиве:</span><span class="sxs-lookup"><span data-stu-id="05447-120">You could choose to pack it like this, without any spaces in the array:</span></span>


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



<span data-ttu-id="05447-121">Более тесная упаковка является компромиссом, а не потребностью в дополнительных инструкциях шейдера для вычисления адреса.</span><span class="sxs-lookup"><span data-stu-id="05447-121">The tighter packing is a trade off versus the need for additional shader instructions for address computation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05447-122">См. также</span><span class="sxs-lookup"><span data-stu-id="05447-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05447-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="05447-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




