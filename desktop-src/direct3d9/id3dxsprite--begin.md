---
description: Подготавливает устройство для рисования спрайтов.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'Метод ID3DXSprite:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713771"
---
# <a name="id3dxspritebegin-method"></a><span data-ttu-id="bd207-103">Метод ID3DXSprite:: Begin</span><span class="sxs-lookup"><span data-stu-id="bd207-103">ID3DXSprite::Begin method</span></span>

<span data-ttu-id="bd207-104">Подготавливает устройство для рисования спрайтов.</span><span class="sxs-lookup"><span data-stu-id="bd207-104">Prepares a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd207-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd207-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="bd207-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd207-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd207-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bd207-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd207-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bd207-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bd207-109">Сочетание одного или нескольких флагов, описывающих параметры визуализации спрайта.</span><span class="sxs-lookup"><span data-stu-id="bd207-109">Combination of zero or more flags that describe sprite rendering options.</span></span> <span data-ttu-id="bd207-110">Для этого метода допустимы следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="bd207-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="bd207-111">D3DXSPRITE \_ алфабленд</span><span class="sxs-lookup"><span data-stu-id="bd207-111">D3DXSPRITE\_ALPHABLEND</span></span>
-   <span data-ttu-id="bd207-112">D3DXSPRITEный \_ \_ стенд</span><span class="sxs-lookup"><span data-stu-id="bd207-112">D3DXSPRITE\_\_BILLBOARD</span></span>
-   <span data-ttu-id="bd207-113">D3DXSPRITE \_ донотмодифи \_ рендерстате</span><span class="sxs-lookup"><span data-stu-id="bd207-113">D3DXSPRITE\_DONOTMODIFY\_RENDERSTATE</span></span>
-   <span data-ttu-id="bd207-114">D3DXSPRITE \_ донотсавестате</span><span class="sxs-lookup"><span data-stu-id="bd207-114">D3DXSPRITE\_DONOTSAVESTATE</span></span>
-   <span data-ttu-id="bd207-115">D3DXSPRITE \_ обжектспаце</span><span class="sxs-lookup"><span data-stu-id="bd207-115">D3DXSPRITE\_OBJECTSPACE</span></span>
-   <span data-ttu-id="bd207-116">D3DXSPRITE \_ \_ Сортировка \_ глубины \_ бакктофронт</span><span class="sxs-lookup"><span data-stu-id="bd207-116">D3DXSPRITE\_\_SORT\_DEPTH\_BACKTOFRONT</span></span>
-   <span data-ttu-id="bd207-117">D3DXSPRITE \_ \_ Сортировка \_ глубины \_ фронттобакк</span><span class="sxs-lookup"><span data-stu-id="bd207-117">D3DXSPRITE\_\_SORT\_DEPTH\_FRONTTOBACK</span></span>
-   <span data-ttu-id="bd207-118">\_ \_ \_ ТЕКСТУРа сортировки D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="bd207-118">D3DXSPRITE\_\_SORT\_TEXTURE</span></span>

