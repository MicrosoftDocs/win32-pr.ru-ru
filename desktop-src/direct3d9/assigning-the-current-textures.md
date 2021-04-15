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
# <a name="assigning-the-current-textures-direct3d-9"></a>Назначение текущих текстур (Direct3D 9)

Direct3D поддерживает список из восьми текущих текстур. Эти текстуры накладываются на все отображаемые им примитивы. В наборе текущих текстур можно использовать только текстуры, созданные как указатели на интерфейс текстуры.

Приложения вызывают метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) для назначения текстур в наборе текущих текстур. Первый параметр должен быть числом в диапазоне 0-7 включительно. Передайте указатель интерфейса текстуры в качестве второго параметра.

В следующем примере кода C++ показано, как текстуру можно назначить набору текущих текстур.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> Программные устройства не поддерживают назначение текстуры более чем одной стадии текстуры за раз.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Смешение текстур](texture-blending.md)
</dt> </dl>

 

 
