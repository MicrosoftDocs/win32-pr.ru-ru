---
title: Хранение переменных и типов для использования шейдерами
description: Объект компоновки класса — это пространство имен для переменных и типов, которые могут совместно использоваться несколькими шейдерами.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984072"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a><span data-ttu-id="c04b8-103">Хранение переменных и типов для использования шейдерами</span><span class="sxs-lookup"><span data-stu-id="c04b8-103">Storing Variables and Types for Shaders to Share</span></span>

<span data-ttu-id="c04b8-104">Объект компоновки класса — это пространство имен для переменных и типов, которые могут совместно использоваться несколькими шейдерами.</span><span class="sxs-lookup"><span data-stu-id="c04b8-104">The class linkage object is a namespace for variables and types that multiple shaders can share.</span></span> <span data-ttu-id="c04b8-105">При передаче объекта компоновки класса в вызове для создания шейдера среда выполнения собирает список переменных и типов, которые могут реализовывать каждый интерфейс в шейдере, и сохраняет имена этих переменных и типов в объекте компоновки класса.</span><span class="sxs-lookup"><span data-stu-id="c04b8-105">When you pass a class linkage object in a call to create a shader, the runtime gathers a list of variables and types that can implement each interface in the shader and stores the names of those variables and types in the class linkage object.</span></span>

<span data-ttu-id="c04b8-106">Поэтому при вызове метода [**ID3D11ClassLinkage:: жетклассинстанце**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) для создания экземпляров класса из объекта компоновки класса среда выполнения может получить переменную или тип, соответствующий имени, которое предоставляется в каждом шейдере (если это имя является допустимым для данного шейдера) и было создано с данным объектом компоновки класса.</span><span class="sxs-lookup"><span data-stu-id="c04b8-106">Therefore, when you call the [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) method to generate class instances from the class linkage object, the runtime can retrieve the variable or type that corresponds to the name that is provided in each shader (if that name is valid for a given shader) and that is created with the given class linkage object.</span></span>

<span data-ttu-id="c04b8-107">Например, предположим, что имеется класс **Light** , реализующий интерфейс **цвета** , и этот класс используется в шейдере вершин и шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="c04b8-107">For example, suppose you have a **Light** class that implements a **Color** interface, and you use this class in your vertex shader and pixel shader.</span></span> <span data-ttu-id="c04b8-108">При создании шейдера (например, путем вызова [**ID3D11Device:: креатепикселшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)) среда выполнения определяет, что тип класса **Light** доступен как в шейдере вершин, так и в Pixel Shader и добавляет тип класса **Light** в объект компоновки класса.</span><span class="sxs-lookup"><span data-stu-id="c04b8-108">When you create a shader (for example, by calling [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), the runtime determines that the **Light** class type is available in both vertex and pixel shaders and adds the **Light** class type to the class linkage object.</span></span> <span data-ttu-id="c04b8-109">Затем можно создать экземпляр **Light** в нужном расположении, привязать ресурсы для обоих шейдеров и передать этот экземпляр в массив экземпляров класса при задании шейдера для устройства (например, путем вызова [**ссылку ID3D11DeviceContext::P ссетшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span><span class="sxs-lookup"><span data-stu-id="c04b8-109">You can then create a **Light** instance at a location that you want, bind the resources for both shaders, and pass this instance in the class instances array when you set the shader to the device (for example, by calling [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span></span> <span data-ttu-id="c04b8-110">Затем среда выполнения выполняет следующую последовательность действий:</span><span class="sxs-lookup"><span data-stu-id="c04b8-110">The runtime then performs the following sequence:</span></span>

1.  <span data-ttu-id="c04b8-111">Проверяет, был ли создан экземпляр с тем же объектом компоновки класса.</span><span class="sxs-lookup"><span data-stu-id="c04b8-111">Verifies that the instance was created with the same class linkage object.</span></span>
2.  <span data-ttu-id="c04b8-112">Проверяет, что тип класса **Light** доступно в шейдерах вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="c04b8-112">Verifies that the **Light** class type is availabe in both vertex and pixel shaders.</span></span>
3.  <span data-ttu-id="c04b8-113">Выбирает правильные таблицы функций, которые могут различаться для шейдеров вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="c04b8-113">Selects the correct function tables, which can be different for the vertex and pixel shaders.</span></span>
4.  <span data-ttu-id="c04b8-114">Отправляет вниз смещения, предоставляемые экземпляром.</span><span class="sxs-lookup"><span data-stu-id="c04b8-114">Sends down the offsets that the instance provides.</span></span>

<span data-ttu-id="c04b8-115">Объект компоновки класса в конечном итоге представляет собой репозиторий типа и имен переменных.</span><span class="sxs-lookup"><span data-stu-id="c04b8-115">The class linkage object is ultimately a repository of type and variable names.</span></span> <span data-ttu-id="c04b8-116">Максимальное число имен, доступных для каждого элемента (типа и переменной), — 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="c04b8-116">The maximum number of names available for each item (type and variable) is 64K.</span></span> <span data-ttu-id="c04b8-117">Чем длиннее имена типа и переменной, тем выше потребность в хранилище для метаданных интерфейса, хранящихся на шейдере.</span><span class="sxs-lookup"><span data-stu-id="c04b8-117">The longer the type and variable names are, the higher the storage requirement is for the interface metadata that is stored per shader.</span></span> <span data-ttu-id="c04b8-118">Это обусловлено тем, что среда выполнения должна хранить сопоставление для этих имен для каждого шейдера.</span><span class="sxs-lookup"><span data-stu-id="c04b8-118">This is because the runtime must store a mapping for these names for each shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c04b8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c04b8-119">Related Topics</span></span>

[<span data-ttu-id="c04b8-120">Динамическая компоновка</span><span class="sxs-lookup"><span data-stu-id="c04b8-120">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a><span data-ttu-id="c04b8-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c04b8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c04b8-122">Динамическая компоновка</span><span class="sxs-lookup"><span data-stu-id="c04b8-122">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 