<span data-ttu-id="bd207-119">Описание флагов и сведения о том, как управлять записью состояния устройства и преобразованиями представлений устройств, см. в разделе [D3DXSPRITE](d3dxsprite.md).</span><span class="sxs-lookup"><span data-stu-id="bd207-119">For a description of the flags and for information on how to control device state capture and device view transforms, see [D3DXSPRITE](d3dxsprite.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd207-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd207-120">Return value</span></span>

<span data-ttu-id="bd207-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd207-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd207-122">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="bd207-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bd207-123">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bd207-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd207-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd207-124">Remarks</span></span>

<span data-ttu-id="bd207-125">Этот метод должен вызываться из [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="bd207-125">This method must be called from inside a [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) .</span></span> <span data-ttu-id="bd207-126">.</span><span class="sxs-lookup"><span data-stu-id="bd207-126">.</span></span> <span data-ttu-id="bd207-127">.</span><span class="sxs-lookup"><span data-stu-id="bd207-127">.</span></span> <span data-ttu-id="bd207-128">Последовательность [**IDirect3DDevice9:: ендсцене**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="bd207-128">[**IDirect3DDevice9::EndScene**](/windows/desktop/api) sequence.</span></span> <span data-ttu-id="bd207-129">**ID3DXSprite:: Begin** не может использоваться в качестве замены для **IDirect3DDevice9:: бегинсцене** или [**ID3DXRenderToSurface:: бегинсцене**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="bd207-129">**ID3DXSprite::Begin** cannot be used as a substitute for either **IDirect3DDevice9::BeginScene** or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

<span data-ttu-id="bd207-130">Этот метод настроит следующие состояния на устройстве.</span><span class="sxs-lookup"><span data-stu-id="bd207-130">This method will set the following states on the device.</span></span>

<span data-ttu-id="bd207-131">Состояния рендеринга:</span><span class="sxs-lookup"><span data-stu-id="bd207-131">Render States:</span></span>



| <span data-ttu-id="bd207-132">Тип ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="bd207-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span></span> | <span data-ttu-id="bd207-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bd207-133">Value</span></span>                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd207-134">D3DRS \_ алфабленденабле</span><span class="sxs-lookup"><span data-stu-id="bd207-134">D3DRS\_ALPHABLENDENABLE</span></span>                                       | <span data-ttu-id="bd207-135">true</span><span class="sxs-lookup"><span data-stu-id="bd207-135">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="bd207-136">D3DRS \_ алфафунк</span><span class="sxs-lookup"><span data-stu-id="bd207-136">D3DRS\_ALPHAFUNC</span></span>                                              | <span data-ttu-id="bd207-137">D3DCMP \_</span><span class="sxs-lookup"><span data-stu-id="bd207-137">D3DCMP\_GREATER</span></span>                                                                                                   |
| <span data-ttu-id="bd207-138">D3DRS \_ алфареф</span><span class="sxs-lookup"><span data-stu-id="bd207-138">D3DRS\_ALPHAREF</span></span>                                               | <span data-ttu-id="bd207-139">0x00</span><span class="sxs-lookup"><span data-stu-id="bd207-139">0x00</span></span>                                                                                                              |
| <span data-ttu-id="bd207-140">D3DRS \_ алфатестенабле</span><span class="sxs-lookup"><span data-stu-id="bd207-140">D3DRS\_ALPHATESTENABLE</span></span>                                        | <span data-ttu-id="bd207-141">алфакмпкапс</span><span class="sxs-lookup"><span data-stu-id="bd207-141">AlphaCmpCaps</span></span>                                                                                                      |
| <span data-ttu-id="bd207-142">D3DRS \_ блендоп</span><span class="sxs-lookup"><span data-stu-id="bd207-142">D3DRS\_BLENDOP</span></span>                                                | <span data-ttu-id="bd207-143">D3DBLENDOP \_ Добавить</span><span class="sxs-lookup"><span data-stu-id="bd207-143">D3DBLENDOP\_ADD</span></span>                                                                                                   |
| <span data-ttu-id="bd207-144">D3DRS \_ Обрезка</span><span class="sxs-lookup"><span data-stu-id="bd207-144">D3DRS\_CLIPPING</span></span>                                               | <span data-ttu-id="bd207-145">true</span><span class="sxs-lookup"><span data-stu-id="bd207-145">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="bd207-146">D3DRS \_ клиппланинабле</span><span class="sxs-lookup"><span data-stu-id="bd207-146">D3DRS\_CLIPPLANEENABLE</span></span>                                        | <span data-ttu-id="bd207-147">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-147">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-148">D3DRS \_ колорвритинабле</span><span class="sxs-lookup"><span data-stu-id="bd207-148">D3DRS\_COLORWRITEENABLE</span></span>                                       | <span data-ttu-id="bd207-149">D3DCOLORWRITEENABLE \_ альфа \| D3DCOLORWRITEENABLE \_ Blue \| D3DCOLORWRITEENABLE \_ зеленый \| D3DCOLORWRITEENABLE \_ красный</span><span class="sxs-lookup"><span data-stu-id="bd207-149">D3DCOLORWRITEENABLE\_ALPHA \| D3DCOLORWRITEENABLE\_BLUE \| D3DCOLORWRITEENABLE\_GREEN \| D3DCOLORWRITEENABLE\_RED</span></span> |
| <span data-ttu-id="bd207-150">D3DRS \_ куллмоде</span><span class="sxs-lookup"><span data-stu-id="bd207-150">D3DRS\_CULLMODE</span></span>                                               | <span data-ttu-id="bd207-151">D3DCULL \_ None</span><span class="sxs-lookup"><span data-stu-id="bd207-151">D3DCULL\_NONE</span></span>                                                                                                     |
| <span data-ttu-id="bd207-152">D3DRS \_ дестбленд</span><span class="sxs-lookup"><span data-stu-id="bd207-152">D3DRS\_DESTBLEND</span></span>                                              | <span data-ttu-id="bd207-153">D3DBLEND \_ инвсркалфа</span><span class="sxs-lookup"><span data-stu-id="bd207-153">D3DBLEND\_INVSRCALPHA</span></span>                                                                                             |
| <span data-ttu-id="bd207-154">D3DRS \_ диффусематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="bd207-154">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>                                  | <span data-ttu-id="bd207-155">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="bd207-155">D3DMCS\_COLOR1</span></span>                                                                                                    |
| <span data-ttu-id="bd207-156">D3DRS \_ енаблеадаптиветесселлатион</span><span class="sxs-lookup"><span data-stu-id="bd207-156">D3DRS\_ENABLEADAPTIVETESSELLATION</span></span>                             | <span data-ttu-id="bd207-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-157">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-158">D3DRS \_ филлмоде</span><span class="sxs-lookup"><span data-stu-id="bd207-158">D3DRS\_FILLMODE</span></span>                                               | <span data-ttu-id="bd207-159">D3DFILL \_</span><span class="sxs-lookup"><span data-stu-id="bd207-159">D3DFILL\_SOLID</span></span>                                                                                                    |
| <span data-ttu-id="bd207-160">D3DRS \_ фоженабле</span><span class="sxs-lookup"><span data-stu-id="bd207-160">D3DRS\_FOGENABLE</span></span>                                              | <span data-ttu-id="bd207-161">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-161">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-162">D3DRS \_ индекседвертексбленденабле</span><span class="sxs-lookup"><span data-stu-id="bd207-162">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>                               | <span data-ttu-id="bd207-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-163">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-164">\_Освещение D3DRS</span><span class="sxs-lookup"><span data-stu-id="bd207-164">D3DRS\_LIGHTING</span></span>                                               | <span data-ttu-id="bd207-165">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-165">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-166">D3DRS \_ ранжефоженабле</span><span class="sxs-lookup"><span data-stu-id="bd207-166">D3DRS\_RANGEFOGENABLE</span></span>                                         | <span data-ttu-id="bd207-167">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-167">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-168">D3DRS \_ сепаратеалфабленденабле</span><span class="sxs-lookup"><span data-stu-id="bd207-168">D3DRS\_SEPARATEALPHABLENDENABLE</span></span>                               | <span data-ttu-id="bd207-169">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-169">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-170">D3DRS \_ шадемоде</span><span class="sxs-lookup"><span data-stu-id="bd207-170">D3DRS\_SHADEMODE</span></span>                                              | <span data-ttu-id="bd207-171">D3DSHADE метод \_ Гуро</span><span class="sxs-lookup"><span data-stu-id="bd207-171">D3DSHADE\_GOURAUD</span></span>                                                                                                 |
| <span data-ttu-id="bd207-172">D3DRS \_ спекуларенабле</span><span class="sxs-lookup"><span data-stu-id="bd207-172">D3DRS\_SPECULARENABLE</span></span>                                         | <span data-ttu-id="bd207-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-173">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-174">D3DRS \_ сркбленд</span><span class="sxs-lookup"><span data-stu-id="bd207-174">D3DRS\_SRCBLEND</span></span>                                               | <span data-ttu-id="bd207-175">D3DBLEND \_ сркалфа</span><span class="sxs-lookup"><span data-stu-id="bd207-175">D3DBLEND\_SRCALPHA</span></span>                                                                                                |
| <span data-ttu-id="bd207-176">D3DRS \_ сргбвритинабле</span><span class="sxs-lookup"><span data-stu-id="bd207-176">D3DRS\_SRGBWRITEENABLE</span></span>                                        | <span data-ttu-id="bd207-177">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-177">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-178">D3DRS \_ стенЦиленабле</span><span class="sxs-lookup"><span data-stu-id="bd207-178">D3DRS\_STENCILENABLE</span></span>                                          | <span data-ttu-id="bd207-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-179">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-180">D3DRS \_ вертексбленд</span><span class="sxs-lookup"><span data-stu-id="bd207-180">D3DRS\_VERTEXBLEND</span></span>                                            | <span data-ttu-id="bd207-181">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd207-181">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="bd207-182">D3DRS \_ WRAP0</span><span class="sxs-lookup"><span data-stu-id="bd207-182">D3DRS\_WRAP0</span></span>                                                  | <span data-ttu-id="bd207-183">0</span><span class="sxs-lookup"><span data-stu-id="bd207-183">0</span></span>                                                                                                                 |



 

<span data-ttu-id="bd207-184">Состояние этапа текстуры:</span><span class="sxs-lookup"><span data-stu-id="bd207-184">Texture Stage States:</span></span>



| <span data-ttu-id="bd207-185">Идентификатор этапа</span><span class="sxs-lookup"><span data-stu-id="bd207-185">Stage Identifier</span></span> | <span data-ttu-id="bd207-186">Тип ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span><span class="sxs-lookup"><span data-stu-id="bd207-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span></span> | <span data-ttu-id="bd207-187">Значение</span><span class="sxs-lookup"><span data-stu-id="bd207-187">Value</span></span>            |
|------------------|---------------------------------------------------------------------------|------------------|
| <span data-ttu-id="bd207-188">0</span><span class="sxs-lookup"><span data-stu-id="bd207-188">0</span></span>                | <span data-ttu-id="bd207-189">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="bd207-189">D3DTSS\_ALPHAARG1</span></span>                                                         | <span data-ttu-id="bd207-190">\_Текстура D3DTA</span><span class="sxs-lookup"><span data-stu-id="bd207-190">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="bd207-191">0</span><span class="sxs-lookup"><span data-stu-id="bd207-191">0</span></span>                | <span data-ttu-id="bd207-192">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="bd207-192">D3DTSS\_ALPHAARG2</span></span>                                                         | <span data-ttu-id="bd207-193">D3DTA \_ диффузный</span><span class="sxs-lookup"><span data-stu-id="bd207-193">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="bd207-194">0</span><span class="sxs-lookup"><span data-stu-id="bd207-194">0</span></span>                | <span data-ttu-id="bd207-195">D3DTSS \_ алфаоп</span><span class="sxs-lookup"><span data-stu-id="bd207-195">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="bd207-196">D3DTOPная \_ модуляция</span><span class="sxs-lookup"><span data-stu-id="bd207-196">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="bd207-197">0</span><span class="sxs-lookup"><span data-stu-id="bd207-197">0</span></span>                | <span data-ttu-id="bd207-198">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="bd207-198">D3DTSS\_COLORARG1</span></span>                                                         | <span data-ttu-id="bd207-199">\_Текстура D3DTA</span><span class="sxs-lookup"><span data-stu-id="bd207-199">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="bd207-200">0</span><span class="sxs-lookup"><span data-stu-id="bd207-200">0</span></span>                | <span data-ttu-id="bd207-201">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="bd207-201">D3DTSS\_COLORARG2</span></span>                                                         | <span data-ttu-id="bd207-202">D3DTA \_ диффузный</span><span class="sxs-lookup"><span data-stu-id="bd207-202">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="bd207-203">0</span><span class="sxs-lookup"><span data-stu-id="bd207-203">0</span></span>                | <span data-ttu-id="bd207-204">D3DTSS \_ колороп</span><span class="sxs-lookup"><span data-stu-id="bd207-204">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="bd207-205">D3DTOPная \_ модуляция</span><span class="sxs-lookup"><span data-stu-id="bd207-205">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="bd207-206">0</span><span class="sxs-lookup"><span data-stu-id="bd207-206">0</span></span>                | <span data-ttu-id="bd207-207">D3DTSS \_ текскурдиндекс</span><span class="sxs-lookup"><span data-stu-id="bd207-207">D3DTSS\_TEXCOORDINDEX</span></span>                                                     | <span data-ttu-id="bd207-208">0</span><span class="sxs-lookup"><span data-stu-id="bd207-208">0</span></span>                |
| <span data-ttu-id="bd207-209">0</span><span class="sxs-lookup"><span data-stu-id="bd207-209">0</span></span>                | <span data-ttu-id="bd207-210">D3DTSS \_ текстуретрансформфлагс</span><span class="sxs-lookup"><span data-stu-id="bd207-210">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>                                             | <span data-ttu-id="bd207-211">\_Отключение D3DTTFF</span><span class="sxs-lookup"><span data-stu-id="bd207-211">D3DTTFF\_DISABLE</span></span> |
| <span data-ttu-id="bd207-212">1</span><span class="sxs-lookup"><span data-stu-id="bd207-212">1</span></span>                | <span data-ttu-id="bd207-213">D3DTSS \_ алфаоп</span><span class="sxs-lookup"><span data-stu-id="bd207-213">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="bd207-214">\_Отключение D3DTOP</span><span class="sxs-lookup"><span data-stu-id="bd207-214">D3DTOP\_DISABLE</span></span>  |
| <span data-ttu-id="bd207-215">1</span><span class="sxs-lookup"><span data-stu-id="bd207-215">1</span></span>                | <span data-ttu-id="bd207-216">D3DTSS \_ колороп</span><span class="sxs-lookup"><span data-stu-id="bd207-216">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="bd207-217">\_Отключение D3DTOP</span><span class="sxs-lookup"><span data-stu-id="bd207-217">D3DTOP\_DISABLE</span></span>  |



 

<span data-ttu-id="bd207-218">Состояния образцов:</span><span class="sxs-lookup"><span data-stu-id="bd207-218">Sampler States:</span></span>



| <span data-ttu-id="bd207-219">Индекс этапа образца</span><span class="sxs-lookup"><span data-stu-id="bd207-219">Sampler Stage Index</span></span> | <span data-ttu-id="bd207-220">Тип ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="bd207-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span></span> | <span data-ttu-id="bd207-221">Значение</span><span class="sxs-lookup"><span data-stu-id="bd207-221">Value</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd207-222">0</span><span class="sxs-lookup"><span data-stu-id="bd207-222">0</span></span>                   | <span data-ttu-id="bd207-223">D3DSAMP \_ аддрессу</span><span class="sxs-lookup"><span data-stu-id="bd207-223">D3DSAMP\_ADDRESSU</span></span>                                               | <span data-ttu-id="bd207-224">D3DTADDRESSный \_ срез</span><span class="sxs-lookup"><span data-stu-id="bd207-224">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="bd207-225">0</span><span class="sxs-lookup"><span data-stu-id="bd207-225">0</span></span>                   | <span data-ttu-id="bd207-226">D3DSAMP \_ аддрессв</span><span class="sxs-lookup"><span data-stu-id="bd207-226">D3DSAMP\_ADDRESSV</span></span>                                               | <span data-ttu-id="bd207-227">D3DTADDRESSный \_ срез</span><span class="sxs-lookup"><span data-stu-id="bd207-227">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="bd207-228">0</span><span class="sxs-lookup"><span data-stu-id="bd207-228">0</span></span>                   | <span data-ttu-id="bd207-229">D3DSAMP \_ магфилтер</span><span class="sxs-lookup"><span data-stu-id="bd207-229">D3DSAMP\_MAGFILTER</span></span>                                              | <span data-ttu-id="bd207-230">D3DTEXF \_ анизотроп, если текстурефилтеркапс включает D3DPTFILTERCAPS \_ магфанисотропик; в противном случае — \_ линейное D3DTEXF</span><span class="sxs-lookup"><span data-stu-id="bd207-230">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MAGFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="bd207-231">0</span><span class="sxs-lookup"><span data-stu-id="bd207-231">0</span></span>                   | <span data-ttu-id="bd207-232">D3DSAMP \_ максмиплевел</span><span class="sxs-lookup"><span data-stu-id="bd207-232">D3DSAMP\_MAXMIPLEVEL</span></span>                                            | <span data-ttu-id="bd207-233">0</span><span class="sxs-lookup"><span data-stu-id="bd207-233">0</span></span>                                                                                                              |
| <span data-ttu-id="bd207-234">0</span><span class="sxs-lookup"><span data-stu-id="bd207-234">0</span></span>                   | <span data-ttu-id="bd207-235">D3DSAMP \_ максанисотропи</span><span class="sxs-lookup"><span data-stu-id="bd207-235">D3DSAMP\_MAXANISOTROPY</span></span>                                          | <span data-ttu-id="bd207-236">максанисотропи</span><span class="sxs-lookup"><span data-stu-id="bd207-236">MaxAnisotropy</span></span>                                                                                                  |
| <span data-ttu-id="bd207-237">0</span><span class="sxs-lookup"><span data-stu-id="bd207-237">0</span></span>                   | <span data-ttu-id="bd207-238">D3DSAMP \_ минфилтер</span><span class="sxs-lookup"><span data-stu-id="bd207-238">D3DSAMP\_MINFILTER</span></span>                                              | <span data-ttu-id="bd207-239">D3DTEXF \_ анизотроп, если текстурефилтеркапс включает D3DPTFILTERCAPS \_ минфанисотропик; в противном случае — \_ линейное D3DTEXF</span><span class="sxs-lookup"><span data-stu-id="bd207-239">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MINFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="bd207-240">0</span><span class="sxs-lookup"><span data-stu-id="bd207-240">0</span></span>                   | <span data-ttu-id="bd207-241">D3DSAMP \_ мипфилтер</span><span class="sxs-lookup"><span data-stu-id="bd207-241">D3DSAMP\_MIPFILTER</span></span>                                              | <span data-ttu-id="bd207-242">D3DTEXF \_ линейный, если текстурефилтеркапс включает D3DPTFILTERCAPS \_ мипфлинеар; в противном случае D3DTEXF \_ Point</span><span class="sxs-lookup"><span data-stu-id="bd207-242">D3DTEXF\_LINEAR if TextureFilterCaps includes D3DPTFILTERCAPS\_MIPFLINEAR; otherwise D3DTEXF\_POINT</span></span>            |
| <span data-ttu-id="bd207-243">0</span><span class="sxs-lookup"><span data-stu-id="bd207-243">0</span></span>                   | <span data-ttu-id="bd207-244">D3DSAMP \_ мипмаплодбиас</span><span class="sxs-lookup"><span data-stu-id="bd207-244">D3DSAMP\_MIPMAPLODBIAS</span></span>                                          | <span data-ttu-id="bd207-245">0</span><span class="sxs-lookup"><span data-stu-id="bd207-245">0</span></span>                                                                                                              |
| <span data-ttu-id="bd207-246">0</span><span class="sxs-lookup"><span data-stu-id="bd207-246">0</span></span>                   | <span data-ttu-id="bd207-247">D3DSAMP \_ сргбтекстуре</span><span class="sxs-lookup"><span data-stu-id="bd207-247">D3DSAMP\_SRGBTEXTURE</span></span>                                            | <span data-ttu-id="bd207-248">0</span><span class="sxs-lookup"><span data-stu-id="bd207-248">0</span></span>                                                                                                              |



 

> [!Note]  
> <span data-ttu-id="bd207-249">Этот метод отключает N-патчи.</span><span class="sxs-lookup"><span data-stu-id="bd207-249">This method disables N-patches.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd207-250">Требования</span><span class="sxs-lookup"><span data-stu-id="bd207-250">Requirements</span></span>



| <span data-ttu-id="bd207-251">Требование</span><span class="sxs-lookup"><span data-stu-id="bd207-251">Requirement</span></span> | <span data-ttu-id="bd207-252">Значение</span><span class="sxs-lookup"><span data-stu-id="bd207-252">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd207-253">Header</span><span class="sxs-lookup"><span data-stu-id="bd207-253">Header</span></span><br/>  | <dl> <span data-ttu-id="bd207-254"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd207-254"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bd207-255">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bd207-255">Library</span></span><br/> | <dl> <span data-ttu-id="bd207-256"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd207-256"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd207-257">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd207-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd207-258">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="bd207-258">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="bd207-259">D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="bd207-259">D3DXSPRITE</span></span>](d3dxsprite.md)
</dt> </dl>

 

 
