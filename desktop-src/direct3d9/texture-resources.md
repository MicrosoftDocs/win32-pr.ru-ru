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
# <a name="texture-resources-direct3d-9"></a>Ресурсы текстуры (Direct3D 9)

Ресурсы текстуры реализуются в интерфейсе [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) . Чтобы получить указатель на интерфейс текстуры, вызовите метод [**IDirect3DDevice9:: креатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) или любую из следующих функций D3DX.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

В следующем примере кода [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) используется для загрузки текстуры из Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



Первый параметр, который [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) принимает, является указателем на интерфейс [**IDirect3DDevice9**](/windows/desktop/api) . Второй параметр сообщает Direct3D имя файла, из которого будет загружена текстура. Третий параметр принимает адрес указателя на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий созданный объект текстуры.

## <a name="rendering-with-texture-resources"></a>Отрисовка с помощью текстурных ресурсов

Direct3D поддерживает наложения нескольких текстур посредством концепции шагов текстурирования. Каждый шаг текстурирования содержит текстуру и операции, которые можно выполнить с текстурой. Текстуры в шагах текстурирования образуют набор текущих текстур. Дополнительные сведения см. в разделе [смешение текстур (Direct3D 9)](texture-blending.md). Состояние каждой текстуры инкапсулируется в шаге текстуры.

В приложении C++ состояние каждой текстуры должно быть задано с помощью метода [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/desktop/api) . Передайте номер этапа (0-7) в качестве значения первого параметра. Установите значение второго параметра равным элементу перечисляемого типа [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . Последний параметр — это значение состояния для определенного состояния текстуры.

Используя указатели на интерфейс текстуры, приложение может отображать смешение до восьми текстур. Задайте текущие текстуры, вызвав метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Direct3D накладывает все текущие текстуры на примитивы, которые она отображает.

> [!Note]  
> Метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) увеличивает число ссылок для назначенной поверхности текстуры. Если текстура больше не нужна, следует задать для текстуры на соответствующем этапе **значение NULL**. Если это не удается сделать, поверхность не будет освобождена, что приведет к утечке памяти.

 

Приложение может установить состояние переноса текстур для текущих текстур, вызвав метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . Передайте значение из D3DRS \_ WRAP0 через D3DRS \_ WRAP7 в качестве значения первого параметра и используйте \_ Флаги D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 и D3DWRAPCOORD \_ 3, чтобы включить перенос в направлениях u, v или w.

Приложения также могут задавать перспективу текстур и состояния фильтрации текстур. См. раздел [Фильтрация текстур (Direct3D 9)](texture-filtering.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Текстуры Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
