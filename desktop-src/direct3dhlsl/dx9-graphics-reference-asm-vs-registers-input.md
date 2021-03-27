---
title: Входной регистр
description: Входной регистр
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986620"
---
# <a name="input-register"></a><span data-ttu-id="59592-103">Входной регистр</span><span class="sxs-lookup"><span data-stu-id="59592-103">Input Register</span></span>

<span data-ttu-id="59592-104">Входной регистр шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="59592-104">Vertex shader input register.</span></span>

<span data-ttu-id="59592-105">Данные из каждой вершины (с использованием одного или нескольких входных потоков вершин) загружаются в входные регистры вершин перед запуском шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="59592-105">Data from each vertex (using one or more input vertex streams) is loaded into the vertex input registers before the vertex shader is run.</span></span> <span data-ttu-id="59592-106">Входные регистры состоят из 16 4-компонентных векторов с плавающей запятой, обозначенных как v0 через версия 15.</span><span class="sxs-lookup"><span data-stu-id="59592-106">The input registers consist of 16 four-component floating-point vectors, designated as v0 through v15.</span></span> <span data-ttu-id="59592-107">Эти регистры доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="59592-107">These registers are read-only.</span></span> <span data-ttu-id="59592-108">Входной регистр привязан к данным вершин через объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="59592-108">An input register is bound to vertex data through a vertex declaration.</span></span>

<span data-ttu-id="59592-109">Ниже перечислены свойства регистра, определяющие принцип работы каждой ККМ.</span><span class="sxs-lookup"><span data-stu-id="59592-109">The following register properties control how each register behaves:</span></span>



| <span data-ttu-id="59592-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="59592-110">Property</span></span>        | <span data-ttu-id="59592-111">Описание</span><span class="sxs-lookup"><span data-stu-id="59592-111">Description</span></span>                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59592-112">Имя</span><span class="sxs-lookup"><span data-stu-id="59592-112">Name</span></span>            | <span data-ttu-id="59592-113">v \[ n \] -n — необязательный номер ККМ.</span><span class="sxs-lookup"><span data-stu-id="59592-113">v\[n\] - n is an optional register number.</span></span> <span data-ttu-id="59592-114">0 — используемое по умолчанию значение, если оно пропущено.</span><span class="sxs-lookup"><span data-stu-id="59592-114">0 is the default value used, if it is omitted.</span></span>     |
| <span data-ttu-id="59592-115">Count</span><span class="sxs-lookup"><span data-stu-id="59592-115">Count</span></span>           | <span data-ttu-id="59592-116">Не более 16 регистров, v0-версия 15.</span><span class="sxs-lookup"><span data-stu-id="59592-116">A maximum of 16 registers, v0 - v15.</span></span>                                                          |
| <span data-ttu-id="59592-117">Разрешения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="59592-117">I/O permissions</span></span> | <span data-ttu-id="59592-118">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="59592-118">Read-only.</span></span> <span data-ttu-id="59592-119">Этот регистр не может быть записан API или в шейдере.</span><span class="sxs-lookup"><span data-stu-id="59592-119">This register cannot be written by the API or within the shader.</span></span>                   |
| <span data-ttu-id="59592-120">Чтение портов</span><span class="sxs-lookup"><span data-stu-id="59592-120">Read ports</span></span>      | <span data-ttu-id="59592-121">1. это количество операций чтения регистра в рамках одной инструкции.</span><span class="sxs-lookup"><span data-stu-id="59592-121">1. This is the number of times a register can be read within a single instruction.</span></span> <span data-ttu-id="59592-122">См. ниже.</span><span class="sxs-lookup"><span data-stu-id="59592-122">See below.</span></span> |



 

<span data-ttu-id="59592-123">Любая одна инструкция может обращаться только к одному входному регистру вершин.</span><span class="sxs-lookup"><span data-stu-id="59592-123">Any single instruction can access only one vertex input register.</span></span> <span data-ttu-id="59592-124">Однако каждый источник в инструкции может независимо свиззле и инвертировать этот вектор по мере считывания.</span><span class="sxs-lookup"><span data-stu-id="59592-124">However, each source in the instruction can independently swizzle and negate that vector as it is read.</span></span>

## <a name="example"></a><span data-ttu-id="59592-125">Например, .</span><span class="sxs-lookup"><span data-stu-id="59592-125">Example</span></span>

<span data-ttu-id="59592-126">Ниже приведен пример использования объявления вершины для привязки данных расположения 2D-вершины для регистрации v0.</span><span class="sxs-lookup"><span data-stu-id="59592-126">Here is an example using a vertex declaration to bind 2D vertex position data to register v0.</span></span>

<span data-ttu-id="59592-127">Объявление вершины принадлежит приложению:</span><span class="sxs-lookup"><span data-stu-id="59592-127">The vertex declaration belongs in the application:</span></span>


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



<span data-ttu-id="59592-128">Ниже приведено соответствующее объявление шейдера вершин:</span><span class="sxs-lookup"><span data-stu-id="59592-128">Here is the corresponding vertex shader declaration:</span></span>


```
dcl_position v0
```





| <span data-ttu-id="59592-129">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="59592-129">Vertex shader versions</span></span> | <span data-ttu-id="59592-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="59592-130">1\_1</span></span> | <span data-ttu-id="59592-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59592-131">2\_0</span></span> | <span data-ttu-id="59592-132">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59592-132">2\_sw</span></span> | <span data-ttu-id="59592-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="59592-133">2\_x</span></span> | <span data-ttu-id="59592-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59592-134">3\_0</span></span> | <span data-ttu-id="59592-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59592-135">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="59592-136">Регистр позиций</span><span class="sxs-lookup"><span data-stu-id="59592-136">Position Register</span></span>      | <span data-ttu-id="59592-137">x</span><span class="sxs-lookup"><span data-stu-id="59592-137">x</span></span>    | <span data-ttu-id="59592-138">x</span><span class="sxs-lookup"><span data-stu-id="59592-138">x</span></span>    | <span data-ttu-id="59592-139">x</span><span class="sxs-lookup"><span data-stu-id="59592-139">x</span></span>     | <span data-ttu-id="59592-140">x</span><span class="sxs-lookup"><span data-stu-id="59592-140">x</span></span>    | <span data-ttu-id="59592-141">x</span><span class="sxs-lookup"><span data-stu-id="59592-141">x</span></span>    | <span data-ttu-id="59592-142">x</span><span class="sxs-lookup"><span data-stu-id="59592-142">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="59592-143">См. также</span><span class="sxs-lookup"><span data-stu-id="59592-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59592-144">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="59592-144">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




