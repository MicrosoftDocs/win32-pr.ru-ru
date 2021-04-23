---
title: Использование констант непосредственно в корневой подписи
description: Приложения могут определять корневые константы в корневой подписи, каждый из которых является набором 32-разрядных значений. Они отображаются на высоком уровне (HLSL) в виде буфера констант. Обратите внимание, что постоянные буферы по историческим причинам просматриваются как наборы 4x32 значений.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104751"
---
# <a name="using-constants-directly-in-the-root-signature"></a><span data-ttu-id="5a14f-105">Использование констант непосредственно в корневой подписи</span><span class="sxs-lookup"><span data-stu-id="5a14f-105">Using Constants Directly in the Root Signature</span></span>

<span data-ttu-id="5a14f-106">Приложения могут определять корневые константы в корневой подписи, каждый из которых является набором 32-разрядных значений.</span><span class="sxs-lookup"><span data-stu-id="5a14f-106">Applications can define root constants in the root signature, each as a set of 32-bit values.</span></span> <span data-ttu-id="5a14f-107">Они отображаются на высоком уровне (HLSL) в виде буфера констант.</span><span class="sxs-lookup"><span data-stu-id="5a14f-107">They appear in High Level Shading Language (HLSL) as a constant buffer.</span></span> <span data-ttu-id="5a14f-108">Обратите внимание, что постоянные буферы по историческим причинам просматриваются как наборы 4x32 значений.</span><span class="sxs-lookup"><span data-stu-id="5a14f-108">Note that constant buffers for historical reasons are viewed as sets of 4x32-bit values.</span></span>

<span data-ttu-id="5a14f-109">Каждый набор пользовательских констант рассматривается как скалярный массив из 32-битных значений, динамически индексируемых и доступных только для чтения из шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a14f-109">Each set of user constants is treated as a scalar array of 32 -bit values, dynamically indexable and read-only from the shader.</span></span> <span data-ttu-id="5a14f-110">За пределами границ индексирование заданного набора корневых констант приводит к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="5a14f-110">Out of bounds indexing a given set of root constants produces undefined results.</span></span> <span data-ttu-id="5a14f-111">В HLSL можно предоставить определения структуры данных для пользовательских констант, чтобы предоставить их типам.</span><span class="sxs-lookup"><span data-stu-id="5a14f-111">In HLSL, data structure definitions can be provided for the user constants to give them types.</span></span> <span data-ttu-id="5a14f-112">Например, если корневая подпись определяет набор из 4 корневых констант, HLSL может накладывать на них следующую структуру.</span><span class="sxs-lookup"><span data-stu-id="5a14f-112">For example, if the root signature defines a set of 4 root constants, HLSL can overlay the following structure on them.</span></span>

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

<span data-ttu-id="5a14f-113">Массивы не допускаются в буферах констант, которые сопоставляются с корневыми константами, так как динамическое индексирование в корневом пространстве подписи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5a14f-113">Arrays are not permitted in constant buffers that get mapped onto root constants since dynamic indexing in the root signature space is not supported.</span></span> <span data-ttu-id="5a14f-114">Например, недопустимо наличие записи в буфере константы, например `float myArray[2];` .</span><span class="sxs-lookup"><span data-stu-id="5a14f-114">For example, it is invalid to have an entry in the constant buffer like `float myArray[2];`.</span></span> <span data-ttu-id="5a14f-115">Буфер констант, сопоставленный с корневыми константами, не может быть массивом. Таким образом, не допускается соотнесение с `cbuffer myCBArray[2]` корневыми константами.</span><span class="sxs-lookup"><span data-stu-id="5a14f-115">A constant buffer that is mapped to root constants cannot itself be an array; therefore, it is invalid to map `cbuffer myCBArray[2]` into root constants.</span></span>

<span data-ttu-id="5a14f-116">Константы могут быть частично заданы.</span><span class="sxs-lookup"><span data-stu-id="5a14f-116">Constants can be partially set.</span></span> <span data-ttu-id="5a14f-117">Например, если корневая подпись определяет 4 32-битные значения в *руттаблебиндслот* 2, то любое подмножество четырех констант может быть задано за раз (остальные остаются неизменными).</span><span class="sxs-lookup"><span data-stu-id="5a14f-117">For example, if the root signature defines four 32-bit values at *RootTableBindSlot* 2, then any subset of the four constants can be set at a time (the others remain unchanged).</span></span> <span data-ttu-id="5a14f-118">Это может быть полезно в пакетах, которые наследуют состояние корневой подписи и могут частично изменить его.</span><span class="sxs-lookup"><span data-stu-id="5a14f-118">This can be useful in bundles that inherit root signature state and can partially change it.</span></span>

<span data-ttu-id="5a14f-119">При задании констант следует соблюдать осторожность в структуре буфера констант, ожидаемой шейдером.</span><span class="sxs-lookup"><span data-stu-id="5a14f-119">When setting constants be careful of the constant buffer layout expected by the shader.</span></span> <span data-ttu-id="5a14f-120">Возможно, константы заполнены `vec4` границами, например.</span><span class="sxs-lookup"><span data-stu-id="5a14f-120">It is possible that constants are padded to `vec4` boundaries, for example.</span></span> <span data-ttu-id="5a14f-121">Чтобы проверить ожидаемый макет, проверьте сведения о отражении в шейдере HLSL.</span><span class="sxs-lookup"><span data-stu-id="5a14f-121">To verify the layout expected, check the reflection information from the HLSL shader.</span></span>

<span data-ttu-id="5a14f-122">Следующие API-интерфейсы (из интерфейса [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) предназначены для непосредственного задания констант в корневой подписи:</span><span class="sxs-lookup"><span data-stu-id="5a14f-122">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting constants directly on the root signature:</span></span>

-   [<span data-ttu-id="5a14f-123">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="5a14f-123">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [<span data-ttu-id="5a14f-124">**SetGraphicsRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="5a14f-124">**SetGraphicsRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [<span data-ttu-id="5a14f-125">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="5a14f-125">**SetComputeRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="5a14f-126">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="5a14f-126">**SetComputeRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

<span data-ttu-id="5a14f-127">Кроме того, см. [**структуру \_ \_ констант D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="5a14f-127">Also, refer to the [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a14f-128">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5a14f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a14f-129">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="5a14f-129">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




