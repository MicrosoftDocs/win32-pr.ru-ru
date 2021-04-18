---
description: В этой таблице перечислены форматы Direct3D 9, которые можно сопоставить с форматом Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Форматы прежних версий: сопоставьте форматы Direct3D 9 с Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230b8ed17984d47a3b57ce287aa9b434a2b92aae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701197"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Форматы прежних версий: сопоставьте форматы Direct3D 9 с Direct3D 10

В этой таблице перечислены форматы Direct3D 9, которые можно сопоставить с форматом Direct3D 10. Форматы Direct3D 10 расходятся от форматов Direct3D 9, чтобы можно было объединить форматы вершин и текстур, чтобы обеспечить использование приложений с перекрестным порядком байтов.



| Формат текстуры, вершины и индекса Direct3D 9 | Эквивалентный формат Direct3D 10                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ неизвестный                        | \_неизвестный формат DXGI \_                                                |
| D3DFMT \_ R8G8B8                         | Недоступно                                                        |
| D3DFMT \_ A8R8G8B8                       | \_Формат DXGI \_ B8G8R8A8 \_ UNORM (DXGI 1,1)                             |
| D3DFMT \_ X8R8G8B8                       | \_Формат DXGI \_ B8G8R8X8 \_ UNORM (DXGI 1,1)                             |
| D3DFMT \_ R5G6B5                         | \_Формат DXGI \_ B5G6R5 \_ UNORM (DXGI 1,2)                               |
| D3DFMT \_ X1R5G5B5                       | Недоступно                                                        |
| D3DFMT \_ A1R5G5B5                       | \_Формат DXGI \_ B5G5R5A1 \_ UNORM (DXGI 1,2)                             |
| D3DFMT \_ A4R4G4B4                       | \_Формат DXGI \_ B4G4R4A4 \_ UNORM (DXGI 1,2)                             |
| D3DFMT \_ R3G3B2                         | Недоступно                                                        |
| D3DFMT \_ A8                             | \_Формат DXGI \_ a8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | Недоступно                                                        |
| D3DFMT \_ X4R4G4B4                       | Недоступно                                                        |
| D3DFMT \_ A2B10G10R10                    | \_R10G10B10A2 формата \_ DXGI                                            |
| D3DFMT \_ A8B8G8R8                       | \_Формат DXGI \_ R8G8B8A8 \_ UNORM или DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB |
| D3DFMT \_ X8B8G8R8                       | Недоступно                                                        |
| D3DFMT \_ G16R16                         | \_Формат DXGI \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | Недоступно                                                        |
| D3DFMT \_ A16B16G16R16                   | \_Формат DXGI \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | Недоступно                                                        |
| D3DFMT \_ P8                             | Недоступно                                                        |
| D3DFMT \_ 8                             | \_Формат DXGI \_ R8 \_ UNORM ¹                                            |
| D3DFMT \_ A8L8                           | Недоступно                                                        |
| D3DFMT \_ A4L4                           | Недоступно                                                        |
| D3DFMT \_ V8U8                           | \_Формат DXGI \_ R8G8 \_ снорм                                            |
| D3DFMT \_ L6V5U5                         | Недоступно                                                        |
| D3DFMT \_ X8L8V8U8                       | Недоступно                                                        |
| D3DFMT \_ Q8W8V8U8                       | \_Формат DXGI \_ R8G8B8A8 \_ снорм                                        |
| D3DFMT \_ V16U16                         | \_Формат DXGI \_ R16G16 \_ снорм                                          |
| D3DFMT \_ W11V11U10                      | Недоступно                                                        |
| D3DFMT \_ A2W10V10U10                    | Недоступно                                                        |
| D3DFMT \_ UYVY                           | Недоступно                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | \_Формат DXGI \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| D3DFMT \_ YUY2                           | Недоступно                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | \_Формат DXGI \_ R8G8 \_ B8G8 \_ UNORM ²                                    |
| D3DFMT \_ DXT1                           | \_Формат DXGI \_ BC1 \_ UNORM или DXGI \_ \_ BC1 \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT2                           | \_Формат DXGI \_ BC2 \_ UNORM или DXGI \_ \_ BC2 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT3                           | \_Формат DXGI \_ BC2 \_ UNORM или DXGI \_ \_ BC2 \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT4                           | \_Формат DXGI \_ BC3 \_ UNORM или DXGI \_ \_ BC3 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT5                           | \_Формат DXGI \_ BC3 \_ UNORM или DXGI \_ \_ BC3 \_ UNORM \_ sRGB           |
| D3DFMT \_ D16 и D3DFMT \_ D16 \_ блокируемых  | \_Формат DXGI \_ D16 \_ UNORM                                             |
| D3DFMT \_ d32                            | Недоступно                                                        |
| D3DFMT \_ D15S1                          | Недоступно                                                        |
| D3DFMT \_ D24S8                          | Недоступно                                                        |
| D3DFMT \_ D24X8                          | Недоступно                                                        |
| D3DFMT \_ D24X4S4                        | Недоступно                                                        |
| D3DFMT \_ D16                            | \_Формат DXGI \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ блокируемый                 | \_Формат DXGI \_ d32 \_ float                                             |
| D3DFMT \_ D24FS8                         | Недоступно                                                        |
| D3DFMT \_ S1D15                          | Недоступно                                                        |
| D3DFMT \_ S8D24                          | \_Формат DXGI \_ D24 \_ UNORM \_ S8 \_ uint                                   |
| D3DFMT \_ X8D24                          | Недоступно                                                        |
| D3DFMT \_ X4S4D24                        | Недоступно                                                        |
| D3DFMT \_ L16                            | \_Формат DXGI \_ R16 \_ UNORM ¹                                           |
| D3DFMT \_ INDEX16                        | \_Формат DXGI \_ R16 \_ uint                                              |
| D3DFMT \_ INDEX32                        | \_Формат DXGI \_ R32 \_ uint                                              |
| D3DFMT \_ Q16W16V16U16                   | \_Формат DXGI \_ R16G16B16A16 \_ снорм                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | Недоступно                                                        |
| D3DFMT \_ R16F                           | \_Формат DXGI \_ R16 \_ float                                             |
| D3DFMT \_ G16R16F                        | \_Формат DXGI \_ R16G16 \_ float                                          |
| D3DFMT \_ A16B16G16R16F                  | \_Формат DXGI \_ R16G16B16A16 \_ float                                    |
| D3DFMT \_ R32F                           | \_Формат DXGI \_ R32 \_ float                                             |
| D3DFMT \_ G32R32F                        | \_Формат DXGI \_ R32G32 \_ float                                          |
| D3DFMT \_ A32B32G32R32F                  | \_Формат DXGI \_ R32G32B32A32 \_ float                                    |
| D3DFMT \_ CxV8U8                         | Недоступно                                                        |
| D3DDECLTYPE \_ FLOAT1                    | \_Формат DXGI \_ R32 \_ float                                             |
| D3DDECLTYPE \_ FLOAT2                    | \_Формат DXGI \_ R32G32 \_ float                                          |
| D3DDECLTYPE \_ FLOAT3                    | \_Формат DXGI \_ R32G32B32 \_ float                                       |
| D3DDECLTYPE \_ FLOAT4                    | \_Формат DXGI \_ R32G32B32A32 \_ float                                    |
| D3DDECLTYPED3DCOLOR                    | Недоступно                                                        |
| D3DDECLTYPE \_ UBYTE4                    | \_Формат DXGI \_ R8G8B8A8 \_ uint ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | \_Формат DXGI \_ R16G16 \_ Синт                                           |
| D3DDECLTYPE \_ SHORT4                    | \_Формат DXGI \_ R16G16B16A16 \_ Синт                                     |
| D3DDECLTYPE \_ UBYTE4N                   | \_Формат DXGI \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | \_Формат DXGI \_ R16G16 \_ снорм                                          |
| D3DDECLTYPE \_ SHORT4N                   | \_Формат DXGI \_ R16G16B16A16 \_ снорм                                    |
| D3DDECLTYPE \_ USHORT2N                  | \_Формат DXGI \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | \_Формат DXGI \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | Недоступно                                                        |
| D3DDECLTYPE \_ DEC3N                     | Недоступно                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | \_Формат DXGI \_ R16G16 \_ float                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | \_Формат DXGI \_ R16G16B16A16 \_ float                                    |



 

1.  Используйте. r свиззле в шейдере для дублирования красного в другие компоненты, чтобы получить поведение Direct3D 9.
2.  В Direct3D 9 данные были масштабированы с помощью 255.0 f, что можно сделать в коде шейдера.
3.  DXT2 и DXT3 одинаковы с точки зрения API. DXT4 и DXT5 одинаковы с точки зрения API. Единственным отличием было предварительное умножение альфа-канала, которое может быть записано приложением и не требует отдельного формата.
4.  Шейдер получает значения UINT, но если целочисленный тип с плавающей запятой в стиле Direct3D 9 (0,0 f, 1,0 f... 255. f), UINT можно преобразовать в объект float32 в шейдере.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ресурсы (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



