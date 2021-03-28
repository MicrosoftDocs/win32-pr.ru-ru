---
title: рвбуффер
description: Буфер чтения и записи.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- Рвбуффер HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334040"
---
# <a name="rwbuffer"></a><span data-ttu-id="8e475-104">рвбуффер</span><span class="sxs-lookup"><span data-stu-id="8e475-104">RWBuffer</span></span>

<span data-ttu-id="8e475-105">Буфер чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8e475-105">A read/write buffer.</span></span>



| <span data-ttu-id="8e475-106">Метод</span><span class="sxs-lookup"><span data-stu-id="8e475-106">Method</span></span>                                                     | <span data-ttu-id="8e475-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8e475-107">Description</span></span>                            |
|------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="8e475-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="8e475-108">**GetDimensions**</span></span>](sm5-object-rwbuffer-getdimensions.md) | <span data-ttu-id="8e475-109">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e475-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="8e475-110">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="8e475-110">**Load**</span></span>](rwbuffer-load.md)                              | <span data-ttu-id="8e475-111">Возвращает одно значение в буфере для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8e475-111">Gets one value in a read-write buffer.</span></span> |
| <span data-ttu-id="8e475-112">[**Оператор\[\]**](sm5-object-rwbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="8e475-112">[**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="8e475-113">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e475-113">Returns a resource variable.</span></span>           |



 

<span data-ttu-id="8e475-114">Переменная ресурса также может быть передана в любую неупорядоченную или блокируемую операцию.</span><span class="sxs-lookup"><span data-stu-id="8e475-114">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="8e475-115">Для объектов **рвбуффер** можно использовать префикс класса хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="8e475-115">**RWBuffer** objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="8e475-116">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="8e475-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="8e475-117">Без этого описателя барьер памяти или синхронизация будут сбрасывать UAV только в пределах текущей группы.</span><span class="sxs-lookup"><span data-stu-id="8e475-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="8e475-118">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8e475-118">Minimum Shader Model</span></span>

<span data-ttu-id="8e475-119">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8e475-119">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="8e475-120">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8e475-120">Shader Model</span></span>                                                                | <span data-ttu-id="8e475-121">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8e475-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8e475-122">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="8e475-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8e475-123">да</span><span class="sxs-lookup"><span data-stu-id="8e475-123">yes</span></span>       |



 

<span data-ttu-id="8e475-124">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8e475-124">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8e475-125">Вершина</span><span class="sxs-lookup"><span data-stu-id="8e475-125">Vertex</span></span> | <span data-ttu-id="8e475-126">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8e475-126">Hull</span></span> | <span data-ttu-id="8e475-127">Домен</span><span class="sxs-lookup"><span data-stu-id="8e475-127">Domain</span></span> | <span data-ttu-id="8e475-128">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8e475-128">Geometry</span></span> | <span data-ttu-id="8e475-129">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8e475-129">Pixel</span></span> | <span data-ttu-id="8e475-130">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8e475-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8e475-131">x</span><span class="sxs-lookup"><span data-stu-id="8e475-131">x</span></span>     | <span data-ttu-id="8e475-132">x</span><span class="sxs-lookup"><span data-stu-id="8e475-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8e475-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e475-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e475-134">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="8e475-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




