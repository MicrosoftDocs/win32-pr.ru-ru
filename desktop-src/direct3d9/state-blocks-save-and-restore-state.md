---
description: Блок состояния — это группа состояний устройства.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Состояние блокировки сохранения и восстановления (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989897"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a><span data-ttu-id="b69b6-103">Состояние блокировки сохранения и восстановления (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b69b6-103">State Blocks Save and Restore State (Direct3D 9)</span></span>

<span data-ttu-id="b69b6-104">Блок состояния — это группа состояний устройства.</span><span class="sxs-lookup"><span data-stu-id="b69b6-104">A state block is a group of device states.</span></span> <span data-ttu-id="b69b6-105">Состояние устройства состоит из состояния прорисовки, состояния вершины, состояния пикселя или всех вышеперечисленных элементов.</span><span class="sxs-lookup"><span data-stu-id="b69b6-105">Device state is made up of render state, vertex state, pixel state, or all of the above.</span></span> <span data-ttu-id="b69b6-106">Блок состояния содержит моментальный снимок текущего состояния устройства или можно создать блок состояния, записывающий каждое изменение состояния, которое делает приложение.</span><span class="sxs-lookup"><span data-stu-id="b69b6-106">A state block contains a snapshot of a device's current state, or you can create a state block that records each state change that your application makes.</span></span>

## <a name="capture-a-block-of-state"></a><span data-ttu-id="b69b6-107">Захватить блок состояния</span><span class="sxs-lookup"><span data-stu-id="b69b6-107">Capture a Block of State</span></span>

<span data-ttu-id="b69b6-108">Выберите тип состояния, которое требуется записать, и создайте блок состояния следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b69b6-108">Choose the type of state that you want to capture, and create a state block like this:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



<span data-ttu-id="b69b6-109">[**IDirect3DDevice9:: креатестатеблокк**](/windows/desktop/api) создает блок состояния и автоматически фиксирует состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b69b6-109">[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) creates a state block, and automatically captures the device state.</span></span> <span data-ttu-id="b69b6-110">Состояние устройства определяется типом блока State в первом аргументе.</span><span class="sxs-lookup"><span data-stu-id="b69b6-110">The device state is specified by the state block type in the first argument.</span></span> <span data-ttu-id="b69b6-111">Это состояние может быть одним из следующих: все состояние устройства (см. раздел [Сохранение всех состояний устройства с помощью статеблокк (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), состояние пикселей (см. раздел [Сохранение состояния пикселов с помощью статеблокк (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) или все состояние вершины (см. раздел [Сохранение состояний вершин с помощью статеблокк (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="b69b6-111">This state can be one of the following: all device state (see [Saving All Device States with a StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), all pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)), or all vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>

<span data-ttu-id="b69b6-112">Система эффектов использует блок состояния для сохранения состояния.</span><span class="sxs-lookup"><span data-stu-id="b69b6-112">The effect system uses a state block to save state.</span></span> <span data-ttu-id="b69b6-113">После вызова [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) создается блок состояния, а состояние фиксируется.</span><span class="sxs-lookup"><span data-stu-id="b69b6-113">After [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called, a state block is created and state is captured.</span></span> <span data-ttu-id="b69b6-114">При вызове [**ID3DXEffect:: end**](id3dxeffect--end.md) состояние блока состояния повторно применяется к устройству.</span><span class="sxs-lookup"><span data-stu-id="b69b6-114">When [**ID3DXEffect::End**](id3dxeffect--end.md) is called, the state block state is reapplied to the device.</span></span>

## <a name="capture-individual-states"></a><span data-ttu-id="b69b6-115">Захватить отдельные состояния</span><span class="sxs-lookup"><span data-stu-id="b69b6-115">Capture Individual States</span></span>

<span data-ttu-id="b69b6-116">Чтобы сохранить пользовательскую последовательность состояния, заключите состояние, которое вы хотите сохранить, в паре [**IDirect3DDevice9:: бегинстатеблокк**](/windows/desktop/api) и [**IDirect3DDevice9:: ендстатеблокк**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) .</span><span class="sxs-lookup"><span data-stu-id="b69b6-116">To save a custom state sequence, wrap the state that you want to save in a [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) and [**IDirect3DDevice9::EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) pair.</span></span> <span data-ttu-id="b69b6-117">Бегинстатеблокк сообщает текущему устройству о необходимости настроить блок состояния и добавить к нему все изменения состояния, происходящие до вызова Ендстатеблокк.</span><span class="sxs-lookup"><span data-stu-id="b69b6-117">BeginStateBlock tells the current device to set up a state block and add to it every state change that occurs until EndStateBlock is called.</span></span> <span data-ttu-id="b69b6-118">Приведем пример:</span><span class="sxs-lookup"><span data-stu-id="b69b6-118">Here's an example:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



<span data-ttu-id="b69b6-119">Это позволит сохранить любое количество изменений состояния в любой последовательности в пользовательском статеблокк.</span><span class="sxs-lookup"><span data-stu-id="b69b6-119">This will save any number of state changes in any sequence to a custom stateblock.</span></span> <span data-ttu-id="b69b6-120">Позже, когда вы хотите использовать статеблокк для сброса состояния устройства, вызовите [**IDirect3DStateBlock9:: Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span><span class="sxs-lookup"><span data-stu-id="b69b6-120">Later, when you want to use the stateblock to reset the device state, call [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span></span> <span data-ttu-id="b69b6-121">Это приведет к перезаписи только состояния устройства, записанного в блоке состояния.</span><span class="sxs-lookup"><span data-stu-id="b69b6-121">This will overwrite only the device state that has been captured in the state block.</span></span> <span data-ttu-id="b69b6-122">Любое другое состояние устройства, которое не было захвачено настраиваемым статеблокк, не будет изменено.</span><span class="sxs-lookup"><span data-stu-id="b69b6-122">Any other device state that was not captured with the custom stateblock will not be changed.</span></span> <span data-ttu-id="b69b6-123">Опять же, поскольку объект статеблокк является интерфейсом, его необходимо освободить после завершения.</span><span class="sxs-lookup"><span data-stu-id="b69b6-123">Once again, since the stateblock object is an interface, you will need to release it when you are done with it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b69b6-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b69b6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b69b6-125">Состояния (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b69b6-125">States (Direct3D 9)</span></span>](states.md)
</dt> </dl>

 

 
