---
description: Чтобы создать устройство Direct3D, сначала создайте объект Direct3D (см. Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Создание устройства (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710689"
---
# <a name="creating-a-device-direct3d-9"></a>Создание устройства (Direct3D 9)

Чтобы создать устройство Direct3D, сначала создайте объект Direct3D (см. [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)). Все устройства отрисовки, созданные объектом Direct3D, используют одни и те же физические ресурсы. Если вы создаете несколько устройств отрисовки из одного объекта Direct3D, это приведет к крайней мере снижения производительности, так как они используют одно и то же оборудование.

Сначала инициализируйте значения для структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) , которая используется для создания устройства Direct3D. В следующем примере кода задается оконное приложение, в котором задний буфер копируется в передний буфер во время операции вертикальной синхронизации.


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



Затем создайте устройство Direct3D. Следующий вызов [**IDirect3D9:: креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) указывает адаптер по умолчанию, устройство уровня абстрагирования оборудования (HAL) и обработку вершин программного обеспечения.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



Обратите внимание, что вызов для создания, освобождения или сброса устройства должен выполняться только в том же потоке, что и оконная процедура окна фокуса.

После создания устройства задайте его состояние.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устройства Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
