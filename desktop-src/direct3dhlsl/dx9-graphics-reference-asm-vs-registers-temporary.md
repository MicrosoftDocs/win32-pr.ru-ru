---
title: Временный регистр (Справочник по HLSL VS)
description: Для хранения промежуточных результатов используется временный регистр шейдера вершин.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335691"
---
# <a name="temporary-register-hlsl-vs-reference"></a><span data-ttu-id="7e9d9-103">Временный регистр (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="7e9d9-103">Temporary Register (HLSL VS reference)</span></span>

<span data-ttu-id="7e9d9-104">Для хранения промежуточных результатов используется временный регистр шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-104">A vertex shader temporary register is used to hold intermediate results.</span></span>

<span data-ttu-id="7e9d9-105">Временный регистр необходимо инициализировать до его использования.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-105">A temporary register must be initialized before it is used.</span></span> <span data-ttu-id="7e9d9-106">Каждый временный регистр имеет доступ с одной записью и с тройным доступом на чтение.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-106">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="7e9d9-107">Это означает, что одна инструкция шейдера может использовать в качестве входных данных до трех временных регистров.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-107">This means that a single shader instruction can use as many as three temporary registers as inputs.</span></span>

<span data-ttu-id="7e9d9-108">Значения во временном регистре, остающиеся из предыдущих вызовов шейдера вершин, использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-108">Values in a temporary register that remain from preceding invocations of the vertex shader cannot be used.</span></span>

<span data-ttu-id="7e9d9-109">Регистр состоит из свойств, определяющих принцип работы каждой ККМ.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-109">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="7e9d9-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="7e9d9-110">Property</span></span>        | <span data-ttu-id="7e9d9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7e9d9-111">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9d9-112">Имя</span><span class="sxs-lookup"><span data-stu-id="7e9d9-112">Name</span></span>            | <span data-ttu-id="7e9d9-113">r \[ n \] .</span><span class="sxs-lookup"><span data-stu-id="7e9d9-113">r\[n\].</span></span> <span data-ttu-id="7e9d9-114">n — необязательный номер регистра.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-114">n is an optional register number.</span></span> <span data-ttu-id="7e9d9-115">Значением по умолчанию является 0, а — значение, используемое, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-115">The default is 0, and is the value used if no value is specified.</span></span>                                                                                 |
| <span data-ttu-id="7e9d9-116">Count</span><span class="sxs-lookup"><span data-stu-id="7e9d9-116">Count</span></span>           | <span data-ttu-id="7e9d9-117">Не более 12 регистров.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-117">A maximum of 12 registers.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="7e9d9-118">Разрешения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="7e9d9-118">I/O permissions</span></span> | <span data-ttu-id="7e9d9-119">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-119">Read/write.</span></span> <span data-ttu-id="7e9d9-120">Этот регистр можно считывать или записывать с помощью API или шейдера.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-120">This register can be read or written by the API or by the shader.</span></span>                                                                                                               |
| <span data-ttu-id="7e9d9-121">Чтение портов</span><span class="sxs-lookup"><span data-stu-id="7e9d9-121">Read ports</span></span>      | <span data-ttu-id="7e9d9-122">Количество операций чтения регистра в одной инструкции равно 3.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-122">The number of times a register can be read within a single instruction is 3.</span></span> <span data-ttu-id="7e9d9-123">Временный регистр — это единственный регистр, который может быть считан и записан более одного раза в одной инструкции.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-123">A temporary register is the only register that can be read and written more than once in a single instruction.</span></span> |



 

<span data-ttu-id="7e9d9-124">Каждый временный регистр имеет доступ с одной записью и с тройным доступом на чтение.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-124">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="7e9d9-125">Таким образом, инструкция может иметь до трех временных регистров в наборе операндов источника входных данных.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-125">Therefore, an instruction can have as many as three temporary registers in its set of input source operands.</span></span>

<span data-ttu-id="7e9d9-126">Не допускается использование значений во временном регистре, остающихся из предыдущих вызовов шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-126">No values in a temporary register that remain from preceding invocations of the vertex shader can be used.</span></span> <span data-ttu-id="7e9d9-127">В шейдерах вершин, которые считывают значение из временного регистра перед записью в него, вызов API Direct3D для создания шейдера вершин будет невозможен.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-127">Vertex shaders that read a value from a temporary register before writing to it will fail the Direct3D API call to create the vertex shader.</span></span>

## <a name="example"></a><span data-ttu-id="7e9d9-128">Например, .</span><span class="sxs-lookup"><span data-stu-id="7e9d9-128">Example</span></span>

<span data-ttu-id="7e9d9-129">Ниже приведен пример использования временного регистра.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-129">Here is an example using a temporary register:</span></span>


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| <span data-ttu-id="7e9d9-130">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="7e9d9-130">Vertex shader versions</span></span> | <span data-ttu-id="7e9d9-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="7e9d9-131">1\_1</span></span> | <span data-ttu-id="7e9d9-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7e9d9-132">2\_0</span></span> | <span data-ttu-id="7e9d9-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7e9d9-133">2\_sw</span></span> | <span data-ttu-id="7e9d9-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7e9d9-134">2\_x</span></span> | <span data-ttu-id="7e9d9-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7e9d9-135">3\_0</span></span> | <span data-ttu-id="7e9d9-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7e9d9-136">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="7e9d9-137">Временный регистр</span><span class="sxs-lookup"><span data-stu-id="7e9d9-137">Temporary Register</span></span>     | <span data-ttu-id="7e9d9-138">x</span><span class="sxs-lookup"><span data-stu-id="7e9d9-138">x</span></span>    | <span data-ttu-id="7e9d9-139">x</span><span class="sxs-lookup"><span data-stu-id="7e9d9-139">x</span></span>    | <span data-ttu-id="7e9d9-140">x</span><span class="sxs-lookup"><span data-stu-id="7e9d9-140">x</span></span>     | <span data-ttu-id="7e9d9-141">x</span><span class="sxs-lookup"><span data-stu-id="7e9d9-141">x</span></span>    | <span data-ttu-id="7e9d9-142">x</span><span class="sxs-lookup"><span data-stu-id="7e9d9-142">x</span></span>    | <span data-ttu-id="7e9d9-143">x</span><span class="sxs-lookup"><span data-stu-id="7e9d9-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="7e9d9-144">См. также</span><span class="sxs-lookup"><span data-stu-id="7e9d9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e9d9-145">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="7e9d9-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




