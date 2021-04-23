---
description: Эффекты тумана могут дать трехмерную сцены более реалистичным.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Состояние тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416372"
---
# <a name="fog-state-direct3d-9"></a><span data-ttu-id="7c68a-103">Состояние тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c68a-103">Fog State (Direct3D 9)</span></span>

<span data-ttu-id="7c68a-104">Эффекты тумана могут дать трехмерную сцены более реалистичным.</span><span class="sxs-lookup"><span data-stu-id="7c68a-104">Fog effects can give a 3D scene greater realism.</span></span> <span data-ttu-id="7c68a-105">Эффекты тумана можно использовать для более имитации тумана.</span><span class="sxs-lookup"><span data-stu-id="7c68a-105">You can use fog effects for more than simulating fog.</span></span> <span data-ttu-id="7c68a-106">Они также могут уменьшить четкость сцены с расстоянием.</span><span class="sxs-lookup"><span data-stu-id="7c68a-106">They can also decrease the clarity of a scene with distance.</span></span> <span data-ttu-id="7c68a-107">Это отражает то, что происходит в реальном мире; по мере того, как объекты становятся более отдаленными от пользователя, их подробности менее различны.</span><span class="sxs-lookup"><span data-stu-id="7c68a-107">This mirrors what happens in the real world; as objects become more distant from the user, their detail is less distinct.</span></span>

<span data-ttu-id="7c68a-108">Дополнительные сведения об использовании тумана в приложении см. в разделе [туман (Direct3D 9)](fog.md).</span><span class="sxs-lookup"><span data-stu-id="7c68a-108">For more information about using fog in your application, see [Fog (Direct3D 9)](fog.md).</span></span>

<span data-ttu-id="7c68a-109">Приложение C++ управляет туманом с помощью состояний отрисовки устройства.</span><span class="sxs-lookup"><span data-stu-id="7c68a-109">A C++ application controls fog through device rendering states.</span></span> <span data-ttu-id="7c68a-110">Перечислимый тип [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) включает состояния, определяющие, используется ли пиксель (таблица) или вершинный туман, какой цвет он имеет, формула тумана, к которой применяется система, и параметры формулы.</span><span class="sxs-lookup"><span data-stu-id="7c68a-110">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes states to control whether pixel (table) or vertex fog is used, what color it is, the fog formula the system applies, and the parameters of the formula.</span></span>

<span data-ttu-id="7c68a-111">Чтобы включить туман, установите \_ для состояния отрисовки D3DRS Фоженабле **значение true**.</span><span class="sxs-lookup"><span data-stu-id="7c68a-111">You enable fog by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span> <span data-ttu-id="7c68a-112">Для цвета тумана можно задать любое значение цвета с помощью \_ состояния рендеринга D3DRS фогколор; альфа-компонент цвета тумана не учитывается.</span><span class="sxs-lookup"><span data-stu-id="7c68a-112">The fog color can be set to any color value by using the D3DRS\_FOGCOLOR render state; the alpha component of the fog color is ignored.</span></span>

<span data-ttu-id="7c68a-113">\_Состояния отрисовки D3DRS фогтаблемоде и D3DRS \_ фогвертексмоде управляют формулой тумана, применяемой для вычислений тумана, и неявно контролируют применяемый тип тумана.</span><span class="sxs-lookup"><span data-stu-id="7c68a-113">The D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states control the fog formula applied for fog calculations, and they indirectly control which type of fog is applied.</span></span> <span data-ttu-id="7c68a-114">Оба состояния рендеринга могут быть заданы для члена перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="7c68a-114">Both render states can be set to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="7c68a-115">Если задать для состояния отрисовки значение D3DFOG \_ None, будет отключена точка или вершина тумана соответственно.</span><span class="sxs-lookup"><span data-stu-id="7c68a-115">Setting either render state to D3DFOG\_NONE disables pixel or vertex fog, respectively.</span></span> <span data-ttu-id="7c68a-116">Если оба состояния рендеринга установлены в допустимые режимы, система применяет только эффекты Pixel тумана.</span><span class="sxs-lookup"><span data-stu-id="7c68a-116">If both render states are set to valid modes, the system applies only pixel fog effects.</span></span>

<span data-ttu-id="7c68a-117">D3DRS \_ фогстарт и D3DRS \_ фоженд отображают параметры формулы тумана для \_ линейного режима D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="7c68a-117">The D3DRS\_FOGSTART and D3DRS\_FOGEND render states control fog formula parameters for the D3DFOG\_LINEAR mode.</span></span> <span data-ttu-id="7c68a-118">\_Состояние визуализации D3DRS фогденсити управляет плотностью тумана в экспоненциальном режиме тумана.</span><span class="sxs-lookup"><span data-stu-id="7c68a-118">The D3DRS\_FOGDENSITY render state controls fog density in the exponential fog modes.</span></span>

<span data-ttu-id="7c68a-119">Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7c68a-119">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c68a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7c68a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c68a-121">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="7c68a-121">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
