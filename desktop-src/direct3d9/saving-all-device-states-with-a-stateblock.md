---
description: Можно использовать блок состояния для записи всех состояний устройства (см. раздел State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Сохранение всех состояний устройств с помощью Статеблокк (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682284"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="b1d5e-103">Сохранение всех состояний устройств с помощью Статеблокк (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1d5e-103">Saving All Device States with a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="b1d5e-104">Можно использовать блок состояния для записи всех состояний устройства (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="b1d5e-104">A state block can be used to capture all device states (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="b1d5e-105">В состояние устройства включаются следующие элементы состояния.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-105">The following state elements are included in the device state:</span></span>

-   <span data-ttu-id="b1d5e-106">Состояние вершины (см. раздел [Сохранение состояний вершин с помощью статеблокк (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="b1d5e-106">Vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="b1d5e-107">Состояние пикселей (см. раздел [Сохранение состояния пикселей с помощью статеблокк (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="b1d5e-107">Pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="b1d5e-108">Каждая текстура, назначенная для образца.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-108">Each texture assigned to a sampler.</span></span>
-   <span data-ttu-id="b1d5e-109">Каждая текстура вершин.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-109">Each vertex texture.</span></span>
-   <span data-ttu-id="b1d5e-110">Каждая текстура карт смещения.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-110">Each displacement map texture.</span></span>
-   <span data-ttu-id="b1d5e-111">Текущая палитра текстур.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-111">The current texture palette.</span></span>
-   <span data-ttu-id="b1d5e-112">Для каждого потока вершин: указатель на буфер вершин, каждый аргумент из [**IDirect3DDevice9:: сетстреамсаурце**](/windows/desktop/api)и разделитель (если он есть) из [**IDirect3DDevice9:: сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="b1d5e-112">For each vertex stream: a pointer to the vertex buffer, each argument from [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api), and the divider (if any) from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="b1d5e-113">Указатель на индексный буфер.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-113">A pointer to the index buffer.</span></span>
-   <span data-ttu-id="b1d5e-114">Окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-114">The viewport.</span></span>
-   <span data-ttu-id="b1d5e-115">Прямоугольник ножниц.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-115">The scissors rectangle.</span></span>
-   <span data-ttu-id="b1d5e-116">Матрицы мира, представления и проекции.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-116">The world, view, and projection matrices.</span></span>
-   <span data-ttu-id="b1d5e-117">Преобразование текстур.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-117">The texture transforms.</span></span>
-   <span data-ttu-id="b1d5e-118">Обтравочные плоскости (если они есть).</span><span class="sxs-lookup"><span data-stu-id="b1d5e-118">The clipping planes (if any).</span></span>
-   <span data-ttu-id="b1d5e-119">Текущий материал.</span><span class="sxs-lookup"><span data-stu-id="b1d5e-119">The current material.</span></span>

<span data-ttu-id="b1d5e-120">Чтобы захватить все состояния устройств с помощью блока State, укажите D3DSBT \_ ALL при вызове [**IDirect3DDevice9:: креатестатеблокк**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="b1d5e-120">To capture all device states with a state block, specify D3DSBT\_ALL when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1d5e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b1d5e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1d5e-122">Состояние блоков сохранения и восстановления</span><span class="sxs-lookup"><span data-stu-id="b1d5e-122">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
