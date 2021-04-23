---
description: В Direct3D 10 доступ к ресурсам текстур осуществляется с помощью представления, которое является механизмом интерпретации ресурса в памяти.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Представления текстур (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06cd98a00782b826713e68304ad7cc132e4e0fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990649"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="85eb5-103">Представления текстур (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="85eb5-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="85eb5-104">В Direct3D 10 доступ к ресурсам текстур осуществляется с помощью представления, которое является механизмом интерпретации ресурса в памяти.</span><span class="sxs-lookup"><span data-stu-id="85eb5-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="85eb5-105">Представление позволяет определенному циклу конвейера получать доступ только к необходимым ему [вложенным ресурсам](d3d10-graphics-programming-guide-resources-types.md) в виде, требуемом для приложения.</span><span class="sxs-lookup"><span data-stu-id="85eb5-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="85eb5-106">Представление поддерживает понятие ресурса без типа.</span><span class="sxs-lookup"><span data-stu-id="85eb5-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="85eb5-107">Ресурс без типа — это ресурс, созданный с использованием определенного размера, но не определенного типа данных.</span><span class="sxs-lookup"><span data-stu-id="85eb5-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="85eb5-108">Данные интерпретируется динамически при привязке к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="85eb5-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="85eb5-109">Ниже представлен пример привязки массива двухмерных текстур с шестью текстурами в качестве ресурса шейдера путем создания для него представления ресурса шейдера.</span><span class="sxs-lookup"><span data-stu-id="85eb5-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="85eb5-110">Затем обращение к ресурсу происходит как к массиву текстур.</span><span class="sxs-lookup"><span data-stu-id="85eb5-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="85eb5-111">(Примечание. Вложенный ресурс невозможно одновременно привязать к конвейеру в качестве ввода и вывода.)</span><span class="sxs-lookup"><span data-stu-id="85eb5-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![Иллюстрация массива текстур с шестью текстурами](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="85eb5-113">При использовании массива двухмерных текстур в качестве цели отрисовки ресурс можно рассматривать как массив двухмерных текстур (в этом примере их 6) с об уровнями MIP (в этом примере их 3).</span><span class="sxs-lookup"><span data-stu-id="85eb5-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="85eb5-114">Создайте объект представления для целевого объекта отрисовки, вызвав метод CreateRenderTargetView.</span><span class="sxs-lookup"><span data-stu-id="85eb5-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="85eb5-115">Затем вызовите OMSetRenderTargets, чтобы установить представление однобуферной отрисовки для конвейера.</span><span class="sxs-lookup"><span data-stu-id="85eb5-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="85eb5-116">Вызовите Draw для отрисовки на целевых объектах и используйте RenderTargetArrayIndex для указания правильной текстуры в массиве.</span><span class="sxs-lookup"><span data-stu-id="85eb5-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="85eb5-117">Можно использовать вложенный ресурс (уровень MIP-карты, комбинацию индекса массива) для привязки к любому массиву подчиненных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85eb5-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="85eb5-118">При необходимости можно выполнить привязку ко второму уровню MIP-карты и обновить только этот уровень, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="85eb5-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![Иллюстрация привязки только ко второму уровню MIP-карты массива текстур](images/d3d10-cube-texture-faces-subresource.png)



|                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85eb5-120">Различия между Direct3D 9 и Direct3D 10. в Direct3D 10 вы больше не выполняете привязку ресурса непосредственно к конвейеру, создаете представление ресурса, а затем устанавливаете представление в конвейер.</span><span class="sxs-lookup"><span data-stu-id="85eb5-120">Differences between Direct3D 9 and Direct3D 10: In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="85eb5-121">Это позволяет выполнять проверку и сопоставление в среде выполнения и драйвере при создании представления, минимизируя проверку типов во время привязки.</span><span class="sxs-lookup"><span data-stu-id="85eb5-121">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="85eb5-122">См. также</span><span class="sxs-lookup"><span data-stu-id="85eb5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85eb5-123">Ресурсы (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="85eb5-123">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




