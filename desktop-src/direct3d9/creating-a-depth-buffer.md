---
description: Буфер глубины — это свойство устройства. Чтобы создать буфер глубины, который управляется Direct3D, задайте соответствующие члены \_ структуры параметров D3DPRESENT, как показано в следующем примере кода.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Создание буфера глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2f79e6ad32aa2c10b92d0233f85d86744d0a2c562b1991c89990d61bad506c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527926"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Создание буфера глубины (Direct3D 9)

Буфер глубины — это свойство устройства. Чтобы создать буфер глубины, который управляется Direct3D, задайте соответствующие члены структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) , как показано в следующем примере кода.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Установив для элемента ЕнаблеаутодепсстенЦил **значение true**, вы указываете Direct3D управлять буферами глубины для приложения. Обратите внимание, что для АутодепсстенЦилформат должен быть задан допустимый формат буфера глубины. Флаг D3DFMT \_ D16 задает 16-разрядный буфер глубины, если он доступен.

Следующий вызов метода [**IDirect3D9:: креатедевице**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) создает устройство, которое затем создает буфер глубины.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



Буфер глубины автоматически устанавливается в качестве целевого объекта рендеринга для устройства. При сбросе устройства буфер глубины автоматически уничтожается и создается заново в новом размере.

Чтобы создать новую поверхность буфера глубины, используйте метод [**IDirect3DDevice9:: креатедепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Чтобы задать новую поверхность буфера глубины для устройства, используйте метод [**IDirect3DDevice9:: сетдепсстенЦилсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .

Чтобы использовать в приложении буфер глубины, необходимо включить буфер глубины. Дополнительные сведения см. в разделе [Включение буферизации глубины (Direct3D 9)](enabling-depth-buffering.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Буферы глубины](depth-buffers.md)
</dt> </dl>

 

 
