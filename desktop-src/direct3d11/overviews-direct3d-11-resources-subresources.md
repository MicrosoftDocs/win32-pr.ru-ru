---
title: Подресурсы (графика Direct3D 11)
description: В этом разделе описываются подресурсы текстуры или части ресурса.
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070924"
---
# <a name="subresources-direct3d-11-graphics"></a><span data-ttu-id="958c3-103">Подресурсы (графика Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="958c3-103">Subresources (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="958c3-104">В этом разделе описываются подресурсы текстуры или части ресурса.</span><span class="sxs-lookup"><span data-stu-id="958c3-104">This topic describes texture subresources, or portions of a resource.</span></span>

<span data-ttu-id="958c3-105">Direct3D может ссылаться на весь ресурс или же на подмножества ресурса.</span><span class="sxs-lookup"><span data-stu-id="958c3-105">Direct3D can reference an entire resource or it can reference subsets of a resource.</span></span> <span data-ttu-id="958c3-106">Под ресурсом понимается подмножество ресурса.</span><span class="sxs-lookup"><span data-stu-id="958c3-106">The term subresource refers to a subset of a resource.</span></span>

<span data-ttu-id="958c3-107">Буфер определяется как один подресурс.</span><span class="sxs-lookup"><span data-stu-id="958c3-107">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="958c3-108">Текстуры немного сложнее, так как существует несколько различных типов текстур (1D, 2D и т. д.), некоторые из которых поддерживают mipmap уровни и (или) массивы текстур.</span><span class="sxs-lookup"><span data-stu-id="958c3-108">Textures are a little more complicated because there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="958c3-109">Самый простой случай — это одномерная текстура, которая определяется как один подресурс (см. следующий рисунок).</span><span class="sxs-lookup"><span data-stu-id="958c3-109">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![иллюстрация одномерной текстуры](images/d3d10-1d-texture.png)

<span data-ttu-id="958c3-111">Это означает, что массив текселей, из которых состоит одномерная текстура, содержится в одном подресурсе.</span><span class="sxs-lookup"><span data-stu-id="958c3-111">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="958c3-112">При развертывании одномерной текстуры с тремя уровнями mipmap можно выполнить визуализацию, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="958c3-112">If you expand a 1D texture with three mipmap levels, it can be visualized like the following illustration.</span></span>

![Иллюстрация одномерной текстуры с тремя уровнями mipmap](images/d3d10-resource-texture1d.png)

<span data-ttu-id="958c3-114">Представьте себе, что это одна текстура, состоящие из трех подресурсов.</span><span class="sxs-lookup"><span data-stu-id="958c3-114">Think of this as a single texture that is made up of three subresources.</span></span> <span data-ttu-id="958c3-115">Подресурс можно индексировать с помощью уровня детализации (Лод) для одной текстуры.</span><span class="sxs-lookup"><span data-stu-id="958c3-115">A subresource can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="958c3-116">При использовании массива текстур для доступа к определенному подресурсу требуется как Лод, так и определенная текстура.</span><span class="sxs-lookup"><span data-stu-id="958c3-116">When using an array of textures, accessing a particular subresource requires both the LOD and the particular texture.</span></span> <span data-ttu-id="958c3-117">Кроме того, API объединяет эти два фрагмента информации в один индекс подресурса, начинающийся с нуля, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="958c3-117">Alternately, the API combines these two pieces of information into a single zero-based subresource index, as shown in the following illustration.</span></span>

![иллюстрация начинающегося с нуля индекса подресурса](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a><span data-ttu-id="958c3-119">Выбор подресурсов</span><span class="sxs-lookup"><span data-stu-id="958c3-119">Selecting Subresources</span></span>

<span data-ttu-id="958c3-120">Некоторые интерфейсы API обращаются ко всему ресурсу (например, метод [**ссылку ID3D11DeviceContext:: копиресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ), другие обращаются к части ресурса (например, метод [**ссылку ID3D11DeviceContext:: Упдатесубресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) или метод [**ссылку ID3D11DeviceContext:: кописубресаурцерегион**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) ).</span><span class="sxs-lookup"><span data-stu-id="958c3-120">Some APIs access an entire resource (for example the [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) method), others access a portion of a resource (for example the [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) method or the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method).</span></span> <span data-ttu-id="958c3-121">Методы, обращающиеся к части ресурса, обычно используют описание представления (например, структуру [**D3D11 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) ) для указания подресурсов для доступа.</span><span class="sxs-lookup"><span data-stu-id="958c3-121">The methods that access a portion of a resource generally use a view description (such as the [**D3D11\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) to specify the subresources to access.</span></span>

<span data-ttu-id="958c3-122">На иллюстрациях в следующих разделах показаны термины, используемые в описании представления при доступе к массиву текстур.</span><span class="sxs-lookup"><span data-stu-id="958c3-122">The illustrations in the following sections show the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="958c3-123">Срез массива</span><span class="sxs-lookup"><span data-stu-id="958c3-123">Array Slice</span></span>

<span data-ttu-id="958c3-124">Учитывая массив текстур, каждая текстура с MIP-карты, *срез массива* (представленный белым прямоугольником) включает одну текстуру и все ее подресурсы, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="958c3-124">Given an array of textures, each texture with mipmaps, an *array slice* (represented by the white rectangle) includes one texture and all of its subresources, as shown in the following illustration.</span></span>

![Иллюстрация среза массива](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="958c3-126">Срез MIP</span><span class="sxs-lookup"><span data-stu-id="958c3-126">Mip Slice</span></span>

<span data-ttu-id="958c3-127">*Срез MIP* (представленный белым прямоугольником) включает один уровень mipmap для каждой текстуры в массиве, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="958c3-127">A *mip slice* (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![Иллюстрация MIP среза](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="958c3-129">Выбор одного подресурса</span><span class="sxs-lookup"><span data-stu-id="958c3-129">Selecting a Single Subresource</span></span>

<span data-ttu-id="958c3-130">Эти два типа срезов можно использовать для выбора одного подресурса, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="958c3-130">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![Иллюстрация выбора подресурса с помощью среза массива и среза MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="958c3-132">Выбор нескольких подресурсов</span><span class="sxs-lookup"><span data-stu-id="958c3-132">Selecting Multiple Subresources</span></span>

<span data-ttu-id="958c3-133">Вы также можете использовать эти два типа срезов с числом mipmap и (или) количеством текстур, чтобы выбрать несколько подресурсов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="958c3-133">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources, as shown in the following illustration.</span></span>

![Иллюстрация выбора нескольких подресурсов](images/d3d10-resource-subresources-2.png)

> [!Note]  
> <span data-ttu-id="958c3-135">[**Представление визуализации-целевого объекта**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) может использовать только один подресурс или срез MIP и не может включать подресурсы из нескольких срезов MIP.</span><span class="sxs-lookup"><span data-stu-id="958c3-135">A [**render-target view**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="958c3-136">Это значит, что каждая текстура в представлении целевого объекта должна иметь одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="958c3-136">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="958c3-137">В [**представлении "шейдер — ресурс**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) " можно выбрать любую прямоугольную область подресурсов, как показано на рисунке.</span><span class="sxs-lookup"><span data-stu-id="958c3-137">A [**shader-resource view**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) can select any rectangular region of subresources, as shown in the figure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="958c3-138">См. также</span><span class="sxs-lookup"><span data-stu-id="958c3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="958c3-139">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="958c3-139">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




