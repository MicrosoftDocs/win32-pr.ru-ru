---
title: Синтаксис потока Out
description: Шейдер геометрии с потоком out объявляется с определенным синтаксисом.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996763"
---
# <a name="stream-out-syntax"></a><span data-ttu-id="76451-103">Синтаксис потока Out</span><span class="sxs-lookup"><span data-stu-id="76451-103">Stream Out Syntax</span></span>

<span data-ttu-id="76451-104">Шейдер геометрии с потоком out объявляется с определенным синтаксисом.</span><span class="sxs-lookup"><span data-stu-id="76451-104">A geometry shader with stream out is declared with a particular syntax.</span></span> <span data-ttu-id="76451-105">В этом разделе описывается синтаксис.</span><span class="sxs-lookup"><span data-stu-id="76451-105">This topic describes the syntax.</span></span> <span data-ttu-id="76451-106">В среде выполнения Effect этот синтаксис будет преобразован в вызов [**ID3D11Device:: креатежеометришадервисстреамаутпут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span><span class="sxs-lookup"><span data-stu-id="76451-106">In the effect runtime, this syntax will be converted to a call to [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span></span>

## <a name="construct-syntax"></a><span data-ttu-id="76451-107">Синтаксис конструкции</span><span class="sxs-lookup"><span data-stu-id="76451-107">Construct Syntax</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| <span data-ttu-id="76451-108">Имя</span><span class="sxs-lookup"><span data-stu-id="76451-108">Name</span></span>                   | <span data-ttu-id="76451-109">Описание</span><span class="sxs-lookup"><span data-stu-id="76451-109">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76451-110">**стреамингшадервар**</span><span class="sxs-lookup"><span data-stu-id="76451-110">**StreamingShaderVar**</span></span> | <span data-ttu-id="76451-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="76451-111">Optional.</span></span> <span data-ttu-id="76451-112">Строка АСЦИ, однозначно определяющая имя переменной шейдера Geometry с выходом из потоков. Это необязательно, так как Конструктгсвиссо можно разместить непосредственно в вызове Сетжеометришадер или Биндинтерфацес.</span><span class="sxs-lookup"><span data-stu-id="76451-112">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="76451-113">**шадервар**</span><span class="sxs-lookup"><span data-stu-id="76451-113">**ShaderVar**</span></span>          | <span data-ttu-id="76451-114">Переменная шейдера geometry или Вершинный шейдер.</span><span class="sxs-lookup"><span data-stu-id="76451-114">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="76451-115">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="76451-115">**OutputDecl0**</span></span>        | <span data-ttu-id="76451-116">Строка, определяющая потоки вывода шейдера в потоке 0. Синтаксис см. ниже.</span><span class="sxs-lookup"><span data-stu-id="76451-116">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |



 

<span data-ttu-id="76451-117">Этот синтаксис был определен в \_ файлах FX 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="76451-117">This is the syntax was defined in fx\_4\_0 files.</span></span> <span data-ttu-id="76451-118">Обратите внимание, что в GS \_ 4 \_ 0 и VS \_ x есть только один поток данных.</span><span class="sxs-lookup"><span data-stu-id="76451-118">Note that in gs\_4\_0 and vs\_x shaders, there is only one stream of data.</span></span> <span data-ttu-id="76451-119">Полученный шейдер будет выводить один поток как в поток, так и в блок средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="76451-119">The resulting shader will output one stream to both the stream out unit and the rasterizer unit.</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| <span data-ttu-id="76451-120">Имя</span><span class="sxs-lookup"><span data-stu-id="76451-120">Name</span></span>                   | <span data-ttu-id="76451-121">Описание</span><span class="sxs-lookup"><span data-stu-id="76451-121">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76451-122">**стреамингшадервар**</span><span class="sxs-lookup"><span data-stu-id="76451-122">**StreamingShaderVar**</span></span> | <span data-ttu-id="76451-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="76451-123">Optional.</span></span> <span data-ttu-id="76451-124">Строка АСЦИ, однозначно определяющая имя переменной шейдера Geometry с выходом из потоков. Это необязательно, так как Конструктгсвиссо можно разместить непосредственно в вызове Сетжеометришадер или Биндинтерфацес.</span><span class="sxs-lookup"><span data-stu-id="76451-124">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="76451-125">**шадервар**</span><span class="sxs-lookup"><span data-stu-id="76451-125">**ShaderVar**</span></span>          | <span data-ttu-id="76451-126">Переменная шейдера geometry или Вершинный шейдер.</span><span class="sxs-lookup"><span data-stu-id="76451-126">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="76451-127">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="76451-127">**OutputDecl0**</span></span>        | <span data-ttu-id="76451-128">Строка, определяющая потоки вывода шейдера в потоке 0. Синтаксис см. ниже.</span><span class="sxs-lookup"><span data-stu-id="76451-128">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="76451-129">**OutputDecl1**</span><span class="sxs-lookup"><span data-stu-id="76451-129">**OutputDecl1**</span></span>        | <span data-ttu-id="76451-130">Строка, определяющая потоки вывода шейдера в потоке 1. Синтаксис см. ниже.</span><span class="sxs-lookup"><span data-stu-id="76451-130">A string defining which shader outputs in stream 1 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="76451-131">**OutputDecl2**</span><span class="sxs-lookup"><span data-stu-id="76451-131">**OutputDecl2**</span></span>        | <span data-ttu-id="76451-132">Строка, определяющая потоки вывода шейдера в потоке 2. Синтаксис см. ниже.</span><span class="sxs-lookup"><span data-stu-id="76451-132">A string defining which shader outputs in stream 2 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="76451-133">**OutputDecl3**</span><span class="sxs-lookup"><span data-stu-id="76451-133">**OutputDecl3**</span></span>        | <span data-ttu-id="76451-134">Строка, определяющая выходные данные шейдера в потоке 3. Синтаксис см. ниже.</span><span class="sxs-lookup"><span data-stu-id="76451-134">A string defining which shader outputs in stream 3 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="76451-135">**растеризедстреам**</span><span class="sxs-lookup"><span data-stu-id="76451-135">**RasterizedStream**</span></span>   | <span data-ttu-id="76451-136">Целое число, указывающее, какой поток будет отправлен в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="76451-136">An integer specifying which stream will be sent to the rasterizer.</span></span>                                                                                                                                                         |



 

<span data-ttu-id="76451-137">Обратите внимание, что \_ \_ шейдеры GS 5 0 могут определять до четырех потоков данных.</span><span class="sxs-lookup"><span data-stu-id="76451-137">Note that gs\_5\_0 shaders can define up to four streams of data.</span></span> <span data-ttu-id="76451-138">Полученный шейдер выводит один поток в потоковую единицу для каждого объявления вывода, отличного от **null** , и один поток, являющийся единицей средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="76451-138">The resulting shader will output one stream to the stream out unit for each non-**NULL** output declaration and one stream the rasterizer unit.</span></span>

## <a name="stream-out-declaration-syntax"></a><span data-ttu-id="76451-139">Синтаксис объявления Stream out</span><span class="sxs-lookup"><span data-stu-id="76451-139">Stream Out Declaration Syntax</span></span>


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| <span data-ttu-id="76451-140">Имя</span><span class="sxs-lookup"><span data-stu-id="76451-140">Name</span></span>              | <span data-ttu-id="76451-141">Описание</span><span class="sxs-lookup"><span data-stu-id="76451-141">Description</span></span>                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76451-142">**Буфер**</span><span class="sxs-lookup"><span data-stu-id="76451-142">**Buffer**</span></span>        | <span data-ttu-id="76451-143">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="76451-143">Optional.</span></span> <span data-ttu-id="76451-144">Целое число, 0 <= buffer < 4, определяющее потоковый буфер, к которому будет переходить значение.</span><span class="sxs-lookup"><span data-stu-id="76451-144">An integer, 0 <= Buffer < 4, specifying which stream out buffer the value will go to.</span></span> |
| <span data-ttu-id="76451-145">**Семантическ**</span><span class="sxs-lookup"><span data-stu-id="76451-145">**Semantic**</span></span>      | <span data-ttu-id="76451-146">Строка вместе с СемантиЦиндекс, указывающая значение для вывода.</span><span class="sxs-lookup"><span data-stu-id="76451-146">A string, along with SemanticIndex, specifying which value to output.</span></span>                                 |
| <span data-ttu-id="76451-147">**семантиЦиндекс**</span><span class="sxs-lookup"><span data-stu-id="76451-147">**SemanticIndex**</span></span> | <span data-ttu-id="76451-148">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="76451-148">Optional.</span></span> <span data-ttu-id="76451-149">Индекс, связанный с семантикой.</span><span class="sxs-lookup"><span data-stu-id="76451-149">The index associated with Semantic.</span></span>                                                         |
| <span data-ttu-id="76451-150">**Mask**</span><span class="sxs-lookup"><span data-stu-id="76451-150">**Mask**</span></span>          | <span data-ttu-id="76451-151">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="76451-151">Optional.</span></span> <span data-ttu-id="76451-152">Маска компонента, указывающая, какие компоненты значения следует выводить.</span><span class="sxs-lookup"><span data-stu-id="76451-152">A component mask, indicating which components of the value to output.</span></span>                       |



 

<span data-ttu-id="76451-153">Существует одна специальная семантика с меткой "$SKIP", которая указывает на пустую семантику, что приводит к несенсорной записи соответствующей памяти в выходном буфере потока.</span><span class="sxs-lookup"><span data-stu-id="76451-153">There is one special Semantic, labeled "$SKIP" which indicates an empty semantic, leaving the corresponding memory in the stream out buffer untouched.</span></span> <span data-ttu-id="76451-154">Семантическая $SKIP не может иметь СемантиЦиндекс, но может иметь маску.</span><span class="sxs-lookup"><span data-stu-id="76451-154">The $SKIP semantic cannot have a SemanticIndex, but can have a Mask.</span></span>

<span data-ttu-id="76451-155">Все выходные объявления потока могут иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="76451-155">The entire stream out declaration can be **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="76451-156">Например, .</span><span class="sxs-lookup"><span data-stu-id="76451-156">Example</span></span>


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="76451-157">См. также</span><span class="sxs-lookup"><span data-stu-id="76451-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76451-158">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="76451-158">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




