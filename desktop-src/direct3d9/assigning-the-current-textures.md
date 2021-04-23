---
description: Direct3D поддерживает список из восьми текущих текстур. Эти текстуры накладываются на все отображаемые им примитивы. В наборе текущих текстур можно использовать только текстуры, созданные как указатели на интерфейс текстуры.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Назначение текущих текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496740"
---
# <a name="assigning-the-current-textures-direct3d-9"></a><span data-ttu-id="30afc-105">Назначение текущих текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="30afc-105">Assigning the Current Textures (Direct3D 9)</span></span>

<span data-ttu-id="30afc-106">Direct3D поддерживает список из восьми текущих текстур.</span><span class="sxs-lookup"><span data-stu-id="30afc-106">Direct3D maintains a list of up to eight current textures.</span></span> <span data-ttu-id="30afc-107">Эти текстуры накладываются на все отображаемые им примитивы.</span><span class="sxs-lookup"><span data-stu-id="30afc-107">It blends these textures onto all the primitive it renders.</span></span> <span data-ttu-id="30afc-108">В наборе текущих текстур можно использовать только текстуры, созданные как указатели на интерфейс текстуры.</span><span class="sxs-lookup"><span data-stu-id="30afc-108">Only textures created as texture interface pointers can be used in the set of current textures.</span></span>

<span data-ttu-id="30afc-109">Приложения вызывают метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) для назначения текстур в наборе текущих текстур.</span><span class="sxs-lookup"><span data-stu-id="30afc-109">Applications call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to assign textures into the set of current textures.</span></span> <span data-ttu-id="30afc-110">Первый параметр должен быть числом в диапазоне 0-7 включительно.</span><span class="sxs-lookup"><span data-stu-id="30afc-110">The first parameter must be a number in the range of 0-7, inclusive.</span></span> <span data-ttu-id="30afc-111">Передайте указатель интерфейса текстуры в качестве второго параметра.</span><span class="sxs-lookup"><span data-stu-id="30afc-111">Pass the texture interface pointer as the second parameter.</span></span>

<span data-ttu-id="30afc-112">В следующем примере кода C++ показано, как текстуру можно назначить набору текущих текстур.</span><span class="sxs-lookup"><span data-stu-id="30afc-112">The following C++ code example demonstrates how a texture can be assigned to the set of current textures.</span></span>


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> <span data-ttu-id="30afc-113">Программные устройства не поддерживают назначение текстуры более чем одной стадии текстуры за раз.</span><span class="sxs-lookup"><span data-stu-id="30afc-113">Software devices do not support assigning a texture to more than one texture stage at a time.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="30afc-114">См. также</span><span class="sxs-lookup"><span data-stu-id="30afc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30afc-115">Смешение текстур</span><span class="sxs-lookup"><span data-stu-id="30afc-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
