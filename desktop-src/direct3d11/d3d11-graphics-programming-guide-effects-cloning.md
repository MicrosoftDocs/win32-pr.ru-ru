---
title: Клонирование результата
description: При клонировании действия создается вторая, почти идентичная копия этого результата.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777240"
---
# <a name="cloning-an-effect"></a><span data-ttu-id="b3998-103">Клонирование результата</span><span class="sxs-lookup"><span data-stu-id="b3998-103">Cloning an Effect</span></span>

<span data-ttu-id="b3998-104">При клонировании действия создается вторая, почти идентичная копия этого результата.</span><span class="sxs-lookup"><span data-stu-id="b3998-104">Cloning an effect creates a second, almost identical copy of the effect.</span></span> <span data-ttu-id="b3998-105">См. следующий единственный квалификатор, поясняющий, почему он не является точным.</span><span class="sxs-lookup"><span data-stu-id="b3998-105">See the following single qualifier for an explanation of why it is not exact.</span></span> <span data-ttu-id="b3998-106">Вторая копия эффекта полезна, когда одной из них требуется использовать платформу Effects в нескольких потоках, так как среда выполнения влияния не является потокобезопасной для поддержания высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="b3998-106">A second copy of an effect is useful when one wants to use the effects framework on multiple threads, since the effect runtime is not thread safe to maintain high performance.</span></span>

<span data-ttu-id="b3998-107">Так как контексты устройств также не являются потокобезопасными, разные потоки должны передавать разные контексты устройств методу ID3DX11EffectPass:: Apply.</span><span class="sxs-lookup"><span data-stu-id="b3998-107">Since device contexts are also non-thread-safe, different threads should pass different device contexts to the ID3DX11EffectPass::Apply method.</span></span>

<span data-ttu-id="b3998-108">Результат можно клонировать с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="b3998-108">An effect can be cloned with the following syntax:</span></span>


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



<span data-ttu-id="b3998-109">В приведенном выше примере Клонированная копия будет инкапсулировать то же состояние, что и исходный результат, независимо от состояния, в котором находится исходный результат.</span><span class="sxs-lookup"><span data-stu-id="b3998-109">In the above example, the cloned copy will encapsulate the same state as the original effect, regardless of what state the original effect is in.</span></span> <span data-ttu-id="b3998-110">В частности:</span><span class="sxs-lookup"><span data-stu-id="b3998-110">In particular:</span></span>

1.  <span data-ttu-id="b3998-111">Если Пеффект оптимизировано, Пклонедный результат оптимизирован</span><span class="sxs-lookup"><span data-stu-id="b3998-111">If pEffect is optimized, pCloned Effect is optimized</span></span>
2.  <span data-ttu-id="b3998-112">Если Пеффект содержит некоторые переменные, управляемые пользователем, Пклонед воздействие будет иметь те же управляемые пользователем переменные (см. одно описание ниже).</span><span class="sxs-lookup"><span data-stu-id="b3998-112">If pEffect has some user-managed variables, pCloned Effect will have the same user-managed variables (see the single description below)</span></span>
3.  <span data-ttu-id="b3998-113">Все ожидающие обновления переменные (пока вызов Apply не обновляет состояние устройства) в Пеффект будет ожидать в Пклонедеффект</span><span class="sxs-lookup"><span data-stu-id="b3998-113">Any pending variable updates (until an Apply call updates device state) in pEffect will be pending in pClonedEffect</span></span>

<span data-ttu-id="b3998-114">Следующие объекты устройств Direct3D 11 являются неизменяемыми или никогда не обновляются платформой Effects, поэтому клонированный эффект будет указывать на те же объекты, что и исходный эффект:</span><span class="sxs-lookup"><span data-stu-id="b3998-114">The following Direct3D 11 device objects are immutable or never updated by the effects framework, so the cloned effect will point to the same objects as the original effect:</span></span>

