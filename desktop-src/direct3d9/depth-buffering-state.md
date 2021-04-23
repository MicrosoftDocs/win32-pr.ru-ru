---
description: Буферизация глубины — это метод удаления скрытых линий и поверхностей. По умолчанию Direct3D не использует буферизацию глубины.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Состояние буферизации глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494919"
---
# <a name="depth-buffering-state-direct3d-9"></a><span data-ttu-id="7cef0-104">Состояние буферизации глубины (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7cef0-104">Depth Buffering State (Direct3D 9)</span></span>

<span data-ttu-id="7cef0-105">Буферизация глубины — это метод удаления скрытых линий и поверхностей.</span><span class="sxs-lookup"><span data-stu-id="7cef0-105">Depth buffering is a method of removing hidden lines and surfaces.</span></span> <span data-ttu-id="7cef0-106">По умолчанию Direct3D не использует буферизацию глубины.</span><span class="sxs-lookup"><span data-stu-id="7cef0-106">By default, Direct3D does not use depth buffering.</span></span>

<span data-ttu-id="7cef0-107">Общие сведения о буферах глубины см. в разделе [буферы глубины (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="7cef0-107">For a conceptual overview of depth buffers, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="7cef0-108">Приложения C++ обновляют состояние буферизации по глубине с помощью \_ состояния рендеринга D3DRS зенабле, используя член перечисления [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) для указания нового значения состояния.</span><span class="sxs-lookup"><span data-stu-id="7cef0-108">C++ applications update the depth-buffering state with the D3DRS\_ZENABLE render state, using a member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumeration to specify the new state value.</span></span>

<span data-ttu-id="7cef0-109">Если приложению требуется предотвратить запись Direct3D в буфер глубины, можно использовать \_ перечислимое значение D3DRS звритинабле, УКАЗАВ D3DZB \_ false в качестве второго параметра для вызова [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="7cef0-109">If your application needs to prevent Direct3D from writing to the depth buffer, it can use the D3DRS\_ZWRITEENABLE enumerated value, specifying D3DZB\_FALSE as the second parameter for the call to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="7cef0-110">В следующем примере кода показано, как задается состояние буфера глубины для включения z-буферизации.</span><span class="sxs-lookup"><span data-stu-id="7cef0-110">The following code example shows how the depth-buffer state is set to enable z-buffering.</span></span>


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



<span data-ttu-id="7cef0-111">Приложение также может использовать \_ состояние отображения D3DRS зфунк для управления функцией сравнения, которую Direct3D использует при выполнении глубины буферизации.</span><span class="sxs-lookup"><span data-stu-id="7cef0-111">Your application can also use the D3DRS\_ZFUNC render state to control the comparison function that Direct3D uses when performing depth buffering.</span></span>

<span data-ttu-id="7cef0-112">Z-смещение — это метод отображения одной поверхности перед другой, даже если их значения глубины одинаковы.</span><span class="sxs-lookup"><span data-stu-id="7cef0-112">Z-biasing is a method of displaying one surface in front of another, even if their depth values are the same.</span></span> <span data-ttu-id="7cef0-113">Этот метод можно использовать для различных эффектов.</span><span class="sxs-lookup"><span data-stu-id="7cef0-113">You can use this technique for a variety of effects.</span></span> <span data-ttu-id="7cef0-114">Распространенным примером является Визуализация теней на стен.</span><span class="sxs-lookup"><span data-stu-id="7cef0-114">A common example is rendering shadows on walls.</span></span> <span data-ttu-id="7cef0-115">И тень, и стенка имеют одинаковое значение глубины.</span><span class="sxs-lookup"><span data-stu-id="7cef0-115">Both the shadow and the wall have the same depth value.</span></span> <span data-ttu-id="7cef0-116">Однако приложение должно отображать тень на стене.</span><span class="sxs-lookup"><span data-stu-id="7cef0-116">However, you want your application to show the shadow on the wall.</span></span> <span data-ttu-id="7cef0-117">Благодаря смещению z-смещения к теневой версии Direct3D отображает их должным образом (см. раздел D3DRS \_ депсбиас).</span><span class="sxs-lookup"><span data-stu-id="7cef0-117">Giving a z-bias to the shadow makes Direct3D display them properly (see D3DRS\_DEPTHBIAS).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cef0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="7cef0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cef0-119">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="7cef0-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
