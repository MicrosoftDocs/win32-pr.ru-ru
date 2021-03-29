---
description: Как и в случае с любой функцией, драйвер, используемый приложением, может не поддерживать все типы буферизации глубины.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Запросы для поддержки буфера глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805291"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>Запросы для поддержки буфера глубины (Direct3D 9)

Как и в случае с любой функцией, драйвер, используемый приложением, может не поддерживать все типы буферизации глубины. Всегда проверяйте возможности драйвера. Хотя большинство драйверов поддерживает буферизацию глубины на основе z, не все они поддерживают буферизацию глубины на основе w. При попытке включить неподдерживаемую схему драйверы не завершаются ошибкой. Вместо этого они переходят на другой метод буферизации глубины, или иногда отключена буферизация глубины, что может привести к отображению сцен с очень высокой глубиной сортировки.

Можно проверить общую поддержку для буферов глубины, запросив Direct3D для устройства вывода, которое будет использоваться приложением перед созданием устройства Direct3D. Если объект Direct3D сообщает, что он поддерживает буферизацию глубины, все аппаратные устройства, создаваемые из этого объекта Direct3D, будут поддерживать z-буферизацию.

Чтобы запросить поддержку буферизации глубины, можно использовать метод [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , как показано в следующем примере кода.


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



[**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) позволяет выбрать устройство для создания на основе возможностей этого устройства. В этом случае устройства, не поддерживающие буферы с 16-разрядной глубиной, отклоняются.

Использование [**IDirect3D9:: чеккдепсстенЦилматч**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) для определения совместимости с набором элементов глубины с целью прорисовки показано в следующем примере кода.


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



Если известно, что драйвер поддерживает буферы глубины, можно проверить поддержку w-buffer. Хотя буферы глубины поддерживаются всеми программами программной прорисовки, w-buffers поддерживаются только в справочных программах, которые не подходят для работы в реальных приложениях. Независимо от типа устройства, используемого приложением, перед включением буферизации глубины на основе w следует проверить поддержку для w-буферов.

1.  После создания устройства вызовите метод [**IDirect3DDevice9:: жетдевицекапс**](/windows/desktop/api) , передав инициализированную структуру [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .
2.  После вызова элемент Линекапс содержит сведения о поддержке этого драйвера для примитивов отрисовки.
3.  Если элемент Растеркапс этой структуры содержит \_ флаг D3DPRASTERCAPS вбуффер, то драйвер поддерживает буферизацию глубины на основе w для этого типа-примитива.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Буферы глубины](depth-buffers.md)
</dt> </dl>

 

 
