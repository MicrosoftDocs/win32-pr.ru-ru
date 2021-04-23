---
title: Предотвращение нежелательных СРВС шейдера пикселей
description: В этом разделе обсуждается, как обойти драйвер, получая пустые представления ресурсов (СРВС), даже если СРВС, отличные от NULL, привязаны к этапу шейдера пикселей.
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996799"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a><span data-ttu-id="8e68a-103">Предотвращение нежелательных СРВС шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="8e68a-103">Preventing Unwanted NULL Pixel Shader SRVs</span></span>

<span data-ttu-id="8e68a-104">Приложения Direct3D 11, работающие на графическом оборудовании Direct3D 9, могут случайно привести к тому, что драйвер **получит ненулевые** представления ресурсов (СРВС), даже если приложения привязывают значения, отличные от **null** , к этапу шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="8e68a-104">Direct3D 11 applications that run on Direct3D 9 graphics hardware could inadvertently cause the driver to receive **NULL** shader-resource views (SRVs) even when the applications bind non-**NULL** SRVs to the pixel shader stage.</span></span> <span data-ttu-id="8e68a-105">Такая ситуация может возникнуть, только если приложения уничтожат СРВС во время их выполнения.</span><span class="sxs-lookup"><span data-stu-id="8e68a-105">This situation can occur only if the applications destroy SRVs while they execute.</span></span> <span data-ttu-id="8e68a-106">В этом разделе обсуждается, как обойти драйвер, получая **пустые** представления ресурсов (СРВС), даже если СРВС, отличные от **null** , привязаны к этапу шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="8e68a-106">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span>

<span data-ttu-id="8e68a-107">Чтобы драйвер не получал ненужные СРВС **null** , приложения должны вызвать [**ссылку ID3D11DeviceContext::P ссетшадерресаурцес**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) , чтобы отменить все СРВС перед вызовом [**ссылку ID3D11DeviceContext::P ссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="8e68a-107">To prevent the driver from receiving unwanted **NULL** SRVs, the applications must call [**ID3D11DeviceContext::PSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) to unset all SRVs before each call to [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span></span> <span data-ttu-id="8e68a-108">Однако если приложения не удаляют СРВС до завершения выполнения кода, им не нужно отменять СРВС.</span><span class="sxs-lookup"><span data-stu-id="8e68a-108">However, if the applications do not destroy SRVs until the end of their code execution, they do not need to unset the SRVs.</span></span>

<span data-ttu-id="8e68a-109">В разделе [справочника 10Level9](d3d11-graphics-reference-10level9.md) перечислены различия между различными методами [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) на различных уровнях функций 10Level9.</span><span class="sxs-lookup"><span data-stu-id="8e68a-109">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e68a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8e68a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e68a-111">Direct3D 11 на оборудовании нижнего уровня</span><span class="sxs-lookup"><span data-stu-id="8e68a-111">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




