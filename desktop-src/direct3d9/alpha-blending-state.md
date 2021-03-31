---
description: Альфа-значение цвета управляет его прозрачностью. Включение альфа-смешения позволяет смешивать цвета, материалы и текстуры на поверхности с прозрачностью на другой поверхности.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Альфа-смешение (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423390"
---
# <a name="alpha-blending-state-direct3d-9"></a><span data-ttu-id="65703-104">Альфа-смешение (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="65703-104">Alpha Blending State (Direct3D 9)</span></span>

<span data-ttu-id="65703-105">Альфа-значение цвета управляет его прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="65703-105">The alpha value of a color controls its transparency.</span></span> <span data-ttu-id="65703-106">Включение альфа-смешения позволяет смешивать цвета, материалы и текстуры на поверхности с прозрачностью на другой поверхности.</span><span class="sxs-lookup"><span data-stu-id="65703-106">Enabling alpha blending allows colors, materials, and textures on a surface to be blended with transparency onto another surface.</span></span>

<span data-ttu-id="65703-107">Дополнительные сведения см. в разделе [смешение текстур с альфа-составляющей (Direct3D 9)](alpha-texture-blending.md) и [смешение текстур (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="65703-107">For more information, see [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) and [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

<span data-ttu-id="65703-108">Приложения, написанные на C++, используют состояние рендеринга [**D3DRS \_ алфабленденабле**](./d3drenderstatetype.md) для включения альфа-прозрачного смешения.</span><span class="sxs-lookup"><span data-stu-id="65703-108">Applications written in C++ use the [**D3DRS\_ALPHABLENDENABLE**](./d3drenderstatetype.md) render state to enable alpha transparency blending.</span></span> <span data-ttu-id="65703-109">API Direct3D позволяет выполнять различные типы альфа-смешения.</span><span class="sxs-lookup"><span data-stu-id="65703-109">The Direct3D API allows many types of alpha blending.</span></span> <span data-ttu-id="65703-110">Однако важно отметить, что трехмерное оборудование пользователя может не поддерживать все режимы смешения, разрешенные Direct3D.</span><span class="sxs-lookup"><span data-stu-id="65703-110">However, it is important to note the user's 3D hardware might not support all the blending states allowed by Direct3D.</span></span>

<span data-ttu-id="65703-111">Тип альфа-смешения, который выполняется, зависит от состояния отрисовки [**D3DRS \_ Сркбленд**](./d3drenderstatetype.md) и **D3DRS \_ дестбленд** .</span><span class="sxs-lookup"><span data-stu-id="65703-111">The type of alpha blending that is done depends on the [**D3DRS\_SRCBLEND**](./d3drenderstatetype.md) And **D3DRS\_DESTBLEND** render states.</span></span> <span data-ttu-id="65703-112">Исходное и целевое состояния смешения используются парами.</span><span class="sxs-lookup"><span data-stu-id="65703-112">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="65703-113">В следующем примере кода показано, как исходное состояние смешения установлено в значение D3DBLEND \_ сркколор, а в качестве целевого состояния смешения установлено значение D3DBLEND \_ инвсркколор.</span><span class="sxs-lookup"><span data-stu-id="65703-113">The following code example demonstrates how the source blend state is set to D3DBLEND\_SRCCOLOR and the destination blend state is set to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="65703-114">Изменение исходного и целевого состояний смешения может привести к отображению объектов эмиссионный в сумрачному или пыли.</span><span class="sxs-lookup"><span data-stu-id="65703-114">Altering the source and destination blend states can give the appearance of emissive objects in a foggy or dusty atmosphere.</span></span> <span data-ttu-id="65703-115">Например, если приложение моделирует огонь, принудительно использовать поля, плазменные беамс или радиант объекты в среде сумрачному, задайте для исходных и целевых состояний Blend значение D3DBLEND \_ .</span><span class="sxs-lookup"><span data-stu-id="65703-115">For instance, if your application models flames, force fields, plasma beams, or similarly radiant objects in a foggy environment, set the source and destination blend states to D3DBLEND\_ONE.</span></span>

<span data-ttu-id="65703-116">Другое приложение альфа-смешения заключается в управлении освещением в трехмерной сцене, также называемом «светлое сопоставление».</span><span class="sxs-lookup"><span data-stu-id="65703-116">Another application of alpha blending is to control the lighting in a 3D scene, also called light mapping.</span></span> <span data-ttu-id="65703-117">Установка для источника Blend состояния значения D3DBLEND \_ ноль, а в качестве целевого состояния Blend \_ — D3DBLEND сркалфа — затемнение сцены в соответствии с информацией об исходном альфа-канале.</span><span class="sxs-lookup"><span data-stu-id="65703-117">Setting the source blend state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCALPHA darkens a scene according to the source alpha information.</span></span> <span data-ttu-id="65703-118">Исходный примитив используется в качестве простой схемы, которая масштабирует содержимое буфера фрейма, чтобы затемнить его при необходимости.</span><span class="sxs-lookup"><span data-stu-id="65703-118">The source primitive is used as a light map that scales the contents of the frame buffer to darken it when appropriate.</span></span> <span data-ttu-id="65703-119">Это приводит к сопоставлению монохромного освещения.</span><span class="sxs-lookup"><span data-stu-id="65703-119">This produces monochrome light mapping.</span></span>

<span data-ttu-id="65703-120">Можно добиться сопоставления цветов, задав для исходного альфа-канала в качестве источника значение D3DBLEND \_ 0, а для параметра состояние перехода — значение D3DBLEND \_ сркколор.</span><span class="sxs-lookup"><span data-stu-id="65703-120">You can achieve color light mapping by setting the source alpha blending state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCCOLOR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65703-121">См. также</span><span class="sxs-lookup"><span data-stu-id="65703-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65703-122">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="65703-122">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
