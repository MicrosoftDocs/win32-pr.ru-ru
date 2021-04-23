---
title: Доступ к ресурсам
description: Существует несколько способов доступа к ресурсам.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997115"
---
# <a name="accessing-resources"></a><span data-ttu-id="e6276-103">Доступ к ресурсам</span><span class="sxs-lookup"><span data-stu-id="e6276-103">Accessing Resources</span></span>

<span data-ttu-id="e6276-104">Существует несколько способов доступа к [ресурсам](overviews-direct3d-11-resources-types.md).</span><span class="sxs-lookup"><span data-stu-id="e6276-104">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span> <span data-ttu-id="e6276-105">Независимо от этого Direct3D гарантирует возврат нуля для любого ресурса, доступ к которому осуществляется вне границ.</span><span class="sxs-lookup"><span data-stu-id="e6276-105">Regardless, Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

-   [<span data-ttu-id="e6276-106">Доступ по смещению в байтах</span><span class="sxs-lookup"><span data-stu-id="e6276-106">Access By Byte Offset</span></span>](#access-by-byte-offset)
-   [<span data-ttu-id="e6276-107">Доступ по индексу</span><span class="sxs-lookup"><span data-stu-id="e6276-107">Access By Index</span></span>](#access-by-index)
-   [<span data-ttu-id="e6276-108">Доступ по методу MIPS</span><span class="sxs-lookup"><span data-stu-id="e6276-108">Access By Mips Method</span></span>](#access-by-mips-method)
-   [<span data-ttu-id="e6276-109">См. также</span><span class="sxs-lookup"><span data-stu-id="e6276-109">Related topics</span></span>](#related-topics)

## <a name="access-by-byte-offset"></a><span data-ttu-id="e6276-110">Доступ по смещению в байтах</span><span class="sxs-lookup"><span data-stu-id="e6276-110">Access By Byte Offset</span></span>

<span data-ttu-id="e6276-111">Доступ к двум новым типам буферов можно получить с помощью смещения в байтах:</span><span class="sxs-lookup"><span data-stu-id="e6276-111">Two new buffer types can be accessed using a byte offset:</span></span>

-   <span data-ttu-id="e6276-112">[**Битеаддрессбуффер**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) — это буфер, предназначенный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e6276-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) is a read-only buffer.</span></span>
-   <span data-ttu-id="e6276-113">[**Рвбитеаддрессбуффер**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) является буфером чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="e6276-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) is a read or write buffer.</span></span>

## <a name="access-by-index"></a><span data-ttu-id="e6276-114">Доступ по индексу</span><span class="sxs-lookup"><span data-stu-id="e6276-114">Access By Index</span></span>

<span data-ttu-id="e6276-115">Типы ресурсов могут использовать индекс для ссылки на определенное расположение в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="e6276-115">Resource types can use an index to reference a specific location in the resource.</span></span> <span data-ttu-id="e6276-116">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="e6276-116">Consider this example:</span></span>


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



<span data-ttu-id="e6276-117">В этом примере присваиваются 4 значения с плавающей запятой, которые хранятся в шаг текселя, расположенном в позиции *POS* в ресурсе 2D-текстуры *митекстуре* , в переменную *myVar* .</span><span class="sxs-lookup"><span data-stu-id="e6276-117">This example assigns the 4 float values that are stored at the texel located at the *pos* position in the *myTexture* 2D texture resource to the *myVar* variable.</span></span>

> [!Note]  
> <span data-ttu-id="e6276-118">Значение по умолчанию для доступа к текстуре таким образом — mipmap уровня 0 (самый подробный уровень).</span><span class="sxs-lookup"><span data-stu-id="e6276-118">The default for accessing a texture in this way is mipmap level zero (the most detailed level).</span></span>

 

> [!Note]  
> <span data-ttu-id="e6276-119">Строка "float4 myVar = Митекстуре \[ POS \] ;" эквивалентна "float4 myVar = Митекстуре. Load (uint3 (POS, 0));".</span><span class="sxs-lookup"><span data-stu-id="e6276-119">The "float4 myVar = myTexture\[pos\];" line is equivalent to "float4 myVar = myTexture.Load(uint3(pos,0));".</span></span> <span data-ttu-id="e6276-120">Доступ по индексу — это новый улучшенный синтаксис HLSL.</span><span class="sxs-lookup"><span data-stu-id="e6276-120">Access by index is a new HLSL syntax enhancement.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6276-121">Компилятор в июне 2010 версии пакета SDK DirectX и более поздних версий позволяет индексировать все типы ресурсов, за исключением [буферов адресов байтов](direct3d-11-advanced-stages-cs-resources.md).</span><span class="sxs-lookup"><span data-stu-id="e6276-121">The compiler in the June 2010 version of the DirectX SDK and later lets you index all resource types except for [byte address buffers](direct3d-11-advanced-stages-cs-resources.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="e6276-122">Компилятор Июнь 2010 и более поздних версий позволяет объявлять локальные переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6276-122">The June 2010 compiler and later lets you declare local resource variables.</span></span> <span data-ttu-id="e6276-123">Вы можете назначить этим переменным глобально определенные ресурсы (например, *митекстуре*) и использовать их так же, как их глобальные аналоги.</span><span class="sxs-lookup"><span data-stu-id="e6276-123">You can assign globally defined resources (like *myTexture*) to these variables and use them the same way as their global counterparts.</span></span>

 

## <a name="access-by-mips-method"></a><span data-ttu-id="e6276-124">Доступ по методу MIPS</span><span class="sxs-lookup"><span data-stu-id="e6276-124">Access By Mips Method</span></span>

<span data-ttu-id="e6276-125">Объекты текстуры имеют метод **MIPS** (например, [**Texture2D. MIPS**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), который можно использовать для указания уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="e6276-125">Texture objects have a **mips** method (for example, [**Texture2D.mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), which you can use to specify the mipmap level.</span></span> <span data-ttu-id="e6276-126">В этом примере считывается цвет, хранящийся в (7, 16) на mipmap уровне 2 в двухмерной текстуре:</span><span class="sxs-lookup"><span data-stu-id="e6276-126">This example reads the color stored at (7,16) on mipmap level 2 in a 2D texture:</span></span>


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



<span data-ttu-id="e6276-127">Это усовершенствование из компилятора Июнь 2010 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e6276-127">This is an enhancement from the June 2010 compiler and later.</span></span> <span data-ttu-id="e6276-128">Выражение "Митекстуре. MIPS \[ 2 \] \[ uint2 (x, y) \] " эквивалентно значению "митекстуре. Load (uint3 (x, y, 2))".</span><span class="sxs-lookup"><span data-stu-id="e6276-128">The "myTexture.mips\[2\]\[uint2(x,y)\]" expression is equivalent to "myTexture.Load(uint3(x,y,2))".</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6276-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e6276-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6276-130">Общие сведения о вычислении шейдера</span><span class="sxs-lookup"><span data-stu-id="e6276-130">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 