---
description: Эффект создается путем его загрузки в платформу Effects.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Создание влияния (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682336"
---
# <a name="create-an-effect-direct3d-10"></a>Создание влияния (Direct3D 10)

Эффект создается путем его загрузки в платформу Effects. Если результат не был скомпилирован, он будет скомпилирован при создании. Эффекты, которые уже загружены в память, можно создать путем вызова [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md). В следующем примере кода используется [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) для создания эффектов из файла.


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



Для чтения результата требуются те же параметры, что и при компиляции влияния, а также устройство и пул.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отрисовка влияния (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



