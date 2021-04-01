---
description: 'Ресурсы текстуры реализуются в интерфейсе IDirect3DTexture9. Чтобы получить указатель на интерфейс текстуры, вызовите метод IDirect3DDevice9:: Креатетекстуре или любую из следующих функций D3DX.'
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Ресурсы текстуры (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262454"
---
# <a name="texture-resources-direct3d-9"></a><span data-ttu-id="733d6-104">Ресурсы текстуры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="733d6-104">Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="733d6-105">Ресурсы текстуры реализуются в интерфейсе [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="733d6-105">Texture resources are implemented in the [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface.</span></span> <span data-ttu-id="733d6-106">Чтобы получить указатель на интерфейс текстуры, вызовите метод [**IDirect3DDevice9:: креатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) или любую из следующих функций D3DX.</span><span class="sxs-lookup"><span data-stu-id="733d6-106">To obtain a pointer to a texture interface, call the [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) method or any of the following D3DX functions.</span></span>

-   [<span data-ttu-id="733d6-107">**D3DXCreateTexture**</span><span class="sxs-lookup"><span data-stu-id="733d6-107">**D3DXCreateTexture**</span></span>](d3dxcreatetexture.md)
-   [<span data-ttu-id="733d6-108">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="733d6-108">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
-   [<span data-ttu-id="733d6-109">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="733d6-109">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
-   [<span data-ttu-id="733d6-110">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="733d6-110">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
-   [<span data-ttu-id="733d6-111">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="733d6-111">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
-   [<span data-ttu-id="733d6-112">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="733d6-112">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
-   [<span data-ttu-id="733d6-113">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="733d6-113">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)

<span data-ttu-id="733d6-114">В следующем примере кода [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) используется для загрузки текстуры из Tiger.bmp.</span><span class="sxs-lookup"><span data-stu-id="733d6-114">The following code example uses [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) to load a texture from Tiger.bmp.</span></span>


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



<span data-ttu-id="733d6-115">Первый параметр, который [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) принимает, является указателем на интерфейс [**IDirect3DDevice9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="733d6-115">The first parameter that [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepts is a pointer to an [**IDirect3DDevice9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="733d6-116">Второй параметр сообщает Direct3D имя файла, из которого будет загружена текстура.</span><span class="sxs-lookup"><span data-stu-id="733d6-116">The second parameter tells Direct3D the name of the file from which to load the texture.</span></span> <span data-ttu-id="733d6-117">Третий параметр принимает адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="733d6-117">The third parameter takes the address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

## <a name="rendering-with-texture-resources"></a><span data-ttu-id="733d6-118">Отрисовка с помощью текстурных ресурсов</span><span class="sxs-lookup"><span data-stu-id="733d6-118">Rendering with Texture Resources</span></span>

<span data-ttu-id="733d6-119">Direct3D поддерживает наложения нескольких текстур посредством концепции шагов текстурирования.</span><span class="sxs-lookup"><span data-stu-id="733d6-119">Direct3D supports multiple texture blending through the concept of texture stages.</span></span> <span data-ttu-id="733d6-120">Каждый шаг текстурирования содержит текстуру и операции, которые можно выполнить с текстурой.</span><span class="sxs-lookup"><span data-stu-id="733d6-120">Each texture stage contains a texture and operations that can be performed on the texture.</span></span> <span data-ttu-id="733d6-121">Текстуры в шагах текстурирования образуют набор текущих текстур.</span><span class="sxs-lookup"><span data-stu-id="733d6-121">The textures in the texture stages form the set of current textures.</span></span> <span data-ttu-id="733d6-122">Дополнительные сведения см. в разделе [смешение текстур (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="733d6-122">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="733d6-123">Состояние каждой текстуры инкапсулируется в шаге текстуры.</span><span class="sxs-lookup"><span data-stu-id="733d6-123">The state of each texture is encapsulated in its texture stage.</span></span>

<span data-ttu-id="733d6-124">В приложении C++ состояние каждой текстуры должно быть задано с помощью метода [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="733d6-124">In a C++ application, the state of each texture must be set with the [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="733d6-125">Передайте номер этапа (0-7) в качестве значения первого параметра.</span><span class="sxs-lookup"><span data-stu-id="733d6-125">Pass the stage number (0-7) as the value of the first parameter.</span></span> <span data-ttu-id="733d6-126">Установите значение второго параметра равным элементу перечисляемого типа [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="733d6-126">Set the value of the second parameter to a member of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="733d6-127">Последний параметр — это значение состояния для определенного состояния текстуры.</span><span class="sxs-lookup"><span data-stu-id="733d6-127">The final parameter is the state value for the particular texture state.</span></span>

<span data-ttu-id="733d6-128">Используя указатели на интерфейс текстуры, приложение может отображать смешение до восьми текстур.</span><span class="sxs-lookup"><span data-stu-id="733d6-128">Using texture interface pointers, your application can render a blend of up to eight textures.</span></span> <span data-ttu-id="733d6-129">Задайте текущие текстуры, вызвав метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="733d6-129">Set the current textures by invoking the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="733d6-130">Direct3D накладывает все текущие текстуры на примитивы, которые она отображает.</span><span class="sxs-lookup"><span data-stu-id="733d6-130">Direct3D blends all current textures onto the primitives that it renders.</span></span>

> [!Note]  
> <span data-ttu-id="733d6-131">Метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) увеличивает число ссылок для назначенной поверхности текстуры.</span><span class="sxs-lookup"><span data-stu-id="733d6-131">The [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method increments the reference count of the texture surface being assigned.</span></span> <span data-ttu-id="733d6-132">Если текстура больше не нужна, следует задать для текстуры на соответствующем этапе **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="733d6-132">When the texture is no longer needed, you should set the texture at the appropriate stage to **NULL**.</span></span> <span data-ttu-id="733d6-133">Если это не удается сделать, поверхность не будет освобождена, что приведет к утечке памяти.</span><span class="sxs-lookup"><span data-stu-id="733d6-133">If you fail to do this, the surface will not be released, resulting in a memory leak.</span></span>

 

<span data-ttu-id="733d6-134">Приложение может установить состояние переноса текстур для текущих текстур, вызвав метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) .</span><span class="sxs-lookup"><span data-stu-id="733d6-134">Your application can set the texture wrapping state for the current textures by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method.</span></span> <span data-ttu-id="733d6-135">Передайте значение из D3DRS \_ WRAP0 через D3DRS \_ WRAP7 в качестве значения первого параметра и используйте \_ Флаги D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 и D3DWRAPCOORD \_ 3, чтобы включить перенос в направлениях u, v или w.</span><span class="sxs-lookup"><span data-stu-id="733d6-135">Pass a value from D3DRS\_WRAP0 through D3DRS\_WRAP7 as the value of the first parameter, and use a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in the u, v, or w directions.</span></span>

<span data-ttu-id="733d6-136">Приложения также могут задавать перспективу текстур и состояния фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="733d6-136">Your application can also set the texture perspective and texture filtering states.</span></span> <span data-ttu-id="733d6-137">См. раздел [Фильтрация текстур (Direct3D 9)](texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="733d6-137">See [Texture Filtering (Direct3D 9)](texture-filtering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="733d6-138">См. также</span><span class="sxs-lookup"><span data-stu-id="733d6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="733d6-139">Текстуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="733d6-139">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
