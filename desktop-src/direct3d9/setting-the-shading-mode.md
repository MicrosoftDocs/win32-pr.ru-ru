---
description: Direct3D позволяет выбрать один режим заливки одновременно.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Настройка режима заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495315"
---
# <a name="setting-the-shading-mode-direct3d-9"></a><span data-ttu-id="8dcb4-103">Настройка режима заливки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8dcb4-103">Setting the Shading Mode (Direct3D 9)</span></span>

<span data-ttu-id="8dcb4-104">Direct3D позволяет выбрать один режим заливки одновременно.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-104">Direct3D enables one shading mode to be selected at a time.</span></span> <span data-ttu-id="8dcb4-105">По умолчанию выбрана заливка Гуро.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-105">By default, Gouraud shading is selected.</span></span> <span data-ttu-id="8dcb4-106">В C++ режим заливки можно изменить, вызвав метод [**IDirect3DDevice9:: сетрендерстате**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8dcb4-106">In C++, you can change the shading mode by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="8dcb4-107">Задайте для параметра *State* значение D3DRS \_ шадемоде.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-107">Set the *State* parameter to D3DRS\_SHADEMODE.</span></span> <span data-ttu-id="8dcb4-108">Параметр *State* должен быть задан членом перечисления [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="8dcb4-108">The *State* parameter must be set to a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumeration.</span></span> <span data-ttu-id="8dcb4-109">В следующих примерах кода показано, как текущий режим заливки приложения Direct3D может быть установлен в плоский режим или в режиме заливки Гуро.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-109">The following sample code examples illustrate how the current shading mode of a Direct3D application can be set to flat or Gouraud shading mode.</span></span>


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a><span data-ttu-id="8dcb4-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8dcb4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dcb4-111">Заливка</span><span class="sxs-lookup"><span data-stu-id="8dcb4-111">Shading</span></span>](shading.md)
</dt> </dl>

 

 
