---
description: Ресурсы — это текстуры и буферы, используемые для отрисовки сцены.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Ресурсы Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acc40cc929f5cedbefaa0b652c67ea59e35212e4da81c4278e3a57f48ea7662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523783"
---
# <a name="direct3d-resources-direct3d-9"></a>Ресурсы Direct3D (Direct3D 9)

Ресурсы — это текстуры и буферы, используемые для отрисовки сцены. Приложения должны создавать, загружать, копировать и использовать ресурсы. В этом разделе приводятся краткие сведения о ресурсах и действиях и методах, используемых приложениями при работе с ресурсами.

Все ресурсы, включая геометрические ресурсы [**IDirect3DIndexBuffer9**](/windows/desktop/api) и [**IDirect3DVertexBuffer9**](/windows/desktop/api), наследуются от интерфейса [**IDirect3DResource9**](/windows/desktop/api) . Ресурсы текстуры, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)и [**IDirect3DVolumeTexture9**](/windows/desktop/api)также наследуются от интерфейса [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .

-   [Свойства ресурсов (Direct3D 9)](resource-properties.md)
-   [Управление ресурсами (Direct3D 9)](manipulating-resources.md)
-   [Блокировка ресурсов (Direct3D 9)](locking-resources.md)
-   [Связи ресурсов (Direct3D 9)](resource-relationships.md)
-   [Управление ресурсами (Direct3D 9)](managing-resources.md)
-   [Ресурсы и стратегии выделения ресурсов, управляемые приложениями (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Буферы индексов (Direct3D 9)](index-buffers.md)
-   [Буферы вершин (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Начало работы](getting-started.md)
</dt> </dl>

 

 
