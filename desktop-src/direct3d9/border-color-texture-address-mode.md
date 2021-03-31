---
description: Режим адреса текстуры цвета границы, определяемый \_ элементом Border D3DTADDRESS перечисляемого типа D3DTEXTUREADDRESS, заставляет Direct3D использовать произвольный цвет, известный как цвет границы, для всех координат текстуры за пределами диапазона от 0,0 до 1,0 включительно.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Режим адресации цветовой текстуры границы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423434"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a><span data-ttu-id="193db-103">Режим адресации цветовой текстуры границы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="193db-103">Border Color Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="193db-104">Режим адреса текстуры цвета границы, определяемый \_ элементом Border D3DTADDRESS перечисляемого типа [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , заставляет Direct3D использовать произвольный цвет, известный как цвет границы, для всех координат текстуры за пределами диапазона от 0,0 до 1,0 включительно.</span><span class="sxs-lookup"><span data-stu-id="193db-104">The border color texture address mode, identified by the D3DTADDRESS\_BORDER member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to use an arbitrary color, known as the border color, for any texture coordinates outside the range of 0.0 through 1.0, inclusive.</span></span>

<span data-ttu-id="193db-105">На следующем рисунке приложение задает применение текстуры к примитиву с помощью рамки красного цвета.</span><span class="sxs-lookup"><span data-stu-id="193db-105">In the following illustration, the application specifies that the texture be applied to the primitive using a red border.</span></span>

![изображение текстуры и текстуры с красной рамкой](images/border.png)

<span data-ttu-id="193db-107">Приложения задают цвет границы путем вызова [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="193db-107">Applications set the border color by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="193db-108">Задайте первый параметр для вызова требуемого идентификатора стадии текстуры, второй параметр — \_ значение состояния D3DSAMP, а третий параметр — для нового цвета границы RGBA.</span><span class="sxs-lookup"><span data-stu-id="193db-108">Set the first parameter for the call to the desired texture stage identifier, the second parameter to the D3DSAMP\_BORDERCOLOR stage state value, and the third parameter to the new RGBA border color.</span></span>

## <a name="related-topics"></a><span data-ttu-id="193db-109">См. также</span><span class="sxs-lookup"><span data-stu-id="193db-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="193db-110">Режимы адресации текстур</span><span class="sxs-lookup"><span data-stu-id="193db-110">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