1.  <span data-ttu-id="b3998-115">Объекты блока State (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span><span class="sxs-lookup"><span data-stu-id="b3998-115">State block objects (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span></span>
2.  <span data-ttu-id="b3998-116">Шейдеры</span><span class="sxs-lookup"><span data-stu-id="b3998-116">Shaders</span></span>
3.  <span data-ttu-id="b3998-117">Экземпляры класса</span><span class="sxs-lookup"><span data-stu-id="b3998-117">Class instances</span></span>
4.  <span data-ttu-id="b3998-118">Текстуры (не включая буферы текстур)</span><span class="sxs-lookup"><span data-stu-id="b3998-118">Textures (not including texture buffers)</span></span>
5.  <span data-ttu-id="b3998-119">Представления неупорядоченного доступа</span><span class="sxs-lookup"><span data-stu-id="b3998-119">Unordered access views</span></span>

<span data-ttu-id="b3998-120">Следующие объекты устройств Direct3D 11 как неизменяемые, так и изменяются средой выполнения Effect (если они не управляются пользователем или единственными в клонированном результате); новые копии этих объектов создаются, если они не являются отдельными:</span><span class="sxs-lookup"><span data-stu-id="b3998-120">The following Direct3D 11 device objects are both immutable and modified by the effect runtime (unless user-managed or single in a cloned effect); new copies of these objects are created when non-single:</span></span>

1.  <span data-ttu-id="b3998-121">Буферы констант</span><span class="sxs-lookup"><span data-stu-id="b3998-121">Constant buffers</span></span>
2.  <span data-ttu-id="b3998-122">Буферы текстуры</span><span class="sxs-lookup"><span data-stu-id="b3998-122">Texture Buffers</span></span>

## <a name="single-constant-buffers-and-texture-buffers"></a><span data-ttu-id="b3998-123">Одноконстантные буферы и буферы текстур</span><span class="sxs-lookup"><span data-stu-id="b3998-123">Single Constant Buffers and Texture Buffers</span></span>

<span data-ttu-id="b3998-124">Обратите внимание, что это обсуждение относится как к постоянным буферам, так и к текстурам, но для простоты чтения предполагается наличие постоянных буферов.</span><span class="sxs-lookup"><span data-stu-id="b3998-124">Note that this discussion applies to both constant buffers and textures, but constant buffers are assumed for ease of reading.</span></span>

<span data-ttu-id="b3998-125">Возможны случаи, когда буфер констант обновляется только одним потоком, но эти данные будут использоваться состоянием устройства, установленным клонированными эффектами.</span><span class="sxs-lookup"><span data-stu-id="b3998-125">There may be cases where a constant buffer is only updated by one thread, but device state set by cloned effects will use this data.</span></span> <span data-ttu-id="b3998-126">Например, основной эффект может обновлять мир и просматривать матрицы, на которые имеются ссылки в виде шейдеров, в клонированных эффектах, которые не изменяют матрицы мира и представления.</span><span class="sxs-lookup"><span data-stu-id="b3998-126">For example, the main effect may update the world and view matrices which are referenced from shaders in cloned effects which do not change the world and view matrices.</span></span> <span data-ttu-id="b3998-127">В таких случаях клонированные эффекты должны ссылаться на текущий буфер констант, а не воссоздавать его.</span><span class="sxs-lookup"><span data-stu-id="b3998-127">In these cases, the cloned effects need to reference the current constant buffer instead of recreating one.</span></span>

<span data-ttu-id="b3998-128">Существует два способа достижения этого результата:</span><span class="sxs-lookup"><span data-stu-id="b3998-128">There are two ways to achieve this desired result:</span></span>

1.  <span data-ttu-id="b3998-129">Используйте ID3DX11EffectConstantBuffer:: Сетконстантбуффер в клонированном результате, чтобы сделать его управляемым пользователем</span><span class="sxs-lookup"><span data-stu-id="b3998-129">Use ID3DX11EffectConstantBuffer::SetConstantBuffer on the cloned effect to make it user-managed</span></span>
2.  <span data-ttu-id="b3998-130">Пометьте константный буфер как "отдельный" в коде HLSL, чтобы среда выполнения Effect считалась как управляемая пользователем после клонирования</span><span class="sxs-lookup"><span data-stu-id="b3998-130">Mark the constant buffer as "single" in the HLSL code, forcing the effect runtime to treat is as user-managed after cloning</span></span>

<span data-ttu-id="b3998-131">Существует два различия между двумя методами, приведенными выше.</span><span class="sxs-lookup"><span data-stu-id="b3998-131">There are two differences between the two methods above.</span></span> <span data-ttu-id="b3998-132">Во-первых, в методе 1 создается новый ID3D11Buffer и вызывается пользователь перед Сетконстантбуффер.</span><span class="sxs-lookup"><span data-stu-id="b3998-132">First, in method 1, a new ID3D11Buffer will be created and user before SetConstantBuffer is called.</span></span> <span data-ttu-id="b3998-133">Кроме того, после вызова Ундосетконстантбуффер в клонированном эффекте переменная в методе 1will указывает на только что созданный буфер (эффект, который будет обновляться при применении), а переменная в методе 2 продолжит указывать на исходный буфер (не обновляя его при применении).</span><span class="sxs-lookup"><span data-stu-id="b3998-133">Also, after calling UndoSetConstantBuffer in the cloned effect, the variable in method 1will point to the newly-created buffer (which effects will update on Apply) while the variable in method 2 will continue to point to the original buffer (not updating it on Apply).</span></span>

<span data-ttu-id="b3998-134">См. Следующий пример в HLSL:</span><span class="sxs-lookup"><span data-stu-id="b3998-134">See the following example in HLSL:</span></span>


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



<span data-ttu-id="b3998-135">При клонировании клонированный результат создаст новый ID3D11Buffer для ObjectData и заполнит его содержимое на Apply, но сослаться на исходный ID3D11Buffer для ViewData.</span><span class="sxs-lookup"><span data-stu-id="b3998-135">While cloning, the cloned effect will create a new ID3D11Buffer for ObjectData, and fill its contents on Apply, but reference the original ID3D11Buffer for ViewData.</span></span> <span data-ttu-id="b3998-136">Единственный квалификатор можно проигнорировать в процессе клонирования, установив флаг D3DX11 для \_ \_ клона действия \_ Force \_ .</span><span class="sxs-lookup"><span data-stu-id="b3998-136">The single qualifier can be ignored in the cloning process by setting the D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3998-137">См. также</span><span class="sxs-lookup"><span data-stu-id="b3998-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3998-138">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="b3998-138">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




