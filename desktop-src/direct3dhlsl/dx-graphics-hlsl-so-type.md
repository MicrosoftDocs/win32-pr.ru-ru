---
title: Объект Stream-Output
description: Объект потокового вывода — это шаблонный объект, который передает данные из этапа геометрического шейдера. Для объявления объекта потокового вывода используйте следующий синтаксис.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413114"
---
# <a name="stream-output-object"></a><span data-ttu-id="5c2fe-104">Объект Stream-Output</span><span class="sxs-lookup"><span data-stu-id="5c2fe-104">Stream-Output Object</span></span>

<span data-ttu-id="5c2fe-105">Объект потокового вывода — это шаблонный объект, который передает данные из [этапа геометрического шейдера](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c2fe-105">A stream-output object is a templated object that streams data out of the [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span> <span data-ttu-id="5c2fe-106">Для объявления объекта потокового вывода используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-106">Use the following syntax to declare a stream-output object.</span></span>



| <span data-ttu-id="5c2fe-107">Inout *стреамаутпутобжект* < имя *типа данных* >  *;*</span><span class="sxs-lookup"><span data-stu-id="5c2fe-107">inout *StreamOutputObject*<*DataType*> *Name;*</span></span> |
|------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5c2fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c2fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2fe-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*Стреамаутпутобжект*  <  *Тип данных*  >    *Имя*</span><span class="sxs-lookup"><span data-stu-id="5c2fe-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject* < *DataType* >   *Name*</span></span>
</dt> <dd>

<span data-ttu-id="5c2fe-110">Объявление объекта потокового вывода (SO).</span><span class="sxs-lookup"><span data-stu-id="5c2fe-110">The stream-output object (SO) declaration.</span></span>



| <span data-ttu-id="5c2fe-111">Типы объектов Stream-Output</span><span class="sxs-lookup"><span data-stu-id="5c2fe-111">Stream-Output Object Types</span></span> | <span data-ttu-id="5c2fe-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5c2fe-112">Description</span></span>                       |
|----------------------------|-----------------------------------|
| <span data-ttu-id="5c2fe-113">*поинтстреам*</span><span class="sxs-lookup"><span data-stu-id="5c2fe-113">*PointStream*</span></span>              | <span data-ttu-id="5c2fe-114">Последовательность примитивных точек</span><span class="sxs-lookup"><span data-stu-id="5c2fe-114">A sequence of point primitives</span></span>    |
| <span data-ttu-id="5c2fe-115">*линестреам*</span><span class="sxs-lookup"><span data-stu-id="5c2fe-115">*LineStream*</span></span>               | <span data-ttu-id="5c2fe-116">Последовательность примитивов линий</span><span class="sxs-lookup"><span data-stu-id="5c2fe-116">A sequence of line primitives</span></span>     |
| <span data-ttu-id="5c2fe-117">*трианглестреам*</span><span class="sxs-lookup"><span data-stu-id="5c2fe-117">*TriangleStream*</span></span>           | <span data-ttu-id="5c2fe-118">Последовательность примитивов треугольника</span><span class="sxs-lookup"><span data-stu-id="5c2fe-118">A sequence of triangle primitives</span></span> |



 

<span data-ttu-id="5c2fe-119">*DataType* — выходной тип данных; может быть любым [типом данных HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="5c2fe-119">*DataType* - Output data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span> <span data-ttu-id="5c2fe-120">Необходимо заключить в угловые скобки.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-120">Must be surrounded by the angle brackets.</span></span>

<span data-ttu-id="5c2fe-121">*Name* — имя переменной; строка ASCII, однозначно определяющая объект.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-121">*Name* - Variable name; an ASCII string that uniquely identifies the object.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="5c2fe-122">Например, .</span><span class="sxs-lookup"><span data-stu-id="5c2fe-122">Example</span></span>

<span data-ttu-id="5c2fe-123">Это пример объявления объекта потокового вывода, который осуществляет потоковую передачу примитивов треугольника, данные которых определяются в \_ структуре PS кубической карты \_ .</span><span class="sxs-lookup"><span data-stu-id="5c2fe-123">This is an example of a stream-output object declaration that streams out triangle primitives whose data is defined by the PS\_CUBEMAP\_IN structure.</span></span> <span data-ttu-id="5c2fe-124">Геометрический шейдер ограничен созданием 18 вершин.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-124">The geometry-shader is limited to generating 18 vertices.</span></span>


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



<span data-ttu-id="5c2fe-125">Это фрагмент кода из [примера CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="5c2fe-125">This is a code snippet from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span></span>

## <a name="stream-output-object-methods"></a><span data-ttu-id="5c2fe-126">Stream-Outputные методы объектов</span><span class="sxs-lookup"><span data-stu-id="5c2fe-126">Stream-Output Object Methods</span></span>

<span data-ttu-id="5c2fe-127">Используйте следующий синтаксис для вызова методов потокового вывода.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-127">Use the following syntax to call stream-output-object methods.</span></span>


```
Object.Method
```



<span data-ttu-id="5c2fe-128">Реализуются следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-128">The following methods are implemented.</span></span>



| <span data-ttu-id="5c2fe-129">Методы</span><span class="sxs-lookup"><span data-stu-id="5c2fe-129">Methods</span></span>                                              | <span data-ttu-id="5c2fe-130">Описание</span><span class="sxs-lookup"><span data-stu-id="5c2fe-130">Description</span></span>                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="5c2fe-131">Добавить</span><span class="sxs-lookup"><span data-stu-id="5c2fe-131">Append</span></span>](dx-graphics-hlsl-so-append.md)             | <span data-ttu-id="5c2fe-132">Добавление выходных данных в существующий поток.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-132">Append output data to an existing stream.</span></span>                        |
| [<span data-ttu-id="5c2fe-133">рестартстрип</span><span class="sxs-lookup"><span data-stu-id="5c2fe-133">RestartStrip</span></span>](dx-graphics-hlsl-so-restartstrip.md) | <span data-ttu-id="5c2fe-134">Завершите текущую примитивную ленту и запустите новую ленту-примитив.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-134">End the current primitive strip and start a new primitive strip.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5c2fe-135">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5c2fe-135">Minimum Shader Model</span></span>

<span data-ttu-id="5c2fe-136">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="5c2fe-136">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="5c2fe-137">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5c2fe-137">Shader Model</span></span>                                                        | <span data-ttu-id="5c2fe-138">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5c2fe-138">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="5c2fe-139">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="5c2fe-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="5c2fe-140">да</span><span class="sxs-lookup"><span data-stu-id="5c2fe-140">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="5c2fe-141">См. также</span><span class="sxs-lookup"><span data-stu-id="5c2fe-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c2fe-142">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="5c2fe-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 