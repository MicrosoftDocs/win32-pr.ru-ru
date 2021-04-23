---
description: Блок состояния можно использовать для захвата только состояния вершины (см. раздел состояния сохранение и восстановление состояния (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Сохранение состояний вершин с помощью Статеблокк (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691999"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="b5321-103">Сохранение состояний вершин с помощью Статеблокк (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b5321-103">Saving Vertex States With a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="b5321-104">Блок состояния можно использовать для захвата только состояния вершины (см. раздел [состояния сохранение и восстановление состояния (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="b5321-104">A state block can be used to capture only vertex state (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="b5321-105">Следующее состояние — состояние вершины:</span><span class="sxs-lookup"><span data-stu-id="b5321-105">The following state is vertex state:</span></span>

-   <span data-ttu-id="b5321-106">Состояние визуализации вершины (см. [конвейер вершин: состояние рендеринга](#vertex-pipeline-render-state)).</span><span class="sxs-lookup"><span data-stu-id="b5321-106">Vertex render state (see [Vertex Pipeline: Render State](#vertex-pipeline-render-state)).</span></span>
-   <span data-ttu-id="b5321-107">Состояние образца вершин (см. раздел [конвейер вершин: состояние](#vertex-pipeline-sampler-state)выборки).</span><span class="sxs-lookup"><span data-stu-id="b5321-107">Vertex sampler state (see [Vertex Pipeline: Sampler State](#vertex-pipeline-sampler-state)).</span></span>
-   <span data-ttu-id="b5321-108">Состояние текстуры вершин (см. раздел [конвейер вершин: состояние текстуры](#vertex-pipeline-texture-state)).</span><span class="sxs-lookup"><span data-stu-id="b5321-108">Vertex texture state (see [Vertex Pipeline: Texture State](#vertex-pipeline-texture-state)).</span></span>
-   <span data-ttu-id="b5321-109">Нпатч режима в [**IDirect3DDevice9:: сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="b5321-109">The NPatch mode segments from [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>
-   <span data-ttu-id="b5321-110">Каждый источник освещения из [**IDirect3DDevice9:: сетлигхт**](/windows/desktop/api), а также включение или выключение освещения с помощью [**IDirect3DDevice9::**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)допустить.</span><span class="sxs-lookup"><span data-stu-id="b5321-110">Each light from [**IDirect3DDevice9::SetLight**](/windows/desktop/api), as well as whether or not the light is enabled with [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>
-   <span data-ttu-id="b5321-111">Текущий шейдер вершин и все константы шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="b5321-111">The current vertex shader and each of the vertex shader constants.</span></span>
-   <span data-ttu-id="b5321-112">Для каждого потока вершин сохраните значение разделителя из [**IDirect3DDevice9:: сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="b5321-112">For each vertex stream, store the divider value from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="b5321-113">Текущее объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="b5321-113">The current vertex declaration.</span></span>

<span data-ttu-id="b5321-114">Чтобы записать состояние вершины в блоке состояния, укажите D3DSBT \_ вертексстате при вызове [**IDirect3DDevice9:: креатестатеблокк**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="b5321-114">To capture vertex state with a state block, specify D3DSBT\_VERTEXSTATE when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="vertex-pipeline-render-state"></a><span data-ttu-id="b5321-115">Конвейер вершин: состояние визуализации</span><span class="sxs-lookup"><span data-stu-id="b5321-115">Vertex Pipeline: Render State</span></span>

<span data-ttu-id="b5321-116">Состояния визуализации устройства влияют на поведение почти каждой части конвейера.</span><span class="sxs-lookup"><span data-stu-id="b5321-116">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="b5321-117">Состояния отрисовки задаются путем вызова [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="b5321-117">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="b5321-118">В следующей таблице содержатся все состояния подготовки к просмотру, настроенные для состояния вершин.</span><span class="sxs-lookup"><span data-stu-id="b5321-118">The following table includes all render states that set-up vertex state:</span></span>



| <span data-ttu-id="b5321-119">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="b5321-119">Render States</span></span>                           | <span data-ttu-id="b5321-120">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b5321-120">Default Value</span></span>          |
|-----------------------------------------|------------------------|
| <span data-ttu-id="b5321-121">D3DRS \_ куллмоде</span><span class="sxs-lookup"><span data-stu-id="b5321-121">D3DRS\_CULLMODE</span></span>                         | <span data-ttu-id="b5321-122">D3DCULL \_ CCW</span><span class="sxs-lookup"><span data-stu-id="b5321-122">D3DCULL\_CCW</span></span>           |
| <span data-ttu-id="b5321-123">D3DRS \_ фогколор</span><span class="sxs-lookup"><span data-stu-id="b5321-123">D3DRS\_FOGCOLOR</span></span>                         | <span data-ttu-id="b5321-124">0</span><span class="sxs-lookup"><span data-stu-id="b5321-124">0</span></span>                      |
| <span data-ttu-id="b5321-125">D3DRS \_ фогтаблемоде</span><span class="sxs-lookup"><span data-stu-id="b5321-125">D3DRS\_FOGTABLEMODE</span></span>                     | <span data-ttu-id="b5321-126">D3DFOG \_ None</span><span class="sxs-lookup"><span data-stu-id="b5321-126">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="b5321-127">D3DRS \_ фогстарт</span><span class="sxs-lookup"><span data-stu-id="b5321-127">D3DRS\_FOGSTART</span></span>                         | <span data-ttu-id="b5321-128">0</span><span class="sxs-lookup"><span data-stu-id="b5321-128">0</span></span>                      |
| <span data-ttu-id="b5321-129">D3DRS \_ фоженд</span><span class="sxs-lookup"><span data-stu-id="b5321-129">D3DRS\_FOGEND</span></span>                           | <span data-ttu-id="b5321-130">1</span><span class="sxs-lookup"><span data-stu-id="b5321-130">1</span></span>                      |
| <span data-ttu-id="b5321-131">D3DRS \_ фогденсити</span><span class="sxs-lookup"><span data-stu-id="b5321-131">D3DRS\_FOGDENSITY</span></span>                       | <span data-ttu-id="b5321-132">1</span><span class="sxs-lookup"><span data-stu-id="b5321-132">1</span></span>                      |
| <span data-ttu-id="b5321-133">D3DRS \_ ранжефоженабле</span><span class="sxs-lookup"><span data-stu-id="b5321-133">D3DRS\_RANGEFOGENABLE</span></span>                   | <span data-ttu-id="b5321-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="b5321-134">**FALSE**</span></span>              |
| <span data-ttu-id="b5321-135">D3DRS \_ окружение</span><span class="sxs-lookup"><span data-stu-id="b5321-135">D3DRS\_AMBIENT</span></span>                          | <span data-ttu-id="b5321-136">0</span><span class="sxs-lookup"><span data-stu-id="b5321-136">0</span></span>                      |
| <span data-ttu-id="b5321-137">D3DRS \_ колорвертекс</span><span class="sxs-lookup"><span data-stu-id="b5321-137">D3DRS\_COLORVERTEX</span></span>                      | <span data-ttu-id="b5321-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="b5321-138">**TRUE**</span></span>               |
| <span data-ttu-id="b5321-139">D3DRS \_ фогвертексмоде</span><span class="sxs-lookup"><span data-stu-id="b5321-139">D3DRS\_FOGVERTEXMODE</span></span>                    | <span data-ttu-id="b5321-140">D3DFOG \_ None</span><span class="sxs-lookup"><span data-stu-id="b5321-140">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="b5321-141">D3DRS \_ Обрезка</span><span class="sxs-lookup"><span data-stu-id="b5321-141">D3DRS\_CLIPPING</span></span>                         | <span data-ttu-id="b5321-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="b5321-142">**TRUE**</span></span>               |
| <span data-ttu-id="b5321-143">\_Освещение D3DRS</span><span class="sxs-lookup"><span data-stu-id="b5321-143">D3DRS\_LIGHTING</span></span>                         | <span data-ttu-id="b5321-144">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="b5321-144">**TRUE**</span></span>               |
| <span data-ttu-id="b5321-145">D3DRS \_ локалвиевер</span><span class="sxs-lookup"><span data-stu-id="b5321-145">D3DRS\_LOCALVIEWER</span></span>                      | <span data-ttu-id="b5321-146">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="b5321-146">**TRUE**</span></span>               |
| <span data-ttu-id="b5321-147">D3DRS \_ емиссивематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="b5321-147">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>           | <span data-ttu-id="b5321-148">\_Материал D3DMCS</span><span class="sxs-lookup"><span data-stu-id="b5321-148">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="b5321-149">D3DRS \_ амбиентматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="b5321-149">D3DRS\_AMBIENTMATERIALSOURCE</span></span>            | <span data-ttu-id="b5321-150">\_Материал D3DMCS</span><span class="sxs-lookup"><span data-stu-id="b5321-150">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="b5321-151">D3DRS \_ диффусематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="b5321-151">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>            | <span data-ttu-id="b5321-152">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="b5321-152">D3DMCS\_COLOR1</span></span>         |
| <span data-ttu-id="b5321-153">D3DRS \_ спекуларматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="b5321-153">D3DRS\_SPECULARMATERIALSOURCE</span></span>           | <span data-ttu-id="b5321-154">D3DMCS \_ COLOR2</span><span class="sxs-lookup"><span data-stu-id="b5321-154">D3DMCS\_COLOR2</span></span>         |
| <span data-ttu-id="b5321-155">D3DRS \_ вертексбленд</span><span class="sxs-lookup"><span data-stu-id="b5321-155">D3DRS\_VERTEXBLEND</span></span>                      | <span data-ttu-id="b5321-156">\_Отключение D3DVBF</span><span class="sxs-lookup"><span data-stu-id="b5321-156">D3DVBF\_DISABLE</span></span>        |
| <span data-ttu-id="b5321-157">D3DRS \_ клиппланинабле</span><span class="sxs-lookup"><span data-stu-id="b5321-157">D3DRS\_CLIPPLANEENABLE</span></span>                  | <span data-ttu-id="b5321-158">0</span><span class="sxs-lookup"><span data-stu-id="b5321-158">0</span></span>                      |
| <span data-ttu-id="b5321-159">D3DRS \_ POINTSIZE</span><span class="sxs-lookup"><span data-stu-id="b5321-159">D3DRS\_POINTSIZE</span></span>                        | <span data-ttu-id="b5321-160">Зависит от драйвера</span><span class="sxs-lookup"><span data-stu-id="b5321-160">Driver dependent</span></span>       |
| <span data-ttu-id="b5321-161">D3DRS \_ POINTSIZE \_ мин</span><span class="sxs-lookup"><span data-stu-id="b5321-161">D3DRS\_POINTSIZE\_MIN</span></span>                   | <span data-ttu-id="b5321-162">1</span><span class="sxs-lookup"><span data-stu-id="b5321-162">1</span></span>                      |
| <span data-ttu-id="b5321-163">D3DRS \_ поинтспритинабле</span><span class="sxs-lookup"><span data-stu-id="b5321-163">D3DRS\_POINTSPRITEENABLE</span></span>                | <span data-ttu-id="b5321-164">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="b5321-164">**FALSE**</span></span>              |
| <span data-ttu-id="b5321-165">D3DRS \_ поинтскалинабле</span><span class="sxs-lookup"><span data-stu-id="b5321-165">D3DRS\_POINTSCALEENABLE</span></span>                 | <span data-ttu-id="b5321-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="b5321-166">**FALSE**</span></span>              |
| <span data-ttu-id="b5321-167">D3DRS \_ поинтскале \_ A</span><span class="sxs-lookup"><span data-stu-id="b5321-167">D3DRS\_POINTSCALE\_A</span></span>                    | <span data-ttu-id="b5321-168">1</span><span class="sxs-lookup"><span data-stu-id="b5321-168">1</span></span>                      |
| <span data-ttu-id="b5321-169">D3DRS \_ поинтскале \_ B</span><span class="sxs-lookup"><span data-stu-id="b5321-169">D3DRS\_POINTSCALE\_B</span></span>                    | <span data-ttu-id="b5321-170">0</span><span class="sxs-lookup"><span data-stu-id="b5321-170">0</span></span>                      |
| <span data-ttu-id="b5321-171">D3DRS \_ поинтскале \_ C</span><span class="sxs-lookup"><span data-stu-id="b5321-171">D3DRS\_POINTSCALE\_C</span></span>                    | <span data-ttu-id="b5321-172">0</span><span class="sxs-lookup"><span data-stu-id="b5321-172">0</span></span>                      |
| <span data-ttu-id="b5321-173">D3DRS \_ мултисамплеантиалиас</span><span class="sxs-lookup"><span data-stu-id="b5321-173">D3DRS\_MULTISAMPLEANTIALIAS</span></span>             | <span data-ttu-id="b5321-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="b5321-174">**TRUE**</span></span>               |
| <span data-ttu-id="b5321-175">D3DRS \_ мултисамплемаск</span><span class="sxs-lookup"><span data-stu-id="b5321-175">D3DRS\_MULTISAMPLEMASK</span></span>                  | <span data-ttu-id="b5321-176">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="b5321-176">0xffffffff</span></span>             |
| <span data-ttu-id="b5321-177">D3DRS \_ патчеджестиле</span><span class="sxs-lookup"><span data-stu-id="b5321-177">D3DRS\_PATCHEDGESTYLE</span></span>                   | <span data-ttu-id="b5321-178">\_Дискретный D3DPATCHEDGE</span><span class="sxs-lookup"><span data-stu-id="b5321-178">D3DPATCHEDGE\_DISCRETE</span></span> |
| <span data-ttu-id="b5321-179">D3DRS \_ POINTSIZE \_ Max</span><span class="sxs-lookup"><span data-stu-id="b5321-179">D3DRS\_POINTSIZE\_MAX</span></span>                   | <span data-ttu-id="b5321-180">1</span><span class="sxs-lookup"><span data-stu-id="b5321-180">1</span></span>                      |
| <span data-ttu-id="b5321-181">D3DRS \_ индекседвертексбленденабле</span><span class="sxs-lookup"><span data-stu-id="b5321-181">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>         | <span data-ttu-id="b5321-182">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="b5321-182">**FALSE**</span></span>              |
| <span data-ttu-id="b5321-183">D3DRS \_ твинфактор</span><span class="sxs-lookup"><span data-stu-id="b5321-183">D3DRS\_TWEENFACTOR</span></span>                      | <span data-ttu-id="b5321-184">0</span><span class="sxs-lookup"><span data-stu-id="b5321-184">0</span></span>                      |
| <span data-ttu-id="b5321-185">D3DRS \_ поситиондегри</span><span class="sxs-lookup"><span data-stu-id="b5321-185">D3DRS\_POSITIONDEGREE</span></span>                   | <span data-ttu-id="b5321-186">D3DDEGREE \_ кубический</span><span class="sxs-lookup"><span data-stu-id="b5321-186">D3DDEGREE\_CUBIC</span></span>       |
| <span data-ttu-id="b5321-187">D3DRS \_ нормалдегри</span><span class="sxs-lookup"><span data-stu-id="b5321-187">D3DRS\_NORMALDEGREE</span></span>                     | <span data-ttu-id="b5321-188">\_Линейная D3DDEGREE</span><span class="sxs-lookup"><span data-stu-id="b5321-188">D3DDEGREE\_LINEAR</span></span>      |
| <span data-ttu-id="b5321-189">D3DRS \_ минтесселлатионлевел</span><span class="sxs-lookup"><span data-stu-id="b5321-189">D3DRS\_MINTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="b5321-190">1</span><span class="sxs-lookup"><span data-stu-id="b5321-190">1</span></span>                      |
| <span data-ttu-id="b5321-191">D3DRS \_ макстесселлатионлевел</span><span class="sxs-lookup"><span data-stu-id="b5321-191">D3DRS\_MAXTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="b5321-192">1</span><span class="sxs-lookup"><span data-stu-id="b5321-192">1</span></span>                      |
| <span data-ttu-id="b5321-193">D3DRS \_ адаптиветесс \_ X</span><span class="sxs-lookup"><span data-stu-id="b5321-193">D3DRS\_ADAPTIVETESS\_X</span></span>                  | <span data-ttu-id="b5321-194">0</span><span class="sxs-lookup"><span data-stu-id="b5321-194">0</span></span>                      |
| <span data-ttu-id="b5321-195">D3DRS \_ адаптиветесс \_ Y</span><span class="sxs-lookup"><span data-stu-id="b5321-195">D3DRS\_ADAPTIVETESS\_Y</span></span>                  | <span data-ttu-id="b5321-196">0</span><span class="sxs-lookup"><span data-stu-id="b5321-196">0</span></span>                      |
| <span data-ttu-id="b5321-197">D3DRS \_ адаптиветесс \_ Z</span><span class="sxs-lookup"><span data-stu-id="b5321-197">D3DRS\_ADAPTIVETESS\_Z</span></span>                  | <span data-ttu-id="b5321-198">1</span><span class="sxs-lookup"><span data-stu-id="b5321-198">1</span></span>                      |
| <span data-ttu-id="b5321-199">D3DRS \_ адаптиветесс \_ W</span><span class="sxs-lookup"><span data-stu-id="b5321-199">D3DRS\_ADAPTIVETESS\_W</span></span>                  | <span data-ttu-id="b5321-200">0</span><span class="sxs-lookup"><span data-stu-id="b5321-200">0</span></span>                      |
| <span data-ttu-id="b5321-201">D3DRS \_ енаблеадаптиветесселлатион "/></span><span class="sxs-lookup"><span data-stu-id="b5321-201">D3DRS\_ENABLEADAPTIVETESSELLATION"/></span></span> | <span data-ttu-id="b5321-202">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="b5321-202">**FALSE**</span></span>              |



 

## <a name="vertex-pipeline-sampler-state"></a><span data-ttu-id="b5321-203">Конвейер вершин: состояние образца</span><span class="sxs-lookup"><span data-stu-id="b5321-203">Vertex Pipeline: Sampler State</span></span>

<span data-ttu-id="b5321-204">Состояния образцов контролируют связанные с выборкой разделы, такие как фильтрация, мозаичное заполнение и режимы адресации текстуры.</span><span class="sxs-lookup"><span data-stu-id="b5321-204">Sampler states control sampling related topics such as filtering, tiling, and texture coordinate address modes.</span></span> <span data-ttu-id="b5321-205">Используйте [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) , чтобы настроить состояние выборки (включая ту, которая используется в блоке тесселяции в качестве образца карт смещения).</span><span class="sxs-lookup"><span data-stu-id="b5321-205">Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) to set up the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="b5321-206">Состояния образца были переименованы с \_ префиксом "D3DSAMP", чтобы включить обнаружение ошибок во время компиляции при переносе из DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="b5321-206">The sampler states have been renamed with a "D3DSAMP\_" prefix to enable compile time error detection when porting from DirectX 8.</span></span>

<span data-ttu-id="b5321-207">В следующей таблице приведены все состояния образцов, которые настроили состояние вершин.</span><span class="sxs-lookup"><span data-stu-id="b5321-207">The following table includes all sampler states that set-up vertex state:</span></span>



| <span data-ttu-id="b5321-208">Состояния образцов</span><span class="sxs-lookup"><span data-stu-id="b5321-208">Sampler States</span></span>      | <span data-ttu-id="b5321-209">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b5321-209">Default Value</span></span> |
|---------------------|---------------|
| <span data-ttu-id="b5321-210">D3DSAMP \_ дмапоффсет</span><span class="sxs-lookup"><span data-stu-id="b5321-210">D3DSAMP\_DMAPOFFSET</span></span> | <span data-ttu-id="b5321-211">256</span><span class="sxs-lookup"><span data-stu-id="b5321-211">256</span></span>           |



 

## <a name="vertex-pipeline-texture-state"></a><span data-ttu-id="b5321-212">Конвейер вершин: состояние текстуры</span><span class="sxs-lookup"><span data-stu-id="b5321-212">Vertex Pipeline: Texture State</span></span>

<span data-ttu-id="b5321-213">Состояние текстуры управляет операциями смешения текстур для многотекстурного смешения.</span><span class="sxs-lookup"><span data-stu-id="b5321-213">Texture states control texture blending operations of the multi-texture blender.</span></span> <span data-ttu-id="b5321-214">Для состояния текстуры настройки используйте [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="b5321-214">Use [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) to set-up texture states.</span></span> <span data-ttu-id="b5321-215">Используйте [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) , чтобы связать текстуру с стадией образца.</span><span class="sxs-lookup"><span data-stu-id="b5321-215">Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to associate a texture with a sampler stage.</span></span>

<span data-ttu-id="b5321-216">В следующей таблице перечислены все состояния текстур, настроенные для состояния вершин.</span><span class="sxs-lookup"><span data-stu-id="b5321-216">The following table includes all the texture states that set-up vertex state:</span></span>



| <span data-ttu-id="b5321-217">Состояния текстуры</span><span class="sxs-lookup"><span data-stu-id="b5321-217">Texture States</span></span>                | <span data-ttu-id="b5321-218">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b5321-218">Default Value</span></span>    |
|-------------------------------|------------------|
| <span data-ttu-id="b5321-219">D3DTSS \_ текскурдиндекс</span><span class="sxs-lookup"><span data-stu-id="b5321-219">D3DTSS\_TEXCOORDINDEX</span></span>         | <span data-ttu-id="b5321-220">0</span><span class="sxs-lookup"><span data-stu-id="b5321-220">0</span></span>                |
| <span data-ttu-id="b5321-221">D3DTSS \_ текстуретрансформфлагс</span><span class="sxs-lookup"><span data-stu-id="b5321-221">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span> | <span data-ttu-id="b5321-222">\_Отключение D3DTTFF</span><span class="sxs-lookup"><span data-stu-id="b5321-222">D3DTTFF\_DISABLE</span></span> |



 

<span data-ttu-id="b5321-223">D3DTSS \_ текскурдиндекс — это состояние обработки фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="b5321-223">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="b5321-224">Если используется программируемый шейдер вершин, это состояние игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b5321-224">If a programmable vertex shader is used, this state is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5321-225">См. также</span><span class="sxs-lookup"><span data-stu-id="b5321-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5321-226">Состояние блоков сохранения и восстановления</span><span class="sxs-lookup"><span data-stu-id="b5321-226">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
