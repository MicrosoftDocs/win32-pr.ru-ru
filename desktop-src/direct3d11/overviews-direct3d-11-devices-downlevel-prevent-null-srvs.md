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
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a>Предотвращение нежелательных СРВС шейдера пикселей

Приложения Direct3D 11, работающие на графическом оборудовании Direct3D 9, могут случайно привести к тому, что драйвер **получит ненулевые** представления ресурсов (СРВС), даже если приложения привязывают значения, отличные от **null** , к этапу шейдера пикселей. Такая ситуация может возникнуть, только если приложения уничтожат СРВС во время их выполнения. В этом разделе обсуждается, как обойти драйвер, получая **пустые** представления ресурсов (СРВС), даже если СРВС, отличные от **null** , привязаны к этапу шейдера пикселей.

Чтобы драйвер не получал ненужные СРВС **null** , приложения должны вызвать [**ссылку ID3D11DeviceContext::P ссетшадерресаурцес**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) , чтобы отменить все СРВС перед вызовом [**ссылку ID3D11DeviceContext::P ссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader). Однако если приложения не удаляют СРВС до завершения выполнения кода, им не нужно отменять СРВС.

В разделе [справочника 10Level9](d3d11-graphics-reference-10level9.md) перечислены различия между различными методами [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) на различных уровнях функций 10Level9.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Direct3D 11 на оборудовании нижнего уровня](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




